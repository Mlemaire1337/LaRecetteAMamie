<template>
  <div id="block">
    <button v-on:click="afficheMessage">
      cliquez ici
    </button>
    <div>
      <p>{{ msg }}</p>
      <div id="#sorry" v-if="seen">
        <h3>Mamie est très triste. Elle n'a pas une très bonne....Vue...</h3>
        <p>+1 point pour cette blague ?</p>
        <input type="radio" id="oui" v-model="checked" value="Merci =)">
        <label for="oui">Oui</label>
        <input type="radio" id="non" v-model="checked" value="Tant pis.">
        <label for="non">Non</label>
        <br>
        <span> {{ checked }}</span>
      </div>
    </div>
    <div>
      <p>indiquez la note ici :</p>
      <p><input v-model.number="note" type="number" id="note">/20</p>
      <h2>{{ note }} /20</h2>
    </div>
    <div>
      <h5 v-if="note>= 20">C'est pas un peu beaucoup ?</h5>
      <h5 v-if="note>= 0 && note< 10">Je l'ai mérité...</h5>
      <h5 v-if="note>= 10 && note< 20">Ouh là... C'est un peu trop gentil</h5>
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
      checked: []
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
