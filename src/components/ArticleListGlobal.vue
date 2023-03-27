<template>
  <div class="mb-10">
    <div class="mb-0">
      <div class="d-flex align-items-center mb-2 mb-lg-3">
        <a class="fs-2 fw-bolder text-gray-900 text-hover-primary me-1" data-question-id="3363" href="javascript:(0)"
          @click="showArticle(article.slug)">
          {{ article.title }}
        </a>
        <div class="d-flex align-items-center flex-grow-1 lh-1 flex-shrink-0">
          <div class="me-2 flex-shrink-0">
            <span class="ms-1" data-bs-toggle="tooltip" title="" data-bs-original-title="Pinned question"
              aria-label="Pinned question"><span class="svg-icon svg-icon-primary svg-icon-1"><svg
                  xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none">
                  <path opacity="0.3"
                    d="M5.78001 21.115L3.28001 21.949C3.10897 22.0059 2.92548 22.0141 2.75004 21.9727C2.57461 21.9312 2.41416 21.8418 2.28669 21.7144C2.15923 21.5869 2.06975 21.4264 2.0283 21.251C1.98685 21.0755 1.99507 20.892 2.05201 20.7209L2.886 18.2209L7.22801 13.879L10.128 16.774L5.78001 21.115Z"
                    fill="black"></path>
                  <path
                    d="M21.7 8.08899L15.911 2.30005C15.8161 2.2049 15.7033 2.12939 15.5792 2.07788C15.455 2.02637 15.3219 1.99988 15.1875 1.99988C15.0531 1.99988 14.92 2.02637 14.7958 2.07788C14.6717 2.12939 14.5589 2.2049 14.464 2.30005L13.74 3.02295C13.548 3.21498 13.4402 3.4754 13.4402 3.74695C13.4402 4.01849 13.548 4.27892 13.74 4.47095L14.464 5.19397L11.303 8.35498C10.1615 7.80702 8.87825 7.62639 7.62985 7.83789C6.38145 8.04939 5.2293 8.64265 4.332 9.53601C4.14026 9.72817 4.03256 9.98855 4.03256 10.26C4.03256 10.5315 4.14026 10.7918 4.332 10.984L13.016 19.667C13.208 19.859 13.4684 19.9668 13.74 19.9668C14.0115 19.9668 14.272 19.859 14.464 19.667C15.3575 18.77 15.9509 17.618 16.1624 16.3698C16.374 15.1215 16.1932 13.8383 15.645 12.697L18.806 9.53601L19.529 10.26C19.721 10.452 19.9814 10.5598 20.253 10.5598C20.5245 10.5598 20.785 10.452 20.977 10.26L21.7 9.53601C21.7952 9.44108 21.8706 9.32825 21.9221 9.2041C21.9737 9.07995 22.0002 8.94691 22.0002 8.8125C22.0002 8.67809 21.9737 8.54505 21.9221 8.4209C21.8706 8.29675 21.7952 8.18392 21.7 8.08899Z"
                    fill="black"></path>
                </svg></span></span><span class="ms-1" data-bs-toggle="tooltip" title=""
              data-bs-original-title="Unresolved" aria-label="Unresolved"><span
                class="svg-icon svg-icon-warning svg-icon-1"><svg xmlns="http://www.w3.org/2000/svg" width="24"
                  height="24" viewBox="0 0 24 24" fill="none">
                  <rect opacity="0.3" x="2" y="2" width="20" height="20" rx="10" fill="black"></rect>
                  <rect x="11" y="14" width="7" height="2" rx="1" transform="rotate(-90 11 14)" fill="black">
                  </rect>
                  <rect x="11" y="17" width="2" height="2" rx="1" transform="rotate(-90 11 17)" fill="black">
                  </rect>
                </svg></span></span>
          </div>
        </div>
      </div>
      <div class="fs-6 fw-normal text-gray-800 mb-3 mb-lg-4 overflow-hidden">
        {{ article.description }}
      </div>
      <div class="d-flex flex-stack flex-wrap">
        <a href="javascript:(0)" @click="showArticle(article.slug)">
          <div class="d-flex align-items-center py-1">
            <div class="symbol symbol-30px me-2">
              <div class="symbol-label fs-3 lh-1 fw-bold text-uppercase bg-primary text-inverse-primary">
                <a href="javascript:(0)" @click="showProfile(article.author.username)"><img
                    :src="article.author.image" /></a>
              </div>
            </div>
            <div class="d-flex flex-column align-items-start justify-content-center">
              <span class="d-flex align-items-center text-gray-900 fs-7 fw-bolder lh-1 mb-2">
                <a class="author" href="javascript:void(0)" @click="showProfile(article.author.username)">{{
                  article.author.username }}</a>
                <span class="badge badge-success fs-9 fw-bold px-2 py-1 h-auto ms-2 rounded-1" data-bs-toggle="tooltip"
                  title="" data-bs-original-title="Keenthemes team">Author</span></span><span
                class="text-muted fs-8 fw-bold lh-1" data-bs-toggle="tooltip" data-bs-dismiss="click" title=""
                data-bs-original-title="10 Jan, 2023 11:48 AM UTC">{{ convertDate(article.createdAt) }}</span>
            </div>
          </div>
        </a>
        <div class="d-flex align-items-center py-1">
          <a href="https://devs.keenthemes.com/question/junmid-full-stack-reactvue-developer-needed#answers"
            data-kt-scroll-toggle="true"
            class="btn btn-sm btn-flex btn-color-gray-500 btn-outline btn-outline-dashed btn-outline-default h-30px px-4 me-2"
            data-bs-toggle="tooltip" data-bs-dismiss="click" title="" data-bs-original-title="By Daniel 6 days ago">
            13 Answers </a><a href="https://devs.keenthemes.com/tags/react"
            class="btn btn-flex btn-sm btn-color-gray-500 btn-bg-light btn-active-primary px-4 me-2 h-30px">
            React </a><a href="https://devs.keenthemes.com/tags/vue"
            class="btn btn-flex btn-sm btn-color-gray-500 btn-bg-light btn-active-primary px-4 me-2 h-30px">
            Vue </a><a href="#" title=""
            data-action="https://devs.keenthemes.com/saved/junmid-full-stack-reactvue-developer-needed" data-method="put"
            data-csrf="faRQAsBBaw0vMuGeJm02UeUK7tYaEH0Js2sNN4Ah"
            data-success-text="The question has been successfully saved" data-bs-toggle="tooltip" data-bs-dismiss="click"
            class="btn btn-sm btn-icon btn-color-gray-500 btn-bg-light btn-active-primary h-30px w-30px me-2 save-ajax"
            data-bs-original-title="Save" aria-label="Save"><span class="svg-icon svg-icon-3"><svg
                xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none">
                <path
                  d="M16.0077 19.2901L12.9293 17.5311C12.3487 17.1993 11.6407 17.1796 11.0426 17.4787L6.89443 19.5528C5.56462 20.2177 4 19.2507 4 17.7639V5C4 3.89543 4.89543 3 6 3H17C18.1046 3 19 3.89543 19 5V17.5536C19 19.0893 17.341 20.052 16.0077 19.2901Z"
                  fill="black"></path>
              </svg></span></a><span
            class="btn btn-sm btn-icon btn-color-gray-500 btn-bg-light btn-active-primary ps-3 pe-2 me-2 h-30px w-30px btn-active cursor-default"
            data-bs-toggle="tooltip" title="" data-bs-original-title="Upvotes"><span data-element="count">1</span><span
              class="svg-icon svg-icon-6 m-0 p-0"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24"
                viewBox="0 0 24 24" fill="none">
                <path opacity="0.5" d="M13 9.59998V21C13 21.6 12.6 22 12 22C11.4 22 11 21.6 11 21V9.59998H13Z"
                  fill="black"></path>
                <path
                  d="M5.7071 7.89291C5.07714 8.52288 5.52331 9.60002 6.41421 9.60002H17.5858C18.4767 9.60002 18.9229 8.52288 18.2929 7.89291L12.7 2.3C12.3 1.9 11.7 1.9 11.3 2.3L5.7071 7.89291Z"
                  fill="black"></path>
              </svg></span></span>
        </div>
      </div>
    </div>
    <div class="separator separator-dashed border-gray-400 opacity-50 my-5 my-lg-8"></div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import router from "@/router";
import convertDate from '@/ts/common';
import { useStore } from "vuex";
import { favoriteArticle, unFavoriteArticle } from "@/api";

export default defineComponent({
  name: "ArticleListGlobal",
  props: {
    index: Number,
    article: {
      type: Object,
      default: () => {
        return {
          slug: "",
          title: "",
          description: "",
          favorited: false,
          favoritesCount: 0,
          createdAt: "",
          author: {
            username: "",
            image: ""
          }
        }
      }
    }
  },
  setup(props) {
    const store = useStore();
    const token = store.state.token;

    const showProfile = (username: string) => {
      router.push({
        name: 'Profile',
        params: { username: username }
      })
    }

    const showArticle = (slug: string) => {
      router.push({
        name: 'ArticleDetail',
        params: { slug: slug }
      })
    }

    const changeFavorite = async (slug: string, favorite: boolean) => {
      if (token == '') {
        await router.push({ name: "Login" });
        return;
      } else {
        if (favorite) {
          const { data } = await unFavoriteArticle(slug);
          props.article.favoritesCount = data.article.favoritesCount;
          props.article.favorited = data.article.favorited;
        } else {
          const { data } = await favoriteArticle(slug);
          props.article.favoritesCount = data.article.favoritesCount;
          props.article.favorited = data.article.favorited;
        }
      }
    }

    return { convertDate, changeFavorite, showProfile, showArticle }
  }
})
</script>

<style scoped></style>