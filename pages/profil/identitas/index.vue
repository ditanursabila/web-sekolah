<template>
  <div class="bg-blue-700 p-8 flex items-center justify-center">
    <div class="backdrop-blur-lg mt-10 bg-white/30 rounded-2xl shadow-xl border border-white/20 p-6 max-w-md w-full">
      <div class="text-center mb-6">
        <h2 class="text-2xl font-bold text-white mb-1">Identitas Sekolah</h2>
        <div class="h-1 w-20 bg-sky-300 mx-auto rounded-full"></div>
      </div>

      <div class="space-y-4">
        <div class="bg-sky-300 backdrop-blur-sm rounded-lg p-3 hover:bg-white/30 transition-all duration-300">
          <p class="text-white/70 text-sm">Nama Sekolah</p>
          <p class="text-white font-medium">SMK Negeri 4 Tasikmalaya</p>
        </div>

        <div class="bg-sky-300 backdrop-blur-sm rounded-lg p-3 hover:bg-white/30 transition-all duration-300">
          <p class="text-white/70 text-sm">NPSN</p>
          <p class="text-white font-medium">20276063</p>
        </div>

        <div class="bg-sky-300 backdrop-blur-sm rounded-lg p-3 hover:bg-white/30 transition-all duration-300">
          <p class="text-white/70 text-sm">Nomor Statistik Sekolah</p>
          <p class="text-white font-medium">401327810004</p>
        </div>
        <div class="bg-sky-300 backdrop-blur-sm rounded-lg p-3 hover:bg-white/30 transition-all duration-300">
          <p class="text-white/70 text-sm">Alamat</p>
          <p class="text-white font-medium">Jalan Depok RT 02 RW 05</p>
        </div>

        <div class="bg-sky-300 backdrop-blur-sm rounded-lg p-3 hover:bg-white/30 transition-all duration-300">
          <p class="text-white/70 text-sm">Telepon</p>
          <p class="text-white font-medium">+(62)265312059</p>
        </div>

        <div class="bg-sky-300 backdrop-blur-sm rounded-lg p-3 hover:bg-white/30 transition-all duration-300">
          <p class="text-white/70 text-sm">Email</p>
          <p class="text-white font-medium">info@smkn4tsm.sch.id</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
useHead({
  title: "Identitas",
  meta: [
    {
      name: "description",
      content: "Identitas Page",
    },
  ],
});
</script>
