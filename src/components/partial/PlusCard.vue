<template>
    <v-col cols="12" lg="4">
        <v-card elevation="10" class="pa-10" dark variant="outlined" :color="color">
            <v-card-text>
                <v-row>
                    <v-icon size="70">
                        {{ icon }}
                    </v-icon>
                    <div class="my-auto ml-auto">
                        <div class="text-h4 my-auto">
                            {{ title }}
                        </div>
                        <div class="text-subtitle-1">
                            {{ value }}
                        </div>
                    </div>
                </v-row>
            </v-card-text>
        </v-card>
    </v-col>
</template>

<script>
export default {
    name: 'PlusCard',
    props: {
        title: String,
        icon: String,
        color: String,
        value: String,
    },
}
</script>