<template>
  <div class="relative">
    <!-- SideBar -->
    <div class=" w-2/6 md:w-1/4 bg-purple-400 fixed text-center h-screen">
      <div class="vcenter">
        <div class="rounded-full w-20 h-20 md:w-24 md:h-24 left-0 right-0 mx-auto overflow-hidden relative">
          <img
          class="absolute -top-1/2"
          src="/profile.jpg"
          alt=""
        />
        </div>
        <ul class="mt-3 text-lg md:text-xl text-white">
          <li><a href="#about">About</a></li>
          <li><a href="#education">Education</a></li>
          <li><a href="#skills">Skills</a></li>
          <li><a href="#portfolio">Portfolio</a></li>
        </ul>
      </div>
    </div>

    <!-- Content -->
    <div class=" w-4/6 md:w-3/4 float-right px-5 overflow-scroll">
      <section id="about" class="h-screen relative">
        <div class="vcenter w-full">
          <h1 class="text-3xl">Mohammed Balfaqih</h1>
          <p class="text-xl opacity-60">Fullstack Developer</p>
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Sit,
            nostrum et. Porro vero officia maxime? Minima, sunt ipsam? Dolor,
            consequatur suscipit dolorem voluptatibus doloremque nisi amet
            consequuntur sunt nesciunt deleniti.
          </p>
          <div class="mt-2">
            <a href="https://github.com/HaMoOoOd25/"><i class="fab fa-lg fa-github p-1"></i></a>
             <a href="instagram.com/hamoodev25"><i class="fab fa-lg fa-instagram p-1"></i></a>
             <a href="https://twitter.com/hamoodev25"><i class="fab fa-lg fa-twitter p-1"></i></a>
             <a href="https://www.linkedin.com/in/hamooood25/"><i class="fab fa-lg fa-linkedin p-1"></i></a>
          </div>
          <a href="#education" class="float-right text-purple-400">Next</a>
        </div>
      </section>

      <section id="education" class="h-screen relative">
        <div class="vcenter w-full">
          <ul>
            <li>
              <h2 class="text-2xl">Al Furqan Highschool</h2>
              <p class="text-xl opacity-60">2019 - 2020</p>
            </li>
            <li>
              <h2 class="text-2xl">Memorial University of Newfoundland</h2>
              <p class="text-xl opacity-60"> Computer Science </p>
              <p class="text-xl opacity-60">2021 - present</p>
            </li>
            <li>
              <h2 class="text-2xl">DApp University Bootcamp</h2>
              <p class="text-xl opacity-60"> Blockchain Development </p>
              <p class="text-xl opacity-60">2021 - present</p>
            </li>
          </ul>
          <a href="#skills" class="float-right text-purple-400">Next</a>
        </div>
      </section>

      <section id="skills" class="h-screen relative">
        <div class="vcenter w-full">
          <h1 class="text-3xl">Skills</h1>
          <ul>
            <li>
              <h2 class="text-2xl">Backend Development</h2>
              <p class="text-xl opacity-60">NodeJs - Fast API - GraphQl</p>
            </li>
            <li>
              <h2 class="text-2xl">Frontend Development</h2>
              <p class="text-xl opacity-60">VueJs - NuxtJs - Vuex - TailwindCss</p>
            </li>
            <li>
              <h2 class="text-2xl">Database</h2>
              <p class="text-xl opacity-60">MongoDb - MySQL</p>
            </li>
            <li>
              <h2 class="text-2xl">Blockchain Development</h2>
              <p class="text-xl opacity-60">Truffle - Metamask - EthersJs - Solditiy</p>
            </li>
          </ul>
          <a href="#portfolio" class="float-right text-purple-400">Next</a>
        </div>
      </section>

      <section id="portfolio" class="relative">
        <div class="w-full">
          <h1 class="text-3xl">Portfolio</h1>
          <ul>
            <li v-for="project, i in projects" :key="i">
              <h2 class="text-2xl">{{ project.title }}</h2>
              <p class="text-xl opacity-60">{{ project.tags }}</p>
              <img class=" w-11/12 right-0 left-0 mx-auto rounded-md p-1" :src="project.image" alt="">
              <p class=" text-lg opacity-60 mt-3">{{ project.description }}</p>
              <p class="text-lg opacity-60 mt-3">You can visit project source code or website <a class=" font-bold text-purple-400" :href="project.link">here</a></p>
            </li>
          </ul>
        </div>
      </section>
    </div>
  </div>
</template>

<script>
export default {
  name: "IndexPage",
  data() {
    return {
      projects: [
        {
          title: 'CoreMenus',
          tags: 'Fullstack Development',
          description: 'Coremenus is a digital menu platform for restaraunts in Qatar. I developed this website for CoreGameDev company located in Qatar. This website has a dashboard for restaraunt managers to adjust their menu to their liking.',
          link: 'https://dashboard.coremenus.com',
          image: '/coremenus.png'
        },
        {
          title: 'Hamood ERC20 Token',
          tags: 'Blockchain and Web development',
          description: 'This is one of my first blockchain projects. I created an ERC20 standard token with solidiy smart contract using truffle. I deployed the smart contract to a local blockchain network. I built another smart contract to be able to trade hamood token with ETH. I also made a website that interacts with the blockchain to swap ETH with my Token.',
          link: 'https://github.com/HaMoOoOd25/hmdTokenSite',
          image: '/hamoodtoken.png'
        }
      ]
    }
  }
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

html {
  @apply bg-gray-200;
  scroll-behavior: smooth;
}
</style>
