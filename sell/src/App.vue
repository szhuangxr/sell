<template>
  <div>
    <!--头部-->
    <v-header :seller="seller"></v-header>
    <!--主体切换-->
    <div class="tab border-1px">
      <div class="tab-item">
        <router-link v-bind:to="/goods">商品</router-link>
      </div>
      <div class="tab-item">
        <router-link v-bind:to="/ratings">评价</router-link>
      </div>
      <div class="tab-item">
        <router-link v-bind:to="/seller">商家</router-link>
      </div>
    </div>
    <!--头部-->
    <keep-alive>
      <router-view : seller="seller"></router-view>
    </keep-alive>
  </div>
</template>

<script type="text/ecmascript-6">
  import header from './components/header/header.vue'
  import {urlParse} from 'common/js/util'
  import data from 'common/json/data.json'
  //const ERR_OK=0;
  export default {
    data () {
      return {
        seller: {},
        id: ()
      },
        created()
      {
      }
    }
  }
</script>

<style lang="stylus" rel="stylesheet/stylus">
</style>
