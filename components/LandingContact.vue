<script setup>
const success = ref(false);
const error = ref(false);

const formData = ref({ name: "", contact: "", email: "", country: "", message: "" });
const closeNot = () => {
  success.value = false;
};
const closeErrorNot = () => {
  error.value = false;
};

const submitForm = async () => {
  const response = await $fetch(
    "https://getform.io/f/84ccb698-eb86-493d-b43a-37086b7d8109",
    {
      method: "POST",
      body: formData.value,
    }
  );
  if (response.success) {
    success.value = true;
    setTimeout(closeNot(), 3000);
    formData.value.name = formData.value.contact = formData.value.email = formData.value.country = formData.value.message = null;
  } else {
    setTimeout(closeErrorNot(), 3000);
    formData.value.name = formData.value.contact = formData.value.email = formData.value.country = formData.value.message = null;
  }
};
</script>

<template>
  <div>
    <div class="w-full py-20 xl:py-32">
      <AppContainer>
        <div class="w-full flex flex-col xl:flex-row gap-10 md:gap-20 items-center lg:items-start">
          <div class="xl:w-1/2 flex flex-col gap-5 xl:translate-x-20" data-aos="fade-right" data-aos-delay="100">
            <h2
              class="text-3xl md:text-5xl font-bold text-orange-500 leading-tight max-w-md"
            >
              Send us a message
            </h2>
            <p class="text-sm md:text-base font-normal text-gray-500 leading-5 max-w-md">
              Take the initiative and reach out to us by sending a message. We are here to assist you and provide prompt, personalized support. 

            </p>
          </div>
          <div class="w-full md:w-1/2 relative" data-aos="fade-left">
            <form
              action="submit"
              @submit.prevent="submitForm()"
              class="mb-0 space-y-4 bg-white w-full rounded-lg p-4 lg:p-8"
            >
              <div>
                <label for="name" class="sr-only">Full name</label>

                <div class="relative">
                  <input
                    type="text"
                    class="w-full rounded-lg border-gray-200 border-2 p-4 pr-12 text-sm shadow-sm"
                    placeholder="Enter Full name"
                    v-model="formData.name"
                    required
                  />

                  <span
                    class="absolute inset-y-0 right-0 grid place-content-center px-4 text-gray-400"
                  >
                    <svg
                      xmlns="http://www.w3.org/2000/svg"
                      fill="none"
                      viewBox="0 0 24 24"
                      stroke-width="1.5"
                      stroke="currentColor"
                      class="w-4 h-4"
                    >
                      <path
                        stroke-linecap="round"
                        stroke-linejoin="round"
                        d="M17.982 18.725A7.488 7.488 0 0012 15.75a7.488 7.488 0 00-5.982 2.975m11.963 0a9 9 0 10-11.963 0m11.963 0A8.966 8.966 0 0112 21a8.966 8.966 0 01-5.982-2.275M15 9.75a3 3 0 11-6 0 3 3 0 016 0z"
                      />
                    </svg>
                  </span>
                </div>
              </div>
              <div>
                <label for="email" class="sr-only">Email</label>

                <div class="relative">
                  <input
                    type="email"
                    class="w-full rounded-lg border-gray-200 border-2 p-4 pr-12 text-sm shadow-sm"
                    placeholder="Enter email"
                    v-model="formData.email"
                    required
                  />

                  <span class="absolute inset-y-0 right-0 grid place-content-center px-4">
                    <svg
                      xmlns="http://www.w3.org/2000/svg"
                      class="h-4 w-4 text-gray-400"
                      fill="none"
                      viewBox="0 0 24 24"
                      stroke="currentColor"
                    >
                      <path
                        stroke-linecap="round"
                        stroke-linejoin="round"
                        stroke-width="2"
                        d="M16 12a4 4 0 10-8 0 4 4 0 008 0zm0 0v1.5a2.5 2.5 0 005 0V12a9 9 0 10-9 9m4.5-1.206a8.959 8.959 0 01-4.5 1.207"
                      />
                    </svg>
                  </span>
                </div>
              </div>

              <div>
                <label for="contact" class="sr-only">Contact Number</label>

                <div class="relative">
                  <input
                    type="tel"
                    class="w-full rounded-lg border-gray-200 p-4 border-2 pr-12 text-sm shadow-sm"
                    placeholder="Enter Telephone Number (Whatsapp)"
                    v-model="formData.contact"
                    required
                  />

                  <span
                    class="absolute inset-y-0 right-0 grid place-content-center px-4 text-gray-400"
                  >
                    <svg
                      xmlns="http://www.w3.org/2000/svg"
                      fill="none"
                      viewBox="0 0 24 24"
                      stroke-width="1.5"
                      stroke="currentColor"
                      class="w-4 h-4"
                    >
                      <path
                        stroke-linecap="round"
                        stroke-linejoin="round"
                        d="M2.25 6.75c0 8.284 6.716 15 15 15h2.25a2.25 2.25 0 002.25-2.25v-1.372c0-.516-.351-.966-.852-1.091l-4.423-1.106c-.44-.11-.902.055-1.173.417l-.97 1.293c-.282.376-.769.542-1.21.38a12.035 12.035 0 01-7.143-7.143c-.162-.441.004-.928.38-1.21l1.293-.97c.363-.271.527-.734.417-1.173L6.963 3.102a1.125 1.125 0 00-1.091-.852H4.5A2.25 2.25 0 002.25 4.5v2.25z"
                      />
                    </svg>
                  </span>
                </div>
              </div>
              <div>
                <label for="contact" class="sr-only">Country</label>

                <div class="relative">
                  <input
                    list="country"
                    class="w-full rounded-lg border-gray-200 border-2 p-4 pr-12 text-sm shadow-sm"
                    placeholder="Country"
                    v-model="formData.country"
                    required
                  />

                  <span
                    class="absolute inset-y-0 right-0 grid place-content-center px-4 text-gray-400"
                  >
                    <svg
                      xmlns="http://www.w3.org/2000/svg"
                      fill="none"
                      viewBox="0 0 24 24"
                      stroke-width="1.5"
                      stroke="currentColor"
                      class="w-4 h-4"
                    >
                      <path
                        stroke-linecap="round"
                        stroke-linejoin="round"
                        d="M3 3v1.5M3 21v-6m0 0l2.77-.693a9 9 0 016.208.682l.108.054a9 9 0 006.086.71l3.114-.732a48.524 48.524 0 01-.005-10.499l-3.11.732a9 9 0 01-6.085-.711l-.108-.054a9 9 0 00-6.208-.682L3 4.5M3 15V4.5"
                      />
                    </svg>
                  </span>
                </div>
              </div>
              <div>
                <label for="contact" class="sr-only">Message</label>

                <div class="relative">
                  <textarea
                    name="message"
                    id="message"
                    v-model="formData.message"
                    required
                    cols="30"
                    rows="10"
                    class="w-full rounded-lg border-gray-200 border-2 p-4 pr-12 text-sm shadow-sm"
                    placeholder="Message"
                  ></textarea>
                </div>
              </div>

              <button
                type="submit"
                class="block w-full  antialiased bg-gradient-to-br from-gray-900 to-black px-5 py-3 text-sm font-medium text-white"
              >
                Send Message
              </button>
            </form>
          </div>
        </div>
      </AppContainer>
    </div>
    <Error v-if="error" />
    <Success
      v-if="success"
      header="Message Sent Successfully"
      message="Thank you for Contacting Izmatrix Limited"
    />
  </div>
</template>
