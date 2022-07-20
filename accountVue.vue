<template>
<table>
  <tr>
    <th>T/N</th>
    <th>Ismi</th>
    <th>Familiyasi</th>
    <th>Telefon raqami</th>
    <th>Manzili</th>
  </tr>
  <tr>
    <td>1</td>
    <td>Bahrom</td>
    <td>Ochilov</td>
    <td>(+90)- 225-54-45</td>
    <td>Samarqand vil. Urgut sh.</td>
  </tr>
  <tr>
    <td>2</td>
    <td>Nodir</td>
    <td>Omonov</td>
    <td>(+93)-343-09-94</td>
    <td>Samarqand vil. Tayloq t.</td>
  </tr>
  <tr>
    <td>3</td>
    <td>Sunnat</td>
    <td>Murodov</td>
    <td>(+97)-500-56-55</td>
    <td>Toshkent vil. Yunusobod t.</td>
  </tr>
  <tr>
    <td>4</td>
    <td>Sunnat</td>
    <td>Murodov</td>
    <td>(+97)-500-56-55</td>
    <td>Toshkent vil. Yunusobod t.</td>
  </tr>
  <tr>
    <td>5</td>
    <td>Sunnat</td>
    <td>Murodov</td>
    <td>(+97)-500-56-55</td>
    <td>Toshkent vil. Yunusobod t.</td>
  </tr>
  <tr>
    <td>6</td>
    <td>Sunnat</td>
    <td>Murodov</td>
    <td>(+97)-500-56-55</td>
    <td>Toshkent vil. Yunusobod t.</td>
  </tr>
  <tr>
    <td>7</td>
    <td>Sunnat</td>
    <td>Murodov</td>
    <td>(+97)-500-56-55</td>
    <td>Toshkent vil. Yunusobod t.</td>
  </tr>
</table>
  <input ref="input" type="text" v-model="myValue">
  <p>Input aksi: {{holat}}</p>
  <p>{{myValue}}</p>
  <input ref="inputId" type="text">
</template>
<script>
export default {
  name: "accountVue",
  data(){
    return{
      myValue: '',
      holat: '',
    }
  },
  methods:{
    myFunc(){
      this.$refs.inputId.focus();
    }
  },

  watch:{
    myValue(){
      this.holat = 'Yozilmoqa...';
      setTimeout(() => {
        this.holat = '';
      },2000)
    }
  },

}
</script>
<style scoped>

table, tr, th, td{
  border-collapse: collapse;
  font-size: 20px;
  margin: 20px;
  border: 1px solid;
}
th{
  background-color: #2c3e50;
  color: white;
  padding: 15px 40px;
}
td{
  background-color: #464683;
  color: pink;
  padding: 15px 40px;
}

</style>