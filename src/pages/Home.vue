<template>
    <div class="home">
        <div class="background">
            <div class="blob blob1"></div>
            <div class="blob blob2"></div>
            <div class="blob blob3"></div>
        </div>
        <div class="absolute top-4 right-4 z-10 text-white rounded-md p-2 w-80 flex flex-col space-y-2" >
            <div class="m-auto">
                <ElasticSlider 
                    v-model="blur"
                    :starting-value="0"
                    :max-value="100"
                    :is-stepped="true"
                    :step-size="5"
                    label="Blur"
                />
            </div>
            <div class="m-auto">
                <ElasticSlider 
                    v-model="borderRadius"
                    :starting-value="0"
                    :max-value="50"
                    :is-stepped="true"
                    :step-size="5"
                    label="Border Radius"
                />
            </div>
        </div>
        <div class="relative flex items-center justify-center h-full">
            <LiquidGlass width="700px" :border-radius="borderRadius + 'px'" :blur="blur + 'px'">
                <div class="flex flex-col h-full p-4">
                    <h1 class="py-2">THE LIQUID CARD</h1>
                    <p class="py-2 text-sm font-semibold">
                        Liquid Glass is a new user interface design language introduced by Apple that focuses on creating translucent, glass-like visual effects, combined with dynamic and responsive interactions. It is designed to bring a dynamic, fluid, and modern feel to devices like iPhone, iPad, Mac, and Apple Watch.
                    </p>
                    <p class="py-2 text-sm text-right font-semibold italic">
                        Design by Apple
                    </p>
                    <div class="mt-auto flex space-x-4 items-center text-white">
                        <LiquidGlass width="50px" height="50px" border-radius="50%">
                            <div class="flex items-center justify-center h-full w-full">
                                <a href="https://github.com/heydayle/liquid-glass">
                                    <svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 24 24"><!-- Icon from Simple Icons by Simple Icons Collaborators - https://github.com/simple-icons/simple-icons/blob/develop/LICENSE.md --><path fill="#ffffff" d="M12 .297c-6.63 0-12 5.373-12 12c0 5.303 3.438 9.8 8.205 11.385c.6.113.82-.258.82-.577c0-.285-.01-1.04-.015-2.04c-3.338.724-4.042-1.61-4.042-1.61C4.422 18.07 3.633 17.7 3.633 17.7c-1.087-.744.084-.729.084-.729c1.205.084 1.838 1.236 1.838 1.236c1.07 1.835 2.809 1.305 3.495.998c.108-.776.417-1.305.76-1.605c-2.665-.3-5.466-1.332-5.466-5.93c0-1.31.465-2.38 1.235-3.22c-.135-.303-.54-1.523.105-3.176c0 0 1.005-.322 3.3 1.23c.96-.267 1.98-.399 3-.405c1.02.006 2.04.138 3 .405c2.28-1.552 3.285-1.23 3.285-1.23c.645 1.653.24 2.873.12 3.176c.765.84 1.23 1.91 1.23 3.22c0 4.61-2.805 5.625-5.475 5.92c.42.36.81 1.096.81 2.22c0 1.606-.015 2.896-.015 3.286c0 .315.21.69.825.57C20.565 22.092 24 17.592 24 12.297c0-6.627-5.373-12-12-12"/></svg>
                                </a>
                            </div>
                        </LiquidGlass>
                        <LiquidGlass width="auto" height="auto" border-radius="5px">
                            <p class="m-auto p-4 text-center">
                                Thank you for checking out this project!
                            </p>
                        </LiquidGlass>
                        <div>Made by Heyday</div>
                    </div>
                </div>
            </LiquidGlass>
        </div>
    </div>
</template>

<script setup lang="ts">
import { onMounted, ref } from 'vue';
import LiquidGlass from '../components/LiquidGlass.vue';
import ElasticSlider from '../components/ui/ElasticSlider/ElasticSlider.vue';

const blur = ref(0);
const borderRadius = ref(20);
</script>

<style scoped>
.home {
    /* background-image: url('/vietnam-flag.jpg'); */
    height: 100vh;
}
</style>