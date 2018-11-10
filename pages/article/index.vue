<template>
  <section class="g-container">
    <div class="g-mn">
      <no-ssr placeholder="Loading...">
        <index-list/>
        <index-list/>
      </no-ssr>
    </div>
    <div class="g-rside"></div>
  </section>

</template>

<script>
  import Header from '~/components/Header.vue'
  import indexList from '~/components/index-list.vue'

  export default {
    components: {
      Header,
      indexList
    },
    created() {

    },
    mounted() {

    }
  }
</script>

<style lang="scss" scoped>
  @import "~assets/css/main.scss";
  .g-container {
    min-height: calc(100vh - 110px);
    padding: 15px;
    justify-content: space-between;
    .g-mn {
      width: 620px;
    }
  }
</style>
