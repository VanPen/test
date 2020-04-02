<template>
   <div id="test">
   <p>{{ fullText }}</p>
   </div>
</template>
<script>
    export default {
       el : '#test',
       data() {
          return {
             hello: "CCCou",
             word: "ouCC",
          }
       },
       computed: {
          fullText: {
             // GETTER
             get: function () {
                return this.hello + ' drdrr' + this.word
             },
// SETTER
             set: function (newValue) {
                const newHelloWord= newValue.split('')
                this.hello= newHelloWord[0]
                this.word= newHelloWord[newHelloWord.length - 1]
             }
          }
       }
    }
</script>

<style scoped>

</style>