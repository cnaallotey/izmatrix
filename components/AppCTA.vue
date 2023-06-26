<script setup>
const images = ref(
    [
       {
        title:'image1',
        location: 'https://images.unsplash.com/photo-1486406146926-c627a92ad1ab?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8NXx8YnVpbGRpbmd8ZW58MHx8MHx8fDA%3D&auto=format&fit=crop&w=900&q=60'
       },
       {
        title:'image2',
        location: 'https://images.unsplash.com/photo-1470075801209-17f9ec0cada6?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1287&q=80'
       },
       {
        title:'image3',
        location: 'https://images.unsplash.com/photo-1554435493-93422e8220c8?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1336&q=80'
       }
    ]
)

const index = ref(0)
</script>
<template>
  <div>
    <div class="w-full py-20 xl:py-32 bg-black overflow-hidden">
      <AppContainer>
        <div class="w-full flex flex-col xl:flex-row gap-20 xl:items-center">
          <div class="md:w-1/2 md:mx-auto lg:mx-0 flex flex-col gap-5" data-aos="fade-right">
            <h2
              class="text-3xl md:text-5xl font-bold text-orange-500 leading-tight max-w-md"
            >
              Get the Best Properties in Ghana for the Best Price
            </h2>
            <p class="text-sm md:text-base font-normal text-gray-100 leading-5 max-w-md">
              Unlock the best of Ghana's real estate market without breaking the bank.
              Discover premium properties at unbeatable prices with Kelitor Ltd. Your
              dream home awaits!
            </p>
          </div>
          <div class="flex lg:w-1/2 flex-col gap-5 md:gap-10">
            <div class="w-full h-[300px] md:h-[500px] overflow-hidden">
              <img :src="images[index].location" class="w-full h-full object-cover object-center" :alt="images[index].title" />
            </div>
            <div class="w-full flex items-center justify-center gap-3">
              <button @click="index--" class="text-white bg-white/10 p-5 rounded-full border-2 border-white/80 disabled:opacity-60"
              :disabled="index==0"
              >
                <span class="sr-only">left</span
                ><span
                  ><svg
                    xmlns="http://www.w3.org/2000/svg"
                    fill="none"
                    viewBox="0 0 24 24"
                    stroke-width="1.5"
                    stroke="currentColor"
                    class="w-6 h-6"
                  >
                    <path
                      stroke-linecap="round"
                      stroke-linejoin="round"
                      d="M19.5 12h-15m0 0l6.75 6.75M4.5 12l6.75-6.75"
                    />
                  </svg>
                </span>
              </button>
              <button @click="index++" class="text-white p-5  bg-white/10 rounded-full border-2 border-white/80 disabled:opacity-60"
              :disabled="index+1 === images.length">
                <span class="sr-only">right</span
                ><span
                  ><svg
                    xmlns="http://www.w3.org/2000/svg"
                    fill="none"
                    viewBox="0 0 24 24"
                    stroke-width="1.5"
                    stroke="currentColor"
                    class="w-6 h-6"
                  >
                    <path
                      stroke-linecap="round"
                      stroke-linejoin="round"
                      d="M4.5 12h15m0 0l-6.75-6.75M19.5 12l-6.75 6.75"
                    />
                  </svg>
                </span>
              </button>
            </div>
          </div>
        </div>
      </AppContainer>
    </div>
  </div>
</template>
