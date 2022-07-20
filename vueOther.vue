<template>
<table v-if="openedClickedNevVue">
  <tr>
    <th>{{openedClickedNevVue.id}}</th>
  </tr>
  <tr><td>{{openedClickedNevVue.fullName}}</td></tr>
  <tr><td>{{openedClickedNevVue.job}}</td></tr>
  <tr><td>{{openedClickedNevVue.age}}</td></tr>
  <tr><td>{{openedClickedNevVue.hobby}}</td></tr>

<!--<h2>{{$route.query}}</h2>-->
<!--  <h2>{{$route.params}}</h2>-->
</table>
</template>

<script>
export default {
  name: "vueOther",
  data() {
    return{
      vueFullNameOther: [
        {
          id: 1,
          fullName: "Botir Toirov",
          job: "Doctor",
          age: 45,
          hobby: "Music",
        },
        {
          id: 2,
          fullName: "Anvar Nosirov",
          job: "Pilot",
          age: 40,
          hobby: "Sport",
        },
        {
          id: 3,
          fullName: "Olim Murodov",
          job: "Manager",
          age: 35,
          hobby: "Kricket",
        }
      ]
    }
  },
  computed: {
    openedClickedNevVue() {
     if (this.$route.query.accountId) {
        return this.vueFullNameOther.find(item => +item.id === +this.$route.query.accountId)
     }
      return null;
    }
  }
}
</script>

<style scoped>
table, th, td {
  border: 2px solid black;
  padding: 5px;
  margin: 20px;
  border-collapse: collapse;
}
</style>