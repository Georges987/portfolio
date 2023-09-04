<template>
  <div class="about">
          <v-img cover height="300" src="img/upload/banner.png"> </v-img>
          <v-container>
              <v-avatar class="mt-n16 border" color="white" size="200">
                <v-avatar image="/img/upload/user.jpg" size="175"></v-avatar>
              </v-avatar>
              <div class="text-h3 mt-4">Georges AYENI</div>
              <p>Rédacteur web | Développeur Web | Développeur Mobile</p>
            </v-container>

            <v-container>
          
              <div class="text-h4">A propos de moi</div>

              <p class="text-grey text-justify">
                Passionné de l'informatique, je me suis très tôt lancé dans le développmement informatique où j'ai appris à
                concevoir et
                conçu de nombreuses solutions informatique. Elle sont disponible ici et sur mon profile GitHub si vous souhaitez
                les voir.
                En quête de nouveau défis, de nouvelle solutions, je m'investis désormais dans la résolution de problèmes. Alors si vous avez un problème à résoudre, contactez-moiet faisons finalisons votre projet ensemble. 
              </p>
        </v-container>

      <v-container>
          <div class="text-h4 my-4">
            Contactez-moi !
          </div>
          <v-form>
            <v-text-field
              label="Votre email"
              color="primary"
            >
            </v-text-field>
            <v-textarea
              label="Dites moi ce dont vous avez besoin"
            ></v-textarea>
          </v-form>
    </v-container>
  </div>
</template>

<script>
export default {
  data: (()=>{

  })
}
</script>
