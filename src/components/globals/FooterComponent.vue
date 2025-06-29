<template>
  <footer id="footer" class="bg-bertumbuh-green text-white pt-14 pb-8 px-14">
    <div class="container mx-auto">
      <div class="content flex flex-col gap-6 xl:flex-row justify-between">
        <div class="left-column basis-1/2">
          <LogoWhite :width="100" :height="100" />
        </div>
        <div class="right-column flex flex-col xl:flex-row gap-8 basis-1/2">
          <div class="inner-column basis-full xl:basis-1/4">
            <h4 class="font-semibold">POSTS</h4>

            <nav class="footer-nav mt-5" aria-label="Posts Navigation">
              <ul class="flex flex-col gap-1">
                <li>
                  <RouterLink to="/posts/category=berita">Berita</RouterLink>
                </li>
                <li>
                  <RouterLink to="/event">Berita</RouterLink>
                </li>
                <li>
                  <RouterLink to="/posts/category=blog">Blog</RouterLink>
                </li>
              </ul>
            </nav>
          </div>
          <div class="inner-column basis-full xl:basis-1/4">
            <h4 class="font-semibold">PROGRAM</h4>

            <nav class="footer-nav mt-5" aria-label="Posts Navigation">
              <ul class="flex flex-col gap-1">
                <li>
                  <RouterLink to="/program/jelajah-bersama">Jelajah Bersama</RouterLink>
                </li>
                <li>
                  <RouterLink to="/program/tanam-pohon">Berita</RouterLink>
                </li>
                <li>
                  <RouterLink to="/program/sosialisasi-hutan">Sosialisasi Hutan</RouterLink>
                </li>
              </ul>
            </nav>
          </div>
          <div class="inner-column basis-full xl:basis-1/3">
            <h4 class="font-semibold">ALAMAT</h4>

            <div class="contact flex flex-col gap-2 mt-5">
              <p>
                Jl. Kh. Wahid Hasyim No.76, Cipeujeuh Wetan, Kec. Lemahabang, Kabupaten Cirebon,
                Jawa Barat, 45183
              </p>

              <a href="#">(0231) 635308</a>
              <a href="">surat@smkn1emahabang.sch.id</a>
            </div>
          </div>
        </div>
      </div>
      <div
        class="below-footer flex flex-col gap-6 xl:gap-0 xl:flex-row justify-between items-center mt-10"
      >
        <div class="social-icons flex flex-row gap-5">
          <a>
            <Instagram />
          </a>
          <a>
            <Facebook />
          </a>
          <a>
            <Twitter />
          </a>
          <a>
            <Mail />
          </a>
        </div>
        <div class="copyright">
          <p class="text-center xl:text-right">
            &copy; 2022 BERTUMBUH | SKENSALA - SMKN 1 LEMAHABANG
          </p>
        </div>
      </div>
    </div>
  </footer>
</template>

<script setup lang="ts">
import { RouterLink } from 'vue-router'
import { Instagram, Facebook, Twitter, Mail } from 'lucide-vue-next'
import LogoWhite from '../logos/LogoWhite.vue'
</script>

<style scoped></style>
