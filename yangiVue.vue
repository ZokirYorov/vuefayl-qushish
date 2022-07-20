<template>
  <ul style="padding: 5px" v-for="(item, index) of objekt" :key="index">
    <li v-text="index + 1"></li>
    <li v-text="item.name"></li>
    <li v-text="item.kurs"></li>
    <li v-text="item.staji"></li>
    <hr>
  </ul>
</template>

<script>
export default {
  name: "yangiVue",

  data(){
    return{
      objekt:[
        { name: "Junior",
          kurs:"Front End",
          staji: 2,
        },
        {
          name: "Middle",
          kurs: "Beck End",
          staji: 3,
        },
        {
          name: "Sinior",
          kurs: "Web Development",
          staji: 4,
        }
      ]
    }
  }
}
</script>

<style scoped>

</style>