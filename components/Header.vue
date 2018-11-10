<template>
  <header class="g-hd">
    <div class="g-container">
      <img src="https://picsum.photos/220/40/?image=11" class="u-logo" alt="">
      <nav class="m-nav">
        <nuxt-link to="/" exact>首页</nuxt-link>
        <nuxt-link to="/article" exact>文章</nuxt-link>
        <nuxt-link to="/about" exact>话题</nuxt-link>
        <nuxt-link to="/about" exact>关于</nuxt-link>
      </nav>
      <div class="m-search">
        <svg class="icon" aria-hidden="true">
          <use xlink:href="#icon-sousuo"></use>
        </svg>
        <input type="text">
      </div>
      <div class="m-options">
        <nuxt-link to="/">
          <svg class="icon" aria-hidden="true">
            <use xlink:href="#icon-dongtai"></use>
          </svg>
        </nuxt-link>
        <nuxt-link to="/1234">
          <svg class="icon" aria-hidden="true">
            <use xlink:href="#icon-shoucang"></use>
          </svg>
        </nuxt-link>
        <nuxt-link to="/213">
          <svg class="icon" aria-hidden="true">
            <use xlink:href="#icon-geren"></use>
          </svg>
        </nuxt-link>
      </div>
    </div>
  </header>
</template>

<script>
  export default {
    name: "Header"
  }
</script>

<style lang="scss" scoped>
  @import "~assets/css/main.scss";

  .g-hd {
    height: 80px;
    padding: 19px 0 20px;
    margin-bottom: 30px;
    font-size: 18px;
    font-weight: bold;
    @include themify($themes) {
      background: themed('header-co');
      border-bottom: 1px solid themed('border-co');
    }
    .g-container {
      align-items: center;
      .u-logo {
        width: 220px;
        height: 40px;
      }
      .m-nav {
        flex-grow: 1;
        margin-left: 20px;
        a {
          margin-left: 30px;
          @include themify($themes) {
            color: themed('font-co-head');
          }
          &.nuxt-link-active {
            @include themify($themes) {
              color: themed('font-co-head-hover');
            }
          }
          &:hover {
            @include themify($themes) {
              color: themed('font-co-head-hover');
            }
          }
        }
      }
      .m-search {
        flex: 1;
        display: flex;
        align-items: center;
        height: 30px;
        padding: 0 10px;
        border-radius: 10px;
        @include themify($themes) {
          background: themed('head-search-bg');
          border: 1px solid themed('border-co');
        }
        .icon {
          color: $font-co-3;
        }
        input {
          flex-grow: 1;
          border: 0;
          outline: none;
          padding: 0 5px;
          font-size: 14px;
          border-radius: 10px;
          background: transparent;
          @include themify($themes) {
            color: themed('font-co-head');
          }
        }
      }
      .m-options {
        margin-left: 20px;
        a {
          margin-left: 15px;
          font-size: 22px;
          @include themify($themes) {
            color: themed('font-co-head');
          }
          &.nuxt-link-active {
            @include themify($themes) {
              color: themed('font-co-head-hover');
            }
          }
        }
      }
    }
  }
</style>
