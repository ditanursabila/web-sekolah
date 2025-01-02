<template>
  <div class="contaner-fluid">
    <div>
      <CoverVidio />
    </div>

    <!-- sambutan -->
    <div class="grid md:grid-cols-2 grid-cols-1 pt-10 md:pt-20 bg-blue-700 mt-10 px-4 md:px-8 gap-8 pb-10">
      <div class="flex flex-col items-center">
        <div class="w-full max-w-md flex flex-col items-center space-y-2">
          <img src="~/assets/img/kepalasekolah.png" alt="Kepala Sekolah" />
        </div>
      </div>

      <div class="mt-4 md:mt-10">
        <div class="block p-4 md:p-6 border border-gray-200 rounded-lg shadow">
          <h5 class="mb-4 md:mb-5 text-2xl md:text-4xl text-center font-bold tracking-tight text-white">Sambutan Kepala Sekolah</h5>
          <p class="font-normal text-justify text-white text-sm md:text-base leading-relaxed">
            Assalamualaikum Warahmatullahi Wabarakatuh
            <br />
            Selamat datang di SMKN 4 Tasikmalaya. Segala puji dan syukur kita panjatkan kehadirat Allah SWT, semoga kita semua ada dalam lindungan-Nya. Dan atas perkenan-Nya pula kami dapat menghadirkan website SMK Negeri 4 Tasikmalaya ini.
            Kami berharap dengan adanya website di SMK Negeri 4 Tasikmalaya ini para pengunjung dapat mengenal lebih jauh tentang sekolah kami sehingga dapat mempererat tali silaturrahmi antara sekolah dengan masyarakat demi kemajuan kita
            bersama. Tiada gading yang tak retak, website kami ini masih dalam proses pengembangan, masih banyak kekurangan yang harus kami perbaiki. Kritik dan sarannya yang membangun sangat kami harapkan untuk pengembangan ke depan.
            Akhirnya, saya mengucapkan terimakasih yang sebesar-besarnya kepada semua pihak yang tidak dapat disebutkan satu segala bantuan dan persatu atas fasilitasnya yang telah diberikan semoga semua yang kita lakukan bermanfaat bagi
            masyarakat. Wassalamu'alaikum Warahmatullahi Wabarakatuh.
          </p>
        </div>
      </div>
    </div>
    <div>
      <Informasi />
    </div>

    <div class="bg-blue-700">
      <Berita :isHomePage="true" />

      <div class="text-center">
        <NuxtLink to="/berita" class="text-white mb-5 font-semibold border border-sky-300 py-2 px-5 hover:px-6 rounded-full inline-flex items-center group transform hover:text-primary hover:-translate-y-1 duration-200"
          >Lihat Semua Berita
          <svg class="w-4 h-4 ml-1 transform group-hover:translate-x-2 duration-200" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14 5l7 7m0 0l-7 7m7-7H3"></path>
          </svg>
        </NuxtLink>
      </div>
    </div>

    <div class="bg-blue-100">
      <Galeri :isHomePage="true" />

      <div class="text-center">
        <NuxtLink to="/galeri" class="text-gray-800 mb-5 font-semibold border border-black py-2 px-5 hover:px-6 rounded-full inline-flex items-center group transform hover:text-primary hover:-translate-y-1 duration-200">
          Lihat Semua Galeri
          <svg class="w-4 h-4 ml-1 transform group-hover:translate-x-2 duration-200" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14 5l7 7m0 0l-7 7m7-7H3"></path>
          </svg>
        </NuxtLink>
      </div>
    </div>

    <Jurusan />
  </div>
</template>

<script setup>
useHead({
  title: "Home",
  meta: [
    {
      name: "description",
      content: "Home Page",
    },
  ],
});
</script>
