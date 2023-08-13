<template>
    <div>
        <v-img class="bg-grey-lighten-2" :aspect-ratio="1" cover @click="setOverlay" :src="url">
            <v-overlay contained v-model="overlay" class="align-center justify-center" scrim="#171717">

                <p class="text-h5 text-center text-white">{{ name }}</p>
                <p class="text-subtitle text-center text-white">{{ subtitle }}</p>
            </v-overlay>

            <!-- <v-overlay v-if="overlay === true" contained class="align-center justify-center">
                <v-btn color="success" @click="setOverlay">
                    Hide Overlay
                </v-btn>
            </v-overlay> -->
        </v-img>
    </div>
    <!-- <v-card height="300" width="250">
        <v-row justify="center">
            <v-btn color="success" class="mt-12" @click="overlay = !overlay">
                Show Overlay
            </v-btn>

            <v-overlay v-model="overlay" contained class="align-center justify-center">
                <v-btn color="success" @click="overlay = false">
                    Hide Overlay
                </v-btn>
            </v-overlay>
        </v-row>
    </v-card> -->
</template>

<script setup>
import { ref } from 'vue'
defineProps({
    name: String,
    subtitle: String,
    url: String,
})

const overlay = ref(false);

let setOverlay = () => {
    overlay.value = !overlay.value
    console.log(overlay.value)
}
</script>