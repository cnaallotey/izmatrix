<script setup>
const logos = ref(
    [
        {
            icon:"gihoc",
            location:'gihoc.png',
            class: "bg-white"
        },
        {
            icon:"ghs",
            location:'ghs.jpg'
        },
        {
            icon:"agility",
            location:'agility.png',
            class: 'bg-white h-40'
        },
        {
            icon:"tis",
            location:'tis.jpg'
        },
        {
            icon:"tuc",
            location:'tuc.png'
        },
        {
            icon:"vra",
            location:'vra.jpg'
        }
    ]
)
</script>


<template>
    <div class="w-full py-20">
     <AppContainer>
        <h2
              class="text-3xl md:text-5xl md:text-center font-bold text-orange-500 leading-tight"
            >
              Our Proud Partners
            </h2>
        <LegoMarqueeBanner :speed="0.5" :hovered-speed="0" class="mt-5 md:mt-10">
    <LegoMarqueeBannerLeft class="w-full gap-20 items-center">
<img v-for="(icon, index) in logos" :key="index" :src="`/images/${icon.location}`" class="h-24 w-auto" :class="icon.class" :alt="icon.icon">
<img v-for="(icon, index) in logos" :key="index" :src="`/images/${icon.location}`" class="h-24 w-auto" :class="icon.class" :alt="icon.icon">
<img v-for="(icon, index) in logos" :key="index" :src="`/images/${icon.location}`" class="h-24 w-auto" :class="icon.class" :alt="icon.icon">
<img v-for="(icon, index) in logos" :key="index" :src="`/images/${icon.location}`" class="h-24 w-auto" :class="icon.class" :alt="icon.icon">
<img v-for="(icon, index) in logos" :key="index" :src="`/images/${icon.location}`" class="h-24 w-auto" :class="icon.class" :alt="icon.icon">
<img v-for="(icon, index) in logos" :key="index" :src="`/images/${icon.location}`" class="h-24 w-auto" :class="icon.class" :alt="icon.icon">
    </LegoMarqueeBannerLeft>
  </LegoMarqueeBanner>
     </AppContainer>
    </div>
</template>