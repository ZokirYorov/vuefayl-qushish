<template>
<div class="sidebar">
  <ul>
    <li :class="{active: openedRoute==='/account'}" @click="$emit('click-li', '/account')">Account</li>
    <li :class="{active: openedRoute==='/product'}" @click="$emit('click-li', '/product')">Products</li>
    <li :class="{active: openedRoute==='/categories'}" @click="$emit('click-li', '/categories')">Categories</li>
    <li :class="{active: openedRoute==='/about'}" @click="$emit('click-li', '/about')">About</li>
    <li :class="{active: openedRoute==='/Info'}" @click="$emit('click-li', '/Info')">Informations</li>
    <li :class="{active: openedRoute==='/other'}" @click="$emit('click-li', '/other')">Other</li>
    <li :class="{active: openedRoute==='/NevVue'}" @click="$emit('click-li', '/NevVue')">NevVue</li>
  </ul>
  <div style="padding-left: 10px">
    <button style="padding: 5px; margin-bottom: 5px; border-radius: 5px;
      background-color: yellow" @click="incrementCount">Count +</button>
    <p>{{count}}</p>

  </div>
</div>
</template>

<script>
export default {
  name: "sidebarVue",

  data(){
    return{
      count:0,
    }
  },
  methods:{
    incrementCount(){
      this.count = this.count + 5
    }
  },
  computed:{
    openedRoute() {
      return this.$route.path
    }
  }
}
</script>

<style scoped>
.sidebar{
  width: 100%;
  height: 100%;
  background-color: #9eff94;
}
ul{
  list-style: none;
  cursor: pointer;
}
li{
  font-size: 18px;
  padding: 7px;
}
li:hover{
  background-color: green;
}
.active{
  background-color: green;
  color: white;
}
</style>