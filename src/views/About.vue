<script setup lang="ts">
const skills = [
  { name: 'C#', icon: 'devicon-csharp-plain colored' },
  { name: 'Java', icon: 'devicon-java-plain colored' },
  { name: 'HTML', icon: 'devicon-html5-plain colored' },
  { name: 'CSS', icon: 'devicon-css3-plain colored' },
  { name: 'JavaScript', icon: 'devicon-javascript-plain colored' },
  { name: 'Vue.js', icon: 'devicon-vuejs-plain colored' },
  { name: 'Node.js', icon: 'devicon-nodejs-plain colored' },
  { name: 'Python', icon: 'devicon-python-plain colored' },
  { name: 'SQL', icon: 'devicon-mysql-plain colored' },
  { name: 'Git', icon: 'devicon-git-plain colored' },
]
  
const softSkills = [
  'Creativity',
  'Ambition',
  'Adaptability',
  'Problem Solving',
  'Team Collaboration',
  'Communication',
]

const experience = [
  {
    company: 'Société Générale',
    position: 'Apprentice Developer',
    period: '2024 - 2026',
    description: 'Research and development apprenticeship focused on innovative solutions and modern technologies.'
  }
]

const education = [
  {
    degree: 'Engineering Degree in IT',
    school: 'EFREI Paris',
    period: '2021 - 2026',
    description: 'Specializing in software engineering with focus on web development and modern architectures.'
  },
  {
    degree: 'Exchange semester',
    school: 'Asia Pacific University',
    period: 'Sept. 2023 - Dec. 2023',
    description: 'International exchange program focusing on cross-cultural software development practices and global tech trends.'
  }
]
</script>

<template>
  <div class="bg-white py-24 sm:py-32">
    <div class="mx-auto max-w-7xl px-6 lg:px-8">
      <div class="mx-auto max-w-2xl lg:text-center">
        <h2 class="text-base font-semibold leading-7 text-indigo-600">About Me</h2>
        <p class="mt-2 text-3xl font-bold tracking-tight text-gray-900 sm:text-4xl">
          Passionate Developer & Problem Solver
        </p>
        <p class="mt-6 text-lg leading-8 text-gray-600">
          I'm a dedicated developer with a strong foundation in both front-end and back-end technologies.
          My passion lies in creating elegant solutions to complex problems and continuously learning new technologies.
        </p>
      </div>

      <div class="mx-auto mt-16 max-w-2xl sm:mt-20 lg:mt-24 lg:max-w-none">
        <dl class="grid max-w-xl grid-cols-1 gap-x-8 gap-y-16 lg:max-w-none lg:grid-cols-2">
          <!-- Technical Skills -->
          <div class="flex flex-col">
            <dt class="flex items-center gap-x-3 text-base font-semibold leading-7 text-gray-900">
              <div class="h-5 w-5 flex-none text-indigo-600">
                <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor">
                  <path d="M3.25 3A2.25 2.25 0 001 5.25v9.5A2.25 2.25 0 003.25 17h13.5A2.25 2.25 0 0019 14.75v-9.5A2.25 2.25 0 0016.75 3H3.25zM2.5 9v5.75c0 .414.336.75.75.75h13.5a.75.75 0 00.75-.75V9h-15zM4 5.25a.75.75 0 00-.75.75v.25h13.5v-.25a.75.75 0 00-.75-.75H4z" />
                </svg>
              </div>
              Technical Skills
            </dt>
            <dd class="mt-4">
              <div class="flex flex-wrap gap-4">
                <div v-for="skill in skills" :key="skill.name"
                  class="flex flex-col items-center gap-2 p-3 rounded-lg border border-gray-200 hover:border-indigo-500 transition-colors">
                  <i :class="skill.icon" class="text-3xl"></i>
                  <span class="text-sm font-medium text-gray-700">{{ skill.name }}</span>
                </div>
              </div>
            </dd>
          </div>

          <!-- Soft Skills -->
          <div class="flex flex-col">
            <dt class="flex items-center gap-x-3 text-base font-semibold leading-7 text-gray-900">
              <div class="h-5 w-5 flex-none text-indigo-600">
                <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor">
                  <path d="M10 9a3 3 0 100-6 3 3 0 000 6zM6 8a2 2 0 11-4 0 2 2 0 014 0zM1.49 15.326a.78.78 0 01-.358-.442 3 3 0 014.308-3.516 6.484 6.484 0 00-1.905 3.959c-.023.222-.014.442.025.654a4.97 4.97 0 01-2.07-.655zM16.44 15.98a4.97 4.97 0 002.07-.654.78.78 0 00.357-.442 3 3 0 00-4.308-3.517 6.484 6.484 0 011.907 3.96 2.32 2.32 0 01-.026.654zM18 8a2 2 0 11-4 0 2 2 0 014 0zM5.304 16.19a.844.844 0 01-.277-.71 5 5 0 019.947 0 .843.843 0 01-.277.71A6.975 6.975 0 0110 18a6.974 6.974 0 01-4.696-1.81z" />
                </svg>
              </div>
              Soft Skills
            </dt>
            <dd class="mt-4">
              <div class="flex flex-wrap gap-2">
                <span v-for="skill in softSkills" :key="skill"
                  class="inline-flex items-center rounded-md bg-pink-50 px-2 py-1 text-sm font-medium text-pink-700 ring-1 ring-inset ring-green-700/10">
                  {{ skill }}
                </span>
              </div>
            </dd>
          </div>

          <!-- Experience -->
          <div class="flex flex-col">
            <dt class="flex items-center gap-x-3 text-base font-semibold leading-7 text-gray-900">
              <div class="h-5 w-5 flex-none text-indigo-600">
                <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor">
                  <path fill-rule="evenodd" d="M6 3.75A2.75 2.75 0 018.75 1h2.5A2.75 2.75 0 0114 3.75v.443c.572.055 1.14.122 1.706.2C17.053 4.582 18 5.75 18 7.07v3.469c0 1.126-.694 2.191-1.83 2.54-1.952.599-4.024.921-6.17.921s-4.219-.322-6.17-.921C2.694 12.73 2 11.665 2 10.539V7.07c0-1.321.947-2.489 2.294-2.676A41.047 41.047 0 016 4.193V3.75zm6.5 0v.325a41.622 41.622 0 00-5 0V3.75c0-.69.56-1.25 1.25-1.25h2.5c.69 0 1.25.56 1.25 1.25zM10 10a1 1 0 00-1 1v.01a1 1 0 001 1h.01a1 1 0 001-1V11a1 1 0 00-1-1H10z" clip-rule="evenodd" />
                  <path d="M3 15.055v-.684c.126.053.255.1.39.142 2.092.642 4.313.987 6.61.987 2.297 0 4.518-.345 6.61-.987.135-.041.264-.089.39-.142v.684c0 1.347-.985 2.53-2.363 2.686a41.454 41.454 0 01-9.274 0C3.985 17.585 3 16.402 3 15.055z" />
                </svg>
              </div>
              Professional Experience
            </dt>
            <dd class="mt-4 space-y-6">
              <div v-for="exp in experience" :key="exp.company" 
                class="relative rounded-lg border border-gray-200 bg-white p-6 shadow-sm">
                <h3 class="text-lg font-semibold text-gray-900">{{ exp.position }}</h3>
                <p class="mt-1 text-sm text-gray-600">{{ exp.company }} | {{ exp.period }}</p>
                <p class="mt-3 text-sm text-gray-600">{{ exp.description }}</p>
              </div>
            </dd>
          </div>

          <!-- Education -->
          <div class="flex flex-col">
            <dt class="flex items-center gap-x-3 text-base font-semibold leading-7 text-gray-900">
              <div class="h-5 w-5 flex-none text-indigo-600">
                <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor">
                  <path d="M10.394 2.08a1 1 0 00-.788 0l-7 3a1 1 0 000 1.84L5.25 8.051a.999.999 0 01.356-.257l4-1.714a1 1 0 11.788 1.838L7.667 9.088l1.94.831a1 1 0 00.787 0l7-3a1 1 0 000-1.838l-7-3zM3.31 9.397L5 10.12v4.102a8.969 8.969 0 00-1.05-.174 1 1 0 01-.89-.89 11.115 11.115 0 01.25-3.762zM9.3 16.573A9.026 9.026 0 007 14.935v-3.957l1.818.78a3 3 0 002.364 0l5.508-2.361a11.026 11.026 0 01.25 3.762 1 1 0 01-.89.89 8.968 8.968 0 00-5.35 2.524 1 1 0 01-1.4 0zM6 18a1 1 0 001-1v-2.065a8.935 8.935 0 00-2-.712V17a1 1 0 001 1z" />
                </svg>
              </div>
              Education
            </dt>
            <dd class="mt-4 space-y-6">
              <div v-for="edu in education" :key="edu.school"
                class="relative rounded-lg border border-gray-200 bg-white p-6 shadow-sm">
                <h3 class="text-lg font-semibold text-gray-900">{{ edu.degree }}</h3>
                <p class="mt-1 text-sm text-gray-600">{{ edu.school }} | {{ edu.period }}</p>
                <p class="mt-3 text-sm text-gray-600">{{ edu.description }}</p>
              </div>
            </dd>
          </div>
        </dl>
      </div>
    </div>
  </div>
</template>