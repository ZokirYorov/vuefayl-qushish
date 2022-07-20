<template>
<table id="table">
  <tr>
    <th>T/N</th>
    <th>Nomi</th>
    <th>Narxi 1 k/g</th>
  </tr>
  <tr>
    <td>1</td>
    <td>Olma</td>
    <td>100 so'm</td>
  </tr>
  <tr>
    <td>2</td>
    <td>Anor</td>
    <td>200 so'm</td>
  </tr>
  <tr>
    <td>3</td>
    <td>Uzum</td>
    <td>150 so'm</td>
  </tr>
  <tr>
    <td>4</td>
    <td>Gusht</td>
    <td>750 so'm</td>
  </tr>
</table>

  <button @click="incrementCount">Count +</button><button @click="diencrementCount">Count -</button>
  <p style="margin-left: 20px; padding: 5px">{{count}}</p>
</template>

<script>


export default {
  name: "productVue",
  data(){
    return{
      count: 0,
    }
  },
  methods:{
    incrementCount(){
      this.count = this.count + 5
    },
    diencrementCount(){
      if (this.count <=0){
        return
      }
      this.count = this.count - 5
    }

  }
}
</script>

<style scoped>
table, th, tr, td{
  border-collapse: collapse;
  border: 1px solid;
  padding: 15px 60px;
  margin: 10px;
  font-size: 20px;
}
th{
  background-color: cadetblue;
}
td:first-child{
  background-color: coral;

}
td:nth-child(2){
  background-color: cadetblue;
}
td:nth-child(3){
  background-color: cyan;
}
button{
  padding: 15px 50px;
  margin: 5px;
  border-radius: 80px;
  border: none;
  color: white;
  background-color: red;
}
button:hover{
  background-color: #5757ff;
}


</style>