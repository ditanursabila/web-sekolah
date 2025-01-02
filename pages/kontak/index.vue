<template>
  <div>
    <section class="py-16 px-4 bg-blue-700">
      <div class="max-w-6xl mx-auto">
        <div class="text-center mb-12 mt-10">
          <h2 class="text-3xl font-bold text-white mb-2">Kontak Kami</h2>
          <div class="w-20 h-1 bg-sky-300 mx-auto rounded-full"></div>
        </div>
        <div class="grid md:grid-cols-2 gap-6">
          <div class="bg-white/90 backdrop-blur rounded-lg p-6 shadow-md">
            <div class="space-y-6">
              <div class="flex items-start space-x-4">
                <div class="p-2 bg-sky-100 rounded-full">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-sky-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z" />
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z" />
                  </svg>
                </div>
                <div>
                  <h3 class="font-semibold text-lg">Alamat:</h3>
                  <p class="text-gray-600">Jl Depok Kel. Sukamenak Kec. Purbaratu Kota Tasikmalaya 46196.</p>
                </div>
              </div>

              <div class="flex items-start space-x-4">
                <div class="p-2 bg-sky-100 rounded-full">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-sky-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" />
                  </svg>
                </div>
                <div>
                  <h3 class="font-semibold text-lg">Email:</h3>
                  <p class="text-gray-600">info@smkn4-tsm.sch.id</p>
                </div>
              </div>

              <div class="flex items-start space-x-4">
                <div class="p-2 bg-sky-100 rounded-full">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-sky-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path
                      stroke-linecap="round"
                      stroke-linejoin="round"
                      stroke-width="2"
                      d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z"
                    />
                  </svg>
                </div>
                <div>
                  <h3 class="font-semibold text-lg">Telepon:</h3>
                  <p class="text-gray-600">+62265312059</p>
                </div>
              </div>

              <div class="mt-6">
                <div class="w-full h-64 bg-gray-200 rounded-lg">
                  <iframe
                    src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3957.2131162969818!2d108.254474!3d-7.329945299999999!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x2e6f59eeb6bda36f%3A0xa9e724a275da6c2d!2sSMK%20Negeri%204%20Tasikmalaya!5e0!3m2!1sid!2sid!4v1735360836269!5m2!1sid!2sid"
                    width="100%"
                    height="100%"
                    style="border: 0"
                    loading="lazy"
                    referrerpolicy="no-referrer-when-downgrade"
                  ></iframe>
                </div>
              </div>
            </div>
          </div>

          <div class="bg-white/90 backdrop-blur rounded-lg p-6 shadow-md">
            <form @submit.prevent="kirimData" class="space-y-4">
              <div class="grid md:grid-cols-2 gap-4">
                <div class="space-y-2">
                  <label class="block text-sm font-medium">Nama Anda</label>

                  <input v-model="form.nama" type="text" placeholder="Masukkan nama anda" class="w-full px-3 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-sky-500" />
                </div>
                <div class="space-y-2">
                  <label class="block text-sm font-medium">Email Anda</label>

                  <input v-model="form.email" type="email" placeholder="Masukkan email anda" class="w-full px-3 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-sky-500" />
                </div>
              </div>

              <div class="space-y-2">
                <label class="block text-sm font-medium">Subjek</label>

                <input v-model="form.subjek" type="text" placeholder="Masukkan subjek pesan" class="w-full px-3 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-sky-500" />
              </div>

              <div class="space-y-2">
                <label class="block text-sm font-medium">Isi Pesan</label>

                <textarea v-model="form.pesan" placeholder="Tulis pesan anda disini" class="w-full h-40 px-3 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-sky-500"></textarea>
              </div>

              <button type="submit" class="w-full bg-sky-600 hover:bg-sky-700 text-white font-medium py-2 px-4 rounded-md transition-colors duration-200">Kirim Pesan</button>
            </form>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup>
useHead({
  title: "Kontak",
  meta: [
    {
      name: "description",
      content: "Kontak Page",
    },
  ],
});

const supabase = useSupabaseClient();
const form = ref({
  nama: "",
  email: "",
  subjek: "",
  pesan: "",
});

const kirimData = async () => {
  const { error } = await supabase.from("kontak").insert([form.value]);
  if (!error) {
    alert("Pesan berhasil dikirim!👏");
  } else {
    alert("Terjadi kesalahan saat mengirim pesan.");
  }
};
</script>
