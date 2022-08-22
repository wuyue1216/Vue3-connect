<template>
  <div class="hello">
    <ul class="tab">
      <li v-for="(item,index) in items" :key="index">
      <a :href="item.title">{{item.title}}</a></li>
    </ul>
    <p id="one">one</p>
    <p id="two">two</p>
    <p id="three">three</p>
    <p id="four">four</p>
    <p id="five">five</p>
    <p id="six">six</p>
    <p id="seven">seven</p>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },
  setup(){
      const items = [{
            title: '#one',
            hash: '#one',
        },{
            title:'#two',
            hash: '#two',
        },{
            title:'#three',
            hash: '#three',
        },{
            title:'#four',
            hash: '#four',
        },{
            title:'#five',
            hash: '#five',
        },{

            title:'#six',
            hash: '#six',
        },{

            title:'#seven',
            hash: '#seven',
        }];
    return{
        items,
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style  lang="scss" scoped>
p{
  width: 100%;
  height: 500px;
}
p:nth-child(even){
  background-color: bisque;
}
ul{
  width: 100%;
  list-style: none;
  display: flex;
  text-align: initial;
  li{
    color: red;
    font-size: 15px;
    flex: 1;
  }
}

</style>
