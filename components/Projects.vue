<template>
  <section data-aos="slide-right" id="projects" class="relative">
    <div class="w-full">
      <h1 class="text-3xl">Projects</h1>
      <ul>
        <li v-for="(project, i) in projects" :key="i">
          <h2 class="text-2xl">{{ project.title }}</h2>
          <p class="text-xl opacity-60">{{ project.tags }}</p>
          <div class="p-2 flex flex-row overflow-x-auto">
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
            <a class="font-bold text-red-900" :href="project.link">here</a>
          </p>
        </li>
      </ul>
    </div>
  </section>
</template>

<script>
export default {
    data() {
        return {
            projects: [
                {
                    title: "CoreMenus",
                    tags: "Fullstack Development",
                    description: "Coremenus is a SaaS platform I am currently working on. It is a fully featured restaraunt digital menu manager. It allow restaraunts to accept orders from tables and cars using a QR Code link.",
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
                    description: "One of the things I saw surgeons do is document every surgery. They keep track of patient name, age, and diagnosis. I have seen that some of them keeps it in an excel sheet, and sometime it's difficult to manage without good knowledge of excel. So I made this Web App with VueJs/NuxtJs to make it easier to keep track of their surgeries. It also shows some analytics to help them get a good insight. It's also mobile first application, so they can access it from any device they have anywhere.",
                    images: [
                        "/surgeon/surgeon1.png",
                        "/surgeon/surgeon2.png",
                    ]
                },
                {
                    title: "School Pickup",
                    tage: "Frontend - Backend - Database - Web Sockets - Ardiuno",
                    description: "I used to pickup my siblings from school everyday during covid. The teachers used Whatsapp group to communicate about which kid should leave. The got hectic when it's crowded outside as there are too many messages to keep up with, and a lot of the times I would need to notify the teachers multiple times. I build this system where every parent or driver would have an NFC tag with their kids data saved. I built an ardiuno system where it will get the kids data and notify each classroom of the kids in the NFC tag",
                    images: [
                        "/school.png",
                    ]
                    
                },
                {
                    title: "Hamood ERC20 Token",
                    tags: "Blockchain and Web development",
                    description: "This is one of my first blockchain projects. I created an ERC20 standard token with solidiy smart contract using truffle. I deployed the smart contract to a local blockchain network. I built another smart contract to be able to trade hamood token with ETH. I also made a website that interacts with the blockchain to swap ETH with my Token.",
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
        }
    }
}
</script>