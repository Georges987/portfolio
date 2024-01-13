<template>
    <v-app class="ap">
        <v-app-bar elevation="10">
            <v-app-bar-title>
                <span class="font-weight-bold">Geor</span><span>ges</span>
            </v-app-bar-title>
            <nav>
                <v-btn :to="lk.route" :class="`${lk.color} capitalize`" v-for="lk in links" :key="lk.name">
                    {{ lk.name }}
                </v-btn>
            </nav>
        </v-app-bar>
        <v-main>
            <slot />
        </v-main>
    </v-app>
</template>
  
<script>

export default {
    components: {},
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