<template>
  <section>
    <div class="hidden img_box banner md:flex justify-center items-center">
      <p class="text-white text-2xl font-semibold">
        <span class="hover:text-yellow-400 transition-all duration-300"
          ><nuxt-link to="/">首頁</nuxt-link></span
        >
        <span> / </span>
        <span>安卓車框</span>
        <span> / </span>
        <span>{{ breadcrumb }}</span>
      </p>
    </div>
    <!---->
    <div class="container mx-auto px-5 py-20">
      <div
        v-for="(i, idx) in filterData"
        :key="idx"
        class="max-w-5xl mx-auto text-center"
      >
        <!---->
        <div>
          <!---->
          <div class="mb-20">
            <h2 class="text-center text-3xl font-semibold mb-5">
              {{ i.bland }} - {{ i.type }}
            </h2>
            <p class="text-xl font-medium mb-5">
              年份 / {{ i.range }} 、 尺寸 / {{ i.size }}
            </p>
            <img
              :src="require(`@/assets/img/carFrame/${i.img}.png`)"
              :alt="i.bland"
              class="w-full mb-10"
            />
          </div>
          <!---->
          <div v-if="i.attachment.imgs.length > 0" class="mb-20">
            <h2 class="text-center text-3xl font-semibold mb-5">
              產品說明
            </h2>
            <p class="text-xl font-medium mb-5">
              {{ i.attachment.desc }}
            </p>
            <img
              v-for="(img, index) in i.attachment.imgs"
              :key="index"
              :src="require(`@/assets/img/carFrame/${img}.png`)"
              class="w-full"
            />
          </div>
          <!---->
        </div>
      </div>
    </div>
    <!---->
    <div class="container mx-auto px-5 py-10 md:py-20">
      <h2 class="text-center text-3xl font-semibold mb-8">推廌搭配安卓機</h2>
      <div class="lg:grid lg:grid-cols-2 xl:grid-cols-4 gap-8">
        <div v-for="(i, idx) in multimedias" :key="idx" class="col-span-1 py-5">
          <nuxt-link
            :to="{
              name: 'multimediaDetail-id',
              query: {
                id: i.id
              }
            }"
          >
            <img
              :src="require(`@/assets/img/multimedia/${i.img}`)"
              :alt="i.name"
              class="w-full"
            />
          </nuxt-link>
          <h2 class="text-lg font-medium mb-5">
            <fa
              class="text-yellow-400 mr-3"
              :icon="['fas', 'arrow-alt-circle-right']"
            />{{ i.name }}
          </h2>
          <hr class="mb-5" />
          <p class="px-2 py-1">
            <fa
              class="text-xs text-yellow-400 mr-3"
              :icon="['fas', 'dot-circle']"
            />硬體：{{ i.core }}
          </p>
          <p class="px-2 py-1">
            <fa
              class="text-xs text-yellow-400 mr-3"
              :icon="['fas', 'dot-circle']"
            />記憶體：{{ i.memory }}
          </p>
          <p class="px-2 py-1">
            <fa
              class="text-xs text-yellow-400 mr-3"
              :icon="['fas', 'dot-circle']"
            />解析度：{{ i.dpi }}
          </p>
          <p class="px-2 py-1">
            <fa
              class="text-xs text-yellow-400 mr-3"
              :icon="['fas', 'dot-circle']"
            />系統：{{ i.system }}
          </p>
          <p class="px-2 py-1">
            <fa
              class="text-xs text-yellow-400 mr-3"
              :icon="['fas', 'dot-circle']"
            />DSP：{{ i.dsp }}
          </p>
          <p class="px-2 py-1">
            <fa
              class="text-xs text-yellow-400 mr-3"
              :icon="['fas', 'dot-circle']"
            />建議售價：{{ i.price }}
          </p>
        </div>
      </div>
    </div>
    <!---->
  </section>
</template>

<script>
import multimedias from "~/static/multimedias.js";
import carFrame from "~/static/carFrame.js";
export default {
  name: "multimediaDetail-id",
  data() {
    return {
      multimedias,
      carFrame,
      filterData: [],
      breadcrumb: ""
    };
  },
  mounted() {
    // console.log(this.$route.query.img);
    this.filterData = this.carFrame.filter(
      item => item.img == this.$route.query.img
    );
    this.breadcrumb = this.filterData[0].bland;
  }
};
</script>

<style scoped>
.banner {
  background-image: url(~assets/img/carFrame/banner.png);
}
@media (min-width: 640px) {
}
@media (min-width: 768px) {
}
@media (min-width: 1024px) {
}
@media (min-width: 1280px) {
}
@media (min-width: 1536px) {
}
</style>
