<template>
  <div>
    <v-container class="my-10">
      <v-row>
        <v-col cols="12" md="6">
          <v-img src="https://cdn.vuetifyjs.com/images/cards/docks.jpg" height="400px" />
        </v-col>
        <v-col cols="12" md="6">
          <v-card-title>
            <h1 class="my-2 text-right">About Me</h1> <v-divider inset></v-divider>
          </v-card-title>
          <v-card-text>
            <p class="text-justify">I'm a Full-Stack Developer with 4+ years of experience. I have a passion for
              programming and enjoy creating new things. I have worked on a wide range of projects, from small
              interactive web applications to large scale enterprise applications. I am a quick learner and have
              excellent problem-solving skills. I am a self-motivated person who can work well alone or as part of a
              team.</p>
          </v-card-text>
        </v-col>
      </v-row>
    </v-container>
    <v-sheet class="d-flex flex-column justify-center bg-black" height="100vh">
      <v-container>
      <v-row height="100vh" align="center">
        <plus-card title="4+" icon="mdi-certificate" color="red" value="années d'expériences" />
        <plus-card title="30+" icon="mdi-check" color="success" value="projets completés" />
        <plus-card title="100%" icon="mdi-time" value="de deadlines respectées" />
    </v-row>
    </v-container>
  </v-sheet>
  </div>
</template>

<script>
import PlusCard from '@/components/partial/PlusCard.vue';


export default
  {
    name: 'HomeView',
    components: {
      PlusCard
    },
  };
</script>

<style>
.m {
  margin: 0;
  padding: 0;
  background-color: black;
}
</style>