<template>
  <section class="relative w-full h-screen">
    <!-- Background Image -->
    <div
      class="absolute inset-0 bg-cover bg-center"
      :style="{ backgroundImage: `url('/src/assets/bg-certificate.png')` }"
    ></div>

    <!-- Overlay warna biru 10% -->
    <div class="absolute inset-0 bg-[#622EFD] opacity-58"></div>

    <!-- Content Hero -->
    <div class="relative z-10 flex flex-col items-center justify-center h-full text-center px-4">
      <h1 class="text-6xl font-bold text-white mb-4">Sertifikat Digital Terverifikasi</h1>
      <p class="text-white text-lg max-w-xl">Ubah setiap pencapaian menjadi bukti konkret yang tidak terbantahkan & terverifikasi blockchain.</p>
      <a href="#daftar" class="mt-6 px-6 py-3 bg-[#622EFD] text-white rounded-md hover:bg-[#4f23c7] transition">Daftar Sekarang</a>
    </div>
  </section>
</template>

<script setup>
</script>

<style scoped>
/* optional: height full untuk mobile bisa ditambah jika mau */
</style>
