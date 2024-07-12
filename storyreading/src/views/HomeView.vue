<template>
  <div class="home">
    <HeaderPage />
    <SlideShow />
    <SearchMobile />
    <NavbarMobile />
    <BannerDownload />
    <NewUpdateMobileVue />
    <TopView />
    <RecommendStory />
    <CompletedStory />
    <Footer />
  </div>
</template>

<script>
// Importing components
import HeaderPage from "@/components/Header/Header2.vue";
import SlideShow from "@/components/Slide/Slide.vue";
import SearchMobile from "@/components/SearchMobile/SearchMobile.vue";
import NavbarMobile from "@/components/Navbar/NavbarMobile.vue";
import NewUpdateMobileVue from "../components/NewUpdate/NewUpdateMobile.vue";
import TopView from "../components/TopView/TopView.vue";
import RecommendStory from "../components/RecommendStory/RecommendStory.vue";
import CompletedStory from "../components/CompletedStory/CompletedStory.vue";
import Footer from "../components/Footer/Footer.vue";
import BannerDownload from "../components/Banner/BannerDownload.vue";
export default {
  name: "HomeView",
  components: {
    HeaderPage,
    SearchMobile,
    SlideShow,
    NavbarMobile,
    NewUpdateMobileVue,
    TopView,
    RecommendStory,
    CompletedStory,
    Footer,
    BannerDownload,
  },
};
</script>
