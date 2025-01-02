<template>
  <div>
    <section class="py-16 px-4 bg-blue-700">
      <div class="max-w-6xl mx-auto mt-10">
        <div class="bg-blue-300 p-6 rounded-lg">
          <div v-for="(news, i) in berita" :key="i">
            <header class="mb-8">
              <h1 class="text-3xl font-bold text-center text-gray-900 dark:text-white mb-4">
                {{ news.judul }}
              </h1>
            </header>

            <div class="relative w-full h-96 mb-8 rounded-lg overflow-hidden">
              <img :src="news.foto" alt="foto" class="w-full h-full object-cover" />
            </div>

            <article class="prose prose-lg max-w-none dark:prose-invert mb-12">
              <p class="text-gray-700 dark:text-gray-300">
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Corporis omnis cum aut possimus illum reprehenderit doloribus minus non labore accusantium magnam nam, laboriosam necessitatibus! Praesentium sit ipsam eos inventore
                repudiandae. Dolore impedit omnis aspernatur beatae maxime hic molestiae laboriosam dolorum, minus porro quis eius eos at, quo vel quas, debitis voluptatum animi. Porro autem architecto quis fuga at quaerat excepturi. Rerum ut nihil
                eveniet suscipit modi fugit molestiae, sequi distinctio, dolor eum ullam natus amet velit excepturi recusandae dolores quos temporibus nisi molestias repellendus numquam. Provident tenetur nobis suscipit enim! Beatae repudiandae
                veritatis quo ullam totam. Accusamus adipisci perferendis nam neque quidem recusandae minus inventore, dolorem quisquam, ex corporis cupiditate sunt quis eius fuga ab molestiae iusto. Et, optio non. Numquam, qui non illo est
                voluptatibus, necessitatibus vitae assumenda accusamus mollitia inventore facilis soluta nesciunt neque eveniet quo maxime. Ipsum quae exercitationem facere autem rerum laborum ut iste, itaque magni.
              </p>
            </article>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup>
useHead({
  title: "Berita",
  meta: [
    {
      name: "description",
      content: "Berita Page",
    },
  ],
});
const supabase = useSupabaseClient();

const berita = ref([]);
const route = useRoute();

const getBerita = async () => {
  const { data, error } = await supabase.from("berita").select("*").eq("id", route.params.id);
  if (data) {
    berita.value = data;
  }
  if (error) throw error;
};

onMounted(() => getBerita());
</script>
