<template>
  <section>
    <footer class="py-12 text-white flex justify-center">
      <div class="container mx-auto p-5">
        <div class="hidden lg:grid grid-cols-12 gap-5 mb-5">
          <div class="col-span-4">
            <div>
              <img
                class="w-3/5 mb-5"
                src="~/assets/img/Header/meimai.svg"
                alt="meimai"
              />
              <p class="text-xl font-medium mb-2">
                Mei-Mai Vechicle electronic LTD.
              </p>
              <div>
                <a
                  class="text-xl icons"
                  href="https://www.facebook.com/MEIMAI.MM"
                  target="_bland"
                  ><fa class="mr-4 fone_size_1" :icon="['fab', 'facebook']"
                /></a>
                <a
                  class="text-xl icons"
                  href="https://www.instagram.com/mm_meimai/"
                  target="_bland"
                  ><fa class="mr-4 fone_size_1" :icon="['fab', 'instagram']"
                /></a>
                <a
                  class="text-xl icons"
                  href="https://www.youtube.com/channel/UCmOgNguLmmeNdXu_hgVPBSw"
                  target="_bland"
                  ><fa class="mr-4 fone_size_1" :icon="['fab', 'youtube']"
                /></a>
              </div>
            </div>
          </div>
          <div class="col-span-4">
            <p class="mb-3">03-2170098</p>
            <p class="mb-3">mm08168168@gmail.com</p>
            <p class="mb-3">桃園市桃園區中信里國信街35號（總公司）</p>
          </div>
          <div class="col-span-4">
            <div>
              <div
                class="fb-page"
                data-href="https://www.facebook.com/MM.MEIMAI"
                data-tabs="timeline"
                data-width="400"
                data-height="200"
                data-small-header="true"
                data-adapt-container-width="true"
                data-hide-cover="false"
                data-show-facepile="true"
              >
                <blockquote
                  cite="https://www.facebook.com/MM.MEIMAI"
                  class="fb-xfbml-parse-ignore"
                >
                  <a href="https://www.facebook.com/MM.MEIMAI"
                    >MEIMAI美邁車用電子有限公司</a
                  >
                </blockquote>
              </div>
            </div>
          </div>
        </div>
        <hr class="hidden lg:block mb-5 border-gray-500" />
        <div>
          <p class="text-center text-white mb-0">
            Copyright © 2022 MEIMAI. All Rights Reserved
          </p>
        </div>
      </div>
    </footer>
    <!--facebook-->
    <div id="fb-root"></div>
  </section>
</template>

<style scoped>
footer {
  /* background-color: rgba(12, 21, 48, 1); */
  background-color: rgba(13, 0, 43, 1);
}
.icons {
  color: rgba(236, 167, 44, 1);
}
a {
  color: rgba(255, 255, 255, 1);
  text-decoration: none;
  transition: all 0.3s;
}
a:hover {
  color: rgba(243, 182, 31, 1);
}
</style>
