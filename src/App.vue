<template >

<div class="text">
      <div id="app">
        <p>5月28日todo-list</p>
        <input v-model="text" type="text">
        <button @click="xyn">提交</button>
        <ol>
        <li v-for="(item,index) in list" :key="index" @click="pengrui(index)">{{item}}</li>
        </ol>
      </div>
  </div>

</template>

<script>


export default {
  name: 'app',
  data(){
    return ({
      list:[
        '联想笔记本',
        '戴尔笔记本',
        '华硕笔记本'
      ],
      text:''
    })
  },
  methods: {
    xyn(){
      this.list.push(this.text),
      this.text=''
    },
    pengrui(index){
      this.list.splice(index,1)
    }
     
    },
    components:{

    }
 
}
</script>

<style>
.text{
  margin:0 auto;
  margin-top: 200px;
  width:400px;
  border:1px solid red;
  background-color: aquamarine;
}
#app{
  border:1px solid green;
  text-align: center;
}
ol{
  list-style: none;
}
input{
  background-color:#C1C1C1;
}
.bood{
  background-color: antiquewhite;
}


</style>
