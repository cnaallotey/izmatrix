<template>
    <div class="relative">
      <div class="w-full py-20 xl:py-32">
        <div class="absolute top-0 w-full h-32 bg-gradient-to-b from-gray-100 to-white"></div>
        <AppContainer>
          <div class="w-full flex flex-col xl:flex-row gap-20 items-center">
            <div class="xl:w-1/2">
              <h2
                class="text-3xl md:text-5xl block font-bold text-orange-500 relative" 
              >
                About us
              </h2>
  
              <div class="flex items-start gap-8 mt-4">
                <div class="w-20 h-1 bg-orange-500 mt-2 hidden md:block"></div>
                <div class="flex flex-col gap-4">
                  <p class="text-base font-normal text-gray-500 leading-5 max-w-sm">
                    Ready to elevate your living experience? Kelitor - where exceptional
                    homes and extraordinary properties meet. Say goodbye to ordinary and
                    hello to extraordinary. Your dream home awaits!
                  </p>
                
                </div>
              </div>
            </div>
            <div class="xl:w-1/2">
              <div
                class="w-full h-[250px] md:h-[500px] bg-slate-100 overflow-hidden" data-aos="fade-up" data-aos-delay="100"
              >
                <img
                  src="https://images.unsplash.com/photo-1603901622056-0a5bee231395?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1462&q=80"
                  class="w-full h-full object-center object-cover"
                  alt=""
                />
              </div>
            </div>
          </div>
        </AppContainer>
      </div>
    </div>
  </template>
  