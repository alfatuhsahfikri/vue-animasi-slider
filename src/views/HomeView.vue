<script setup>
import { onMounted } from 'vue';
import { setupSlider } from '@/utils/slider.js';

const heroes = [
  {
    "id": 1,
    "name": "Templar Assassin",
    "image": "/img/dota1.jpg",
    "avatar": "/img/avatar/avatar1.png",
    "roles": "Carry / Escape",
    "desc": "Lanaya, the Templar Assassin, came to her calling by a path of curious inquiry. Possessed of a scientific bent, she spent her early years engaged in meticulous study of nature's laws — peering into grimoires of magic and alchemy, recreating experiments from charred fragments of the Violet Archives, and memorizing observations of the Keen recordkeepers. Already quiet and secretive by nature, the difficulty of acquiring these objects further reinforced her skills of stealth.",
    "quote": "Your death was a secret I can no longer hide."
  },
  {
    "id": 2,
    "name": "Dragon Knight",
    "image": "/public/img/dota2.jpg",
    "avatar": "/public/img/avatar/avatar2.png",
    "roles": "Carry / Pusher / Durable / Disabler / Initiator / Nuker",
    "desc": "After years on the trail of a legendary Eldwurm, the Knight Davion found himself facing a disappointing foe the dreaded Slyrak had grown ancient and frail, its wings tattered, its few remaining scales stricken with scale-rot, its fangs ground to nubs, and its fire-gouts no more threatening than a pack of wet matchsticks.",
    "quote": "Let my face be the last thing you see."
  },
  {
    "id": 3,
    "name": "Mirana",
    "image": "/public/img/dota3.jpg",
    "avatar": "/public/img/avatar/avatar3.png",
    "roles": "Carry / Support / Escape / Nuker Disabler",
    "desc": "Born to a royal family, a blood princess next in line for the Solar Throne, Mirana willingly surrendered any claim to mundane land or titles when she dedicated herself completely to the service of Selemene, Goddess of the Moon.",
    "quote": "They should have run while they had the chance."
  },
  {
    "id": 4,
    "name": "Clockwerk",
    "image": "/public/img/dota4.jpg",
    "avatar": "/public/img/avatar/avatar4.png",
    "roles": "Initiator / Disabler / Durable / Nuker",
    "desc": "Rattletrap descends from the same far-flung kindred as Sniper and Tinker, and like many of the Keen Folk, has offset his diminutive stature through the application of gadgetry and wit. The son of the son of a clockmaker, Rattletrap was many years apprenticed to that trade before war rode down from the mountains and swept the plains villages free of such innocent vocations.",
    "quote": "What time is it? It's killing time."
  },
  {
    "id": 5,
    "name": "Ursa",
    "image": "/public/img/dota5.jpg",
    "avatar": "/public/img/avatar/avatar5.png",
    "roles": "Carry / Durable / Disabler",
    "desc": "Ulfsaar the warrior is the fiercest member of an ursine tribe, protective of his land and his people. During the long winters, while the mothers sleep and nurse their cubs, the males patrol the lands above—as tireless, vigilant defenders of their ancient ways.",
    "quote": "I go now to the river, to wash your blood from my claws."
  }
]

onMounted(() => {
  setupSlider(); // Logika dijalankan setelah HTML siap
});
</script>

<template>
  <main>
    <div class="slider">
      <div class="list">
        <!-- Looping untuk List Utama -->
        <div v-for="hero in heroes" :key="hero.id" class="item">
          <img :src="hero.image" :alt="hero.name" />
          <div class="detail">
            <div class="title">Dota 2</div>
            <div class="name">{{ hero.name }}</div>
            <figure>
              <img :src="hero.avatar" :alt="hero.name" />
              <figcaption>{{ hero.roles }}</figcaption>
            </figure>
            <div class="desc">{{ hero.desc }}</div>
            <a href="#" class="more">More details &raquo;</a>
          </div>
        </div>
      </div>

      <div class="thumbnail">
        <!-- Looping untuk Thumbnail -->
        <div v-for="hero in heroes" :key="'thumb-' + hero.id" class="item">
          <img :src="hero.image" :alt="'thumbnail ' + hero.id" />
          <div class="detail">
            <div class="name">{{ hero.name }}</div>
            <blockquote>{{ hero.quote }}</blockquote>
          </div>
        </div>
      </div>

      <!-- Arrows Navigation -->
      <div class="arrows">
        <button id="prev">&lt;</button>
        <button id="next">&gt;</button>
      </div>
      <div class="loading-bar"></div>
    </div>
  </main>
</template>

<style scoped></style>
