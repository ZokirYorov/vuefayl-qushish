<template>

<div v-for="(item, index) of Objects" :key="index" style="width: 400px; display: flex; justify-content: space-between">
  <span style="justify-content: space-between; display: flex">{{`${item.firstName} ${item.lastName}`}}</span>     <button @click="openNevVue(item)">Info</button>
  <br><br>
<!--  <div v-text="person.firstName"></div>-->
<!--  <div v-text="person.lastName"></div>-->
<!--  <div v-text="person.age"></div>-->
<!--  <button @click="buttonClick">Click</button>-->
</div>
</template>

<script>
export default {
  name: "NewVue",
  data() {
    return{
      Objects: [
        {
          id: 1,
          firstName: "Botir",
          lastName: "Toirov "
        },
        {
          id: 2,
          firstName: "Anvar",
          lastName: "Nosirov",
        },
        {
          id: 3,
          firstName: "Olim",
          lastName: "Murodov",
        },
      ]
    }
  },
  props:{
    person:{
      type: Object,
      required:true
    }
  },
  methods:{
    openNevVue(NevVue) {
      this.$router.push('/other?accountId=' + NevVue.id)
    }
    // buttonClick(){
    //   this.$emit('click-button')
    // }
  }
}
</script>

<style scoped>

</style>