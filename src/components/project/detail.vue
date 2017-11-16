<template>
  <div class="page-detail">
    <q-card>
      <q-card-media>
        <q-parallax :src="logo" :height="200">
          <div slot="loading">Loading...</div>
        </q-parallax>
        <q-card-title slot="overlay">
          最会游
          <span slot="subtitle">
            2017.10 | 200万 | 20%
          </span>
        </q-card-title>
      </q-card-media>
      <q-card-title>
        评分
        <q-rating slot="subtitle" v-model="stars" :max="5" />
        <div slot="right" class="row items-center">
          <span>我是股东</span>
          <q-btn flat round small color="red"><q-icon name="favorite" /></q-btn>
        </div>
      </q-card-title>
      <q-card-main>
        <p>项目概况</p>
        <p style="font-size:12px;" class="text-faded">1. 2017年11月15号关于董事会、监事会延期换届的公告</p>
        <p style="font-size:12px;" class="text-faded">2. 2017年11月主要财务信息公告</p>
      </q-card-main>
      <q-card-separator />
      <q-card-actions>
        <!-- <q-btn flat round small><q-icon name="event" /></q-btn> -->
        <q-btn flat color="primary"><q-icon name="settings_phone" /></q-btn>
        <q-btn flat color="primary"><q-icon name="mail" /></q-btn>
        <q-btn flat color="primary"><q-icon name="thumb_up" /></q-btn>
        <!-- <q-btn flat color="primary">Reserve</q-btn> -->
      </q-card-actions>
    </q-card>
  </div>
</template>
<script>
export default {
  data () {
    return {
      logo: require('src/assets/default.png'),
      stars: 4
    }
  }
}
</script>
<style>
</style>
