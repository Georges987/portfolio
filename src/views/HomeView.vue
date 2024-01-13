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
            <p class="text-justify">Je suis un développeur Full-Stack avec plus de 4 ans d'expérience. J'ai une passion
              pour la programmation et j'apprécie créer de nouvelles choses. J'ai travaillé sur une gamme étendue de
              projets, allant de petites applications web interactives à des applications d'entreprise à grande échelle.
              Je suis un apprenant rapide et je possède d'excellentes compétences en résolution de problèmes. Je suis une
              personne autonome qui peut travailler efficacement seul ou en équipe.</p>
          </v-card-text>
        </v-col>
      </v-row>
    </v-container>
    <v-sheet class="d-flex flex-column justify-center bg-black align-center" height="100vh">
      <h1 class="font-weight-bold">Pourquoi moi ?</h1>
      <v-divider class="my-10" width="50%"></v-divider>
      <v-container>
        <v-row height="100vh" align="center">
          <plus-card title="4+" icon="mdi-certificate" color="red" value="années d'expériences" />
          <plus-card title="30+" icon="mdi-check" color="success" value="projets completés" />
          <plus-card title="100%" icon="mdi-timer" value="de deadlines respectées" />
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
}</style>