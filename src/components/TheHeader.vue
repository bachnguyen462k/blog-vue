<template>
  <div
    id="kt_header"
    class="header align-items-stretch"
    data-kt-sticky="true"
    data-kt-sticky-animation="false"
    data-kt-sticky-name="header"
    data-kt-sticky-offset="100px"
  >
    <div
      class="container-xxl d-flex align-items-stretch justify-content-between"
    >
      <div
        class="d-flex align-items-center flex-grow-1 flex-lg-grow-0 me-5 me-lg-10"
      >
        <a href="https://devs.keenthemes.com"
          ><img
            alt="Logo"
            src="https://devs.keenthemes.com/assets/media/logos/default.svg"
            class="d-none d-lg-block w-lg-200px h-30px" /><img
            alt="Logo"
            src="https://devs.keenthemes.com/assets/media/logos/mobile.svg"
            class="d-block d-lg-none h-30px"
        /></a>
        <div
          class="btn btn-icon btn-active-icon-primary ms-1 d-flex d-lg-none"
          id="kt_aside_mobile_toggle"
        >
          <span class="svg-icon svg-icon-1"
            ><svg
              xmlns="http://www.w3.org/2000/svg"
              width="24"
              height="24"
              viewBox="0 0 24 24"
              fill="none"
            >
              <path
                opacity="0.3"
                d="M11 21H21C21.6 21 22 20.6 22 20V4C22 3.4 21.6 3 21 3H11C10.4 3 10 3.4 10 4V20C10 20.6 10.4 21 11 21Z"
                fill="black"
              />
              <path
                d="M7 21H3C2.4 21 2 20.6 2 20V4C2 3.4 2.4 3 3 3H7C7.6 3 8 3.4 8 4V20C8 20.6 7.6 21 7 21Z"
                fill="black"
              /></svg
          ></span>
        </div>
      </div>
      <div
        class="d-flex align-items-center justify-content-between flex-lg-grow-1"
      >
        <div class="d-flex align-items-center" id="kt_header_nav">
          <div
            class="header-menu align-items-stretch px-4 px-lg-0"
            data-kt-drawer="true"
            data-kt-drawer-name="header-menu"
            data-kt-drawer-activate="{default: true, lg: false}"
            data-kt-drawer-overlay="true"
            data-kt-drawer-width="{default:'200px', '300px': '250px'}"
            data-kt-drawer-direction="start"
            data-kt-drawer-toggle="#kt_header_menu_mobile_toggle"
            data-kt-swapper="true"
            data-kt-swapper-mode="prepend"
            data-kt-swapper-parent="{default: '#kt_body', lg: '#kt_header_nav'}"
          >
            <div
              class="menu menu-rounded menu-column menu-lg-row menu-state-bg menu-title-gray-700 menu-state-title-primary menu-state-icon-primary menu-state-bullet-primary menu-arrow-gray-400 fw-bold my-5 my-lg-0 align-items-stretch"
              id="#kt_header_menu"
              data-kt-menu="true"
            >
              <div class="menu-item me-lg-1">
                <a class="menu-link py-3" 
                  ><span class="menu-title">
                    <router-link
                      to="/"
                      class="nav-link"
                      @click="selected(home)"
                      :class="{ active: home }"
                      active-class="active"
                      >Home</router-link
                    >
                  </span></a
                >
              </div>

              <div class="menu-item me-lg-1">
                <a class="menu-link py-3" href="https://graphics.keenthemes.com"
                  ><span class="menu-title">
                    <router-link
                      to="/editor/"
                      class="nav-link"
                      @click="selected(article)"
                      :class="{ active: article }"
                      active-class="active"
                      >New Article</router-link
                    >
                  </span></a
                >
              </div>
            </div>
          </div>
        </div>
        <div class="d-flex align-items-center">
          <form
            id="kt_sidebar_search_form"
            action="https://devs.keenthemes.com/search"
            method="GET"
            class="w-200px w-xxl-250px position-relative d-none d-lg-block"
            autocomplete="off"
          >
            <span
              class="svg-icon svg-icon-4 svg-icon-gray-700 position-absolute top-50 translate-middle-y ms-4"
              ><svg
                xmlns="http://www.w3.org/2000/svg"
                width="24"
                height="24"
                viewBox="0 0 24 24"
                fill="none"
              >
                <rect
                  opacity="0.5"
                  x="17.0365"
                  y="15.1223"
                  width="8.15546"
                  height="2"
                  rx="1"
                  transform="rotate(45 17.0365 15.1223)"
                  fill="black"
                />
                <path
                  d="M11 19C6.55556 19 3 15.4444 3 11C3 6.55556 6.55556 3 11 3C15.4444 3 19 6.55556 19 11C19 15.4444 15.4444 19 11 19ZM11 5C7.53333 5 5 7.53333 5 11C5 14.4667 7.53333 17 11 17C14.4667 17 17 14.4667 17 11C17 7.53333 14.4667 5 11 5Z"
                  fill="black"
                /></svg></span
            ><input
              type="text"
              class="form-control form-control-sm bg-transparent ps-11 fs-7"
              name="search"
              placeholder="Search"
            /><input type="submit" class="page_speed_758359108" tabindex="-1" />
          </form>
          <a class="btn btn-sm btn-primary fw-bolder flex-shrink-0 px-4 ms-3">
            Ask <span class="d-none d-md-inline">Question</span></a
          >
          <form
            action="https://devs.keenthemes.com/search"
            method="GET"
            class="btn btn-icon btn-active-icon-primary position-relative d-lg-none cursor-pointer ms-1"
            autocomplete="off"
          >
            <span
              class="svg-icon svg-icon-1 position-absolute start-50 top-50 translate-middle"
              ><svg
                xmlns="http://www.w3.org/2000/svg"
                width="24"
                height="24"
                viewBox="0 0 24 24"
                fill="none"
              >
                <rect
                  opacity="0.5"
                  x="17.0365"
                  y="15.1223"
                  width="8.15546"
                  height="2"
                  rx="1"
                  transform="rotate(45 17.0365 15.1223)"
                  fill="black"
                />
                <path
                  d="M11 19C6.55556 19 3 15.4444 3 11C3 6.55556 6.55556 3 11 3C15.4444 3 19 6.55556 19 11C19 15.4444 15.4444 19 11 19ZM11 5C7.53333 5 5 7.53333 5 11C5 14.4667 7.53333 17 11 17C14.4667 17 17 14.4667 17 11C17 7.53333 14.4667 5 11 5Z"
                  fill="black"
                /></svg></span
            ><input
              type="text"
              class="form-control form-control-flush bg-transparent px-0"
              name="search"
              placeholder=""
            />
          </form>
          <div
            class="d-flex align-items-center ms-0 ms-lg-3"
            id="kt_header_user_menu_toggle"
            v-if="isLogin"
          >
            <div
              class="btn btn-active-light d-flex align-items-center bg-hover-light py-2 px-2 px-md-3"
              data-kt-menu-trigger="click"
              data-kt-menu-attach="parent"
              data-kt-menu-placement="bottom-end"
            >
              <div
                class="d-none d-md-flex flex-column align-items-end justify-content-center me-2"
              >
                <span class="text-muted fs-9 fw-bold lh-1 mb-1">Xin chào!</span
                ><span class="text-dark fs-7 fw-bolder lh-1">bach nguyen</span>
              </div>
              <div class="symbol symbol-30px">
                <img
                  src="https://lh3.googleusercontent.com/a/AATXAJwYAsuzoxZ45zu2PQgXtU2QIpgL4lCLCzRZA6D7=s96-c"
                  alt="avatar"
                />
              </div>
            </div>
            <div
              class="menu menu-sub menu-sub-dropdown menu-column menu-rounded menu-gray-600 menu-state-bg-light-primary fw-bold py-4 fs-6 w-275px"
              data-kt-menu="true"
            >
              <div class="menu-item px-3">
                <div class="menu-content d-flex align-items-center px-3">
                  <div class="symbol symbol-40px me-3">
                    <img
                      src="https://lh3.googleusercontent.com/a/AATXAJwYAsuzoxZ45zu2PQgXtU2QIpgL4lCLCzRZA6D7=s96-c"
                      alt="avatar"
                    />
                  </div>
                  <div class="d-flex flex-column">
                    <div class="fw-bolder d-flex align-items-center fs-5">
                      bach nguyen
                      <span
                        class="badge badge-light-success fw-bolder fs-8 px-2 py-1 ms-2"
                      ></span>
                    </div>
                    <a
                      href="#"
                      class="fw-bold text-muted text-hover-primary fs-7"
                      >nguyenbach.dev@gmail.com</a
                    >
                  </div>
                </div>
              </div>
              <div class="separator my-2"></div>
              <div class="menu-item px-5">
                <a
                  href="https://devs.keenthemes.com/my-question"
                  class="menu-link px-5"
                  ><span class="menu-text">My Questions</span
                  ><span class="menu-badge"
                    ><span
                      class="badge badge-light-danger badge-circle fw-bolder fs-7"
                      >0</span
                    ></span
                  ></a
                >
              </div>
              <div class="menu-item px-5">
                <a
                  href="https://keenthemes.com/account/downloads"
                  class="menu-link px-5"
                  ><span class="menu-text">My Downloads</span></a
                >
              </div>
              <div class="separator my-2"></div>
              <div class="menu-item px-5 my-1">
                <a
                  href="https://devs.keenthemes.com/account/edit"
                  class="menu-link px-5"
                >
                  Account Settings
                </a>
              </div>
              <div class="menu-item px-5">
                <a
                  href="#"
                  data-action="https://devs.keenthemes.com/account/signout"
                  data-method="post"
                  data-csrf="thvLYpDlnAMioKNmH3cq4PCOLwgYINosDwKuJb4q"
                  data-reload="true"
                  class="button-ajax menu-link px-5"
                >
                  Sign Out
                </a>
              </div>
            </div>
          </div>
          <div
            class="d-flex align-items-center ms-0 ms-lg-3"
            id="kt_header_user_menu_toggle"
          >
            <button
              class="btn btn-sm btn-icon btn-active-icon-primary d-flex d-lg-none"
              data-bs-toggle="modal"
              data-bs-target="#page_modal_account_login"
            >
              <span class="svg-icon svg-icon-1"
                ><svg
                  xmlns="http://www.w3.org/2000/svg"
                  width="24"
                  height="24"
                  viewBox="0 0 24 24"
                  fill="none"
                >
                  <path
                    opacity="0.3"
                    d="M22 12C22 17.5 17.5 22 12 22C6.5 22 2 17.5 2 12C2 6.5 6.5 2 12 2C17.5 2 22 6.5 22 12ZM12 7C10.3 7 9 8.3 9 10C9 11.7 10.3 13 12 13C13.7 13 15 11.7 15 10C15 8.3 13.7 7 12 7Z"
                    fill="black"
                  ></path>
                  <path
                    d="M12 22C14.6 22 17 21 18.7 19.4C17.9 16.9 15.2 15 12 15C8.8 15 6.09999 16.9 5.29999 19.4C6.99999 21 9.4 22 12 22Z"
                    fill="black"
                  ></path></svg
              ></span></button
            >
            <router-link to="/login" class="nav-link" @click="selected(signIn)" :class="{ active: signIn }"
            active-class="active" v-if="!isLogin">
            <button
              class="btn btn-sm btn-primary px-4 fw-bolder d-none d-lg-flex me-2"
              data-bs-toggle="modal"
              data-bs-target="#page_modal_account_login"
            >
              Sign In
            </button>
            </router-link>
          </div>
          <button
            class="btn btn-sm btn-icon btn-active-icon-primary d-flex d-lg-none me-n1 ms-1"
            id="kt_header_menu_mobile_toggle"
            v-if="isLogin"
          >
            <span class="svg-icon svg-icon-2"
              ><svg
                xmlns="http://www.w3.org/2000/svg"
                width="24"
                height="24"
                viewBox="0 0 24 24"
                fill="none"
              >
                <path
                  d="M21 7H3C2.4 7 2 6.6 2 6V4C2 3.4 2.4 3 3 3H21C21.6 3 22 3.4 22 4V6C22 6.6 21.6 7 21 7Z"
                  fill="black"
                />
                <path
                  opacity="0.3"
                  d="M21 14H3C2.4 14 2 13.6 2 13V11C2 10.4 2.4 10 3 10H21C21.6 10 22 10.4 22 11V13C22 13.6 21.6 14 21 14ZM22 20V18C22 17.4 21.6 17 21 17H3C2.4 17 2 17.4 2 18V20C2 20.6 2.4 21 3 21H21C21.6 21 22 20.6 22 20Z"
                  fill="black"
                /></svg
            ></span>
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { onMounted, ref } from "vue";
import { useStore } from "vuex";

export default {
  name: "TheHeader",
  setup() {
    const store = useStore();
    const isLogin = ref(false);
    const home = ref(false);
    const article = ref(false);
    const setting = ref(false);
    const signIn = ref(false);
    const signUp = ref(false);
    const allHide = () => {
      home.value = false;
      article.value = false;
      setting.value = false;
      signUp.value = false;
      signIn.value = false;
    };

    const selected = (headerName: boolean) => {
      allHide();
      headerName = true;
    };

    onMounted(() => {
      if (store.state.token == "") {
        isLogin.value = false;
      } else {
        isLogin.value = true;
      }
    });

    return {
      isLogin,
      home,
      article,
      setting,
      signIn,
      signUp,
      allHide,
      selected,
    };
  },
};
</script>

<style scoped></style>
