<template>
  <div id="app">
    <img id="logo" alt="Vue logo" src="./assets/logo.png">
    <h1 class="title">Random Fontawesome Icon Generator</h1>
    <p>(click refresh on your browser to see a new one)</p>
<!--    <button v-on:click="generate()" class="button is-normal">Make it so</button>-->
    <br>
    <div class="container box">
      <span id="fa-icon" class="icon is-large is-vcentered">
<!--        <pre>{{ htmlCode() }}</pre>-->
           <i :class="selectedIcon + ' fa-7x'"></i>
      </span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      iconArray: [
        'fal fa-abacus',
        'fal fa-magic',
        'fal fa-alicorn',
        'fal fa-angry',
        'fal fa-amp-guitar',
        'fal fa-badger-honey',
        'fal fa-bacon',
        'fal fa-bone-break',
        'fal fa-blender-phone',
        'fal fa-bomb',
        'fal fa-bong',
        'fal fa-bug',
        'fal fa-alien',
        'fal fa-cat-space',
        'fal fa-comet',
        'fal fa-flux-capacitor',
        'fal fa-meteor',
        'fal fa-portal-enter',
        'fal fa-space-station-moon-alt',
        'fal fa-starship-freighter',
        'fal fa-dagger',
        'fal fa-dragon',
        'fal fa-flask-potion',
        'fal fa-skull-crossbones',
        'fal fa-wand-magic',
        'fal fa-cow',
        'fal fa-deer-rudolph',
        'fal fa-dog',
        'fal fa-frog',
        'fal fa-narwhal',
        'fal fa-otter',
        'fal fa-sheep',
        'fal fa-skull-crossbones',
        'fal fa-sparkles',
        'fal fa-cookie-bite',
        'fal fa-coffee-pot',
        'fal fa-code-branch',
        'fal fa-cloud-meatball',
        'fal fa-code-branch',
        'fal fa-code-commit',
        'fal fa-female',
        'fal fa-fort-awesome',
        'fal fa-eye',
        'fal fa-flushed',
        'fal fa-flask-poison',
        'fal fa-grin-squint-tears',
        'fal fa-grin-tongue',
        'fal fa-grimace'
      ],
      selectedIcon: this.selectedIcon
    }
  },
  methods: {
    // htmlCode () {
    //   let html = '<i class="fa-7x '
    //   html += this.selectedIcon
    //   html += '"></i>'
    //   return html
    // },
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
