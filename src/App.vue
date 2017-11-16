<template>
  <q-layout ref="layout" view="hHh LpR lFr" class="bg-blue-1">
    <!-- <q-toolbar slot="header"> -->
    <!-- </q-toolbar> -->

    <!-- Navigation Tabs -->
    <q-tabs slot="navigation">
      <q-route-tab slot="title" to="/p/add" label="添加" />
      <q-route-tab slot="title" to="/p/invests" label="投资" />
      <q-route-tab slot="title" to="/p/detail" label="详情" />
      <q-route-tab slot="title" to="/p/process" label="进展" />
      <q-route-tab slot="title" to="/p/schedule" label="日历" />
    </q-tabs>

    <!-- Don't drop "q-app" class -->
    <div id="q-app">
      <router-view />
    </div>

    <!-- Footer -->
    <q-toolbar slot="footer">
      <q-tabs position="bottom" class="shadow-2 layout-footer transition-generic fixed-bottom" align="justify">
        <q-route-tab slot="title" to="/" icon="home" label="" />
        <q-tab slot="title" icon="message" label="" count="5" />
        <q-tab slot="title" icon="account_box" label="" />
      </q-tabs>
    </q-toolbar>
  </q-layout>
</template>

<script>
/*
 * Root component
 */
export default {}
</script>

<style lang="stylus">
@import '~variables'

main
  margin-top 40px
  padding 10px 5px

header
  margin 0
  height 10px
  background-color $primary
</style>
