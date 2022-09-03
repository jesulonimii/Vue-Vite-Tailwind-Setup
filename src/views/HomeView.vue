<template>
  <div class="w-full flex">
    <div class="flex flex-col w-full h-full border-x-2 border-slate-700">
    <div class="font-outfit font-[700] px-10 pt-10 pb-5 text-white font-bold text-3xl capitalize">{{ this.$route.name }}</div>

    <main class="w-full h-full px-10 py-2">
      <!-- Genres Bar -->
      <div class="flex w-full">
        <emoji-chip emoji="🍿" text="All" link="/genre/" />
        <emoji-chip emoji="😀" text="Comedy" link="/genre/comedy" />
        <emoji-chip emoji="🦄" text="Fantasy" link="/genre/fantasy" />
        <emoji-chip emoji="😲" text="Thriller" link="/genre/fantasy" class="active-chip" />
        <emoji-chip emoji="👽" text="Sci-Fi" link="/genre/sci-fi" />
      </div>

      <!-- Featured Movies -->
      <div class="flex flex w-full w-full my-8 relative">

<!--        <div class="hidden w-[90%] aspect-video h-fit">
          <video controls class="w-full h-full rounded-2xl object-cover">
            <source :src=vidLink >
          </video>
        </div>-->
        <div class="flex flex-col p-12 justify-end w-[90%] absolute bg-gradient-to-t from-black to-transparent aspect-video h-fit rounded-md">

          <div id="overlay" class="flex flex-col">
            <h3 class="font-outfit font-bold text-3xl">The Gray Man</h3>
            <h3 class="text-sm text-gray-300 pr-24 my-2">{{description}}</h3>
            <h3 class="text-sm text-gray-400 my-1">2022 • Thriller • 2h 2m</h3>

            <div class="w-full flex">
              <Button name="Watch now" link="" class="my-2"/>
              <icon-button link="" icon="plus" class="m-2"/>
            </div>
          </div>

        </div>

        <div class="w-[90%] aspect-video h-fit bg-cover rounded-md" style="background-image: url('https://m.media-amazon.com/images/M/MV5BMjRhYjYwM2EtZWU1ZC00ZjFlLWExYjItZjlkNTczNzgxMWExXkEyXkFqcGdeQXZ3ZXNsZXk@._V1_.jpg')">

        </div>


      </div>

    </main>

  </div>
    <div class="w-[40%] py-10 px-8 h-full">
    <div class="flex flex-col">
      <p class="font-bold font-outfit">Popular Movies 🔥</p>
      <div class="flex flex-col w-full my-4">
        <movie-card-small name="Top Gun Maverick" img="/img/tgm.jpg" genre="Action, Drama" link="/movie/1" :stars=5 />
        <movie-card-small name="Doctor Strange: Multiverse of madness" img="/img/dsmom.jpg" genre="Action, Adventure, Fantasy" link="/movie/tgm" :stars=4 />
      </div>
      <fade-button class="w-full rounded-lg justify-center" name="See More" link="more" />
    </div>

    <div class="flex flex-col my-12">
      <p class="font-bold font-outfit">Watchlist 🍿</p>
      <div class="flex flex-col w-full my-4">
        <movie-card-small name="The Gray man" img="/img/the-gray-man.jpg" genre="Action, Thriller" link="/movie/1" :stars=4 />
        <movie-card-small name="Doctor Strange: Multiverse of madness" img="/img/dsmom.jpg" genre="Action, Adventure, Fantasy" link="/movie/tgm" :stars=4 />
        <movie-card-small name="The Batman" img="/img/batman.jpg" genre="Action, Crime, Drama" link="/movie/tgm" :stars=4 />

      </div>
    </div>


  </div>
  </div>
</template>

<script setup>

import EmojiChip from "../components/EmojiChip.vue";
import Button from "../components/Button.vue";
import FadeButton from "../components/FadeButton.vue";
import IconButton from "../components/IconButton.vue";
import MovieCardSmall from "../components/MovieCardSmall.vue";

const vidLink = "/videos/trailer-day-shift.mp4";

const description = "When the CIA's most skilled operative-whose true identity is known to none-accidentally uncovers dark agency secrets, a psychopathic former colleague puts a bounty on his head, setting off a global manhunt by international assassins."
</script>

<style scoped>
  .active-chip {
    background-color: #f59e0b;
  }
</style>