<template>
  <div>
    <h3>{{"モンスト攻撃力計算"}}</h3>
    <div id="stadardPower">
      <h5>基本攻撃力</h5>
      <input v-model="message" placeholder="edit me">
      <select v-model="selected">
        <option disabled=""></option>
        <option v-for="option in options" v-bind:value="option.name" v-bind:key="option.id">
          {{ option.name }}
        </option>
        <p>{{ selected }}</P>
      </select>
    </div>
    <div id="attribute">
      <h5>属性倍率</h5>
      <input type="radio" id="up" value="up" v-model="picked">
      <label for="up">アップ</label>
      <input type="radio" id="upup" value="upup" v-model="picked">
      <label for="upup">属性効果アップ</label>
      <input type="radio" id="upupup" value="upupup" v-model="picked">
      <label for="upupup">属性効果超アップ</label>
    </div>
    <div id="soulskil">
      <h5>ソウルスキル</h5>
      <input type="radio" id="soulup" value="soulup" v-model="picked">
      <label for="soulup">無印</label>
      <input type="radio" id="soulupup" value="soulupup" v-model="picked">
      <label for="soulupup">上</label>
      <input type="radio" id="soulupupup" value="soulupupup" v-model="picked">
      <label for="soulupupup">極</label>
    </div>
    <div id="killer">
      <h5>キラー</h5>
      <input type="radio" id="killersta" value="killersta" v-model="picked">
      <label for="killersta">無印</label>
      <input type="radio" id="killerM" value="killerM" v-model="picked">
      <label for="killerM">M</label>
      <input type="radio" id="killerL" value="killerL" v-model="picked">
      <label for="killerL">L</label>
      <input type="radio" id="killerEL" value="killerEL" v-model="picked">
      <label for="killerEL">EL</label>
    </div>
    <ul></ul>
    <h3></h3>
    <ul></ul>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
