<template>
  <v-app>
    <v-container>
      <v-row>
        <v-col cols="3" md="2">
          <img alt="Vue logo" src="./assets/logo.png" class="logo" />
        </v-col>
        <v-col cols="9" md="10">
          <h1>資産運用シミュレーション</h1>
        </v-col>
      </v-row>
      <router-view></router-view>

      <v-footer class="bg-indigo-lighten-1 text-center d-flex flex-column">
        <v-row>
          <a href="https://takayoshi-makabe.github.io/" class="footer__contents"
            >About me</a
          >
          <router-link to="/" class="footer__contents">ホーム</router-link>
          <router-link to="policy" class="footer__contents"
            >プライバシーポリシー</router-link
          >
        </v-row>
        <div>
          <v-btn
            v-for="icon in icons"
            :key="icon.icon"
            class="mx-4"
            :icon="icon.icon"
            :href="icon.url"
            variant="text"
          ></v-btn>
        </div>
        <div class="footer__contents">
          Copyright © 2023 MAKABE Takayoshi. All Rights Reserved.
        </div>
      </v-footer>
    </v-container>
  </v-app>
</template>

<script>
export default {
  name: "App",

  data() {
    return {
      icons: [
        { icon: "mdi-github", url: "https://github.com/takayoshi-makabe" },
        { icon: "mdi-twitter", url: "https://twitter.com/Takayoshi_ma" },
        {
          icon: "mdi-linkedin",
          url: "https://www.linkedin.com/in/takayoshi-makabe-00376718b/",
        },
      ],
    };
  },
};
</script>

<style scoped>
h1 {
  text-align: left;
  position: relative;
  padding: 0.3em;
  margin-top: 0.7em;
  margin-left: 30px;
  font-size: clamp(17px, 2.5vw, 50px);
}
h1:after {
  content: "";
  position: absolute;
  left: 0;
  bottom: 0em;
  width: 100%;
  height: 10px;
  margin: -15px 0;
  background: repeating-linear-gradient(
    -45deg,
    rgb(166, 17, 7),
    rgb(191, 5, 5) 2px,
    white 2px,
    white 4px
  );
}
.footer__contents {
  color: white;
  margin: 20px 6px;
  font-size: clamp(11px, 2.5vw, 19px);
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #241102;
  margin-top: 60px;
}
.logo {
  text-align: left;
  margin-top: 1em;
  margin-bottom: 2em;
  margin-left: 2em;
  width: 100%;
}
</style>
