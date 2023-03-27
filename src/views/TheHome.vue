<template>
  <div class="home-page">
    <div class="wrapper d-flex flex-column flex-row-fluid mt-5 mt-lg-12" data-kt-scroll="true"
      data-kt-scroll-activate="{default: false, lg: true}" data-kt-scroll-min-height="auto"
      data-kt-scroll-dependencies="#kt_header" data-kt-scroll-wrappers="#kt_aside" data-kt-scroll-offset="5px"
      id="kt_wrapper" style="min-height: 290px">
      <div class="content flex-column-fluid lh-lg" id="kt_content">
        <div class="toolbar d-flex flex-stack flex-wrap mb-5 mb-lg-7" id="kt_toolbar">
          <div class="page-title d-flex flex-stack flex-grow-1 py-1">
            <h1 class="d-flex align-items-center p-0 my-1">
              <span class="text-dark fw-bolder fs-1"> All Questions </span><small class="text-muted fs-6 fw-bold ms-1">
                (2871) </small>
            </h1>
          </div>
        </div>
        <div class="post" id="kt_post">
          <div>
            <article-list-global v-for="(article, index) in articleLists" :key="article.slug" :article="article">
            </article-list-global>
          </div>
          <pagination-component v-model="currentPage" :numberOfPages="numberOfPages"></pagination-component>
         
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import articleList from "@/components/ArticleListFeed.vue";
import articleListGlobal from "@/components/ArticleListGlobal.vue";
import tagLists from "@/components/TagList.vue";
import pagination from "@/components/PaginationComponent.vue";
import { usePaginationApi } from "@/api/usePaginationAPI";
import { onMounted, ref } from "vue";
import { useStore } from "vuex";
export default {
  name: "TheHome",
  components: {
    "article-list-feed": articleList,
    "article-list-global": articleListGlobal,
    "tag-lists": tagLists,
    "pagination-component": pagination,
  },
  setup() {
    const store = useStore();
    const isLogin = ref(false);
    const feedActive = ref(true);
    const globalActive = ref(false);

    const currentPage = ref(1);
    const rowsPerPage = ref(20);

    const {
      articleLists,
      listsAreLoading,
      isEmpty,
      loadLists,
      feedLists,
      numberOfPages,
    } = usePaginationApi(currentPage, rowsPerPage);

    const feedSelect = async () => {
      feedActive.value = true;
      globalActive.value = false;
      await feedLists();
    };

    const globalSelect = async () => {
      feedActive.value = false;
      globalActive.value = true;
      await loadLists();
    };

    onMounted(async () => {
      isLogin.value = store.state.token ? true : false;
      if (isLogin.value == false) {
        await loadLists();
        globalActive.value = true;
      } else {
        await feedLists();
        feedActive.value = true;
      }
    });

    return {
      listsAreLoading,
      isEmpty,
      isLogin,
      currentPage,
      rowsPerPage,
      numberOfPages,
      feedActive,
      globalActive,
      articleLists,
      feedSelect,
      globalSelect,
    };
  },
};
</script>

<style lang="scss"></style>
