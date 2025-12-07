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

    <!-- Section: How Certifyme Works -->
    <section class="py-32 bg-gray-50 relative">
    
      <!-- Title with background card -->
    <div class="flex justify-center mb-20">
      <div class="rounded-[60px] px-12 py-8" style="background-color: rgba(98, 46, 253, 0.1);">
        <h2 class="text-center text-5xl font-bold text-[#622EFD]">How Certifyme Works</h2>
      </div>
    </div>

      <!-- Cards Container -->
      <div class="flex flex-col items-center gap-10">
        <!-- Card 1 -->
        <div class="w-[90%] max-w-[1000px] bg-white border-2 border-[#622EFD] rounded-[10px] p-6 shadow-md relative min-h-[150px]">
          <img src="/src/assets/institusi.png" alt="Institusi Logo" class="w-16 h-16 mb-4">
          <h3 class="text-xl font-bold mb-2">1. Institusi Menerbitkan</h3>
          <p class="text-gray-700">Organisasi/kampus menerbitkan sertifikat langsung ke blockchain dengan validasi otomatis.</p>
        </div>

        <!-- Card 2 -->
        <div class="w-[90%] max-w-[1000px] bg-white border-2 border-[#622EFD] rounded-[10px] p-6 shadow-md relative min-h-[150px]">
          <img src="/src/assets/mahasiswa.png" alt="Mahasiswa Logo" class="w-16 h-16 mb-4">
          <h3 class="text-xl font-bold mb-2">2. Mahasiswa menerima</h3>
          <p class="text-gray-700">Sertifikat otomatis masuk ke portofolio digital yang bisa dibagikan ke publik.</p>
        </div>

        <!-- Card 3 -->
        <div class="w-[90%] max-w-[1000px] bg-white border-2 border-[#622EFD] rounded-[10px] p-6 shadow-md relative min-h-[150px]">
          <img src="/src/assets/verifikasi.png" alt="Verifikasi Logo" class="w-16 h-16 mb-4">
          <h3 class="text-xl font-bold mb-2">3. Verifikasi Instan</h3>
          <p class="text-gray-700">Perekrut dapat memverifikasi keaslian sertifikat dalam hitungan detik.</p>
        </div>
      </div>
    </section>

    <!-- WHY CERTIFYME IS QUALIFIED SECTION -->
    <section class="w-full py-24 relative" style="background-color: rgba(98,46,253,0.1);">
      <div class="max-w-7xl mx-auto flex justify-center items-center px-6 md:px-0 space-x-12">

        <!-- Logo Medal -->
        <div class="flex-shrink-0">
          <img src="/src/assets/icon-medal.png" alt="Medal" class="w-100 h-100 object-contain"/>
        </div>

        <!-- Text Content -->
        <div class="max-w-xl text-left">
          <!-- Title -->
          <h2 class="text-5xl font-bold text-[#622EFD] leading-snug mb-6">
            WHY CERTIFYME<br/>
            IS QUALIFIED
          </h2>

          <!-- Paragraph -->
          <p class="text-black text-lg leading-relaxed">
            Certifyme dikembangkan oleh tim berpengalaman di edutech. Kami membantu institusi menerbitkan sertifikat cepat dan aman. Peserta langsung mendapat bukti kredibel, dan perekrut dapat memverifikasi keasliannya dalam detik. Sistem kami memastikan setiap sertifikat selalu valid dan terpercaya.
          </p>
        </div>

      </div>
    </section>

    <!-- PRICING SECTION -->
    <section class="w-full bg-white py-24">
      <div class="max-w-7xl mx-auto text-center px-6">
        <!-- Title -->
        <h2 class="text-5xl font-bold text-[#622EFD] mb-4">
          Pilih Paket yang Tepat untuk Anda
        </h2>
        <p class="text-black text-lg mb-12">
          Mulai gratis, upgrade kapan saja. Tidak ada biaya tersembunyi
        </p>

        <!-- Cards -->
        <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-10">
          
          <!-- Card 1: Pioneer -->
          <div class="border-3 border-black rounded-[20px] p-8 flex flex-col items-start">
          <h3 class="font-bold text-3xl mb-2">Pioneer</h3>
      
          <!-- Harga -->
          <p class="text-2xl font-bold mb-1 inline">
            RP 0
            <span class="font-normal"> / bulan</span>
          </p>
          
          <!-- Subtext -->
          <p class="text-sm text-black mb-4">Untuk mahasiswa & freelancer</p>
          <button class="w-full py-3 border border-black text-black font-semibold rounded-md mb-4 hover:bg-black hover:text-white transition">
            Mulai Gratis
          </button>
            <hr class="w-full border-gray-500 mb-4" />
            <ul class="space-y-2 text-left w-full">
              <li class="flex items-center">
                <img src="/src/assets/ceklis.png" alt="Ceklis" class="w-4 h-4 mr-2" />
                1 sertifikat/bulan
              </li>
              <li class="flex items-center">
                <img src="/src/assets/ceklis.png" alt="Ceklis" class="w-4 h-4 mr-2" />
                Portofolio publik
              </li>
              <li class="flex items-center">
                <img src="/src/assets/ceklis.png" alt="Ceklis" class="w-4 h-4 mr-2" />
                Verifikasi instan
              </li>
              <li class="flex items-center">
                <img src="/src/assets/ceklis.png" alt="Ceklis" class="w-4 h-4 mr-2" />
                Watermark Certifyme
              </li>
            </ul>
          </div>

          <!-- Card 2: Bishop -->
         <div class="relative border-3 border-[#622EFD] rounded-[20px] p-8 flex flex-col items-start">
          <!-- Populer Label -->
          <div class="absolute top-0 right-0 bg-[#622EFD] text-white text-xs px-3 py-1 rounded-tr-[20px] rounded-bl-none rounded-tl-none rounded-br-[0px]">
            Populer
          </div>

          <!-- Title -->
          <h3 class="font-bold text-3xl mb-2">Bishop</h3>

          <!-- Harga -->
          <p class="text-2xl font-bold mb-1 inline">
            RP 49K
            <span class="font-normal"> / bulan</span>
          </p>

          <!-- Subtext -->
          <p class="text-sm text-black mb-4">Untuk Konten Kreator & Kursus Kecil</p>

          <!-- Button full width sesuai card -->
          <button class="w-full py-3 bg-[#622EFD] border border-black text-white font-semibold rounded-md mb-4 hover:bg-[#4a21b8] transition">
            Mulai Bishop
          </button>
            <hr class="w-full border-gray-500 mb-4" />
            <ul class="space-y-2 text-left w-full">
              <li class="flex items-center">
                <img src="/src/assets/ceklis.png" alt="Ceklis" class="w-4 h-4 mr-2" />
                10 Sertifikat/bulan
              </li>
              <li class="flex items-center">
                <img src="/src/assets/ceklis.png" alt="Ceklis" class="w-4 h-4 mr-2" />
                Semua fitur Pioneer
              </li>
              <li class="flex items-center">
                <img src="/src/assets/ceklis.png" alt="Ceklis" class="w-4 h-4 mr-2" />
                Template premium
              </li>
              <li class="flex items-center">
                <img src="/src/assets/ceklis.png" alt="Ceklis" class="w-4 h-4 mr-2" />
                Prioritas Email
              </li>
              <li class="flex items-center">
                <img src="/src/assets/ceklis.png" alt="Ceklis" class="w-4 h-4 mr-2" />
                Tanpa Watermark
              </li>
            </ul>
          </div>

          <!-- Card 3: King -->
          <div class="border-3 border-black rounded-[20px] p-8 flex flex-col items-start">
          <h3 class="font-bold text-3xl mb-2">King</h3>
      
          <!-- Harga -->
          <p class="text-2xl font-bold mb-1 inline">
            RP 349K
            <span class="font-normal"> / bulan</span>
          </p>
          
          <!-- Subtext -->
          <p class="text-sm text-black mb-4">Untuk Lembaga pendidikan, Bootcamp</p>
          <button class="w-full py-3 border border-black text-black font-semibold rounded-md mb-4 hover:bg-black hover:text-white transition">
            Mulai King
          </button>
            <hr class="w-full border-gray-500 mb-4" />
            <ul class="space-y-2 text-left w-full">
              <li class="flex items-center">
                <img src="/src/assets/ceklis.png" alt="Ceklis" class="w-4 h-4 mr-2" />
                500 Sertifikat/bulan
              </li>
              <li class="flex items-center">
                <img src="/src/assets/ceklis.png" alt="Ceklis" class="w-4 h-4 mr-2" />
                Semua fitur Bishop
              </li>
              <li class="flex items-center">
                <img src="/src/assets/ceklis.png" alt="Ceklis" class="w-4 h-4 mr-2" />
                Bulk Upload (CSV)
              </li>
              <li class="flex items-center">
                <img src="/src/assets/ceklis.png" alt="Ceklis" class="w-4 h-4 mr-2" />
                Dashboard Analytics
              </li>
              <li class="flex items-center">
                <img src="/src/assets/ceklis.png" alt="Ceklis" class="w-4 h-4 mr-2" />
                Custom template & watermark
              </li>
              <li class="flex items-center">
                <img src="/src/assets/ceklis.png" alt="Ceklis" class="w-4 h-4 mr-2" />
                Pengelolaan 5 akun admin
              </li>
              <li class="flex items-center">
                <img src="/src/assets/ceklis.png" alt="Ceklis" class="w-4 h-4 mr-2" />
                Akses API dasar (untuk integrasi)
              </li>
            </ul>
          </div>
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
