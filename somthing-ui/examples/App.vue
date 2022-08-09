<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <Demo></Demo>
    <Card
    imgSrc="react.png"
    summary="summary test test test"
    :width="370"
    :imgHeight="100"
    >
    <template v-slot:footer>
      <div class="footer">
        <div class="level">level test</div>
        <div class="price">$199.00</div>
      </div>
      
    </template>
    </Card>
    <Button type="primary" disabled round icon="info"></Button>
    <Button type="danger"  round icon="info" @click="handleClick"></Button>
   
  </div>
</template>

<script>

export default {
  name: 'App',
  methods:{
    handleClick(){
      alert(123)
    }
  }

}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.footer{
  display: flex;
  justify-content: space-between;

}

.level{
  /* display: flex; */

  /* flex:1; */
  
  font-size: 14px;
  color: red;
  padding-left:10px ;
  /* justify-content: space-between; */
  /* text-align: left; */
  /* padding-left: 10px; */
}

.price{
  /* display: flex; */
  /* flex:1; */
  font-size: 14px;
  color: red;
  padding-right: 10px;
  /* justify-content: space-between; */
  
  /* text-align: right; */
  /* padding-left: 10px; */
}
</style>
