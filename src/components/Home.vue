<template>
  <div>
    <h1 class="title">Random Fontawesome Icon Generator</h1>
    <button @click="generate()" class="button is-normal">Make it so</button>
    <br>
    <div class="container box">
      <span id="fa-icon" v-if="selectedIcon">
        <i :class="selectedIcon"></i>
      </span>
    </div>

  </div>
</template>

<script>
export default {
  name: 'home',
  data () {
    return {
      iconArray: [
        'fal fa-abacus',
        'fal fa-magic',
        'fal fa-alicorn'
      ],
      selectedIcon: null
    }
  },
  methods: {
    randomIcon (items) {
      return items[Math.floor(Math.random() * items.length)]
    },
    generate () {
      this.selectedIcon = this.randomIcon(this.iconArray)
    }
  },
  created () {
    this.selectedIcon = this.randomIcon(this.iconArray)
  }
}
</script>

<style scoped>
.box {
  padding: 100px;
}

fa-icon {
  width: 50px;
}

</style>
