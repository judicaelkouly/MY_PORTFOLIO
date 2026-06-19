<template>
  <div class="relative font-inter antialiased">

    <main class="mb-20 relative min-h-screen flex flex-col justify-center overflow-hidden">
      <h1 class="text-[#00e5ff] font-bold text-center text-3xl mb-6">Mes Certifications</h1>
        <div class="w-full max-w-5xl mx-auto px-4 md:px-6 py-24">

            <!-- Card slider  -->
            <section class="px-12">
                <div class="max-w-lg mx-auto relative">

                    <input id="article-01" type="radio" name="slider" class="sr-only peer/01">
                    <input id="article-02" type="radio" name="slider" class="sr-only peer/02">
                    <input id="article-03" type="radio" name="slider" class="sr-only peer/03" checked>
                    <input id="article-04" type="radio" name="slider" class="sr-only peer/04">
                    <input id="article-05" type="radio" name="slider" class="sr-only peer/05">

                    <div class="
                        absolute inset-0 scale-[67.5%] z-20 transition-all duration-500 ease-[cubic-bezier(0.25,1,0.5,1)]
                        peer-focus-visible/01:[&_article]:ring
                        peer-focus-visible/01:[&_article]:ring-indigo-300
                        peer-checked/01:relative
                        peer-checked/01:z-50
                        peer-checked/01:translate-x-0
                        peer-checked/01:scale-100
                        peer-checked/01:[&>label]:pointer-events-none
                        peer-checked/02:-translate-x-20
                        peer-checked/02:scale-[83.75%]
                        peer-checked/02:z-40
                        peer-checked/03:-translate-x-40
                        peer-checked/03:z-30
                        peer-checked/04:-translate-x-40
                        peer-checked/04:opacity-0
                        peer-checked/05:-translate-x-40
                    ">
                        <label class="absolute inset-0" for="article-01"><span class="sr-only">Focus on the big picture</span></label>
                        <article class="bg-gray-600 border border-custom p-6 rounded-lg shadow-2xl">
                            <header class="mb-2">
                                <img class="inline-flex rounded-full shadow mb-3" src="https://cruip-tutorials.vercel.app/card-slider/icon.svg" width="44" height="44" alt="Icon" />
                                <h1 class="text-xl font-bold text-black">Focus on the big picture</h1>
                            </header>
                            <div class="text-sm leading-relaxed space-y-4 mb-2">
                                <p>
                                    Many desktop publishing packages and web page editors now use Pinky as their default model text, and a search for more variants will uncover many web sites still in their infancy.
                                </p>
                                <p>
                                    All the generators tend to repeat predefined chunks as necessary, making this the first true generator on the Internet.
                                </p>
                            </div>

                        </article>
                    </div>

                    <div class="
                        absolute inset-0 scale-[67.5%] z-20 transition-all duration-500 ease-[cubic-bezier(0.25,1,0.5,1)]
                        peer-focus-visible/02:[&_article]:ring
                        peer-focus-visible/02:[&_article]:ring-indigo-300
                        peer-checked/01:translate-x-20
                        peer-checked/01:scale-[83.75%]
                        peer-checked/01:z-40
                        peer-checked/02:relative
                        peer-checked/02:z-50
                        peer-checked/02:translate-x-0
                        peer-checked/02:scale-100
                        peer-checked/02:[&>label]:pointer-events-none
                        peer-checked/03:-translate-x-20
                        peer-checked/03:scale-[83.75%]
                        peer-checked/03:z-40
                        peer-checked/04:-translate-x-40
                        peer-checked/04:z-30
                        peer-checked/05:-translate-x-40
                        peer-checked/05:opacity-0
                    ">
                        <label class="absolute inset-0" for="article-02"><span class="sr-only">Focus on the big picture</span></label>
                        <article class="bg-gray-600 p-6 rounded-lg shadow-2xl">
                            <header class="mb-2">
                                <img class="inline-flex rounded-full shadow mb-3" src="https://cruip-tutorials.vercel.app/card-slider/icon.svg" width="44" height="44" alt="Icon" />
                                <h1 class="text-xl font-bold text-black">Focus on the big picture</h1>
                            </header>
                            <div class="text-sm leading-relaxed space-y-4 mb-2">
                                <p>
                                    Many desktop publishing packages and web page editors now use Pinky as their default model text, and a search for more variants will uncover many web sites still in their infancy.
                                </p>
                                <p>
                                    All the generators tend to repeat predefined chunks as necessary, making this the first true generator on the Internet.
                                </p>
                            </div>

                        </article>
                    </div>

                    <div class="
                        absolute inset-0 scale-[67.5%] z-20 transition-all duration-500 ease-[cubic-bezier(0.25,1,0.5,1)]
                        peer-focus-visible/03:[&_article]:ring
                        peer-focus-visible/03:[&_article]:ring-indigo-300
                        peer-checked/01:translate-x-40
                        peer-checked/01:z-30
                        peer-checked/02:translate-x-20
                        peer-checked/02:scale-[83.75%]
                        peer-checked/02:z-40
                        peer-checked/03:relative
                        peer-checked/03:z-50
                        peer-checked/03:translate-x-0
                        peer-checked/03:scale-100
                        peer-checked/03:[&>label]:pointer-events-none
                        peer-checked/04:-translate-x-20
                        peer-checked/04:scale-[83.75%]
                        peer-checked/04:z-40
                        peer-checked/05:-translate-x-40
                        peer-checked/05:z-30
                    ">
                        <label class="absolute inset-0" for="article-03"><span class="sr-only">Focus on the big picture</span></label>
                        <article class="bg-gray-600 p-6 rounded-lg shadow-2xl">
                            <header class="mb-2">
                                <img class="inline-flex rounded-full shadow mb-3" src="https://cruip-tutorials.vercel.app/card-slider/icon.svg" width="44" height="44" alt="Icon" />
                                <h1 class="text-xl font-bold text-black">Focus on the big picture</h1>
                            </header>
                            <div class="text-sm leading-relaxed space-y-4 mb-2">
                                <p>
                                    Many desktop publishing packages and web page editors now use Pinky as their default model text, and a search for more variants will uncover many web sites still in their infancy.
                                </p>
                                <p>
                                    All the generators tend to repeat predefined chunks as necessary, making this the first true generator on the Internet.
                                </p>
                            </div>

                        </article>
                    </div>

                    <div class="
                        absolute inset-0 scale-[67.5%] z-20 transition-all duration-500 ease-[cubic-bezier(0.25,1,0.5,1)]
                        peer-focus-visible/04:[&_article]:ring
                        peer-focus-visible/04:[&_article]:ring-indigo-300

                        peer-checked/01:translate-x-40
                        peer-checked/01:opacity-0

                        peer-checked/02:translate-x-40
                        peer-checked/02:z-30

                        peer-checked/03:translate-x-20
                        peer-checked/03:scale-[83.75%]
                        peer-checked/03:z-40

                        peer-checked/04:relative
                        peer-checked/04:z-50
                        peer-checked/04:translate-x-0
                        peer-checked/04:scale-100
                        peer-checked/04:[&>label]:pointer-events-none

                        peer-checked/05:-translate-x-20
                        peer-checked/05:scale-[83.75%]
                        peer-checked/05:z-40
                    ">
                        <label class="absolute inset-0" for="article-04"><span class="sr-only">Focus on the big picture</span></label>
                        <article class="bg-gray-600 p-6 rounded-lg shadow-2xl">
                            <header class="mb-2">
                                <img class="inline-flex rounded-full shadow mb-3" src="https://cruip-tutorials.vercel.app/card-slider/icon.svg" width="44" height="44" alt="Icon" />
                                <h1 class="text-xl font-bold text-black">Focus on the big picture</h1>
                            </header>
                            <div class="text-sm leading-relaxed space-y-4 mb-2">
                                <p>
                                    Many desktop publishing packages and web page editors now use Pinky as their default model text, and a search for more variants will uncover many web sites still in their infancy.
                                </p>
                                <p>
                                    All the generators tend to repeat predefined chunks as necessary, making this the first true generator on the Internet.
                                </p>
                            </div>

                        </article>
                    </div>

                    <div class="
                        absolute inset-0 scale-[67.5%] z-20 transition-all duration-500 ease-[cubic-bezier(0.25,1,0.5,1)]
                        peer-focus-visible/05:[&_article]:ring
                        peer-focus-visible/05:[&_article]:ring-indigo-300
                        peer-checked/01:translate-x-40
                        peer-checked/02:translate-x-40
                        peer-checked/02:opacity-0
                        peer-checked/03:translate-x-40
                        peer-checked/03:z-30
                        peer-checked/04:translate-x-20
                        peer-checked/04:scale-[83.75%]
                        peer-checked/04:z-40
                        peer-checked/05:relative
                        peer-checked/05:z-50
                        peer-checked/05:translate-x-0
                        peer-checked/05:scale-100
                        peer-checked/05:[&>label]:pointer-events-none
                    ">
                        <label class="absolute inset-0" for="article-05"><span class="sr-only">Focus on the big picture</span></label>
                        <article class="bg-gray-600 p-6 rounded-lg shadow-2xl">
                            <header class="mb-2">
                                <img class="inline-flex rounded-full shadow mb-3" src="https://cruip-tutorials.vercel.app/card-slider/icon.svg" width="44" height="44" alt="Icon" />
                                <h1 class="text-xl font-bold text-black">Focus on the big picture</h1>
                            </header>
                            <div class="text-sm leading-relaxed space-y-4 mb-2">
                                <p>
                                    Many desktop publishing packages and web page editors now use Pinky as their default model text, and a search for more variants will uncover many web sites still in their infancy.
                                </p>
                                <p>
                                    All the generators tend to repeat predefined chunks as necessary, making this the first true generator on the Internet.
                                </p>
                            </div>

                        </article>
                    </div>
                </div>
            </section>
            <!-- End: Card slider  -->

        </div>

   <!-- title -->
<div class="text-center p-10">
  <h1 class="font-bold text-[#00e5ff] text-3xl mb-4">Projets réalisés</h1>
</div>

<!-- ✅ Grid Section - Starts Here 👇 -->
<section class="w-fit mx-auto grid grid-cols-1 lg:grid-cols-3 md:grid-cols-2 justify-items-center justify-center gap-y-20 gap-x-14 mt-10 mb-5">

  <div class="w-90 bg-slate-400 shadow-md rounded-xl duration-500 hover:scale-105 hover:shadow-xl">

      <img src="https://images.unsplash.com/photo-1649261191606-cb2496e97eee?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwcm9maWxlLXBhZ2V8NDR8fHxlbnwwfHx8fA%3D%3D&auto=format&fit=crop&w=500&q=60" alt="Product" class="h-90 w-90 object-cover rounded-t-xl" />
      <div class="px-4 py-3 w-90">
        <span class="text-black mr-3  text-xs">Brand</span>
        <span class="text-black mr-3  text-xs">Brand</span>
        <span class="text-black mr-3  text-xs">Brand</span>
        <span class="text-black mr-3 text-xs">Brand</span>
        <p class="text-lg font-bold text-black truncate block capitalize">My_Shop</p>
        <p class="text-lg ">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Aspernatur, sunt laudantium! Molestias perspiciatis eius eveniet! Saepe ducimus recusandae ipsam porro enim repudiandae praesentium voluptatem ab a, laboriosam molestias sint dolorum!</p>
        <div class="flex items-center mt-5">
          <a href="">
          <Icon icon="ri:github-fill" width="30" color="black"/>
          </a>
          <div class="ml-auto">
             <a href="">
            <Icon icon="icon-park-outline:eyes" width="30" color="black" />
            </a>
          </div>
        </div>
      </div>

  </div>

  <div class="w-90 bg-slate-400 shadow-md rounded-xl duration-500 hover:scale-105 hover:shadow-xl">

      <img src="https://images.unsplash.com/photo-1649261191606-cb2496e97eee?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwcm9maWxlLXBhZ2V8NDR8fHxlbnwwfHx8fA%3D%3D&auto=format&fit=crop&w=500&q=60" alt="Product" class="h-90 w-90 object-cover rounded-t-xl" />
      <div class="px-4 py-3 w-90">
        <span class="text-black mr-3  text-xs">Brand</span>
        <span class="text-black mr-3  text-xs">Brand</span>
        <span class="text-black mr-3  text-xs">Brand</span>
        <span class="text-black mr-3 text-xs">Brand</span>
        <p class="text-lg font-bold text-black truncate block capitalize">My_Shop</p>
        <p class="text-lg ">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Aspernatur, sunt laudantium! Molestias perspiciatis eius eveniet! Saepe ducimus recusandae ipsam porro enim repudiandae praesentium voluptatem ab a, laboriosam molestias sint dolorum!</p>
        <div class="flex items-center mt-5">
          <a href="">
          <Icon icon="ri:github-fill" width="30" color="black"/>
          </a>
          <div class="ml-auto">
             <a href="">
            <Icon icon="icon-park-outline:eyes" width="30" color="black" />
            </a>
          </div>
        </div>
      </div>

  </div>

  <div class="w-90 bg-slate-400 shadow-md rounded-xl duration-500 hover:scale-105 hover:shadow-xl">

      <img src="https://images.unsplash.com/photo-1649261191606-cb2496e97eee?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwcm9maWxlLXBhZ2V8NDR8fHxlbnwwfHx8fA%3D%3D&auto=format&fit=crop&w=500&q=60" alt="Product" class="h-90 w-90 object-cover rounded-t-xl" />
      <div class="px-4 py-3 w-90">
        <span class="text-black mr-3  text-xs">Brand</span>
        <span class="text-black mr-3  text-xs">Brand</span>
        <span class="text-black mr-3  text-xs">Brand</span>
        <span class="text-black mr-3 text-xs">Brand</span>
        <p class="text-lg font-bold text-black truncate block capitalize">My_Shop</p>
        <p class="text-lg ">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Aspernatur, sunt laudantium! Molestias perspiciatis eius eveniet! Saepe ducimus recusandae ipsam porro enim repudiandae praesentium voluptatem ab a, laboriosam molestias sint dolorum!</p>
        <div class="flex items-center mt-5">
          <a href="">
          <Icon icon="ri:github-fill" width="30" color="black"/>
          </a>
          <div class="ml-auto">
             <a href="">
            <Icon icon="icon-park-outline:eyes" width="30" color="black" />
            </a>
          </div>
        </div>
      </div>

  </div>

  <div class="w-90 bg-slate-400 shadow-md rounded-xl duration-500 hover:scale-105 hover:shadow-xl">

      <img src="https://images.unsplash.com/photo-1649261191606-cb2496e97eee?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwcm9maWxlLXBhZ2V8NDR8fHxlbnwwfHx8fA%3D%3D&auto=format&fit=crop&w=500&q=60" alt="Product" class="h-90 w-90 object-cover rounded-t-xl" />
      <div class="px-4 py-3 w-90">
        <span class="text-black mr-3  text-xs">Brand</span>
        <span class="text-black mr-3  text-xs">Brand</span>
        <span class="text-black mr-3  text-xs">Brand</span>
        <span class="text-black mr-3 text-xs">Brand</span>
        <p class="text-lg font-bold text-black truncate block capitalize">My_Shop</p>
        <p class="text-lg ">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Aspernatur, sunt laudantium! Molestias perspiciatis eius eveniet! Saepe ducimus recusandae ipsam porro enim repudiandae praesentium voluptatem ab a, laboriosam molestias sint dolorum!</p>
        <div class="flex items-center mt-5">
          <a href="">
          <Icon icon="ri:github-fill" width="30" color="black"/>
          </a>
          <div class="ml-auto">
             <a href="">
            <Icon icon="icon-park-outline:eyes" width="30" color="black" />
            </a>
          </div>
        </div>
      </div>

  </div>

  <div class="w-90 bg-slate-400 shadow-md rounded-xl duration-500 hover:scale-105 hover:shadow-xl">

      <img src="https://images.unsplash.com/photo-1649261191606-cb2496e97eee?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwcm9maWxlLXBhZ2V8NDR8fHxlbnwwfHx8fA%3D%3D&auto=format&fit=crop&w=500&q=60" alt="Product" class="h-90 w-90 object-cover rounded-t-xl" />
      <div class="px-4 py-3 w-90">
        <span class="text-black mr-3  text-xs">Brand</span>
        <span class="text-black mr-3  text-xs">Brand</span>
        <span class="text-black mr-3  text-xs">Brand</span>
        <span class="text-black mr-3 text-xs">Brand</span>
        <p class="text-lg font-bold text-black truncate block capitalize">My_Shop</p>
        <p class="text-lg ">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Aspernatur, sunt laudantium! Molestias perspiciatis eius eveniet! Saepe ducimus recusandae ipsam porro enim repudiandae praesentium voluptatem ab a, laboriosam molestias sint dolorum!</p>
        <div class="flex items-center mt-5">
          <a href="">
          <Icon icon="ri:github-fill" width="30" color="black"/>
          </a>
          <div class="ml-auto">
             <a href="">
            <Icon icon="icon-park-outline:eyes" width="30" color="black" />
            </a>
          </div>
        </div>
      </div>

  </div>

  <div class="w-90 bg-slate-400 shadow-md rounded-xl duration-500 hover:scale-105 hover:shadow-xl">

      <img src="https://images.unsplash.com/photo-1649261191606-cb2496e97eee?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwcm9maWxlLXBhZ2V8NDR8fHxlbnwwfHx8fA%3D%3D&auto=format&fit=crop&w=500&q=60" alt="Product" class="h-90 w-90 object-cover rounded-t-xl" />
      <div class="px-4 py-3 w-90">
        <span class="text-black mr-3  text-xs">Brand</span>
        <span class="text-black mr-3  text-xs">Brand</span>
        <span class="text-black mr-3  text-xs">Brand</span>
        <span class="text-black mr-3 text-xs">Brand</span>
        <p class="text-lg font-bold text-black truncate block capitalize">My_Shop</p>
        <p class="text-lg ">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Aspernatur, sunt laudantium! Molestias perspiciatis eius eveniet! Saepe ducimus recusandae ipsam porro enim repudiandae praesentium voluptatem ab a, laboriosam molestias sint dolorum!</p>
        <div class="flex items-center mt-5">
          <a href="">
          <Icon icon="ri:github-fill" width="30" color="black"/>
          </a>
          <div class="ml-auto">
             <a href="">
            <Icon icon="icon-park-outline:eyes" width="30" color="black" />
            </a>
          </div>
        </div>
      </div>

  </div>
</section>



    </main>




</div>
<FooterView/>
</template>


<script setup>
import { Icon } from '@iconify/vue'
import FooterView from './FooterView.vue';
</script>
 <style>
@import 'https://fonts.googleapis.com/icon?family=Material+Icons';
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@200;300;400&display=swap');



.hr-text {
  line-height: 1em;
  position: relative;
  outline: 0;
  border: 0;
  color: black;
  text-align: center;
  height: 1.5em;
  opacity: 0.5;
}
.hr-text:before {
  content: "";
  background: linear-gradient(to right, transparent, #818078, transparent);
  position: absolute;
  left: 0;
  top: 50%;
  width: 100%;
  height: 1px;
}
.hr-text:after {
  content: attr(data-content);
  position: relative;
  display: inline-block;
  color: black;
  padding: 0 0.5em;
  line-height: 1.5em;
  color: #818078;
  background-color: #fcfcfa;
}
</style>
