<template>
  <article class="m-mlist">
    <header class="m-meta">
      <img src="https://picsum.photos/40/40/?image=19" alt="">
      <div class="info">
        <p>instagram</p>
        <p>Raleigh, North Carolina</p>
      </div>
    </header>
    <div class="m-body">
      <p>比如薯片这些是内容部分部分部分</p>
      <img src="https://picsum.photos/618/310/?image=22" alt="">
    </div>
    <div class="options">
      <svg class="icon" aria-hidden="true">
        <use xlink:href="#icon-dianzan"></use>
      </svg>
      <svg class="icon" aria-hidden="true">
        <use xlink:href="#icon-zhuanfa"></use>
      </svg>
      <svg class="icon" aria-hidden="true">
        <use xlink:href="#icon-shoucang"></use>
      </svg>
    </div>
    <div class="m-reply">
      <div class="m-list">
        <nuxt-link to="">
          <img src="https://picsum.photos/30/30/?image=72" alt="">
          <span>用户名:</span>
        </nuxt-link>
        <p>说的深恶么么么么么么么么么么么么么说的深恶么么么么么么么么么么么么么说的深恶么么么么么么么么么么么么么</p>
        <svg class="icon" aria-hidden="true">
          <use xlink:href="#icon-dianzan"></use>
        </svg>
      </div>
      <div class="u-textarea">
        <textarea name="" id="" placeholder="说点什么吧"></textarea>
      </div>
    </div>
  </article>
</template>

<script>
  export default {
    name: "index-list"
  }
</script>

<style lang="scss" scoped>
  @import "~assets/css/main.scss";

  .m-mlist {
    width: 620px;
    border: 1px solid $bd-co-1;
    background: #fff;
    box-shadow: 0 2px 12px 0 rgba(0,0,0,.1);
    margin-bottom: 40px;
    .m-meta {
      display: flex;
      height: 60px;
      padding: 10px 15px;
      border-bottom: 1px solid $bd-co-2;
      img {
        width: 40px;
        height: 40px;
        border-radius: 50%;
      }
      .info {
        flex: 1;
        margin-left: 10px;
        p {
          line-height: 20px;
        }
        p:nth-of-type(1) {
          color: $font-co-2;
          font-weight: bold;
        }
        p:nth-of-type(2) {
          color: $font-co-2;
          font-size: 14px;
        }
      }
    }
    .m-body {
      p {
        padding: 5px 10px;
        line-height: 22px;
        color: $font-co-2;
      }
      img {
        display: inline-block;
        width: 618px;
        height: 310px;
      }
    }
    .options {
      padding: 10px 15px;
      .icon {
        font-size: 20px;
        margin-right: 10px;
        &:nth-of-type(3) {
          float: right;
        }
      }
    }
    .m-reply {
      padding: 0 15px;
      .m-list {
        display: flex;
        align-items: flex-start;
        margin-bottom: 10px;
        font-size: 12px;
        a {
          display: flex;
          align-items: flex-start;
          img {
            width: 30px;
            height: 30px;
            border-radius: 50px;
          }
          span {
            line-height: 24px;
            margin-left: 10px;
            max-width: 100px;
            color: $link-co;
          }
        }
        p {
          flex: 1;
          margin-left: 5px;
          line-height: 24px;
          color: $font-co-2;
        }
        .icon {
          margin-top: 5px;
          font-size: 16px;
        }
      }
      .u-textarea {
        margin-bottom: 20px;
        textarea {
          width: 100%;
          padding: 5px 10px;
          line-height: 20px;
          color: $font-co-2;
          resize: none;
          border-radius: 5px;
          border-color: $bd-co-2;
          outline: none;
        }
      }
    }
  }
</style>
