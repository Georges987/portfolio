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
      <v-divider class="my-10" width="50%"></v-divider>
      <div>
        <v-btn class="mx-2" variant="outlined" prepend-icon="mdi-download">
          Télécharger mon CV
        </v-btn>
        <v-btn class="mx-2" variant="outlined" prepend-icon="mdi-phone">
          Me contacter
        </v-btn>
      </div>
    </v-sheet>

    <v-sheet class="d-flex flex-column justify-center align-center" height="100vh">
      <v-container>
        <v-row>
          <v-col cols="12" lg="5">
            <h1 class="my-2">
              {{ iskill ? 'Mes Compétences' : 'Mes Outils' }}
            </h1>
            <p>
              {{ iskill ? 'Je développe des interfaces utilisateur simples, intuitives et réactives pour les applications web et mobiles.En tant que développeur Full - Stack, je possède une expertise dans la création d\'applications web complètes.' : 'Dans mon processus de développement, j\'optimise mon efficacité en utilisant une sélection d\'outils de pointe.' }}
            </p>
            <v-switch v-model="iskill" hide-details inset :label="iskill ? 'Mes Compétences' : 'Mes Outils'"></v-switch>
          </v-col>
          <v-col cols="12" lg="6">
            <v-row v-if="iskill" align="start">
              <v-col v-for="ic in skills" :key="ic">
              <v-tooltip location="top" :text="ic.title">
                <template v-slot:activator="{ props }">
                <v-card v-bind="props" width="65" variant="outlined" :color="ic.color">
                  <v-card-text>
                    <v-row>
                      <v-col cols="2">
                        <v-icon :color="ic.color" size="30px">{{ ic.icon }}</v-icon>
                      </v-col>
                    </v-row>
                  </v-card-text>
                </v-card>
              </template>
              </v-tooltip>
              </v-col>
            </v-row>
            <v-row v-else align="start">
              <v-col v-for="ic in outils" :key="ic">
              <v-tooltip location="top" :text="ic.title">
                <template v-slot:activator="{ props }">
                <v-card v-bind="props" width="65" variant="outlined" :color="ic.color">
                  <v-card-text>
                    <v-row>
                      <v-col cols="2">
                        <v-icon :color="ic.color" size="30px">{{ ic.icon }}</v-icon>
                      </v-col>
                    </v-row>
                  </v-card-text>
                </v-card>
              </template>
              </v-tooltip>
              </v-col>
            </v-row>
          </v-col>
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

    data() {
      return {
        iskill: false,
        skills: [
          {
            title: 'HTML',
            icon: 'mdi-language-html5',
            color: 'red',
          },
          {
            title: 'CSS',
            icon: 'mdi-language-css3',
            color: 'blue',
          },
          {
            title: 'Javascript',
            icon: 'mdi-language-javascript',
            color: 'yellow',
          },
          {
            title: 'VueJS',
            icon: 'mdi-vuejs',
            color: 'green',
          },
          {
            title: 'NuxtJS',
            icon: 'mdi-nuxt',
            color: 'green',
          },
          {
            title: 'NodeJS',
            icon: 'mdi-nodejs',
            color: 'green',
          },
          {
            title: 'PHP',
            icon: 'mdi-language-php',
            color: 'purple',
          },
          {
            title: 'Laravel',
            icon: 'mdi-laravel',
            color: 'red',
          },
          {
            title: 'MySQL',
            icon: 'mdi-database',
            color: 'blue',
          },
          {
            title: 'Sass',
            icon: 'mdi-sass',
            color: 'pink',
          },
          {
            title: 'Firebase',
            icon: 'mdi-firebase',
            color: 'yellow',
          },
          {
            title: 'Wordpress',
            icon: 'mdi-wordpress',
            color: 'blue',
          },
          {
            title: 'Bootstrap',
            icon: 'mdi-bootstrap',
            color: 'purple',
          },
          {
            title: 'Vuetify',
            icon: 'mdi-vuetify',
            color: 'primary',
          },
          {
            title: 'Materialize',
            icon: 'mdi-material-design',
            color: 'blue',
          },
          {
            title: 'Tailwind',
            icon: 'mdi-tailwind',
            color: 'blue',
          },
          {
            title: 'Angular',
            icon: 'mdi-angular',
            color: 'red',
          },
          {
            title: 'React',
            icon: 'mdi-react',
            color: 'blue',
          },
        ],
        outils: [
          {
            title: 'Git',
            icon: 'mdi-git',
            color: 'red',
          },
          {
            title: 'Github',
            icon: 'mdi-github',
            color: 'black',
          },
          {
            title: 'Gitlab',
            icon: 'mdi-gitlab',
            color: 'orange',
          },
          {
            title: 'Bitbucket',
            icon: 'mdi-bitbucket',
            color: 'blue',
          },
          {
            title: 'VSCode',
            icon: 'mdi-microsoft-visual-studio-code',
            color: 'blue',
          },
          {
            title: 'WebStorm',
            icon: 'mdi-application',
            color: 'blue',
          },
          {
            title: 'Docker',
            icon: 'mdi-docker',
            color: 'blue',
          },
          {
            title: 'Trello',
            icon: 'mdi-trello',
            color: 'blue',
          },
          {
            title: 'Slack',
            icon: 'mdi-slack',
            color: 'pink',
          },
          {
            title: 'Discord',
            icon: 'mdi-discord',
            color: 'purple',
          },
          {
            title: 'Google Meet',
            icon: 'mdi-video',
            color: 'red',
          },
          {
            title: 'ChatGPT',
            icon: 'mdi-chat',
            color: 'green',
          },
          {
            title: 'Zoom',
            icon: 'mdi-video',
            color: 'blue',
          },
          {
            title: 'Google Drive',
            icon: 'mdi-google-drive',
            color: 'red',
          },
          {
            title: 'Google Docs',
            icon: 'mdi-file-document',
            color: 'blue',
          },
          {
            title: 'Google Keep',
            icon: 'mdi-google-keep',
            color: 'yellow',
          },
          {
            title: 'Google Analytics',
            icon: 'mdi-google-analytics',
            color: 'blue',
          },
          {
            title: 'Google My Business',
            icon: 'mdi-google-my-business',
            color: 'blue',
          },
          {
            title: 'Terminal',
            icon: 'mdi-console',
            color: 'green',
          }
        ]
      }
    },
  };
</script>

<style>
.m {
  margin: 0;
  padding: 0;
  background-color: black;
}</style>