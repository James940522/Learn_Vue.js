<template>
  <div>
    <div class="menu">
      <a v-for="(el, idx) in 메뉴들" :key="idx">{{ el }}</a>
    </div>
    <div v-for="(el, idx) in products" :key="idx">
      <h4 :style="스타일">{{ el }}</h4>
      <p>{{ price[idx] }}만원</p>
      <button @click="신고수[idx]++">허위매물신고</button>
      <span>신고수 : {{ 신고수[idx] }}</span>
    </div>
    <!-- <div>
      <h4 :style="스타일">{{ products[0] }}</h4>
      <p>{{ price1 }}만원</p>
    </div>
    <div>
      <h4 :style="스타일">{{ products[1] }}</h4>
      <p>{{ price2 }}만원</p>
    </div>
    <div>
      <h4 :style="스타일">{{ products[2] }}</h4>
      <p>{{ price3 }}만원</p>
    </div> -->
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      // 데이터 보관함 object 자료로 저장
      신고수: [0, 0, 0],
      price: [60, 70, 80],
      스타일: "color: blue",
      메뉴들: ["Home", "Shop", "About"],
      products: ["역삼동원룸", "천호동원룸", "마포구원룸"],
    };
  },
  components: {},
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.menu {
  background: darkslateblue;
  padding: 15px;
  border-radius: 5px;
}

.menu a {
  color: white;
  padding: 10px;
}
</style>
