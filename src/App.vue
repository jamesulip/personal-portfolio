<script>
import { ref } from "vue";
import { Switch } from "@headlessui/vue";
export default {
  components: {
    Switch,
  },

  setup() {
    const enabled = ref(false);
    const darkMode = ref(true);
    const stacks = ref([
      {
        type: "spacer",
        text: "Front End",
      },
      {
        src: "https://raw.githubusercontent.com/devicons/devicon/master/icons/bootstrap/bootstrap-plain-wordmark.svg",
        alt: "bootstrap",
        text: "Bootstrap",
        link: "https://getbootstrap.com/",
      },
      {
        src: "https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original-wordmark.svg",
        alt: "css3",
        text: "CSS3",
        link: "https://www.w3.org/Style/CSS/",
      },
      {
        src: "https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original-wordmark.svg",
        alt: "html5",
        text: "HTML5",
        link: "https://www.w3.org/MarkUp/",
      },
      {
        src: "https://www.vectorlogo.zone/logos/tailwindcss/tailwindcss-icon.svg",
        alt: "tailwind",
        text: "Tailwind CSS",
        link: "https://tailwindcss.com/",
      },
      {
        src: "https://raw.githubusercontent.com/devicons/devicon/master/icons/vuejs/vuejs-original-wordmark.svg",
        alt: "vuejs",
        text: "Vue.js",
        link: "https://vuejs.org/",
      },
      {
        src: "https://www.vectorlogo.zone/logos/nuxtjs/nuxtjs-icon.svg",
        alt: "nuxtjs",
        text: "Nuxt.js",
        link: "https://nuxtjs.org/",
      },
      {
        src: "https://bestofjs.org/logos/vuetify.svg",
        alt: "vuetify",
        text: "Vuetify",
        link: "https://vuetifyjs.com/",
      },

      {
        src: "https://raw.githubusercontent.com/devicons/devicon/master/icons/android/android-original-wordmark.svg",
        alt: "android",
        text: "Android",
        link: "https://developer.android.com/",
      },
      {
        src: "https://upload.wikimedia.org/wikipedia/commons/d/d1/Ionic_Logo.svg",
        alt: "ionic",
        text: "Ionic",
        link: "https://ionicframework.com/",
      },
      {
        src: "https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-original.svg",
        alt: "javascript",
        text: "JavaScript",
        link: "https://developer.mozilla.org/en-US/docs/Web/JavaScript",
      },
      // end front end

      // Backend
      {
        type: "spacer",
        text: "Back End",
      },
      {
        src: "https://raw.githubusercontent.com/devicons/devicon/master/icons/nodejs/nodejs-original-wordmark.svg",
        alt: "nodejs",
        text: "Node.js",
        link: "https://nodejs.org/en/",
      },
      {
        src: "https://raw.githubusercontent.com/devicons/devicon/master/icons/mysql/mysql-original-wordmark.svg",
        alt: "mysql",
        text: "MySQL",
        link: "https://www.mysql.com/",
      },
      {
        src: "https://laravel.com/img/logomark.min.svg",
        alt: "laravel",
        text: "Laravel",
        link: "https://laravel.com/",
      },

      {
        src: "https://raw.githubusercontent.com/devicons/devicon/master/icons/php/php-original.svg",
        alt: "php",
        text: "PHP",
        link: "https://www.php.net/",
      },
      // end backend
      {
        type: "spacer",
        text: "Desktop Applications",
      },
      {
        src: "https://raw.githubusercontent.com/devicons/devicon/master/icons/dot-net/dot-net-original-wordmark.svg",
        alt: "windows",
        text: ".NET",
        link: "https://www.microsoft.com/net/",
      },
      {
        text: "Repositories",
        type: "spacer",
      },
      {
        src: "https://raw.githubusercontent.com/devicons/devicon/master/icons/github/github-original-wordmark.svg",
        alt: "github",
        link: "https://github.com/jamesulip",
      },
      {
        src: "https://raw.githubusercontent.com/devicons/devicon/master/icons/gitlab/gitlab-original-wordmark.svg",
        alt: "gitlab",
        link: "https://gitlab.com/jamesulip",
      },
      {
        src: "https://raw.githubusercontent.com/devicons/devicon/master/icons/bitbucket/bitbucket-original-wordmark.svg",
        alt: "bitbucket",
        link: "https://bitbucket.org/jamesulip",
      },
      {
        text: "Others",
        type: "spacer",
      },
      {
        src: "https://raw.githubusercontent.com/devicons/devicon/master/icons/docker/docker-original-wordmark.svg",
        alt: "docker",
      },
      {
        src: "https://raw.githubusercontent.com/devicons/devicon/master/icons/amazonwebservices/amazonwebservices-original-wordmark.svg",
        alt: "aws",
      },
      {
        alt: "Digital Ocean",
        src: "https://raw.githubusercontent.com/devicons/devicon/master/icons/digitalocean/digitalocean-original-wordmark.svg",
      },
      {
        src: "https://cdn.worldvectorlogo.com/logos/arduino-1.svg",
        alt: "arduino",
      },
    ]);
    function firstCode() {
      // accept 2 integer then sum them
      const num1 = prompt("Enter first number");
      const num2 = prompt("Enter second number");
      alert(
        "The sum of " +
          num1 +
          " and " +
          num2 +
          " is " +
          (parseInt(num1) + parseInt(num2))
      );
    }
    return {
      enabled,
      darkMode,
      stacks,
      firstCode,
    };
  },
};
</script>

<template>
  <div :class="{ dark: darkMode }">
    <div class="relative dark:bg-gray-800">
      <div class="absolute top-5 left-5">
        <!-- create button for toogling dark mode , moon icon-->
        <button v-if="darkMode" @click="darkMode = false" class="text-white">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            class="h-6 w-6"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
            stroke-width="2"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              d="M20.354 15.354A9 9 0 018.646 3.646 9.003 9.003 0 0012 21a9.003 9.003 0 008.354-5.646z"
            />
          </svg>
        </button>
        <button v-else @click="darkMode = true">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            class="h-6 w-6"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
            stroke-width="2"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              d="M12 3v1m0 16v1m9-9h-1M4 12H3m15.364 6.364l-.707-.707M6.343 6.343l-.707-.707m12.728 0l-.707.707M6.343 17.657l-.707.707M16 12a4 4 0 11-8 0 4 4 0 018 0z"
            />
          </svg>
        </button>
      </div>
      <div class="h-screen flex">
        <div
          class="max-w-7xl m-auto py-16 px-4 sm:py-24 sm:px-6 lg:px-8 lg:flex lg:justify-between"
        >
          <div class="max-w-xl self-center">
            <h2
              class="text-xl text-gray-400 sm:text-1xl sm:tracking-tight lg:text-2xl flex"
            >
              Hello there
              <!-- <div class="animate-wiggle">👋</div> -->
              , Im
            </h2>
            <h2
              class="text-3xl lg:text-4xl sm:text-5xl font-semibold text-white sm:tracking-tight"
            >
              James Santos Ulip
            </h2>
            <div class="mt-5 flex gap-x-2">
              <a
                target="_blank"
                class="text-gray-400 hover:text-white"
                href="https://github.com/jamesulip"
                ><span class="sr-only">GitHub repository</span>
                <svg class="w-8 h-8" viewBox="0 0 24 24">
                  <path
                    fill="currentColor"
                    d="M12,2A10,10 0 0,0 2,12C2,16.42 4.87,20.17 8.84,21.5C9.34,21.58 9.5,21.27 9.5,21C9.5,20.77 9.5,20.14 9.5,19.31C6.73,19.91 6.14,17.97 6.14,17.97C5.68,16.81 5.03,16.5 5.03,16.5C4.12,15.88 5.1,15.9 5.1,15.9C6.1,15.97 6.63,16.93 6.63,16.93C7.5,18.45 8.97,18 9.54,17.76C9.63,17.11 9.89,16.67 10.17,16.42C7.95,16.17 5.62,15.31 5.62,11.5C5.62,10.39 6,9.5 6.65,8.79C6.55,8.54 6.2,7.5 6.75,6.15C6.75,6.15 7.59,5.88 9.5,7.17C10.29,6.95 11.15,6.84 12,6.84C12.85,6.84 13.71,6.95 14.5,7.17C16.41,5.88 17.25,6.15 17.25,6.15C17.8,7.5 17.45,8.54 17.35,8.79C18,9.5 18.38,10.39 18.38,11.5C18.38,15.32 16.04,16.16 13.81,16.41C14.17,16.72 14.5,17.33 14.5,18.26C14.5,19.6 14.5,20.68 14.5,21C14.5,21.27 14.66,21.59 15.17,21.5C19.14,20.16 22,16.42 22,12A10,10 0 0,0 12,2Z"
                  />
                </svg>
              </a>

              <a
                target="_"
                href="http://facebook.com/UlipJames"
                class="text-gray-400 hover:text-white"
              >
                <span class="sr-only">GitHub repository</span>
                <svg class="w-8 h-8" viewBox="0 0 24 24">
                  <path
                    fill="currentColor"
                    d="M12 2.04C6.5 2.04 2 6.53 2 12.06C2 17.06 5.66 21.21 10.44 21.96V14.96H7.9V12.06H10.44V9.85C10.44 7.34 11.93 5.96 14.22 5.96C15.31 5.96 16.45 6.15 16.45 6.15V8.62H15.19C13.95 8.62 13.56 9.39 13.56 10.18V12.06H16.34L15.89 14.96H13.56V21.96A10 10 0 0 0 22 12.06C22 6.53 17.5 2.04 12 2.04Z"
                  />
                </svg>
              </a>
              <a
                target="_"
                href="http://facebook.com/UlipJames"
                class="text-gray-400 hover:text-white"
              >
                <span class="sr-only">Gitlab repository</span>
                <svg class="w-8 h-8" viewBox="0 0 24 24">
                  <path
                    fill="currentColor"
                    d="M21.94 13.11L20.89 9.89C20.89 9.86 20.88 9.83 20.87 9.8L18.76 3.32C18.65 3 18.33 2.75 17.96 2.75C17.6 2.75 17.28 3 17.17 3.33L15.17 9.5H8.84L6.83 3.33C6.72 3 6.4 2.75 6.04 2.75H6.04C5.67 2.75 5.35 3 5.24 3.33L3.13 9.82C3.13 9.82 3.13 9.83 3.13 9.83L2.06 13.11C1.9 13.61 2.07 14.15 2.5 14.45L11.72 21.16C11.89 21.28 12.11 21.28 12.28 21.15L21.5 14.45C21.93 14.15 22.1 13.61 21.94 13.11M8.15 10.45L10.72 18.36L4.55 10.45M13.28 18.37L15.75 10.78L15.85 10.45H19.46L13.87 17.61M17.97 3.94L19.78 9.5H16.16M14.86 10.45L13.07 15.96L12 19.24L9.14 10.45M6.03 3.94L7.84 9.5H4.23M3.05 13.69C2.96 13.62 2.92 13.5 2.96 13.4L3.75 10.97L9.57 18.42M20.95 13.69L14.44 18.42L14.46 18.39L20.25 10.97L21.04 13.4C21.08 13.5 21.04 13.62 20.95 13.69"
                  />
                </svg>
              </a>
              <a
                target="_"
                href="mailto:ulip.james@gmail.com"
                class="text-gray-400 hover:text-white flex gap-2"
              >
                <span class="sr-only">Business Gmail</span>
                <svg class="w-8 h-8" viewBox="0 0 24 24">
                  <path
                    fill="currentColor"
                    d="M20,8L12,13L4,8V6L12,11L20,6M20,4H4C2.89,4 2,4.89 2,6V18A2,2 0 0,0 4,20H20A2,2 0 0,0 22,18V6C22,4.89 21.1,4 20,4Z"
                  />
                </svg>
                ulip.james@gmail.com
              </a>
            </div>
          </div>
          <div class="sm:order-last">
            <!-- <img
              class="w-40 mb-5 -scale-x-100 rounded-full"
              alt="Tangina burado na yung mukha ko sa edit XD"
              src="./assets/88959118_2948458481878646_7262408940095275008_n-removebg-preview.png"
            /> -->
          </div>
        </div>
        <div></div>
      </div>
      <div class="w-full grid absolute bottom-5">
        <div class="mx-auto">
          <!-- arrow down button pointing down -->
          <button @click="enabled = !enabled" class="text-white flex text-2xl">
            <div class="flex">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                class="animate-bounce w-4 h-4"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
                stroke-width="2"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  d="M19 14l-7 7m0 0l-7-7m7 7V3"
                />
              </svg>
            </div>
            <div class="text-lg">ABOUT ME</div>
          </button>
        </div>
      </div>
    </div>

    <div class="max-h-[70vh] relative grid bg-gray-500">
      <div class="absolute inset-0">
        <!-- <img
          class="w-full h-full object-cover"
          src="https://images.unsplash.com/photo-1525130413817-d45c1d127c42?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1920&q=60&&sat=-100"
          alt=""
        /> -->
        <div
          class="absolute inset-0 bg-gray-800 mix-blend-multiply"
          aria-hidden="true"
        ></div>
      </div>
      <div
        class="relative max-w-7xl mx-auto py-12 sm:py-12 px-4 sm:px-6 lg:px-8"
      >
        <h1
          class="text-2xl font-semibold tracking-tight text-white md:text-3xl lg:text-4xl"
        >
          About Me
        </h1>
        <p class="aboutme">
          I'm a full-stack web developer with a passion for developing and
          designing. I'm currently working at
          <a class="text-yellow-600" href="https://www.tigergraphics.com.ph"
            >Tigergraphics</a
          >
          as a Software Developer but also serving as I.T support.
        </p>
        <p class="aboutme">
          I started to get into programming when I was in 2nd year high school
          back in 2009. I was amazed by the first code i wrote in HTML and
          javascript the called
          <a
            class="text-yellow-500 italic hover:text-yellow-300 cursor-pointer"
            @click="firstCode"
            >"The Sum of"</a
          >. when i was in college i shift my interest to game development and
          embedded systems (raspberry pi, arduino).
        </p>

        <p class="aboutme">
          I have a B.S. in Computer Science from the
          <a class="" href="http://"
            >University of AMA University and Colleges</a
          >. I enjoy working on projects that are both challenging and fun. I'm
          always looking to learn new things and improve my skills.
        </p>
      </div>
      <div class="my-auto z-[10]">
        <div
          class="max-w-7xl mx-auto py-12 px-4 sm:px-6 lg:py-16 lg:px-8 bg-white lg:bg-transparent"
        >
          <div class="lg:grid lg:grid-cols-2 lg:gap-8 lg:items-center">
            <div>
              <h2 class="text-3xl font-extrabold text-gray-900 sm:text-4xl">
                Languages and Tools
              </h2>
              <p class="mt-3 max-w-3xl text-lg text-gray-800">
                I am a self taught developer and I have a strong interest in any
                kind of programming language. I have experience with HTML, CSS,
                Javascript, PHP, C, C#, SQL, Arduino and many more. I have
                experience working with the following languages and frameworks.
                Specially laravel and vue.js. which i have been using for the
                past few years.
              </p>
              <p class="mt-3 max-w-3xl text-lg text-gray-800">
                I have also experience on working with Internet of Things (IOT)
                devices. Connecting iot devices to web applications. Live car
                GPS tracker and monitoring.
                <img
                  class="w-60"
                  src="./assets/gpstracking.png"
                  alt="Live Gps tracking"
                />
              </p>
            </div>

            <div
              class="mt-8 z-[10] p-3 shadow-lg rounded-lg grid grid-cols-3 gap-0 md:grid-cols-4 lg:mt-0 lg:grid-cols-5 bg-white"
            >
              <template v-for="stack in stacks" :key="stack.alt">
                <div v-if="stack.type == 'spacer'" class="col-span-5">
                  <div class="relative py-2">
                    <div
                      class="absolute inset-0 flex items-center"
                      aria-hidden="true"
                    >
                      <div class="w-full border-t border-gray-300"></div>
                    </div>
                    <div class="relative flex justify-center">
                      <span
                        v-html="stack.text"
                        class="px-2 bg-white text-lg text-gray-700 font-semibold"
                      >
                      </span>
                    </div>
                  </div>
                </div>
                <a
                  :href="stack.link"
                  target="_stack"
                  v-else
                  class="col-span-1 flex border justify-center p-6 bg-gray-50"
                >
                  <img class="max-h-12" :src="stack.src" :alt="stack.alt" />
                </a>
              </template>
            </div>
          </div>
        </div>
      </div>
      <div class="fixed top-0 right-0 p-3">
        <div class="mx-auto text-white">WIP</div>
      </div>
    </div>
  </div>
</template>
<style>
.aboutme {
  @apply mt-6 max-w-3xl text-xl text-gray-300;
}
</style>
