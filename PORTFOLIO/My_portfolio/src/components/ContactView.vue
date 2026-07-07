<template>
  <section class="border border-custom rounded-xl">
    <h1 class="text-center font-extrabold text-[#00e5ff] text-3xl mt-12 tracking-tight">
      Me contacter
    </h1>
    <div class="w-12 h-1 bg-indigo-500 mx-auto rounded-full mt-3"></div>

    <!-- Nouveau paragraphe captivant -->
    <p class="text-center  mt-6 max-w-xl mx-auto px-6 text-base sm:text-lg leading-relaxed">
      Un projet en tête, une opportunité de collaboration ou simplement envie d'échanger sur les dernières technos ? Choisissez le canal qui vous convient le mieux, je serai ravi de vous répondre !
    </p>

    <div class="container px-6 py-12 mx-auto">
      <div class="lg:flex lg:items-stretch lg:-mx-6 gap-8">

        <div class="lg:w-1/2 lg:mx-6 flex flex-col justify-center">
          <h2 class="text-2xl font-semibold text-[#00e5ff] lg:text-3xl mb-8">
            Vous préférez...
          </h2>

          <div class="space-y-6">
            <a href="https://wa.me/2250556654351" target="_blank" class="flex items-center gap-3 text-gray-600 dark:text-gray-400 hover:text-[#00e5ff] dark:hover:text-[#00e5ff] transition-colors duration-300 group">
              <div class="p-2 rounded-lg  border border-transparent group-hover:border-cyan-500/20">
                <Icon icon="logos:whatsapp-icon" width="26" />
              </div>
              <span class="text-base font-medium">+225 05 56 65 43 51</span>
            </a>

            <a href="tel:+2250556654351" class="flex items-center gap-3 text-gray-600 dark:text-gray-400 hover:text-[#00e5ff] dark:hover:text-[#00e5ff] transition-colors duration-300 group">
              <div class="p-2 rounded-lg border border-transparent group-hover:border-cyan-500/20 text-blue-500 dark:text-blue-400">
                <Icon icon="solar:phone-calling-rounded-linear" width="26" />
              </div>
              <span class="text-base font-medium">+225 05 56 65 43 51</span>
            </a>

            <a href="mailto:judicael.kouli@epitech.eu" class="flex items-center gap-3 text-gray-600 dark:text-gray-400 hover:text-[#00e5ff] dark:hover:text-[#00e5ff] transition-colors duration-300 group">
              <div class="p-2 rounded-lg border border-transparent group-hover:border-cyan-500/20 text-blue-500 dark:text-blue-400">
                <Icon icon="solar:letter-linear" width="26" />
              </div>
              <span class="text-base font-medium truncate">judicael.kouli@epitech.eu</span>
            </a>
          </div>

          <div class="mt-12">
            <h3 class="text-[#00e5ff] font-medium mb-4">Ou via les réseaux...</h3>
            <div class="flex items-center gap-4">
              <a class="p-2 rounded-full text-gray-500 dark:text-gray-400 hover:text-[#00e5ff] dark:hover:text-[#00e5ff] border border-transparent hover:border-cyan-500/20 transition-all duration-300 hover:-translate-y-1" href="https://github.com/judicaelkouly" target="_blank" title="GitHub">
                <Icon icon="mdi:github" width="26" />
              </a>

              <a class="p-2 rounded-full text-gray-500 dark:text-gray-400 hover:text-[#00e5ff] dark:hover:text-[#00e5ff] border border-transparent hover:border-cyan-500/20 transition-all duration-300 hover:-translate-y-1" href="https://www.linkedin.com/in/kouli" target="_blank" title="LinkedIn">
                <Icon icon="mdi:linkedin" width="26" />
              </a>

            </div>
          </div>
        </div>

        <div class="mt-8 lg:w-1/2 lg:mx-6">
          <div class="w-full px-8 py-10 mx-auto overflow-hidden rounded-lg shadow-2xl lg:max-w-xl shadow-gray-300/50">
            <h1 class="text-lg font-medium text-[#00e5ff] text-center">M'envoyer un message</h1>

            <form class="mt-6" ref="form" @submit.prevent="sendEmail">
              <div class="flex-1">
                <label class="block mb-2 text-sm text-gray-600 dar:text-gray-200">Full Name</label>
                <input
                  type="text"
                  placeholder="John Doe"
                  name="full-name"
                  required
                  class="block w-full px-5 py-3 mt-2 placeholder-gray-400 border border-custom rounded-md dar:placeholder-gray-600 dar:bg-gray-900 dar:text-gray-300 dar:border-gray-700 focus:border-blue-400 dar:focus:border-blue-400 focus:ring-blue-400 focus:outline-none focus:ring focus:ring-opacity-40"
                />
              </div>

              <div class="flex-1 mt-6">
                <label class="block mb-2 text-sm text-gray-600 dar:text-gray-200">Email address</label>
                <input
                  type="email"
                  placeholder="johndoe@example.com"
                  name="email"
                  required
                  class="block w-full px-5 py-3 mt-2 placeholder-gray-400 border border-custom rounded-md dar:placeholder-gray-600 dar:bg-gray-900 dar:text-gray-300 dar:border-gray-700 focus:border-blue-400 dar:focus:border-blue-400 focus:ring-blue-400 focus:outline-none focus:ring focus:ring-opacity-40"
                />
              </div>

              <div class="flex-1 mt-6">
                <label class="block mb-2 text-sm text-gray-600 dar:text-gray-200">Sujet</label>
                <input
                  type="text"
                  placeholder="sujet*"
                  name="subject"
                  required
                  class="block w-full px-5 py-3 mt-2 placeholder-gray-400 border border-custom rounded-md dar:placeholder-gray-600 dar:bg-gray-900 dar:text-gray-300 dar:border-gray-700 focus:border-blue-400 dar:focus:border-blue-400 focus:ring-blue-400 focus:outline-none focus:ring focus:ring-opacity-40"
                />
              </div>

              <div class="w-full mt-6">
                <label class="block mb-2 text-sm text-gray-600 dar:text-gray-200">Message</label>
                <textarea
                  name="message"
                  required
                  class="block w-full h-32 px-5 py-3 mt-2 placeholder-gray-400 border border-custom rounded-md md:h-48 dar:placeholder-gray-600 dar:bg-gray-900 dar:text-gray-300 dar:border-gray-700 focus:border-blue-400 dar:focus:border-blue-400 focus:ring-blue-400 focus:outline-none focus:ring focus:ring-opacity-40"
                  placeholder="Message"
                ></textarea>
              </div>

              <button
                type="submit"
                :disabled="isSending"
                class="w-full px-6 py-3 mt-6 text-sm font-medium tracking-wide text-white transition-colors duration-300 transform bg-blue-400 rounded-md hover:bg-blue-500 focus:outline-none focus:ring focus:ring-blue-300 focus:ring-opacity-50 disabled:opacity-50 disabled:cursor-not-allowed"
              >
                {{ isSending ? 'Envoi en cours...' : 'Envoyer mon message' }}
              </button>

              <p v-if="statusMessage" :class="statusSuccess ? 'text-green-500' : 'text-red-500'" class="mt-4 text-sm text-center">
                {{ statusMessage }}
              </p>
            </form>
          </div>
        </div>

      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'
import { Icon } from '@iconify/vue'
import emailjs from '@emailjs/browser'

const form = ref(null)
const isSending = ref(false)
const statusMessage = ref('')
const statusSuccess = ref(false)

const sendEmail = () => {
  isSending.value = true
  statusMessage.value = ''

  emailjs
    .sendForm('service_ptyi3bi', 'template_4s9pq7x', form.value, {
      publicKey: 'GOH39Ip3bsYibs9O3',
    })
    .then(() => {
      statusSuccess.value = true
      statusMessage.value = 'Message envoyé avec succès !'
      form.value.reset()
    })
    .catch((error) => {
      statusSuccess.value = false
      statusMessage.value = "Une erreur est survenue, veuillez réessayer."
      console.log('FAILED...', error.text)
    })
    .finally(() => {
      isSending.value = false
    })
}
</script>
