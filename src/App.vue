<template>
  <div id="app">
    <img id="logo" alt="Vue logo" src="./assets/logo.png">
    <h1 class="title">Random Fontawesome Icon Generator</h1>
    <p>(click refresh on your browser to see a new one)</p>
<!--    <button v-on:click="generate()" class="button is-normal">Make it so</button>-->
<!--    TODO:  add button to spin icon once it's loaded by adding :class="fa-spin" when clicked -->
    <br>
    <div class="container box">
      <span id="fa-icon" class="icon is-large is-vcentered">
           <i v-bind:style="mycolor"  :class="'fal fa-' + selectedIcon + ' fa-7x'"></i>
      </span>
    </div>
<!--    <h1 >{{ mycolor }}</h1>-->
  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      mycolor: {
        color: '#' + (Math.random() * 0xFFFFFF << 0).toString(16)
      },
      iconArray: [
        'abacus',
        'magic',
        'alicorn',
        'angry',
        'amp-guitar',
        'badger-honey',
        'bacon',
        'bone-break',
        'blender-phone',
        'bomb',
        'bong',
        'bug',
        'alien',
        'cat-space',
        'comet',
        'flux-capacitor',
        'meteor',
        'portal-enter',
        'space-station-moon-alt',
        'starship-freighter',
        'dagger',
        'dragon',
        'flask-potion',
        'skull-crossbones',
        'wand-magic',
        'cow',
        'deer-rudolph',
        'dog',
        'frog',
        'narwhal',
        'otter',
        'sheep',
        'skull-crossbones',
        'sparkles',
        'cookie-bite',
        'coffee-pot',
        'code-branch',
        'cloud-meatball',
        'code-branch',
        'code-commit',
        'female',
        'fort-awesome',
        'eye',
        'flushed',
        'flask-poison',
        'grin-squint-tears',
        'grin-tongue',
        'grimace',
        'stroopwafel',
        'brackets-curly',
        'rocket-launch',
        'gamepad-alt',
        'game-console-handheld',
        'globe-snow'
      ],
      selectedIcon: this.selectedIcon
    }
  },
  methods: {
    randomItem (items) {
      return items[Math.floor(Math.random() * items.length)]
    },
    generate () {
      console.log(this.selectedIcon)
      this.selectedIcon = this.randomItem(this.iconArray)
    }
  },
  created () {
    this.selectedIcon = this.randomItem(this.iconArray)
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

#logo {
  width: 100px;
}

button {
  margin: 20px;
}
.box {
  width: 300px;
  height: 300px;
  padding: 100px;
}
</style>
