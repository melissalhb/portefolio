<script setup lang="ts">
import forestJumpImage from '../assets/forest_jump.jpg';
import cineQuizImage from '../assets/cine_quiz.png';

const projects = [
  {
    title: 'CineQuiz',
    description: 'Interactive web platform where movie enthusiasts can test their knowledge through engaging quizzes, featuring admin-created questions and hints.',
    tech: ['MySQL', 'HTML', 'JavaScript', 'CSS', ''],
    image: cineQuizImage,
    link: '#'
  },
  {
    title: 'Forest Jump',
    description: 'Fast-paced 2D game built with Python and Pygame, where players control a ninja who jumps to dodge obstacles and throws shurikens to counter attacks.',
    tech: ['Python', 'Design graphique', 'Travail d’équipe', 'Gestion de projet'],
    image: forestJumpImage,
    link: 'https://github.com/melissalhb/forest_jump'
  },
]
</script>

<template>
  <div class="bg-white py-24 sm:py-32">
    <div class="mx-auto max-w-7xl px-6 lg:px-8">
      <div class="mx-auto max-w-2xl text-center">
        <h2 class="text-3xl font-bold tracking-tight text-gray-900 sm:text-4xl">My Projects</h2>
        <p class="mt-2 text-lg leading-8 text-gray-600">Check out some of my recent work</p>
      </div>
      <div class="mx-auto mt-16 grid max-w-2xl grid-cols-1 gap-x-8 gap-y-20 lg:mx-0 lg:max-w-none lg:grid-cols-3">
        <article v-for="project in projects" :key="project.title" class="flex flex-col items-start">
          <div class="relative w-full">
            <img :src="project.image" alt="" class="aspect-[16/9] w-full rounded-2xl bg-gray-100 object-cover sm:aspect-[2/1] lg:aspect-[3/2]">
          </div>
          <div class="max-w-xl">
            <div class="mt-8 flex items-center gap-x-4 text-xs">
              <span v-for="tech in project.tech" :key="tech"
                class="relative z-10 rounded-full bg-gray-50 px-3 py-1.5 font-medium text-gray-600 hover:bg-gray-100">
                {{ tech }}
              </span>
            </div>
            <div class="group relative">
              <h3 class="mt-3 text-lg font-semibold leading-6 text-gray-900 group-hover:text-gray-600">
                <a :href="project.link">
                  <span class="absolute inset-0"></span>
                  {{ project.title }}
                </a>
              </h3>
              <p class="mt-5 line-clamp-3 text-sm leading-6 text-gray-600">{{ project.description }}</p>
            </div>
          </div>
        </article>
      </div>
    </div>
  </div>
</template>