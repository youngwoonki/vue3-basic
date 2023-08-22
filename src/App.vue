<template>
  <h1 @click="increase">
    <!-- h1을 클릭할때마다 increase함수가 실행되서 1씩 오른다. -->
    {{ count }}
  </h1>
  <div v-if="count>4"> 
    <!-- count가 4보다 클때만 나오게 조건을 넣어준것. -->
    4보다 큽니다!
  </div>
  <ul>
    <Fruit
      v-for="fruit in fruits"
      :key="fruit"
      :name="fruit">
      {{ fruit }}
    </Fruit>
  </ul>
</template>

<script>
import Fruit from '~/components/Fruit'

export default{
  components:{
    // hello:Fruit
    Fruit
  },
  data(){
    return{
      count:0,
      fruits: ['Apple', 'Banana', 'Cherry']
    }
  },
  methods:{
    increase(){
      this.count += 1 // this는 script부분에서 count를 찾은것.
    }
  }
}
</script>

<style lang="scss"> // lang을 scss로
  h1{
    font-size: 50px;
    color: royalblue;
  }
  ul{
    li{
      font-size: 40px;
    }
  }
</style>