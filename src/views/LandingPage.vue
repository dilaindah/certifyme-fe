<template>
  <div class="w-full">

    <!-- Navbar -->
    <Navbar />

    <!-- HERO SECTION -->
    <section class="relative w-full h-screen">
      
      <!-- Background Image -->
      <div
        class="absolute inset-0 bg-cover bg-center"
        :style="{ backgroundImage: `url('/src/assets/bg-certificate.png')` }"
      ></div>

      <!-- Overlay warna biru -->
      <div class="absolute inset-0 bg-[#622EFD] opacity-60"></div>

      <!-- Content Hero -->
      <div
        class="relative z-10 flex flex-col items-center justify-center h-full text-center px-4"
      >
        <h1 class="text-6xl font-bold text-white mb-4">
          Sertifikat Digital Terverifikasi
        </h1>

        <p class="text-white text-lg max-w-xl">
          Ubah setiap pencapaian menjadi bukti konkret yang tidak terbantahkan &
          terverifikasi blockchain.
        </p>

        <!-- Button Group -->
        <div class="mt-6 flex space-x-4">
          <!-- Mulai Gratis -->
          <a
            href="/register"
            class="px-6 py-3 bg-white text-[#622EFD] rounded-md font-semibold hover:bg-[#E9DEFF] transition"
          >
            Mulai Gratis
          </a>

          <!-- Lihat Demo -->
          <a
            href="/demo"
            class="px-6 py-3 bg-transparent border border-white text-white rounded-md font-semibold hover:bg-white hover:text-[#622EFD] transition"
          >
            Lihat Demo
          </a>
        </div>
      </div>
    </section>

    <!-- TESTIMONIAL SECTION -->
    <section class="w-full bg-white py-24 relative overflow-hidden">
      
      <!-- Dekorasi Ellipse kiri atas -->
      <img 
        src="/src/assets/Ellipse4.png"
        alt=""
        class="absolute top-0 left-0 w-40 h-60"
      />

      <!-- Dekorasi Ellipse kanan bawah -->
      <img 
        src="/src/assets/Ellipse5.png"
        alt=""
        class="absolute bottom-0 right-0 w-40 h-60"
      />

      <!-- Title -->
      <h2 class="text-center text-5xl font-bold text-[#622EFD] mb-20">
        Hear From Our Users
      </h2>

      <!-- Cards -->
      <div
        class="max-w-6xl mx-auto grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-10 px-6"
      >
        <!-- Card -->
        <div
          v-for="(item, i) in testimonials"
          :key="i"
          class="rounded-[50px] p-8 bg-gradient-to-b from-[#3A1C97] to-[#622EFD] shadow-[0_35px_70px_rgba(98,46,253,0.60)] text-center"
        >
          <img
            :src="item.photo"
            alt="User"
            class="w-20 h-20 rounded-full mx-auto mb-4 border-4 border-white/20"
          />

          <h3 class="text-white font-semibold text-lg mb-2">
            {{ item.name }}
          </h3>

          <div class="flex justify-center mb-4">
          <span class="text-yellow-400 text-xl mx-0.5">★</span>
          <span class="text-yellow-400 text-xl mx-0.5">★</span>
          <span class="text-yellow-400 text-xl mx-0.5">★</span>
          <span class="text-yellow-400 text-xl mx-0.5">★</span>
          <span class="text-yellow-400 text-xl mx-0.5">★</span>
          </div>

          <p class="text-white/90 text-sm leading-relaxed">
            "{{ item.text }}"
          </p>
        </div>
      </div>
    </section>

    
  </div>
</template>

<script setup>
import Navbar from '../components/Navbar.vue'

const testimonials = [
  {
    name: "Monica",
    text: "Platform paling praktis untuk kirim sertifikat ke peserta kelas. Hemat waktu banget!",
    photo: "https://randomuser.me/api/portraits/women/44.jpg",
  },
  {
    name: "Steven",
    text: "Gampang banget nerima sertifikat dari event kampus.",
    photo: "https://randomuser.me/api/portraits/men/32.jpg",
  },
  {
    name: "Sanya Paramitha",
    text: "Verifikasinya cepat, bantu kami cek keaslian kandidat dengan sekali klik.",
    photo: "https://randomuser.me/api/portraits/women/68.jpg",
  },
];
</script>

<style scoped>
</style>
