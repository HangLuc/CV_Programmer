<template>
  <div id="app">
    <span>H</span>
    <div v-for="item in itemList">
      <span>{{item.name}}</span>
    </div>
  </div>
</template>
<script>
  import axios from "axios";
  export default {
    name: "app",
    data() {
      return {
        itemList: []
      }
    },
    mounted() {
      this.getData();
    },
    methods: {
      getData() {
        axios.get('http://localhost:8080/api/test').then(response => {
          console.log(response.data);

          this.itemList=response.data;
          console.log(this.itemList.nick);
        }, response => {
          console.log("error");
        });
      }
    }
  }
</script>
