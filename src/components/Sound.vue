<template>
  <v-container fluid grid-list-lg>
    <v-layout wrap>
      <v-flex xs4 v-for="(sound, index) in sounds" :key="index">
        <v-card v-on:click="play(sound.file)">
          <v-card-text class="d-flex flex-column justify-center align-center">
            <v-icon color="blue-grey darken-2" x-large>play_arrow</v-icon>
            <p>{{ sound.title }}</p>
          </v-card-text>
        </v-card>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  name: 'Sound',
  data() {
    return {
      sounds: [
        {
          title: 'Ambulance',
          file: 'ambulance.mp3'
        },
        {
          title: 'Bell',
          file: 'bell.mp3'
        },
        {
          title: 'Bullet',
          file: 'bullet.mp3'
        },
        {
          title: 'Cow',
          file: 'cow.mp3'
        },
        {
          title: 'Explosion',
          file: 'explosion.mp3'
        },
        {
          title: 'Fizzle',
          file: 'fizzle.mp3'
        },
        {
          title: 'Movie',
          file: 'movie.mp3'
        },
        {
          title: 'Punch',
          file: 'punch.mp3'
        },   
        {
          title: 'telephone',
          file: 'telephone.mp3'
        },
      ]
    }
  },
  methods: {
    play(name) {
      const audio = new Audio(require('@/assets/sounds/' + name));
      audio.play();
    }
  }
}
</script>

<style>

</style>