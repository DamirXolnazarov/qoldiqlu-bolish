<script setup>

</script>

<template>
  <div class="area">

    <input class="input" type="text" v-model="son" placeholder="a"><br>
    <input class="input" type="text" v-model="daraja" placeholder="b"><br>
    <input class="input" type="text" v-model="boluvchi" placeholder="boluvchi"><br>
    <button class="input" @click="qoldiq">click</button><br>
    <span class="input">qoldiq: {{ this.qoldi }}</span><br>
    <span class="input">bolinma: {{ this.bolinma }}</span><br>
  </div>
</template>
<script>
export default {
  data() {
    return {
      qoldi: 0,
      bolinma: 0,
      son: 0,
      daraja: 0,
      boluvchi: 0,
      // son: 0,
      // daraja: 0,
      // boluvchi: 0
    }
  },
  methods: {
    qoldiq(){
      this.umu = Math.pow(this.son, this.daraja)
      this.qoldi = this.umu % this.boluvchi
      this.bolinma = Math.floor(this.umu/this.boluvchi)
    }
  },
}
</script>

<style scoped>
.area{
  width: 100%;
  height: 100vh;
  padding: 30px 30px;
}
.input{
  width: 100%;
  height: 50px;
  font-size: 30px;
}
</style>
