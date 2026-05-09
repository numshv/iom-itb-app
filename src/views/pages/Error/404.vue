<template>
  <div class="overflow-hidden">
    <HeaderItem />
  </div>
  <div class="md:py-20 py-10 bg-white flex flex-col items-center justify-center px-[18px] md:px-[70px] text-center">

    <div class="relative mb-4 select-none">
      <span
        class="text-[80px] md:text-[120px] font-[800] leading-none"
        style="color: #003793;"
      >404</span>
    </div>

    <h1
      class="font-[800] text-[20px] md:text-[28px] leading-tight mb-3"
      style="color: #003793;"
    >
      Halaman Tidak Ditemukan
    </h1>
    <p
      class="font-[500] text-[13px] md:text-[14px] opacity-60 mb-8 max-w-[480px]"
      style="color: #003793;"
    >
      {{ message }}
    </p>

    <a
      href="/"
      class="inline-flex items-center gap-2 px-5 py-2.5 text-[14px] font-[600] text-white rounded-full hover:opacity-80 transition-opacity"
      style="background-color: #003793;"
    >
      <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 19l-7-7m0 0l7-7m-7 7h18"/>
      </svg>
      Kembali ke Beranda
    </a>

  </div>
</template>

<script>
import { useMeta } from "vue-meta";
export default {
  name: "PageNotFound",
  props: {
    message: {
      type: String,
      default: "Halaman yang kamu cari tidak ada atau telah dipindahkan.",
    },
  },
  setup() {
    useMeta({ title: "404 - Halaman Tidak Ditemukan" });
  },
};
</script>