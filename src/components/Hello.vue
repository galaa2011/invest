<template>
  <div class="hello">
    <h4>欢迎使用</h4>
    <q-gallery-carousel dots infinite autoplay :src="slider"></q-gallery-carousel>
  </div>
</template>

<script>
export default {
  name: 'hello',
  data () {
    return {
      slider: [
        require('src/assets/default.png'),
        require('src/assets/default.png'),
        require('src/assets/default.png')
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="stylus">
@import '~variables'

.hello
  text-align center
  margin-top 50px
  a
    color #35495E

ul
  list-style-type none
  padding 0

li
  display inline-block
  margin 0 10px
</style>
