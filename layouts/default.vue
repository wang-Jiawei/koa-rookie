<template>
  <div :class="themeClass">
    <Header/>
    <nuxt/>
  </div>
</template>

<script>
  import Header from '~/components/Header.vue'

  export default {
    components: {
      Header
    },
    data() {
      return {
        theme: ''
      }
    },
    computed: {
      themeClass() {
        return `theme-${this.theme}`;
      }
    },
    created() {
      this.theme = Math.random() > 0.5 ? 'theme1' : 'theme2';
      this.$nextTick(() => {
        this.$nuxt.$loading.start();
        setTimeout(() => this.$nuxt.$loading.finish(), 200)
      })
    },
    mounted() {

    }
  }
</script>
<style lang="scss">
  @import "~normalize.css";
  @import "~assets/css/main.scss";

  html {
    font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, 'Helvetica Neue', Arial, sans-serif;
    font-size: 14px;
    word-spacing: 1px;
    -ms-text-size-adjust: 100%;
    -webkit-text-size-adjust: 100%;
    -moz-osx-font-smoothing: grayscale;
    -webkit-font-smoothing: antialiased;
    box-sizing: border-box;
    background: $main-co;
  }

  *,
  *:before,
  *:after {
    box-sizing: border-box;
    margin: 0;
  }

  .button--green {
    display: inline-block;
    border-radius: 4px;
    border: 1px solid #3b8070;
    color: #3b8070;
    text-decoration: none;
    padding: 10px 30px;
  }

  .button--green:hover {
    color: #fff;
    background-color: #3b8070;
  }

  .button--grey {
    display: inline-block;
    border-radius: 4px;
    border: 1px solid #35495e;
    color: #35495e;
    text-decoration: none;
    padding: 10px 30px;
    margin-left: 15px;
  }

  .button--grey:hover {
    color: #fff;
    background-color: #35495e;
  }
</style>
