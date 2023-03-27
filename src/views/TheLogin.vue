<template>
  <div class="auth-page">
    <div class="modal-dialog modal-md modal-dialog-centered modal-dialog-scrollable">
      <div class="modal-content p-10">
        <div class="modal-body pt-0 scroll-y">
          <form id="page_account_signin_form" class="page_account_signin_form_modal">
            <input type="hidden" name="_token" value="thvLYpDlnAMioKNmH3cq4PCOLwgYINosDwKuJb4q" />
            <h3 class="text-center text-dark fw-bolder fs-1 pt-5 mb-10">
              Sign In
            </h3>
            <div id="page_account_signin_message" class="d-none py-5"></div>
            <div class="form-group mb-10">
              <label class="font-size-base fw-bold mb-3">Email/Tài khoản</label>
              <fieldset class="form-group">
                <input type="email" placeholder="Email" v-model="user.email"
                  class="form-control form-control-lg form-control-solid" />
              </fieldset>
            </div>
            <div class="form-group mb-10">
              <div class="d-flex justify-content-between mb-3">
                <label class="fs-base fw-bold">Mật khẩu</label><a class="text-right fw-bold text-primary"
                  id="page_account_password_reset_toggle">Quên mật khẩu ?</a>
              </div>
              <fieldset class="form-group">
                <input class="form-control form-control-lg form-control-solid" type="password" placeholder="Password"
                  v-model="user.password" />
              </fieldset>
            </div>
            <div class="form-group mb-0 d-flex justify-content-between pt-2 mb-10">
              <button @click="Login" class="btn btn-custom btn-primary fw-bold py-4 px-7 me-3">
                <span class="indicator-label"> Đăng Nhập</span></button>
              <a href="https://devs.keenthemes.com/account/redirect/google?redirect_uri=https://devs.keenthemes.com/question/custom-styling-for-kt-datatables-in-vuejs"
                class="btn btn-custom btn-light-primary fw-bold flex-grow-1 py-4 px-7" data-action="signin-google"><svg
                  xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 20 20" fill="none"
                  class="h-20px me-2">
                  <path
                    d="M19.9895 10.1871C19.9895 9.36767 19.9214 8.76973 19.7742 8.14966H10.1992V11.848H15.8195C15.7062 12.7671 15.0943 14.1512 13.7346 15.0813L13.7155 15.2051L16.7429 17.4969L16.9527 17.5174C18.879 15.7789 19.9895 13.221 19.9895 10.1871Z"
                    fill="#4285F4" />
                  <path
                    d="M10.1993 19.9313C12.9527 19.9313 15.2643 19.0454 16.9527 17.5174L13.7346 15.0813C12.8734 15.6682 11.7176 16.0779 10.1993 16.0779C7.50243 16.0779 5.21352 14.3395 4.39759 11.9366L4.27799 11.9466L1.13003 14.3273L1.08887 14.4391C2.76588 17.6945 6.21061 19.9313 10.1993 19.9313Z"
                    fill="#34A853" />
                  <path
                    d="M4.39748 11.9366C4.18219 11.3166 4.05759 10.6521 4.05759 9.96565C4.05759 9.27909 4.18219 8.61473 4.38615 7.99466L4.38045 7.8626L1.19304 5.44366L1.08875 5.49214C0.397576 6.84305 0.000976562 8.36008 0.000976562 9.96565C0.000976562 11.5712 0.397576 13.0882 1.08875 14.4391L4.39748 11.9366Z"
                    fill="#FBBC05" />
                  <path
                    d="M10.1993 3.85336C12.1142 3.85336 13.406 4.66168 14.1425 5.33717L17.0207 2.59107C15.253 0.985496 12.9527 0 10.1993 0C6.2106 0 2.76588 2.23672 1.08887 5.49214L4.38626 7.99466C5.21352 5.59183 7.50242 3.85336 10.1993 3.85336Z"
                    fill="#EB4335" />
                </svg> Sign In with Google </a>
            </div>
            <div class="text-center fw-bolder fs-6">
              <span class="text-muted me-2">Or</span><a class="text-primary" id="page_account_signup_toggle">
                <router-link to="/register"> Tạo tài khoản?</router-link>
              </a>
            </div>
          </form>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { reactive, ref } from "vue";
import { signIn } from "@/api";
import router from "@/router";
import { useStore } from "vuex";

export default {
  name: "TheLogin",

  setup() {
    const user = reactive({
      email: "",
      password: "",
    });

    const store = useStore();

    let loginValidation = ref(false);

    const Login = async () => {
      try {
        const { data } = await signIn(user);
        await store.dispatch("LOGIN", data.user);
        await router.push({ name: "Home" });
      } catch (error: any) {
        const code = error.response.data.errors.code;
        if (code == "EMAIL_NULL_OR_INVALID") {
          loginValidation.value = true;
        } else if (code == "PASSWORD_WRONG") {
          loginValidation.value = true;
        }
      }
    };
    return { user, loginValidation, Login };
  },
};
</script>

<style scoped></style>
