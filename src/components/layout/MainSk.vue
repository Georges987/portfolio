<template>
    <v-app>
        <v-app-bar absolute :class="$route.name == 'home' ? 'text-white' : ''" class="bg-transparent" elevation="10">
            <v-app-bar-title>
                <span class="font-weight-bold">Geor</span><span>ges</span>
            </v-app-bar-title>
            <nav>
                <v-btn :to="lk.route" :class="`text-capitalize`" v-for="lk in links" :key="lk.name">
                    {{ lk.name }}
                </v-btn>
            </nav>
        </v-app-bar>
        <banner-home image="images/banner/slash.png">
            <div class="text-h2">Welcome !</div>
            <div class="my-5">
                <span>I am </span><span> Web | Mobile Developer</span>
            </div>
            <div>
                <v-btn class="mx-2" rounded="xl" variant="outlined">
                    View my Work
                </v-btn>
                <v-btn class="mx-2 text-black" rounded="xl">
                    Hire me !
                </v-btn>
            </div>
        </banner-home>
        <v-main>
            <slot />
        </v-main>
    </v-app>
</template>
  
<script>
import BannerHome from "@/components/partial/BannerHome.vue"
export default {
    components: {
        BannerHome
    },
    props: {
        links: {
            type: Object,
            default: () => ({}),
        }
    },
    data: () => ({

    }),
    computed: {},
}
</script>