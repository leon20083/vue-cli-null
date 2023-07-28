<!-- eslint-disable -->
<template>
  <!-- Приветик {{ name }} -->
  <!-- <template v-if="msg === 1">
    <div class="">{{ msg }}</div>
  </template>
  <template v-else-if="msg === 2">
    <div class="">{{ msg }}</div>
  </template>
  <template v-else>
    <div class="">{{ msg }}</div>
  </template> -->
  <div class="">
    <!-- <button @click.right="onClick('some value', $event)">Click</button>
    <a href="" @click.prevent="onLinkClick">Link</a>
    <input type="text" id="input" @keyup.enter="onKeyAp">
    <h1>{{ text }}</h1> -->
    <ul>
      <li class="" v-for="(color, index) of colors" :key="index">{{index + 1}} - {{ color }}</li>
      <li v-for="user of users" :key="user.id"> {{ user.name }} {{ user.age }}</li>
      <li v-for="(product, name, index) of products" :key="index">{{index+1}} {{ name }} - {{ product }}</li>
    </ul>
  </div>
</template>

<script>

export default {
  name: 'App',
  components: {
  },
  data() {
    return {
      // name: 'Leonid',
      // msg: 3,
      // text: '',
      colors: ['green', 'yelow', 'blue'],
      users: [{
        id: 1,
        name: 'Иван',
        age: 30,
      },
      {
        id: 2,
        name: 'Leonid',
        age: 47,
      },
      ],
      products:{
        brand: 'Apple',
        model: 'iPhone 11 Pro',
        price: '$1000',
      },
    };
  },
  methods: {
    // onClick(value, e) {
    //   console.log(value, e);
    // },
    // onLinkClick() {
    //   console.log('link click');
    // },
    // onKeyAp(e) {
    //   console.log(e);
    //   this.text = e.target.value;
    // },
  },
};
</script>

<style lang="sass">
#app
  font-family: Avenir, Helvetica, Arial, sans-serif
  -webkit-font-smoothing: antialiased
  -moz-osx-font-smoothing: grayscale
  text-align: center
  color: #2c3e50
  margin-top: 60px

</style>
