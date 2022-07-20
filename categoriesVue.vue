<template>
  <div style="background-color: burlywood;height: 430px; width: 200px; margin: 10px; padding: 10px">
    <h2>Mijozlar ro'yxati!</h2>
    <div v-for="(item, index) of object" :key="index" style="border:1px solid; font-size: 20px;background-color: #f2f2f2; width: 150px; min-height: 100px; margin: 10px; padding: 5px" >
      <div v-text="item.firstName"></div>
      <div v-text="item.lastName"></div>
      <div v-text="item.age"></div>
      <button @click="clickButton">Click item</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "categoriesVue",

  data(){
    return{
      object:[
        {
          firstName: "Bahrom",
          lastName: "Ochilov",
          age: 22,
        },
        {
          firstName: "Nodir",
          lastName: "Omonov",
          age: 28,
        },
        {
          firstName: "Sunnat",
          lastName: "Murodov",
          age: 30,
        }
      ]
    }
  },
  methods:{
    clickButton(index){
      this.object.splice(index,1)
    }
  }
}
</script>

<style scoped>
button{
  margin: 5px;
  background-color: #5757ff;
  color: white;
  padding: 5px;
  border-radius: 4px;
}
</style>