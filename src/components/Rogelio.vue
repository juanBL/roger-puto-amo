<template>
  <div class="hello">
    <p>
      Hola Duckers, algunos os preguntareís como es posible hablar como nuestro querido amigo Roger.
    </p>
    <p>
      Os lo pongo fácil introduce una frase como escribiría una persona normal y yo lo traduciré al rogelium.
    </p>

    <br>
    <label>
      <textarea v-model="message" @keypress="handlePress" placeholder="Inserta líneas para traducir al rogelium" cols="40" rows="5"/>
    </label>

    <button v-on:click="resetText">Reset</button>
    <br>
    <br>
    <span><strong>ROGELIUM:</strong></span>
    <p v-html="rogelium"/>

  </div>

</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data(){
    return {
      message : '',
      rogelium : ''
    }
  },
  methods: {
    handlePress(e) {
      console.log(e);
      this.rogelium =  this.rogelium + "<br/>" + e.key
    },
    resetText: function ( ) {
      this.message = '';
      this.rogelium = ''
    }
  }
}
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
