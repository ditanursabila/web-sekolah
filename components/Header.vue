<template>
  <nav :class="'fixed top-0 w-full z-50 transition-all duration-300 border-gray-200 dark:border-gray-700 ' + (scrolled ? ' backdrop-blur-md shadow-md' : 'bg-transparent')">
    <div class="max-w-screen-xl flex flex-wrap items-center justify-between mx-auto p-4">
      <nuxt-link to="/">
        <img src="assets/img/LOGO-SMK4.png" class="h-20" alt="Logo" />
      </nuxt-link>

      <button
        @click="toggleMobileMenu"
        type="button"
        class="inline-flex items-center p-2 w-10 h-10 justify-center text-sm text-gray-500 rounded-lg md:hidden hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-gray-200 dark:text-gray-400 dark:hover:bg-gray-700 dark:focus:ring-gray-600"
        aria-controls="navbar-dropdown"
        :aria-expanded="isMobileMenuOpen"
      >
        <span class="sr-only">Open Menu</span>
        <svg class="w-5 h-5" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 17 14">
          <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M1 1h15M1 7h15M1 13h15" />
        </svg>
      </button>

      <div class="w-full md:block md:w-auto" :class="isMobileMenuOpen ? 'block' : 'hidden'" id="navbar-dropdown">
        <ul class="flex flex-col font-medium p-4 md:p-0 mt-4 border md:space-x-8 rtl:space-x-reverse md:flex-row md:mt-0 md:border-0">
          <li>
            <nuxt-link to="/">
              <div
                class="block py-2 px-3 rounded hover:bg-blue-300 md:hover:bg-transparent md:border-0 md:hover:text-sky-300 md:p-0 dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent"
                :class="scrolled ? 'text-white dark:text-white' : 'text-white'"
              >
                BERANDA
              </div>
            </nuxt-link>
          </li>
          <li>
            <button
              id="dropdownNavbarLink"
              data-dropdown-toggle="dropdownNavbar"
              class="flex items-center justify-between w-full py-2 px-3 rounded hover:bg-blue-300 md:hover:bg-transparent md:border-0 md:hover:text-sky-300 md:p-0 md:w-auto dark:hover:bg-gray-700 md:dark:hover:bg-transparent"
              :class="scrolled ? 'text-white dark:text-white' : 'text-white'"
            >
              PROFIL
              <svg class="w-2.5 h-2.5 ms-2.5" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 10 6">
                <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="m1 1 4 4 4-4" />
              </svg>
            </button>
            <!-- Dropdown menu -->
            <div id="dropdownNavbar" class="z-10 hidden font-normal bg-white divide-y divide-gray-100 rounded-lg shadow w-44 dark:bg-gray-700 dark:divide-gray-600">
              <ul class="py-2 text-sm text-gray-700 dark:text-gray-400" aria-labelledby="dropdownLargeButton">
                <li>
                  <nuxt-link to="../profil/identitas">
                    <div class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white">IDENTITAS SEKOLAH</div>
                  </nuxt-link>
                </li>
                <li>
                  <nuxt-link to="../profil/sejarah">
                    <div class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white">SEJARAH</div>
                  </nuxt-link>
                </li>
                <li>
                  <nuxt-link to="../profil/visimisi">
                    <div class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white">VISI & MISI</div>
                  </nuxt-link>
                </li>
              </ul>
            </div>
          </li>
          <li>
            <nuxt-link to="/galeri">
              <div
                class="block py-2 px-3 rounded hover:bg-blue-300 md:hover:bg-transparent md:border-0 md:hover:text-sky-300 md:p-0 dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent"
                :class="scrolled ? 'text-white dark:text-white' : 'text-white'"
              >
                GALERI
              </div>
            </nuxt-link>
          </li>
          <li>
            <nuxt-link to="/ekskul">
              <div
                class="block py-2 px-3 rounded hover:bg-blue-300 md:hover:bg-transparent md:border-0 md:hover:text-sky-300 md:p-0 dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent"
                :class="scrolled ? 'text-white dark:text-white' : 'text-white'"
              >
                EKSTRAKURIKULER
              </div>
            </nuxt-link>
          </li>
          <li>
            <button
              id="dropdownNavbarLink1"
              data-dropdown-toggle="dropdownNavbar1"
              class="flex items-center justify-between w-full py-2 px-3 rounded hover:bg-blue-300 md:hover:bg-transparent md:border-0 md:hover:text-sky-300 md:p-0 md:w-auto dark:hover:bg-gray-700 md:dark:hover:bg-transparent"
              :class="scrolled ? 'text-white dark:text-white' : 'text-white'"
            >
              KARYA SISWA
              <svg class="w-2.5 h-2.5 ms-2.5" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 10 6">
                <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="m1 1 4 4 4-4" />
              </svg>
            </button>

            <div id="dropdownNavbar1" class="z-10 hidden font-normal bg-white divide-y divide-gray-100 rounded-lg shadow w-44 dark:bg-gray-700 dark:divide-gray-600">
              <ul class="py-2 text-sm text-gray-700 dark:text-gray-400" aria-labelledby="dropdownLargeButton">
                <li>
                  <a href="https://perpus-digitals.vercel.app/" target="_blank" class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white">E-PERPUS</a>
                </li>
                <li>
                  <a href="https://face-presensi.vercel.app/" target="_blank" class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white">FACE PRESENSI</a>
                </li>
                <li>
                  <a href="https://sinponis.vercel.app/login" target="_blank" class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white">POIN SISWA</a>
                </li>
                <li>
                  <a href="https://bookingapp-amber.vercel.app/" target="_blank" class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white">BOKING AULA</a>
                </li>
              </ul>
            </div>
          </li>
          <li>
            <nuxt-link to="/kontak">
              <div
                class="block py-2 px-3 rounded hover:bg-blue-300 md:hover:bg-transparent md:border-0 md:hover:text-sky-300 md:p-0 dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent"
                :class="scrolled ? 'text-white dark:text-white' : 'text-white'"
              >
                KONTAK
              </div>
            </nuxt-link>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script setup>
import { ref, onMounted, onBeforeMount, onBeforeUnmount } from "vue";
import { initDropdowns } from "flowbite";

const scrolled = ref(false);
const isMobileMenuOpen = ref(false);

const handleScroll = () => {
  scrolled.value = window.scrollY > 50;
};

const toggleMobileMenu = () => {
  isMobileMenuOpen.value = !isMobileMenuOpen.value;
};

onMounted(() => {
  window.addEventListener("scroll", handleScroll);
  initDropdowns();
});

onBeforeMount(() => {
  initDropdowns();
});

onBeforeUnmount(() => {
  window.removeEventListener("scroll", handleScroll);
});
</script>
