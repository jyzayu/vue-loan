<template>
  <main>

<section class="py-5 text-center container">
  <div class="row py-lg-5">
    <div class="col-lg-6 col-md-8 mx-auto">
    </div>
  </div>
</section>

<div class="album py-5 bg-body-tertiary">
  <div class="container">

    <div class="row row-cols-1 row-cols-sm-2 row-cols-md-3 g-3">
      <div class="col" v-for="(item,i) in state.items.data" :key="i">
        <Card :item="item"/>
      </div>
    </div>
  </div>
</div>

  </main>
</template>
/* eslint-disable */
<script>
import Card from "@/components/Card";
import axios from "axios";
import { reactive } from "vue";

export default {
  name: 'HomeComponent',
  components: {
    Card,
  },
  setup() {
    const state = reactive({
      items: []
    })
      axios.get("/terms").then((res) =>{
        state.items = res.data
    })

    return {state}
  }
}


</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>