<script setup>
const services = ref([
  {
    title: "Architecture",
    img:
      "https://images.unsplash.com/photo-1603901622056-0a5bee231395?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1462&q=80",
  },
  {
    title: "Master Planning",
    img:
      "https://images.unsplash.com/photo-1489514354504-1653aa90e34e?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8MTR8fGNvbnN0cnVjdGlvbiUyMHBsYW5uaW5nfGVufDB8fDB8fHww&auto=format&fit=crop&w=500&q=60",
  },
  {
    title: "Space Planning",
    img:
      "https://images.unsplash.com/photo-1541888946425-d81bb19240f5?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80",
  },
  {
    title: "Development Consulting",
    img:
      "https://images.unsplash.com/photo-1567954970774-58d6aa6c50dc?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1632&q=80",
  },
  {
    title: "Construction Management and Supervision",
    img:
      "https://images.unsplash.com/photo-1630061712710-2539eb457c55?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=882&q=80",
  },
]);
</script>

<template>
  <div
    class="w-full py-20 antialiased bg-gradient-to-l from-gray-900 via-black to-gray-800 relative"
  >
    <AppContainer>
      <div class="w-full grid md:grid-cols-2 lg:grid-cols-3">
        <div class="pr-8 flex flex-col justify-center pb-10 md:pb-0">
          <h1
            class="mb-1 text-3xl font-bold leading-none text-orange-500 md:text-5xl xl:text-5xl sm:mb-3"
          >
            <a href="#_">Our Services</a>
          </h1>
          <p class="font-medium text-gray-200">
            Designs and layouts to help you with your app.
          </p>
        </div>
        <div
          v-for="(service, index) in services"
          :key="index"
          class="w-full h-80 bg-cover overflow-hidden bg-center relative"
          :class="`bg-[url('${service.img}')]`"
        >
        <img :src="service.img" class="w-full h-full absolute object-cover object-center" alt="">
          <div
            class="w-full h-full bg-gradient-to-tr from-gray-900 relative to-transparent flex flex-col justify-end p-6"
          >
            <h3 class="text-3xl font-bold text-white">{{ service.title }}</h3>
          </div>
        </div>
      </div>
    </AppContainer>
  </div>
</template>
