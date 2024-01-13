<template>
    <v-sheet v-if="image != null" color="black" class="text-white" height="100vh">
        <v-parallax :src="image" class="d-flex flex-wrap" height="100%" width="100%">
            <div style="height: 100%;" class="d-flex flex-column justify-center align-center">
                <slot />
            </div>
        </v-parallax>
    </v-sheet>
    <v-carousel v-if="images != null">
        <v-carousel-item></v-carousel-item>
    </v-carousel>
</template>

<script>
export default {
    props: {
        image: {
            type: String,
            default: null,
        },
        images: {
            type: Object,
            default: null
        }
    },
}
</script>