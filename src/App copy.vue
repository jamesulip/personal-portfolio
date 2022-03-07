<script setup>
</script>

<template>
  <div class="dark">
    <div>
      <div class="py-16">
        <Switch v-model="enabled" :class="enabled ? 'bg-teal-900' : 'bg-teal-700'"
          class="relative inline-flex flex-shrink-0 h-[38px] w-[74px] border-2 border-transparent rounded-full cursor-pointer transition-colors ease-in-out duration-200 focus:outline-none focus-visible:ring-2 focus-visible:ring-white focus-visible:ring-opacity-75">
          <span class="sr-only">Use setting</span>
          <span aria-hidden="true" :class="enabled ? 'translate-x-9' : 'translate-x-0'"
            class="pointer-events-none inline-block h-[34px] w-[34px] rounded-full bg-white shadow-lg transform ring-0 transition ease-in-out duration-200" />
        </Switch>asdasd
      </div>
    </div>
    <div class="dark:bg-gray-800">
      <div>
        <div class="h-screen flex">
          <div class="max-w-7xl  m-auto py-16 px-4 sm:py-24 sm:px-6 lg:px-8 lg:flex lg:justify-between">
            <div class="max-w-xl self-center">
              <h2 class="text-xl text-white sm:text-1xl sm:tracking-tight lg:text-2xl flex">Hello there <div
                  class="animate-wiggle">👋</div> , Im</h2>
              <h2 class="text-4xl font-extrabold text-white sm:text-5xl sm:tracking-tight lg:text-6xl underline">James
                Santos Ulip</h2>
              <p class="mt-5 text-xl text-gray-400">
                I'm a full-stack web developer with a passion for developing and designing.
                I'm currently working at <a class="text-yellow-500"
                  href="https://www.tigergraphics.com.ph">Tigergraphics</a> as a Software Developer.
                I have a B.S. in Computer Science from the University of AMA UNIVERSITY AND COLLEGES year 2016.
                I enjoy working on projects that are both challenging and fun.
                I'm always looking to learn new things and improve my skills.
              </p>
              <div>
                <!-- git logo with link  -->
                <div>
                  <a class="flex items-center justify-center" href="">
                    <svg class="h-6 w-6 text-gray-400" fill="currentColor" viewBox="0 0 24 24">
                      <path
                        d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118" />
                    </svg>
                  </a>
                </div>

              </div>
            </div>
            <div>
              <img class="w-96 -scale-x-100" alt="Tangina burado na yung mukha ko sa edit XD"
                src="./assets/88959118_2948458481878646_7262408940095275008_n-removebg-preview.png" />
            </div>
          </div>
        </div>
      </div>
      <div class="h-screen grid m-auto">
        <img alt="Vue logo" src="./assets/viber_image_2022-03-03_17-07-58-479.jpg" />
      </div>

    </div>
  </div>
</template>