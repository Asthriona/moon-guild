<template>
  <div class="Footer text-center">
      <v-footer v-bind="localAttrs" :padless="padless" dark>
          <v-card-text class="white--text">
            2019 - {{ new Date().getFullYear() }} —
            <strong class="text-uppercase">Moon</strong> <span class="text-uppercase">guild</span> - All Right Reserved.<br />
            Code Made by
            <a
              href="https://rainboomstudio.com/"
              target="_blank"
              rel="noopener noreferrer"
              >Rainboom Studio</a
            > ●
            Hosting
            <a
              href="https://team.yukiko.app/"
              target="_blank"
              rel="noopener noreferrer"
              >Yukiko Dev Team</a
            > ●
            DNS Powered by
            <a
              href="https://Asthriona.com"
              target="_blank"
              rel="noopener noreferrer"
              >Asthriona ltd.</a
            ><br />
            Domain uptime: {{ longTime }} <br />
            <div class="foot_logo">
              <p>Operating Company</p>
              <div class="figure">
                <img
                  src="https://cdn.nishikino.xyz/asthriona/icons/footLogo.png"
                  alt="Asthriona Logo"
                  style="width: 100%"
                />
              </div>
            </div>
          </v-card-text>
      </v-footer>
  </div>
</template>

<script>
export default {
    name: 'The-Footer',
    data() {
        return {
            icons: [
                'mdi-home',
                'mdi-email',
                'mdi-calendar',
                'mdi-account',
                'mdi-delete',
            ],
            longTime: 0,
            padless: true,
            variant: 'absolute',
        }
    },
      methods: {
    //Code by Aimee (http://www.mangoya.cn/#/)
    runTime() {
      //运行倒计时
      var oldTime = new Date("2022/04/21 22:09:00");
      setInterval(() => {
        const nowTime = new Date();
        const longTime = nowTime - oldTime;
        const days = parseInt(longTime / 1000 / 60 / 60 / 24, 10); //计算剩余的天数
        const hours = parseInt((longTime / 1000 / 60 / 60) % 24, 10); //计算剩余的小时
        const minutes = parseInt((longTime / 1000 / 60) % 60, 10); //计算剩余的分钟
        const seconds = parseInt((longTime / 1000) % 60, 10); //计算剩余的秒数
        this.longTime =
          days +
          " Days, " +
          hours +
          " Hours, " +
          minutes +
          " Minutes, " +
          seconds +
          " Seconds, ";
      }, 1000);
      console.log(
        "Moon Guild\nHosted by Nishikino Networks, \nDNS by Asthriona ltd.\nCode by Asthriona \nTheme by Asthriona"
      );
    }
  },
  created() {
    this.runTime();
  },
    computed: {
        localAttrs() {
            const attrs = {}
        if(this.variant === 'default') {
            attrs.absolute = false,
            attrs.fixed = false
        } else {
            attrs[this.variant] = true
        }
        return attrs
        },
    }
};
</script>

<style scoped>
.foot_logo {
  display: table;
  max-width: 300px;
  width: 100%;
  margin: 0 auto 12px;
}
.foot_logo p {
  display: table-cell;
  width: 9em;
  vertical-align: middle;
  font-size: 12px;
}
</style>