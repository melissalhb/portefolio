<script setup lang="ts">
const greeting = "Hello!"
const intro = "I'm"
const name = "Melissa Lacheb"
//const title = "Full Stack Developer"
const description = "I'm a passionate developer with expertise in building modern web."

const downloadCV = () => {
  // Replace this URL with the actual URL of your CV
  const cvUrl = '../project/src/assets/Melissa_Lacheb_CV.pdf'
  const link = document.createElement('a')
  link.href = cvUrl
  link.download = 'Melissa_Lacheb_CV.pdf'
  document.body.appendChild(link)
  link.click()
  document.body.removeChild(link)
}
</script>

<template>
  <main class="min-h-screen bg-white pt-16">
    <div class="relative isolate px-6 pt-14 lg:px-8">
      <div class="mx-auto max-w-2xl py-32 sm:py-48 lg:py-56">
        <div class="text-center">
          <h1 class="text-4xl font-bold tracking-tight text-gray-900 sm:text-6xl custom-font spaced-text mb-4">
            {{ greeting }}
          </h1>
          <h2 class="text-4xl font-bold tracking-tight text-gray-900 sm:text-6xl custom-font spaced-text mt-4">
            {{ intro }} <span class="gradient-text">{{ name }}</span>
          </h2>
            <!--<p class="mt-6 text-lg leading-8 text-gray-600">{{ title }}</p>-->
          <p class="mt-6 text-lg leading-8 text-gray-600">{{ description }}</p>
          <div class="mt-10 flex items-center justify-center gap-x-6">
            <a href="#projects"
              class="rounded-md bg-indigo-600 px-3.5 py-2.5 text-sm font-semibold text-white shadow-sm hover:bg-indigo-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600">
              View My Work
            </a>
            <button @click="downloadCV"
              class="rounded-md bg-white px-3.5 py-2.5 text-sm font-semibold text-indigo-600 shadow-sm ring-1 ring-inset ring-indigo-600 hover:bg-indigo-50">
              Download CV
            </button>
            <a href="#contact" class="text-sm font-semibold leading-6 text-gray-900">
              Contact Me <span aria-hidden="true">→</span>
            </a>
          </div>
        </div>
      </div>
    </div>
  </main>
</template>

<style>
@font-face {
  font-family: 'Brasika Display';
  src: url('src/assets/fonts/brasika-display-trial.woff') format('woff');
}

.custom-font {
  font-family: 'Brasika Display', sans-serif;
}

.spaced-text {
  letter-spacing: 0.02em; /* Adjust the value as needed */
}

.gradient-text {
  background-image: linear-gradient(45deg, #f5af19, #f57119, #f111c0, #b719f5, #116bf1, #b719f5, #f111c0, #f57119, #f5af19);
  -webkit-background-clip: text;
  background-clip: text;
  color: transparent;
  background-size: 700%;
  animation: animatedText 8s infinite alternate linear;
}

@keyframes animatedText {
  0% {
    background-position: 0% 50%;
  }
  100% {
    background-position: 100% 50%;
  }
}
</style>