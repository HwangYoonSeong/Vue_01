<template>
  <div class="red lighten-3 pa-3">
    <h3>User Info</h3>
    <p>{{nameOfChild}}</p>
    <p>{{sayHello}}</p>
    <v-btn color="primary" @click="switchName()">ChangeName</v-btn>
  </div>
</template>

<script>
export default {
  props: {
    nameOfChild: {
      type: String,
      default: "LEGO"
    }
  },
  computed: {
    sayHello () {
      return this.nameOfChild + ' Hello'
    }
  },
  methods: {
    switchName () {
      this.nameOfChild = "Hwang"
    }
  }

}
</script>