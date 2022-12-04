<template>
  <div class="relative">
    <!-- SideBar -->
    <div
      class="w-2/6 md:w-1/4 bg-red-900 fixed text-center h-screen"
      data-aos="slide-right"
    >
      <div class="vcenter">
        <div
          class="rounded-full w-20 h-20 md:w-24 md:h-24 left-0 right-0 mx-auto overflow-hidden relative"
        >
          <img class="absolute" src="/profile.jpg" alt="" />
        </div>
        <ul class="mt-3 text-lg md:text-xl text-white">
          <li><a href="#about">About</a></li>
          <li><a href="#education">Education</a></li>
          <li><a href="#positions">Positions</a></li>
          <li><a href="#skills">Skills</a></li>
          <li><a href="#portfolio">Portfolio</a></li>
        </ul>
      </div>
    </div>

    <!-- Content -->
    <div class="w-4/6 md:w-3/4 float-right px-5 overflow-scroll">
      <section id="about" class="h-screen relative" data-aos="slide-right">
        <div class="vcenter w-full">
          <h1 class="text-3xl">Mohammed Balfaqih</h1>
          <p class="text-xl opacity-60">Fullstack Developer</p>
          <p>
            Hello, I am a 20 years old self-taught fullstack developer. I am currently
            studying computer science at Memorial University. I adore
            programming and love to keep up to date with the latest technology. My goal is to help advancing health care with computers.
          </p>
          <div class="mt-2">
            <a href="https://github.com/HaMoOoOd25/"
              ><i class="fab fa-lg fa-github p-1"></i
            ></a>
            <a href="instagram.com/hamoodev25"
              ><i class="fab fa-lg fa-instagram p-1"></i
            ></a>
            <a href="https://twitter.com/hamoodev25"
              ><i class="fab fa-lg fa-twitter p-1"></i
            ></a>
            <a href="https://www.linkedin.com/in/hamooood25/"
              ><i class="fab fa-lg fa-linkedin p-1"></i
            ></a>
          </div>
          <a href="#education" class="float-right text-red-900">Next</a>
        </div>
      </section>

      <section data-aos="slide-right" id="education" class="h-screen relative">
        <div class="vcenter w-full">
          <ul>
            <h1 class="text-3xl">Education</h1>
            <li>
              <h2 class="text-2xl">Memorial University of Newfoundland</h2>
              <p class="text-xl opacity-60">Computer Science</p>
              <p class="text-xl opacity-60">2021 - present</p>
            </li>
          </ul>
          <a href="#skills" class="float-right text-red-900">Next</a>
        </div>
      </section>

      <section data-aos="slide-right" id="skills" class="h-screen relative">
        <div class="vcenter w-full">
          <h1 class="text-3xl">Skills</h1>
          <ul>
            <li>
              <h2 class="text-2xl">Backend Development</h2>
              <p class="text-xl opacity-60">NodeJs - Fast API - Django - Flask - GraphQl</p>
            </li>
            <li>
              <h2 class="text-2xl">Frontend Development</h2>
              <p class="text-xl opacity-60">
                VueJs - NuxtJs - Vuex - React - NextJs - TailwindCss
              </p>
            </li>
            <li>
              <h2 class="text-2xl">Database</h2>
              <p class="text-xl opacity-60">MongoDb - MySQL - SQLite</p>
            </li>
          </ul>
          <a href="#positions" class="float-right text-red-900">Next</a>
        </div>
      </section>

      <section data-aos="slide-right" id="positions" class="h-screen relative">
        <div class="vcenter w-full">
          <ul>
            <li>
              <h2 class="text-2xl">Coremenus (CoreGameDev)</h2>
              <p class="text-xl opacity-60">Fullstack Developer / Co-Founder</p>
              <p class="text-xl opacity-60">2020 - present</p>
              <a href="https://dashboard.coremenus.com"
                ><i class="fas fa-lg fa-globe p-1"></i
              ></a>
            </li>
            <li>
              <h2 class="text-2xl">MUN COMPUTER SCIENCE SOCIETY</h2>
              <p class="text-xl opacity-60">Event Coordinator</p>
              <p class="text-xl opacity-60">2021 - present</p>
              <a href="https://muncompsci.ca/"
                ><i class="fas fa-lg fa-globe p-1"></i
              ></a>
            </li>
            <li>
              <h2 class="text-2xl">DIAG LAB</h2>
              <p class="text-xl opacity-60">Data Quality Assurance Analyst</p>
              <p class="text-xl opacity-60">2022 - present</p>
              <a href="https://www.cs.mun.ca/~kpopuri/"
                ><i class="fas fa-lg fa-globe p-1"></i
              ></a>
            </li>
            <li>
              <h2 class="text-2xl">Hackfrost NL</h2>
              <p class="text-xl opacity-60">Operation Team Member</p>
              <p class="text-xl opacity-60">2022 - present</p>
              <a href="https://hackfrostnl.ca/"
                ><i class="fas fa-lg fa-globe p-1"></i
              ></a>
            </li>
          </ul>
          <a href="#portfolio" class="float-right text-red-900">Next</a>
        </div>
      </section>

      <section data-aos="slide-right" id="portfolio" class="relative">
        <div class="w-full">
          <h1 class="text-3xl">Portfolio</h1>
          <ul>
            <li v-for="(project, i) in projects" :key="i">
              <h2 class="text-2xl">{{ project.title }}</h2>
              <p class="text-xl opacity-60">{{ project.tags }}</p>
              <div class="p-2 flex flex-row overflow-x-scroll">
                <img
                  v-for="(image, i) in project.images"
                  :key="i"
                  class="portfolio-image mx-2 right-0 left-0 rounded-xl border-4 border-red-900"
                  :src="image"
                  alt=""
                />
              </div>
              <p class="text-lg opacity-60 mt-3">{{ project.description }}</p>
              <p v-if="project.link" class="text-lg opacity-60 mt-3">
                You can visit project source code or website
                <a class="font-bold text-purple-400" :href="project.link"
                  >here</a
                >
              </p>
            </li>
          </ul>
        </div>
      </section>
    </div>
  </div>
</template>

<script>
import "animate.css";
import AOS from "aos";
import "aos/dist/aos.css";

export default {
  name: "IndexPage",
  mounted() {
    AOS.init();
  },
  data() {
    return {
      projects: [
        {
          title: "CoreMenus",
          tags: "Fullstack Development",
          description:
            "Coremenus is a SaaS platform I am currently working on. It is a fully featured restaraunt digital menu manager. It allow restaraunts to accept orders from tables and cars using a QR Code link.",
          link: "https://dashboard.coremenus.com",
          images: [
            "/coremenus/coremenus.png",
            "/coremenus/coremenus2.png",
            "/coremenus/coremenus3.png",
            "/coremenus/coremenus4.png",
            "/coremenus/coremenus5.png",
          ],
        },
        {
            title: "Surgeon Journal",
            tage: "Frontend Development",
            description: "One of the things I saw surgeons do is document every surgery. They keep track of patient name, age, and diagnosis. I have seen that some of them keeps it in an excel sheet, and sometime it's difficult to manage without good knowledge of excel. So I made this Web App with VueJs/NuxtJs to make it easier to keep track of their surgeries. It also shows some analytics to help them get a good insight. It's also mobile first application, so they can access it from any device they have anywhere."
        },
        {
            title: "School Pickup",
            tage: "Frontend - Backend - Database - Web Sockets - Ardiuno",
            description: "I used to pickup my siblings from school everyday during covid. The teachers used Whatsapp group to communicate about which kid should leave. The got hectic when it's crowded outside as there are too many messages to keep up with, and a lot of the times I would need to notify the teachers multiple times. I build this system where every parent or driver would have an NFC tag with their kids data saved. I built an ardiuno system where it will get the kids data and notify each classroom of the kids in the NFC tag"
        },
        {
          title: "Hamood ERC20 Token",
          tags: "Blockchain and Web development",
          description:
            "This is one of my first blockchain projects. I created an ERC20 standard token with solidiy smart contract using truffle. I deployed the smart contract to a local blockchain network. I built another smart contract to be able to trade hamood token with ETH. I also made a website that interacts with the blockchain to swap ETH with my Token.",
          link: "https://github.com/HaMoOoOd25/hmdTokenSite",
          images: ["/hamoodtoken.png"],
        },
        {
          title: "IRATUS",
          tags: "Full Stack Development",
          description: "",
          images: ["/iratus.png"],
        }
      ],
    };
  },
};
</script>

<style>
li {
  @apply p-3;
}

.vcenter {
  margin: 0;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}

.portfolio-image {
  width: 550px;
}

html {
  @apply bg-gray-200;
  scroll-behavior: smooth;
}

.slide-enter-active,
.slide-leave-active {
  transition: all 1s ease;
}

.slide-enter-from,
.slide-leave-to {
  width: 0;
}

.slide-enter-to,
.slide-leave-from {
  width: auto;
}
</style>
