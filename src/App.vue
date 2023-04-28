<!-- Composition API -->

<script setup>
   import {ref} from "vue";
   const count =ref(0);

   const addToCount=()=>{
    count.value=count.value+1;
   }
   const substractFromCount=()=>{
    count.value=count.value-1;
   }
</script>


<!-- Option API  -->
<!-- <script>
export default ({
  data() {
    return {
      count: 0
    }
  },
  methods: {
    addToCount() {
      this.count = this.count + 1;
    },
    substractFromCount() {
      this.count = this.count - 1;
    }
  }
})
</script> -->
<template>
  <main>
    <div>
      <h4>The current count is...</h4>
      <h1>{{ count }}</h1>
      <button @click="addToCount()">+</button>
      <button @click="substractFromCount()">-</button>
    </div>
  </main>
</template>

 <!-- scoped meaning   -->
<style scoped>
main {
  background-color: aliceblue;
  height: 100vh;
  widows: 100vw;
  display: flex;
  align-items: center;
  justify-content: center;

}

button {
  margin: 1vw;
}

div {
  text-align: center;
  font-family: 'Courier New', Courier, monospace;
}
</style>