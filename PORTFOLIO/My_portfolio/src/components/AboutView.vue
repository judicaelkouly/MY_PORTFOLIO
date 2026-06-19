<template>
<div>




     <section class="flex flex-col md:flex-row items-center justify-center gap-10 max-md:px-4">
    <div class="relative shadow-2xl shadow-indigo-600/40 rounded-2xl overflow-hidden shrink-0">
        <img class="max-w-md w-full object-cover rounded-2xl"
            src="/public/about.png"
            alt="">

    </div>
    <div class="text-sm max-w-lg">
        <h1 class="text-xl font-semibold ">Un peu à prpos de moi...</h1>
        <div class="w-24 h-[3px] rounded-full bg-gradient-to-r from-indigo-600 to-[#DDD9FF]"></div>
        <p class="mt-8">PrebuiltUI helps you build faster by transforming your design vision into fully functional,
            production-ready UI components.
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Velit accusamus enim voluptas inventore,
            qui nulla possimus necessitatibus iusto, cupiditate error porro eligendi ex, alias modi explicabo dolorum! Magnam, in facilis?
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Illum est
            rem alias provident ad corrupti debitis quia labore quo r
            epellat esse ut aperiam, modi sequi quos voluptatibus in nulla ipsum?
          </p>


    </div>
</section>
    <section class="bg-animated cyber-grid py-20 relative overflow-hidden">
        <div class="container mx-auto px-4">
            <h2 class="text-3xl text-[#00e5ff] font-bold mb-12 ">Intérêts personnels</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <div class="feature-card rounded-lg p-6 floating">
                    <div class="text-5xl mb-4 text-cyan-400 feature-icon">
                        <Icon icon="lsicon:marketing-filled" width="26" />
                    </div>
                    <h3 class="text-2xl font-bold mb-2">Marketing</h3>
                    <p class="">Interface directly with our advanced AI using cutting-edge neural technology.</p>
                </div>
                <div class="feature-card rounded-lg p-6 floating" style="animation-delay: 1s;">
                    <div class="text-5xl mb-4 text-pink-500 feature-icon">
                        <Icon icon="streamline-kameleon-color:windows-coding-duo" width="26" />
                    </div>
                    <h3 class="streamline-kameleon-color:windows-coding-duo">Coding</h3>
                    <p class="">Unbreakable security powered by quantum entanglement protocols.</p>
                </div>
                <div class="feature-card rounded-lg p-6 floating" style="animation-delay: 2s;">
                    <div class="text-5xl mb-4 text-purple-500 feature-icon">
                        <Icon icon="flat-color-icons:manager" width="26" />
                    </div>
                    <h3 class="text-2xl font-bold mb-2">Community Manager</h3>
                    <p class="">Experience fully immersive 3D holographic environments.</p>
                </div>
                <div class="feature-card rounded-lg p-6 floating" style="animation-delay: 0.5s;">
                    <div class="text-5xl mb-4 text-green-400 feature-icon">
                        <Icon icon="mdi:business-outline" width="26" />
                    </div>
                    <h3 class="text-2xl font-bold mb-2">Business</h3>
                    <p class="">Microscopic nodes form an intelligent, self-healing network infrastructure.</p>
                </div>
                <div class="feature-card rounded-lg p-6 floating" style="animation-delay: 1.5s;">
                    <div class="text-5xl mb-4 text-yellow-400 feature-icon">
                       <Icon icon="hugeicons:marketing" width="26" />
                    </div>
                    <h3 class="text-2xl font-bold mb-2">Communication</h3>
                    <p class="">Harness the power of stars with our miniaturized fusion reactors.</p>
                </div>

            </div>
        </div>
    </section>

     <FooterView/>

      </div>
</template>

<script setup>
import { Icon } from '@iconify/vue'
import FooterView from './FooterView.vue';

</script>

<style>
  /* Gradient text */
        .gradient-text {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        /* Animated gradient border */
        .gradient-border {
            position: relative;
            background: linear-gradient(#0a0a0a, #0a0a0a) padding-box,
                        linear-gradient(135deg, #667eea, #764ba2, #f093fb) border-box;
            border: 2px solid transparent;
        }
</style>
