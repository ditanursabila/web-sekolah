<template>
  <div class="relative w-full h-screen overflow-hidden">
    <div class="absolute inset-0">
      <video class="w-full h-full object-cover pointer-events-none" autoplay loop muted playsinline>
        <source src="~/assets/vidio/vid.mp4" type="video/mp4" />
      </video>
    </div>

    <div class="relative z-10 h-full bg-black bg-opacity-50">
      <div class="flex items-center justify-center h-full">
        <div class="text-white text-center px-4">
          <h1 class="font-bold text-2xl md:text-3xl lg:text-4xl mb-2">SELAMAT DATANG</h1>
          <h2 class="font-semibold text-lg md:text-xl lg:text-2xl">Di Website SMK Negeri 4 Tasikmalaya</h2>
          <h3 class="font-semibold text-lg md:text-xl lg:text-2xl mt-3 text-white border-t border-b border-white py-3 px-6 inline-block">SMK Pusat Keunggulan</h3>
        </div>
      </div>
      <Sosmed />
    </div>
  </div>
</template>
