<template>
  <section id="vue_agile">
    <client-only placeholder="Loading...">
      <agile :autoplay="true">
        <div class="slide">
          <img
            class="md:hidden"
            src="@/assets/img/carousel/Phone_android.png"
          />
          <img
            class="hidden md:block"
            src="@/assets/img/carousel/banner-android.png"
          />
        </div>
        <div class="slide">
          <img
            class="md:hidden"
            src="@/assets/img/carousel/Phone_blindspot.png"
          />
          <img
            class="hidden md:block"
            src="@/assets/img/carousel/banner-blindspot.png"
          />
        </div>
        <div class="slide">
          <img
            class="md:hidden"
            src="@/assets/img/carousel/Phone_fittings.png"
          />
          <img
            class="hidden md:block"
            src="@/assets/img/carousel/banner-fittings.png"
          />
        </div>
        <template slot="prevButton">
          <!-- <i class="fas fa-chevron-left"></i>
          <fa class="mr-4 fone_size_1" :icon="['fas', 'fa-chevron-left']" /> -->
        </template>
        <template slot="nextButton">
          <!-- <i class="fas fa-chevron-right"></i>
          <fa class="mr-4 fone_size_1" :icon="['fas', 'fa-chevron-right']" /> -->
        </template>
      </agile>
    </client-only>
  </section>
</template>

<style>
.agile__nav-button {
  background: transparent;
  border: none;
  color: #fff;
  cursor: pointer;
  font-size: 24px;
  height: 100%;
  position: absolute;
  top: 0;
  transition-duration: 0.3s;
  width: 80px;
}
.agile__nav-button:hover {
  background-color: rgba(0, 0, 0, 0.5);
  opacity: 1;
}
.agile__nav-button--prev {
  left: 0;
}
.agile__nav-button--next {
  right: 0;
}
.agile__dots {
  bottom: 50px;
  left: 50%;
  position: absolute;
  transform: translateX(-50%);
}
.agile__dot {
  margin: 0 10px;
}
.agile__dot button {
  background-color: transparent;
  border: 1px solid #fff;
  border-radius: 50%;
  cursor: pointer;
  display: block;
  height: 10px;
  font-size: 0;
  line-height: 0;
  margin: 0;
  padding: 0;
  transition-duration: 0.3s;
  width: 10px;
}
.agile__dot--current button,
.agile__dot:hover button {
  background-color: #fff;
}

.slide {
  display: block;
  width: 100%;
  max-height: 900px;
  /* height: auto; */
  -o-object-fit: cover;
  object-fit: cover;
  object-position: center;
}
.slide img {
  width: 100%;
  max-height: 900px;
}
</style>
