<template>
  <div id="block">
    <button v-on:click="afficheMessage">
      cliquez ici
    </button>
    <div>
      <p>{{ msg }}</p>
      <p id="#sorry" v-if="seen"> Mamie est très triste. Elle n'a pas une très bonne....Vue...</p>
    </div>
    <div>
      <p>indiquez la note ici :</p>
      <p><input v-model.number="note" type="number">/20</p>
      <h2>{{ note }} /20</h2>
    </div>
    <div>
      <h5>{{ messageNote }}</h5>
    </div>
  </div>
</template>
<script>

export default {
  name: 'Msg',
  data () {
    return {
      msg: '¯\\_(ツ)_/¯',
      seen: false,
      note: 20,
      messageNote: "C'est quoi ma note ? =)"
    }
  },
  methods: {
    afficheMessage () {
      if (this.seen === true) {
        this.seen = false
      } else {
        this.seen = true
      }
    }
  }

}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  h1, h2 {
    font-weight: normal;
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
