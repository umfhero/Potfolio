<template>
  <div class="home">
    <!-- <img alt="Vue logo" src="../assets/logo.png" /> -->
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <v-img
      dark
      max-height="500px"
      src="https://images.unsplash.com/photo-1519638399535-1b036603ac77?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=1631&q=80"
    >
      <v-layout fill-height align-center>
        <v-container>
          <v-row align="center" justify="center" class="white--text">
            <v-col cols="12">
              <div
                :class="{'display-2 font-weight-bold ': $vuetify.breakpoint.smAndUp, 'title font-weight-bold': $vuetify.breakpoint.smAndDown}"
              >Welcome to my page.</div>
              <div
                :class="{'headline': $vuetify.breakpoint.smAndUp, 'subtitle-1': $vuetify.breakpoint.smAndDown}"
              >I enjoy making 3D, 2D and coding artworks.</div>
            </v-col>
          </v-row>
        </v-container>
      </v-layout>
    </v-img>
    <v-container class="mt-5">
      <v-layout wrap>
        <v-flex xs12>
          <div class="display-1 font-weight-bold" id="about">This is me</div>
        </v-flex>
        <v-flex xs12 mt-5>
          <div class="body-1">{{aboutText}}</div>
          <div
            class="body-1 mt-3"
          >I'm always open for commissions if you want a character brought to life or maybe a website. Or a script that will automatically order you a cup of warm coffee.</div>
        </v-flex>
      </v-layout>
      <v-layout wrap my-5>
        <v-flex xs12>
        </v-flex>
        <v-flex xs12 class="mt-5">
          <v-layout wrap>
            <template v-for="(app, i) in apps">
              <v-flex :key="i" xs12 sm6 md4>
                <p-portfolio-app :app="app" />
              </v-flex>
            </template>
          </v-layout>
        </v-flex>
      </v-layout>
      <v-layout wrap my-5>
        <v-flex xs12 mb-5>
          <div class="display-1 font-weight-bold" id="contact">Contacts :)</div>
        </v-flex>
        <template v-for="(contact, i) in contactLinks">
          <v-flex sm6 md4 xs12 :key="i">
            <p-contact-info :contact="contact" />
          </v-flex>
        </template>
      </v-layout>
      <!-- <v-layout wrap my-5>
        <v-flex xs12>
          <div class="display-1 font-weight-bold">Press</div>
        </v-flex>
        <v-flex xs12>
          <v-layout>
            <v-card width="">
              <v-card-title>Press card</v-card-title>
            </v-card>
          </v-layout>
        </v-flex>
      </v-layout>-->
    </v-container>
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from "@/components/HelloWorld.vue";
import PPortfolioApp from "@/components/PPortfolioApp.vue";
import PContactInfo from "@/components/PContactInfo.vue";

export default {
  name: "home",
  components: {
    // HelloWorld,
    PPortfolioApp,
    PContactInfo
  },
  data() {
    return {
      aboutText:
        "I enjoy making code in my free time and I love experimenting with the possibilities, I also like to make 3D art of characters and I use this daily creative hobby to help inspire learning my love for code. I started with automating many things, for example, I made a bot to automatically open a web browser, search and enter. I find it crazy how far coding can go which makes me always curious.",
        
      apps: [
        {
          name: "2D Art wwwwwwwwwwwwwwwwwwww Process",
          price: "Procreate",
          logo: "food-vision-logo.png",
          platforms: [
            {

            }
          ],
          description:
            "One of the many arts I started was 2D, I would draw on an Ipad using the software Procreate, and would try to use reference to improve my skills over time and eventually over 5 years have found my art style. It’s simple but I'm able to show a lot of character with each peace now. :)",
          technologies: [
            {

            },
            {

            },
            {

            }
          ],
          code: {
            name: "github",
            icon: "mdi-github",
            link: ""
          }
        },
        {
          name: "Python",
          price: "Python 3.8",
          logo: "finance-logo.png",
          platforms: [
            {

            },
            {

            }
          ],
          description:
            "When I started my journey with Python, it was very scary. A new language, with so many different possibilities, becomes overwhelming very quickly. But slowing it down by finding a couple of projects I could do with it and narrowing it down made it so much easier. I began with the basics, the print functions, the first “hello world” and then went on to make a converter for currencies, the joy I had from seeing the code work was priceless, the dread from when it didn’t make me more scared. But this love for code then involved into web automation and making many mundane tasks I had at the time done quicker. It took me around a year to learn the necessary steps I needed but I still have a long journey ahead which I can't wait for! ",
          technologies: [
            {

            },
            {

            },
            {
 
            },
            {

            },
            {

            }
          ],
          code: {
            name: "github",
            icon: "mdi-github",
          }
        },
        {
          name: "Ikea 3D Commercial",
          price: "Blender",
          logo: "baguette-logo.png",
          platforms: [
            {

            },
            {

            }
          ],
          description:
            "Alongside my business with 3D modelling, I got a commission from a director who wanted a mock-up on some IKEA lamps, I got given around five working days to complete full renders and ended up only having time to render seven of the nine renders they wanted due to computer power which we had discussed, I wasn’t able to get the place holder job but it was a great experience working so close to a director and working for them, and can't wait for my next small project.",
          technologies: [
            {

            },
            {

            },
            {

            },
            {

            }
          ],
          code: {
            name: "github",
            icon: "mdi-github",
            link: ""
          }
        },
        {
          name: "3D Modeling ",
          price: "Blender",
          logo: "facebook-logo.png",
          platforms: [
            {

            }
          ],
          description:
            "Around 2019, I stumbled upon a very appealing post made by a user on Instagram, I instantly fell in love with it and asked what software they used, they replied Blender. I searched it up, found tutorials and eminently fell in love with it. The 3D view I was given from it and the capabilities that I couldn’t get from ordinary 2D software blew my mind. I remember rendering my first project, a doughnut, I was so proud of myself, yet I wanted to push myself even further. I would always try learning all the different functions of the blender, the nodes, the textures and how each part works. I became very good quickly and after 3 years I'm proud of where I am and what I have accomplished, iv gotten commission and even started a shop selling the models I had made which came quite profitable.",
          technologies: [
            {

            },
            {
   
            }
          ],
          code: {
            name: "github",
            icon: "mdi-github",

          }
        },
        {
          name: "3D Lighting Course",
          price: "Blender",
          logo: "firebird-logo.png",
          platforms: [
            {
              name: "web",


            }
          ],
          description:
            "After a while of learning 3D software , it come apparent that I was lacking in lihgting, lighting is a key functionality of making the final render look clean and crisp, so in advance to this, I began learning through courses on how to do lighting, how to set my camera and where my focus should be set, nowadays I don’t even have to think about it and it’s second nature to me.",
          technologies: [
            {

            },
            {

            },
            {

            }
          ],
          code: {
            name: "github",
            icon: "mdi-github",
          }
        },
        {
          name: "PS5 3D Commercial",
          price: "BLENDER",
          logo: "logo.png",
          platforms: [
            {
              name: "web",

            }
          ],
          description:
            "I had also been experimenting with realistic advert type renders, one of them one a PS5 mock-up, this was all made by me, the models the lighting and text. I wanted to see how close to a real advert I could get alongside an editing skill. It came out nicely and I'm very proud of it, and I keep learning how to make it more cinematic than before.",
          technologies: [
            {

            },
            {

            },
            {

            },
            {

            }
          ],
          code: {
            name: "github",

            link: "https://github.com/uzirthapa/ecommerce-skeleton"
          }
        },
        {
          name: "Sacred Summits",
          price: "LIVE",
          logo: "ss-logo-high-res.png",
          platforms: [
            {
              name: "web",
              icon: "mdi-web",
              link: "https://sacred-summits-web.firebaseapp.com/"
            }
          ],
          description:
            "Sacred Summits was looking for a redesign of their website and they asked me to come up with a sample. This is what I came up with.",
          technologies: [
            {
              name: "VueJS",
              icon: "mdi-vuejs",
              link: "https://vuejs.org/"
            },
            {
              name: "Vuetify",
              icon: "mdi-vuetify",
              link: "https://vuetifyjs.com/"
            },
            {
              name: "Firebase",
              icon: "mdi-firebase",
              link: "https://firebase.google.com/"
            }
          ],
          code: {
            name: "github",
            icon: "mdi-github",
            link: ""
          }
        }
      ],
      contactLinks: [
        {
          name: "Email",
          value: "umfhero@gmail.com",
          link: "mailto:umfhero@gmail.com",
          icon: "mdi-email"
        },
        {
          name: "Instagram",
          value: "@umflhero",
          link: "https://www.instagram.com/umflhero/",
          icon: "mdi-instagram"
        }
      ]
    };
  }
};
</script>
