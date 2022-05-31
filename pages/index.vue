<script setup lang="ts">
import HeroMain from "~~/components/HeroMain.vue";
</script>
<template>
    <div>
        <HeroMain />
        <div class="container px-6 py-8 mx-auto">
            <div class="items-center lg:flex">
                <section class="relative py-16 bg-white min-w-screen animation-fade animation-delay">
                    <div class="container px-0 px-8 mx-auto sm:px-12 xl:px-5">
                        <p
                            class="text-xs font-bold text-left text-pink-500 uppercase sm:mx-6 sm:text-center sm:text-normal sm:font-bold">
                            Got a Question? We’ve got recipes.
                        </p>
                        <h3
                            class="mt-1 text-2xl font-bold text-left text-gray-800 sm:mx-6 sm:text-3xl md:text-4xl lg:text-5xl sm:text-center sm:mx-0">
                            Latest Recipes
                        </h3>
                        <ContentList path="/recipes" v-slot="{ list }">
                            <!-- <ul>
                                <li v-for="item in list" :key="item._path">
                                    <router-link :to="item._path">{{ item.title }}</router-link>
                                </li>
                            </ul> -->
                            <div v-for="recipe in list" :key="recipe._path"
                                class="w-full px-6 py-6 mx-auto mt-10 bg-white border border-gray-200 rounded-lg sm:px-8 md:px-12 sm:py-8 sm:shadow lg:w-5/6 xl:w-2/3">
                                <h3 class="text-lg font-bold text-purple-500 sm:text-xl md:text-2xl">
                                   <NuxtLink :to="recipe._path">{{ recipe.title }}</NuxtLink> 
                                </h3>
                                <p class="mt-2 text-base text-gray-600 sm:text-lg md:text-normal">
                                    {{ recipe.description }}
                                </p>
                            </div>
                        </ContentList>
                    </div>
                </section>
            </div>
        </div>
    </div>
</template>
