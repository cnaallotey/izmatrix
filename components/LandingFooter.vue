<script setup>
const socials = [
  {
    name: "facebook",
    url: "https://www.facebook.com/KelitorGh/",
    class: "text-[#4267B2]",
    icon: "ri:facebook-circle-fill",
  },
  {
    name: "instagram",
    url: "https://instagram.com/kelitor?igshid=YmMyMTA2M2Y=",
    class: "text-[#405DE6]",
    icon: "entypo-social:instagram-with-circle",
  },
  {
    name: "twitter",
    url: "https://twitter.com/kelitor_RE",
    class: "text-blue-500",
    icon: "mdi:twitter-circle",
  },
];
</script>

<template>
  <div class="w-full antialiased bg-gradient-to-br from-gray-900 to-black py-20">
    <AppContainer>
      <div class="w-full flex flex-col-reverse md:flex-row items-center justify-between">
        <div
          class="flex flex-col lg:flex-row items-center md:items-start w-fit gap-5 lg:items-center"
        >
          <a
            href="#_"
            class="md:flex items-center w-1/4 py-4 pl-6 pr-4 space-x-2 font-extrabold text-white md:py-0 hidden"
          >
            <span
              class="flex items-center justify-center flex-shrink-0 w-8 h-8 text-gray-900 rounded-full bg-gradient-to-br from-white via-gray-200 to-white"
            >
              <svg
                class="w-auto h-5 -translate-y-px"
                viewBox="0 0 69 66"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="m31.2 12.2-3.9 12.3-13.4.5-13.4.5 10.7 7.7L21.8 41l-3.9 12.1c-2.2 6.7-3.8 12.4-3.6 12.5.2.2 5-3 10.6-7.1 5.7-4.1 10.9-7.2 11.5-6.8.6.4 5.3 3.8 10.5 7.5 5.2 3.8 9.6 6.6 9.8 6.4.2-.2-1.4-5.8-3.6-12.5l-3.9-12.2 8.5-6.2c14.7-10.6 14.8-9.6-.4-9.7H44.2L40 12.5C37.7 5.6 35.7 0 35.5 0c-.3 0-2.2 5.5-4.3 12.2Z"
                  fill="currentColor"
                />
              </svg>
            </span>
            <span>LOGO</span>
          </a>
          <p class="text-sm font-normal text-white/80">
            All Rights Reserved <sup>©</sup> . Izmatrix Limited 2023
          </p>
        </div>
        <div class="flex flex-col md:flex-row items-center gap-4">
          <ul class="inline-flex items-center gap-4 md:pr-4 md:border-r border-white">
            <li class="text-sm text-white"><NuxtLink to="#">Home</NuxtLink></li>
            <li class="text-sm text-white"><NuxtLink to="#">About</NuxtLink></li>
            <li class="text-sm text-white"><NuxtLink to="#">Services</NuxtLink></li>
            <li class="text-sm text-white"><NuxtLink to="#">Contact</NuxtLink></li>
          </ul>
          <div
            class="flex items-center justify-center md:justify-start w-full md:w-fit gap-2 mb-5 md:mb-0"
          >
            <a
              v-for="social in socials"
              :key="social"
              :href="social.url"
              target="_blank"
              class="text-white inline-flex items-center rounded-full bg-white/20 hover:text-orange-500"
            >
              <Icon :name="social.icon" class="w-8 lg:w-6 h-8 lg:h-6 shrink-0" /><span
                class="sr-only"
                >{{ social.name }}</span
              >
            </a>
          </div>
        </div>
        <a
          href="#_"
          class="flex items-center w-fit space-x-2 font-extrabold text-white md:py-0 mb-10 md:hidden"
        >
          <span
            class="flex items-center justify-center flex-shrink-0 w-8 h-8 text-gray-900 rounded-full bg-gradient-to-br from-white via-gray-200 to-white"
          >
            <svg
              class="w-auto h-5 -translate-y-px"
              viewBox="0 0 69 66"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="m31.2 12.2-3.9 12.3-13.4.5-13.4.5 10.7 7.7L21.8 41l-3.9 12.1c-2.2 6.7-3.8 12.4-3.6 12.5.2.2 5-3 10.6-7.1 5.7-4.1 10.9-7.2 11.5-6.8.6.4 5.3 3.8 10.5 7.5 5.2 3.8 9.6 6.6 9.8 6.4.2-.2-1.4-5.8-3.6-12.5l-3.9-12.2 8.5-6.2c14.7-10.6 14.8-9.6-.4-9.7H44.2L40 12.5C37.7 5.6 35.7 0 35.5 0c-.3 0-2.2 5.5-4.3 12.2Z"
                fill="currentColor"
              />
            </svg>
          </span>
          <span>LOGO</span>
        </a>
      </div>
    </AppContainer>
  </div>
</template>
