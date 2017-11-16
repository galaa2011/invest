<template>
  <div class="page-add">
    <q-card>
      <q-card-title>
      </q-card-title>
      <q-card-main>
        <div class="form-area">
          <q-field label="添加项目">
            <q-input v-model="name" dark color="yellow" />
          </q-field>
          <q-field label="投资金额">
            <q-input v-model="money" type="number" dark color="yellow" prefix="￥" suffix="元" />
          </q-field>
          <q-field label="占股比例">
            <q-input v-model="ratio" type="number" dark color="secondary" prefix="" suffix="%" />
          </q-field>
        </div>
        <div style="text-align:center;margin-top:2vh;">
          <q-btn round color="secondary" icon="perm_identity" @click="add" />
        </div>
      </q-card-main>
    </q-card>
  </div>
</template>
<script>
export default {
  data () {
    return {
      name: '',
      money: '',
      ratio: ''
    }
  },
  methods: {
    add () {
      this.$router.push({path: '/p/invests'})
    }
  }
}
</script>
<style scoped>
.page-add .form-area {
  background: #424242;
  padding: 5px 15px 15px;
  box-shadow: 0 1px 5px rgba(0,0,0,.2), 0 2px 2px rgba(0,0,0,.14), 0 3px 1px -2px rgba(0,0,0,.12);
  border-radius: 2px;
}
</style>
