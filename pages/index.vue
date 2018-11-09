<template>
    <section class="g-container">
      <div class="g-mn">
        <index-list/>
        <index-list/>
        <index-list/>
        <index-list/>
        <index-list/>
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
    mounted() {
      (async function () {
        await new Promise((resolve, reject) => {
          setTimeout(()=>{
            console.log(3+4);
          },2000);
        }).catch((err) => {
          console.log(1);
        });
        setTimeout(()=>{
          console.log(2);
        },1000);
      })()
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
