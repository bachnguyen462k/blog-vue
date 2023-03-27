<template>
<div id="kt_aside" class="aside" data-kt-drawer="true" data-kt-drawer-name="aside"
                    data-kt-drawer-activate="{default: true, lg: false}" data-kt-drawer-overlay="true"
                    data-kt-drawer-width="{default:'200px', '300px': '225px'}" data-kt-drawer-direction="start"
                    data-kt-drawer-toggle="#kt_aside_mobile_toggle" data-kt-sticky="true"
                    data-kt-sticky-name="aside-sticky" data-kt-sticky-offset="{default: false, lg: '0px'}"
                    data-kt-sticky-release-offset="{lg: '600px'}" data-kt-sticky-width="{lg: '225px'}"
                    data-kt-sticky-left="auto" data-kt-sticky-top="94px" data-kt-sticky-animation="false"
                    data-kt-sticky-zindex="95">
                    <div class="hover-scroll-overlay-y my-5 my-lg-5 w-100 ps-4 ps-lg-0 pe-4 me-1"
                        id="kt_aside_menu_wrapper" data-kt-scroll="true"
                        data-kt-scroll-activate="{default: false, lg: true}" data-kt-scroll-height="auto"
                        data-kt-scroll-dependencies="#kt_header" data-kt-scroll-wrappers="#kt_aside"
                        data-kt-scroll-offset="5px">
                        <div class="menu menu-column menu-active-bg menu-hover-bg menu-title-gray-700 fs-5 menu-rounded w-100"
                            id="#kt_aside_menu" data-kt-menu="true">
                            <div class="menu-item">
                                <div class="menu-content pb-2"><span
                                        class="menu-section text-muted text-uppercase fs-7 fw-bolder">Public</span>
                                </div>
                            </div>
                            <div class="menu-item"><a href="https://devs.keenthemes.com" class="menu-link "><span
                                        class="menu-title">All Questions</span><span class="menu-badge">2,804</span></a>
                            </div>
                            <div class="menu-item"><a href="https://devs.keenthemes.com/popular"
                                    class="menu-link "><span class="menu-title">Popular</span></a></div>
                            <div class="menu-item"><a href="https://devs.keenthemes.com/tags" class="menu-link "><span
                                        class="menu-title">Tags</span></a></div>
                            <div class="menu-item pt-5">
                                <div class="menu-content pb-2"><span
                                        class="menu-section text-muted text-uppercase fs-7 fw-bolder">My Activity</span>
                                </div>
                            </div>
                            <div class="menu-item"><a href="https://devs.keenthemes.com/my-question"
                                    class="menu-link "><span class="menu-title">My Questions</span><span
                                        class="menu-badge"></span></a></div>
                            <div class="menu-item"><a href="https://devs.keenthemes.com/enrolled"
                                    class="menu-link "><span class="menu-title">Enrolled</span><span
                                        class="menu-badge"></span></a></div>
                            <div class="menu-item"><a href="https://devs.keenthemes.com/saved" class="menu-link "><span
                                        class="menu-title">Saved</span><span class="menu-badge"></span></a></div>
                            <div class="menu-item pt-5">
                                <div class="menu-content pb-2"><span
                                        class="menu-section text-muted text-uppercase fs-7 fw-bolder">Categories</span>
                                </div>
                            </div>
                            <div class="menu-item"><a href="https://devs.keenthemes.com/categories/suggestions"
                                    class="menu-link "><span class="menu-title">Suggestions</span><span
                                        class="menu-badge">83</span></a></div>
                            <div class="menu-item"><a href="https://devs.keenthemes.com/categories/pre-sale-questions"
                                    class="menu-link "><span class="menu-title">Pre-sale Questions</span><span
                                        class="menu-badge">117</span></a></div>
                            <div class="menu-item"><a href="https://devs.keenthemes.com/categories/metronic"
                                    class="menu-link active"><span class="menu-title">Metronic</span><span
                                        class="menu-badge">2,331</span></a></div>
                            <div class="menu-item"><a href="https://devs.keenthemes.com/categories/getbootstrap"
                                    class="menu-link "><span class="menu-title">Getbootstrap</span><span
                                        class="menu-badge">58</span></a></div>
                            <div class="menu-item"><a href="https://devs.keenthemes.com/categories/market"
                                    class="menu-link "><span class="menu-title">KeenThemes Market</span><span
                                        class="menu-badge">53</span></a></div>
                        </div>
                    </div>
                </div>
  </template>
  
  <script lang="ts">
  export default {
    name: "TheAside"
  }
  </script>
  
  <style scoped>
  
  </style>