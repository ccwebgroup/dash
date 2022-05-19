<style lang="sass">
.services-section
  margin-bottom: 100px
.bg-services-section
  absolute: bottom
  top: -20px
</style>
<template>
  <q-page class="bg-body">
    <div class="row">
      <div class="col-6 q-pt-xl q-px-lg items-center text-bold text-white">
        <q-card flat class="bg-transparent">
          <q-card-section>
            <div class="text-h3">
              We provide the most advance
              <span class="text-weight-bolder text-amber-9">TECHNOLOGY</span>
            </div>
            <div class="text-h4">for your business</div>
          </q-card-section>
          <q-card-actions>
            <q-btn
              class="text-h6 text-bold"
              text-color="dark"
              padding="sm 80px"
              color="amber-9"
              label="Get Qoute"
            />
          </q-card-actions>
        </q-card>
      </div>
      <div class="col-6">
        <Vue3Lottie :animationData="marketing2" :height="500" :width="500" />
      </div>
    </div>

    <div class="services-section bg-white q-py-xl relative-position">
      <!-- <img class="services-section" src="~assets/bg-svg/rect-light.svg" /> -->
      <div class="text-h3 text-bold text-primary text-center q-mb-xl">
        What do we offer?
      </div>
      <div class="row justify-center q-px-md q-gutter-md">
        <div
          v-for="service in services"
          :key="service.title"
          class="col-12 col-md-4"
        >
          <q-card class="border-rounded">
            <q-card-section>
              <q-item>
                <q-item-section avatar>
                  <q-avatar v-if="services" size="60px">
                    <img :src="'png/' + service.icon" alt="" />
                  </q-avatar>
                </q-item-section>
                <q-item-section>
                  <q-item-label class="text-h5">{{
                    service.title
                  }}</q-item-label>
                </q-item-section>
              </q-item>
              <div class="q-pa-md text-subtitle2">
                {{ service.text }}
              </div>
            </q-card-section>
          </q-card>
        </div>
      </div>
    </div>

    <div class="client-section q-pb-xl">
      <div class="text-h4 text-center text-white">Our Clients</div>
      <div class="flex flex-center q-gutter-sm">
        <div
          v-for="client in clients"
          :key="client.name"
          class="border-rounded q-pa-lg"
        >
          <q-img
            ratio="1"
            width="100px"
            :src="'clients/' + client.logo"
            alt=""
          />
          <div class="text-subtitle1 text-center text-white">
            {{ client.name }}
          </div>
        </div>
      </div>
    </div>

    <div class="team-section">
      <div class="text-h4 text-center text-white">Meet Our Team</div>

      <div class="flex flex-center q-gutter-sm">
        <div>
          <img src="" alt="" />
          <div class="text-h6">Joven Villar</div>
          <div class="text-caption">CEO</div>
        </div>
      </div>
    </div>

    <div class="bg-grey-10 q-pa-lg text-white fix-bottom">
      <div class="row">
        <div class="col-4"></div>
        <div class="col-4">
          <div class="text-h6">Services</div>
          <div
            class="text-grey-2 q-ml-sm"
            v-for="(item, i) in services"
            :key="i"
          >
            {{ item.title }}
          </div>
        </div>
        <div class="col-4"></div>
      </div>
      <div class="subtiltle1 text-center">All rights reserved 2022.</div>
    </div>
  </q-page>
</template>
<script setup>
import marketing1 from "src/lottie/marketing1.json";
import marketing2 from "src/lottie/marketing2.json";

const teams = [{ name: "Joven Villar", role: "CEO", photo: "jv.png" }];

const clients = [
  { name: "Burger King", logo: "burger-king.png" },
  { name: "AXA", logo: "AXA-logo.png" },
  { name: "Shantahl", logo: "shantahl_logo.png" },
  { name: "PC Shop", logo: "pc.png" },
];

const services = [
  {
    title: "Web Design",
    icon: "001-web-design.png",
    text: "We build website with better UI/EX design suitable for your bussiness.",
  },
  {
    title: "System Development",
    icon: "002-software.png",
    text: "We develop systems for your office automation and business transactions.",
  },
  {
    title: "Google Ads",
    icon: "google.png",
    text: "We manage google ads according to your prefered set up and target the right clients.",
  },
  {
    title: "Facebook Ads",
    icon: "005-facebook.png",
    text: "Making facebook ads more effective using the modified targets.",
  },
  {
    title: "Ad Creatives",
    icon: "004-graphic-designer.png",
    text: "We make brand logo, ad creatives and other graphic materials for your business.",
  },
  {
    title: "Social Media Management",
    icon: "006-social-media.png",
    text: "We manage your social media interactions, daily post, chat bots and more.",
  },
];
</script>

