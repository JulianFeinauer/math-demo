<template>
<div>
  This is a question:
  <b>{{ x }} + {{ y }}</b>
  =
  <ion-input placeholder="?" v-model="input" @keyup="checkResult"></ion-input>
  <div>
    {{ message }}
  </div>
</div>
</template>

<script>
import {IonInput} from "@ionic/vue";

export default {
  name: "Question",
  components: { IonInput },
  props: {
    x: Number,
    y: Number,
    result: Number
  },
  data() {
    return {
      input: '',
      message: "Asdf"
    }
  },
  watch: {
    "input": function(val) {
      console.log("Result:", this.result, ", input", val)
      if (this.result === val) {
        this.message = "Yay!"
      } else {
        this.message = ":("
      }
    }
  }
}
</script>

<style scoped>

</style>
