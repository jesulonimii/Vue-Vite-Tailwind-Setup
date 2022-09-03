<template>
  <main class="bg-red-500 w-full h-full px-10 py-2">
    <!-- Genres Bar -->
    <div class="flex w-full">
      <emoji-chip emoji="🍿" text="All" link="/genre/" />
      <emoji-chip emoji="😀" text="Comedy" link="/genre/comedy" />
      <emoji-chip emoji="🦄" text="Fantasy" link="/genre/fantasy" />
      <emoji-chip emoji="🦄" text="Fantasy" link="/genre/fantasy" />
      <emoji-chip emoji="👽" text="Sci-Fi" link="/genre/sci-fi" />


    </div>
  </main>
</template>

<script setup>

import EmojiChip from "../components/EmojiChip.vue";
</script>