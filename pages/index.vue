<template>
    <section class="g-container">
      <div class="g-mn">
        <index-list/>
        <index-list/>
        <index-list/>
        <index-list/>
        <index-list/>
      </div>
      <right-side></right-side>
    </section>

</template>

<script>
  import Header from '~/components/Header.vue'
  import indexList from '~/components/index-list.vue'
  import rightSide from '~/components/right-side.vue'

  export default {
    components: {
      Header,
      indexList,
      rightSide
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
