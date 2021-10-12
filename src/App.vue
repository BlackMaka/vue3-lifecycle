<template>
  <h1>{{ count }}</h1>
</template>

<script>
export default {
  data(){
    return{
      count:2
    }
  },
  beforeCreate(){
    console.log(`beforeCreate, (데이터/돔에 접근 불가) count : ${this.count}`);
  },
  created(){
    console.log(`created : 인스턴스가 생성된 후에 코드를 실행하는데 사용됩니다, (데이터만 접근가능) count : ${this.count}`);
  },
  beforeMount(){
    console.log(`beforeMount 돔에 접근 불가능, h1 : ${document.querySelector('h1')}`);
  },
  mounted(){
    console.log(`mounted : 화면에 렌더링 될때 실행 / 돔에 접근가능, h1 : ${document.querySelector('h1')}`);
  }
}
</script>

<style>

</style>