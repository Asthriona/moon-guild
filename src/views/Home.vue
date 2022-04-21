<template>
  <div class="home">
    <v-container>
      <v-banner>
        <div class="header">
          <span class="font-weight-light display-2">We Are</span> <br />
          <p><span class="font-weight-bold text-uppercase display-3">Moon</span>
          <span class="font-weight-light text-uppercase display-3">Guild</span></p>
          <span class="font-weight-light headline">Your new World Of Warcraft Experience</span>
        </div>
      </v-banner>
      <v-row>
        <v-col cols="12">
          <div class="article">
          <p>
            <span class="display-2">Who are We?</span> <br>
            <span class="font-weight-bold text-uppercase">Moon</span>
          <span class="font-weight-light text-uppercase">Guild</span>
          is a recently created guild, based on Magtheridon we put focus around socials, and progressions. Our goal is first of all having fun all together playing this amazing game that is World Of Warcraft. We are also a group of people who are all passionate about the game and want to make it better.
          <b>We do not try hard!</b> try hard might be good for some, but we know from experiance whene to stop to keep the experiance fun for everyone, No Try Hard at Moon Guild, Just fun!
          If you too want to experiance the Moon Guild, join us!
          </p>
          <p>
            <span class="display-1"> Events</span> <br>
            Here we love those! WoW events havent been made to be experianced alone! Lots of us like to take part in it, sitting in voice chat (Muted or not we wont judge), and playing together.
          </p>
          <p>
            <span class="display-1">Acceptation</span> <br>
            Everyone is welcome in Moon Guild! No one is here to judge anyone, and our staff allways keep an eye out to make sure eveyone is accepted. <br>
            We have player from every horizons, They, and you are all the most welcome!
          </p>
          </div>
        </v-col>
        <v-col cols="12" class="text-center">
          <span class="display-2">Join us!</span> <br>
          <div class="icon" v-for="icon in icons" :key="icon.name">
            <a :href="icon.link" class="no-link" target="_blank" rel="noopener noreferrer"> <v-icon size="50">{{ icon.icon }}</v-icon></a>
          </div>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: "Home",
  data() {
    return {
      icons: [
        {
          name: "Discord",
          icon: "mdi-discord",
          link: "https://discord.gg/Vq6wC3dyNh"
        },
        {
          name: "WoW Armory",
          icon: "mdi-armory",
          link: "https://worldofwarcraft.com/en-gb/guild/eu/magtheridon/moon-guild"
        }
      ]
    }
  },
};
</script>

<style scoped>
.header {
  text-align: center;
  height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
.no-link {
  color: #fff !important;
  text-decoration: none !important;
  cursor: pointer !important;
}
</style>