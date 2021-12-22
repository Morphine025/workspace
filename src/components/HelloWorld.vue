<template>
  <div class="hello">
    <label for="">
     <p>Self introduction</p> 
      <br>
      <textarea :cols="width" :rows="height" v-model='content' :maxlength="total"></textarea>
      <br>
      <p>还能输入{{count}}字</p>
    </label>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data() {
    return {
      content:''
    }
  },
  computed:{
    count(){
      return this.total -this.content.length;
    }
  },
  props: {
    total:{
      type:Number,
      default:200
    },
    title:{
      type:String,
      default:'多行文本标题'
    },
    width:{
      type:Number,
      default:20
    },
    height:{
      type:Number,
      default:3
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
