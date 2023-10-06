<script>
import HelloWorld from './components/HelloWorld.vue'
export default {
  data() {
    return {
      plusNum: 0,
      neNum: 0,
      totalNum: 0,
      arr: []
    }
  },
  methods: {
    cool() {
      let obj = {
        name: "cool",
        money: 100
      }

      let obj2 = {
        name: "cool",
        money: -50
      }
      this.arr.push(obj)
      this.arr.push(obj2)
      
    }
  },
  components: {
    HelloWorld
  }
}
</script>

<template>
  <div class="bgArea">
    <div class="blueArea">
      <h1>{{ totalNum }}</h1>
    </div>
    <div class="whiteArea">
      <div class="top">
        <h1>{{ plusNum }}</h1>
        <h1>{{ neNum }}</h1>
      </div>
      <div class="btn">
        <button type="button" class="numBtn" v-on:click="cool">BTN</button>
      </div>
      <div class="content">
        <div class="block" v-for="item in arr">
          <span>{{ item.name }}</span>
          <span>{{ item.money }}</span>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.bgArea {
  width: 100%;
  height: 100vh;
  display: flex;

  .blueArea {
    width: 40vw;
    height: 100vh;
    background-color: #4b85a0;
  }

  .whiteArea {
    width: 60vw;
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction:column;
    .content{
      width:60% ;
      height: 40vh;
      
      .block{
        display: flex;
        justify-content: space-between;
        font-size: 24pt;
      }
    }
  }

}
</style>
