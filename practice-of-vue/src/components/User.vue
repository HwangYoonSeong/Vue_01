<template>
  <div class="blue lighten-3 pa-3">
    <h1>User Components</h1>
    <p>Name: {{name}}</p>

    <v-btn color="success" @click="changeName()">ChangeName</v-btn>
    <br />
    <br />
    <v-layout row wrap>
      <v-flex xs12 sm6>
        <UserDetail :nameOfChild="name"></UserDetail>
      </v-flex>
      <v-flex xs12 sm6>
        <UserEdit></UserEdit>
      </v-flex>
    </v-layout>
  </div>
</template>

<script>
import UserDetail from "./UserDetail.vue"
import UserEdit from "./UserEdit.vue"

export default {
  components: {
    UserDetail,
    UserEdit
  },
  data () {
    return {
      name: "Vue.js"
    }
  },
  methods: {
    changeName () {
      this.name = "YoonCastle"
    }
  }



}
</script>