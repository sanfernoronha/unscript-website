<template>
  <v-container id="apply" fluid>
    <!-- Welcome -->
    <section id="hero">
      <v-row no-gutters>
        <v-img
          :min-height="'calc(100vh - ' + $vuetify.application.top + 'px)'"
          src="https://images.unsplash.com/photo-1487017159836-4e23ece2e4cf?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1951&q=80"
        >
          <div class="wrap-banner">
            <v-theme-provider>
              <v-container fill-height id="main-title">
                <v-row align="center" class="black--text mx-auto" justify="center">
                  <v-col class="black--text text-center" cols="12" tag="h1">
                    <br />

                    <v-container>
                      <Countdown end="March 21, 2020" class="white--text mr-7"></Countdown>
                      <span
                        :class="[
                          $vuetify.breakpoint.smAndDown
                            ? 'display-1'
                            : 'display-4'
                        ]"
                        class="font-weight-black"
                        v-for="(alphabet, id) in characters"
                        :key="id"
                        :style="{ color: alphabet.color }"
                      >{{ alphabet.char }}</span>
                      <br />
                      <span class="white--text">21st-22nd March, 2020</span>
                      <br />
                      <a
                        href="#"
                        class="d-block mb-5 caption"
                        data-aos="fade-up"
                        data-aos-delay="500"
                      >
                        <span>
                          <button
                            id="devfolio-apply-now"
                            :class="[
                          $vuetify.breakpoint.smAndDown
                            ? 'dev1'
                            : 'dev2'
                        ]"
                          >
                            <svg
                              class="logo"
                              xmlns="http://www.w3.org/2000/svg"
                              fill="#fff"
                              viewBox="0 0 115.46 123.46"
                              style="height:20px;width:20px;margin-right:8px"
                            >
                              <path
                                d="M115.46 68a55.43 55.43 0 0 1-50.85 55.11S28.12 124 16 123a12.6 12.6 0 0 1-10.09-7.5 15.85 15.85 0 0 0 5.36 1.5c4 .34 10.72.51 20.13.51 13.82 0 28.84-.38 29-.38h.26a60.14 60.14 0 0 0 54.72-52.47c.05 1.05.08 2.18.08 3.34z"
                              />
                              <path
                                d="M110.93 55.87A55.43 55.43 0 0 1 60.08 111s-36.48.92-48.58-.12C5 110.29.15 104.22 0 97.52l.2-83.84C.38 7 5.26.94 11.76.41c12.11-1 48.59.12 48.59.12a55.41 55.41 0 0 1 50.58 55.34z"
                              />
                            </svg>Apply with Devfolio
                          </button>
                        </span>
                      </a>
                    </v-container>
                  </v-col>

                  <v-btn
                    class="align-self-end"
                    fab
                    outlined
                    @click="$vuetify.goTo('#about')"
                    color="white"
                  >
                    <v-icon>mdi-chevron-double-down</v-icon>
                  </v-btn>
                </v-row>
              </v-container>
            </v-theme-provider>
            <vue-particles color="#dedede" class="particles-js"></vue-particles>
          </div>
        </v-img>
      </v-row>
    </section>
    <!-- about -->
    <!-- <section id="about-me" class="red lighten-2">
      <div class="py-12"></div>

      <v-container class="text-center ma-0 pa-0">
        <h2 class="display-2 font-weight-bold mb-3">ABOUT UNSCRIPT</h2>

        <v-responsive class="mx-0 mb-8" width="56">
          <v-divider class="mb-1"></v-divider>

          <v-divider></v-divider>
        </v-responsive>

        <v-responsive
          class="mx-auto title font-weight-light mb-8"
          max-width="720"
        >Technology is nothing. What's important is that you have a faith in people, that they're basically good and smart, and if you give them tools, they'll do wonderful things with them.</v-responsive>

        <v-avatar class="elevation-12 mb-12 grey darken-4" size="100">
          <v-img src="../assets/unscript.png"></v-img>
        </v-avatar>

    <div></div>-->
    <!-- <v-container fluid>
          <v-row no-gutters justify-lg="center" justify-sm="center">
            <v-col cols="12" lg="3" sm="12" class="pa-0 ma-0">
              <v-alert outlined type="success" text class="grey darken-4">24 hours hackathon</v-alert>
            </v-col>
          </v-row>
    </v-container>-->
    <!-- </v-container>

      <div class="py-12"></div>
    </section>-->
    <section id="about" class="red lighten-2">
      <div class="py-12"></div>

      <v-container class="text-center">
        <h2 class="display-2 font-weight-bold mb-3">ABOUT UNSCRIPT</h2>

        <v-responsive class="mx-auto mb-8" width="56">
          <v-divider class="mb-1"></v-divider>

          <v-divider></v-divider>
        </v-responsive>

        <v-responsive
          class="mx-auto title font-weight-light mb-8"
          max-width="720"
        >Technology is nothing. What's important is that you have a faith in people, that they're basically good and smart, and if you give them tools, they'll do wonderful things with them.</v-responsive>

        <v-avatar class="elevation-12 mb-12 black darken-1" size="128">
          <v-img src="../assets/unscript.png"></v-img>
        </v-avatar>

        <div></div>

        <!-- <v-btn color="grey" href="https://vuetifyjs.com" outlined large>
          <span class="grey--text text--darken-1 font-weight-bold">Vuetify Documentation</span>
        </v-btn>-->
        <v-responsive>
          <v-list-item>
            <v-list-item-content>
              <v-list-item-title>
                <v-icon class="mr-2 black--text darken-1">mdi-checkbox-marked-circle</v-icon>24 Hours Hackathon
              </v-list-item-title>
            </v-list-item-content>
          </v-list-item>
          <v-list-item>
            <v-list-item-content>
              <v-list-item-title>
                <v-icon class="mr-2 black--text darken-1">mdi-checkbox-marked-circle</v-icon>4 Domains
              </v-list-item-title>
            </v-list-item-content>
          </v-list-item>
          <v-list-item>
            <v-list-item-content>
              <v-list-item-title>
                <v-icon class="mr-2 black--text darken-1">mdi-checkbox-marked-circle</v-icon>50+ Teams
              </v-list-item-title>
            </v-list-item-content>
          </v-list-item>
          <v-list-item>
            <v-list-item-content>
              <v-list-item-title>
                <v-icon class="mr-2 black--text darken-1">mdi-checkbox-marked-circle</v-icon>A Lot To Learn
              </v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-responsive>
      </v-container>

      <div class="py-12"></div>
    </section>

    <!-- timeline -->
    <section class="pa-4 grey darken-4" id="schedule">
      <p class="display-1 text-center white--text">Schedule</p>
      <p class="text-center white--text">15th March, 2020</p>
      <v-container fluid class="pl-4 pr-4 pt-0">
        <v-timeline>
          <v-timeline-item color="red lighten-2" small>
            <template v-slot:opposite>
              <span class="white--text">11:59 PM</span>
            </template>
            <v-card class="elevation-2" color="red lighten-2">
              <v-card-title
                :class="[
                          $vuetify.breakpoint.smAndDown
                            ? 'subtitle-2'
                            : 'headline'
                        ]"
              >Registration Ends</v-card-title>
            </v-card>
          </v-timeline-item>
        </v-timeline>
      </v-container>
      <p class="text-center white--text">17th March, 2020</p>
      <v-container fluid class="pl-4 pr-4 pt-0">
        <v-timeline :reverse="true">
          <v-timeline-item color="red lighten-2" small>
            <template v-slot:opposite>
              <span class="white--text">11:59 PM</span>
            </template>
            <v-card class="elevation-2" color="red lighten-2">
              <v-card-title
                :class="[
                          $vuetify.breakpoint.smAndDown
                            ? 'subtitle-2'
                            : 'headline '
                        ]"
              >Shortlisted Teams Announced</v-card-title>
            </v-card>
          </v-timeline-item>
        </v-timeline>
      </v-container>
      <p class="text-center white--text">20th March, 2020</p>
      <v-container fluid class="pl-4 pr-4 pt-0">
        <v-timeline>
          <v-timeline-item color="red lighten-2" small>
            <template v-slot:opposite>
              <span class="white--text">12:00 PM</span>
            </template>
            <v-card class="elevation-2" color="red lighten-2">
              <v-card-title
                :class="[
                          $vuetify.breakpoint.smAndDown
                            ? 'subtitle-2'
                            : 'headline'
                        ]"
              >Release Of Problem Statements</v-card-title>
            </v-card>
          </v-timeline-item>
        </v-timeline>
      </v-container>
      <p class="text-center white--text">Day 1 - 20st March, 2020</p>
      <v-container fluid class="pl-4 pr-4 pt-0">
        <v-timeline reverse="true">
          <v-timeline-item color="red lighten-2" small>
            <template v-slot:opposite>
              <span class="white--text">8:30 AM</span>
            </template>
            <v-card class="elevation-2" color="red lighten-2">
              <v-card-title
                :class="[
                          $vuetify.breakpoint.smAndDown
                            ? 'subtitle-2'
                            : 'headline'
                        ]"
              >Registration</v-card-title>
            </v-card>
          </v-timeline-item>
          <v-timeline-item color="red lighten-2" small>
            <template v-slot:opposite>
              <span class="white--text">9:30 AM</span>
            </template>
            <v-card class="elevation-2" color="red lighten-2">
              <v-card-title
                :class="[
                          $vuetify.breakpoint.smAndDown
                            ? 'subtitle-2'
                            : 'headline'
                        ]"
              >Inaugral Ceremony</v-card-title>
            </v-card>
          </v-timeline-item>
          <v-timeline-item color="red lighten-2" small>
            <template v-slot:opposite>
              <span class="white--text">11:00 AM</span>
            </template>
            <v-card class="elevation-2" color="red lighten-2">
              <v-card-title
                :class="[
                          $vuetify.breakpoint.smAndDown
                            ? 'subtitle-2'
                            : 'headline'
                        ]"
              >Coding Begins!</v-card-title>
            </v-card>
          </v-timeline-item>
          <v-timeline-item color="red lighten-2" small>
            <template v-slot:opposite>
              <span class="white--text">2:00 PM</span>
            </template>
            <v-card class="elevation-2" color="red lighten-2">
              <v-card-title
                :class="[
                          $vuetify.breakpoint.smAndDown
                            ? 'subtitle-2'
                            : 'headline'
                        ]"
              >Lunch</v-card-title>
            </v-card>
          </v-timeline-item>
          <v-timeline-item color="red lighten-2" small>
            <template v-slot:opposite>
              <span class="white--text">4:00 PM</span>
            </template>
            <v-card class="elevation-2" color="red lighten-2">
              <v-card-title
                :class="[
                          $vuetify.breakpoint.smAndDown
                            ? 'subtitle-2'
                            : 'headline'
                        ]"
              >Mentoring Session</v-card-title>
            </v-card>
          </v-timeline-item>
          <v-timeline-item color="red lighten-2" small>
            <template v-slot:opposite>
              <span class="white--text">6:00 PM</span>
            </template>
            <v-card class="elevation-2" color="red lighten-2">
              <v-card-title
                :class="[
                          $vuetify.breakpoint.smAndDown
                            ? 'subtitle-2'
                            : 'headline'
                        ]"
              >First Judging Round</v-card-title>
            </v-card>
          </v-timeline-item>
          <v-timeline-item color="red lighten-2" small>
            <template v-slot:opposite>
              <span class="white--text">9:00 PM</span>
            </template>
            <v-card class="elevation-2" color="red lighten-2">
              <v-card-title
                :class="[
                          $vuetify.breakpoint.smAndDown
                            ? 'subtitle-2'
                            : 'headline'
                        ]"
              >Dinner</v-card-title>
            </v-card>
          </v-timeline-item>
        </v-timeline>
      </v-container>
      <p class="text-center white--text">Day 12 - 21st March, 2020</p>
      <v-container fluid class="pl-4 pr-4 pt-0">
        <v-timeline>
          <v-timeline-item color="red lighten-2" small>
            <template v-slot:opposite>
              <span class="white--text">12:00 AM</span>
            </template>
            <v-card class="elevation-2" color="red lighten-2">
              <v-card-title
                :class="[
                          $vuetify.breakpoint.smAndDown
                            ? 'subtitle-2'
                            : 'headline'
                        ]"
              >Midnight Surprise!</v-card-title>
            </v-card>
          </v-timeline-item>
          <v-timeline-item color="red lighten-2" small>
            <template v-slot:opposite>
              <span class="white--text">8:30 AM</span>
            </template>
            <v-card class="elevation-2" color="red lighten-2">
              <v-card-title
                :class="[
                          $vuetify.breakpoint.smAndDown
                            ? 'subtitle-2'
                            : 'headline'
                        ]"
              >Breakfast</v-card-title>
            </v-card>
          </v-timeline-item>
          <v-timeline-item color="red lighten-2" small>
            <template v-slot:opposite>
              <span class="white--text">9:00 AM</span>
            </template>
            <v-card class="elevation-2" color="red lighten-2">
              <v-card-title
                :class="[
                          $vuetify.breakpoint.smAndDown
                            ? 'subtitle-2'
                            : 'headline'
                        ]"
              >Second Judging Round</v-card-title>
            </v-card>
          </v-timeline-item>
          <v-timeline-item color="red lighten-2" small>
            <template v-slot:opposite>
              <span class="white--text">10:45 AM</span>
            </template>
            <v-card class="elevation-2" color="red lighten-2">
              <v-card-title
                :class="[
                          $vuetify.breakpoint.smAndDown
                            ? 'subtitle-2'
                            : 'headline'
                        ]"
              >Shortlisting Of Top 10 Teams</v-card-title>
            </v-card>
          </v-timeline-item>
          <v-timeline-item color="red lighten-2" small>
            <template v-slot:opposite>
              <span class="white--text">11:00 AM</span>
            </template>
            <v-card class="elevation-2" color="red lighten-2">
              <v-card-title
                :class="[
                          $vuetify.breakpoint.smAndDown
                            ? 'subtitle-2'
                            : 'headline'
                        ]"
              >Presentation & Final Judging Round</v-card-title>
            </v-card>
          </v-timeline-item>
          <v-timeline-item color="red lighten-2" small>
            <template v-slot:opposite>
              <span class="white--text">1:00 AM</span>
            </template>
            <v-card class="elevation-2" color="red lighten-2">
              <v-card-title
                :class="[
                          $vuetify.breakpoint.smAndDown
                            ? 'subtitle-2'
                            : 'headline'
                        ]"
              >Announcing The Results</v-card-title>
            </v-card>
          </v-timeline-item>
        </v-timeline>
      </v-container>
    </section>

    <!-- FAQs -->
    <section class="red lighten-2">
      <v-container fluid>
        <v-row no-gutters justify-lg="center" justify-sm="center">
          <v-col cols="12" lg="8" sm="12" class="pa-0 ma-0">
            <v-expansion-panels focusable dark>
              <v-expansion-panel
                v-for="(item,i) in faqs"
                :key="i"
                class="mt-2 grey darken-4 white--text"
              >
                <v-expansion-panel-header>{{item.question}}</v-expansion-panel-header>
                <v-expansion-panel-content>{{item.answer}}</v-expansion-panel-content>
              </v-expansion-panel>
            </v-expansion-panels>
          </v-col>
        </v-row>
      </v-container>
    </section>

    <!-- Footer -->
    <v-footer dark padless>
      <v-card flat tile class="indigo lighten-1 white--text text-center" width="100%">
        <!-- <v-card-text>
          <v-btn v-for="icon in icons" :key="icon" class="mx-4 white--text" icon>
            <v-icon size="24px">{{ icon }}</v-icon>
          </v-btn>
        </v-card-text>

        <v-card-text
          class="white--text pt-0"
        >Phasellus feugiat arcu sapien, et iaculis ipsum elementum sit amet. Mauris cursus commodo interdum. Praesent ut risus eget metus luctus accumsan id ultrices nunc. Sed at orci sed massa consectetur dignissim a sit amet dui. Duis commodo vitae velit et faucibus. Morbi vehicula lacinia malesuada. Nulla placerat augue vel ipsum ultrices, cursus iaculis dui sollicitudin. Vestibulum eu ipsum vel diam elementum tempor vel ut orci. Orci varius natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus.</v-card-text>-->
        <v-container fluid>
          <v-row no-gutters>
            <v-col cols="12" lg="4" sm="12" xs="12">
              <v-card class="pa-2 transparent" outlined tile>
                <v-card-title>ABOUT</v-card-title>
                <v-card-text class="text-justify">
                  UnScript 2020 is the annual 24-hour hackathon held by Fr.
                  CRCE which consists of 4 domains and a prize for each
                  domain
                </v-card-text>
              </v-card>
            </v-col>
            <v-col cols="12" lg="4" sm="12" xs="12">
              <v-card class="pa-2 transparent" outlined tile>
                <v-card-title>QUICK LINKS</v-card-title>
                <v-list class="transparent">
                  <v-list-item-group>
                    <v-list-item v-for="(item, i) in items" :key="i">
                      <v-list-item-content>
                        <v-list-item-title v-text="item.text" class="text-justify"></v-list-item-title>
                      </v-list-item-content>
                    </v-list-item>
                  </v-list-item-group>
                </v-list>
              </v-card>
            </v-col>
            <v-col cols="12" lg="4" sm="12" xs="12">
              <v-card class="pa-2 transparent" outlined tile>
                <v-card-title>CONNECT WITH US</v-card-title>
                <v-card-text class="text-justify">
                  Address : Fr. Conceicao Rodrigues College of Engineering,
                  Bandstand, Bandra(W), Mumbai-400050.
                </v-card-text>
                <v-card-text class="text-justify">
                  Princeton Baretto : +91 83694 04826
                  <br />Sumit Gupta : +91 8097453379
                </v-card-text>
                <v-card-text class="text-justify">Email : codelabscrce@gmail.com</v-card-text>
              </v-card>
            </v-col>
          </v-row>
        </v-container>

        <v-divider></v-divider>
        <v-card-text>
          <v-btn large v-for="icon in icons" :key="icon" class="mx-2 white--text" icon>
            <v-icon size="24px">{{ icon }}</v-icon>
          </v-btn>
        </v-card-text>

        <v-card-text class="white--text">
          {{ new Date().getFullYear() }}Design by CodeLabsCRCE —
          <strong>UnScript 2k20</strong>
        </v-card-text>
      </v-card>
    </v-footer>
  </v-container>
</template>

<script>
import Countdown from "vuejs-countdown";
export default {
  name: "HelloWorld",

  data: () => ({
    //

    items: [
      {
        icon: "mdi-inbox",
        text: "Inbox"
      },
      {
        icon: "mdi-star",
        text: "Star"
      },
      {
        icon: "mdi-send",
        text: "Send"
      },
      {
        icon: "mdi-email-open",
        text: "Drafts"
      }
    ],
    characters: [
      { char: "U", color: "blue" },
      { char: "N", color: "purple" },
      { char: "S", color: "green" },
      { char: "C", color: "orange" },
      { char: "R", color: "yellow" },
      { char: "I", color: "blue" },
      { char: "P", color: "green" },
      { char: "T", color: "red" },
      { char: "2K20", color: "orange" }
    ],
    icons: [
      "mdi-facebook",
      "mdi-twitter",
      "mdi-google-plus",
      "mdi-linkedin",
      "mdi-instagram"
    ],
    model: 1,
    faqs: [
      {
        question: "Q. What is a hackathon?",
        answer:
          "A hackathon is an event where in participating teams are provided different real-life problems and they have to design a technological solution to anyone of the problems given in the given time limit. The final product developed should be usable in real life."
      },
      {
        question: "Q. Can I code before coming to a hackathon?",
        answer:
          "You can come prepared with half baked codes, write your own APIs and modules."
      },
      {
        question: "Q. How do I form a team?",
        answer:
          "Each team should comprise of a maximum of 3 members including the team leader. Team members can be from different colleges."
      },
      {
        question: "Q. How do I register for UnScript 2k20?",
        answer:
          "All team members need to register on Devfolio (Link mentioned at the top). Deadline for the same is 15th March 2020."
      },
      {
        question: "Q. What if I have never been to a hackathon before?",
        answer:
          "For beginners, it will be a great start for working on problem statements where mentors from Tech Industries like MSCI, BrowserStack, TIAA, etc will be there to help you out with your projects. So, there is nothing to worry about any errors while you work. You will also have a good exposure to a coding atmosphere."
      },
      {
        question: "Q. What should I bring?",
        answer:
          "Participants are required to get their own laptops with all the necessary softwares installed, chargers, spike guard, student ID, Gov. ID and can get a pillow and blankets as per your convenience."
      },
      {
        question: "Q. When will the problem statements be released?",
        answer:
          "Problem statements will be released 1 day prior to the main event."
      },
      {
        question: "Q. How will we be notified about the selection?",
        answer:
          "Selected teams will be notified on Devfolio as well as get a confirmation email. Note: Registration does not confirm selection"
      }
    ]
  }),

  components: {
    Countdown
  }
};
</script>

<style lang="scss">
.wrap-banner {
  position: relative;
  -webkit-align-items: center;
  -ms-flex-align: center;
  align-items: center;
  display: -webkit-flex;
  display: flex;
  height: 100%;
  justify-content: center;
  color: transparent;
}
.particles-js {
  background-size: cover;
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: 0;
}

#apply {
  padding: 0;
}
#main-title {
  height: auto;
  width: auto;
  z-index: 1;
  margin-top: -10%;
  opacity: 100%;
}
#devfolio-apply-now {
  -ms-flex-align: center;
  -webkit-box-align: center;
  align-items: center;
  background-color: #3770ff;
  border-radius: 3px;
  border: none;
  color: #ffffff;
  cursor: pointer;
  display: -ms-flexbox;
  display: -webkit-box;
  display: flex;
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial,
    sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol";
  font-size: 18px;
  font-weight: 600;
  padding: 12px 20px;
  text-align: center;
  text-transform: lowercase;
}

#devfolio-apply-now:not([disabled]) {
  cursor: pointer;
}

#devfolio-apply-now:hover {
  background-color: #2954bf !important;
}

.dev1 {
  margin-left: 12%;
  margin-top: 10%;
}
.dev2 {
  margin-left: 34%;
  margin-top: 10%;
}
.v-card__text,
.v-card__title {
  word-break: normal !important; /* maybe !important  */
}
.v-application--is-ltr
  .v-timeline:not(.v-timeline--dense):not(.v-timeline--reverse):before {
  left: calc(50% - 1px);
  right: initial;
  background-color: white;
}
.v-application--is-ltr .v-timeline--reverse:not(.v-timeline--dense):before {
  right: calc(50% - 1px);
  left: initial;
  background-color: white;
}
</style>
