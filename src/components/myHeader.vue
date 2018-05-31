<template>
  <div class="myHeader">
    <img src="../assets/suger.png" alt="">
    <h1>Sugar Store</h1>
  </div>
</template>
<script>
export default {
  name:"myHeader",
  data(){
    return{
      msg:"Welcome to Your Vue.js App"
    };
  }
};
</script>
<style scoped>
.myHeader{
  width:100%;
  height: 75px;
  background-color:#F3758E;
  color:antiquewhite;
}
img{
  float: left;
  width: 75px;
  height: 75px;
  clear: both;
}
h1{
  float: left;
}
</style>


