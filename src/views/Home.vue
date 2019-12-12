<template>
  <div class="ion-page">
    <ion-header>
      <ion-toolbar>
        <ion-title>Sifritko TEST</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content class="ion-padding">
      <InputComponent v-on:get-zadani="vyresSifru"/>
      <ReseniComponent v-bind:reseni="reseni"/>
    </ion-content>



  </div>
</template>

<script>
// @ is an alias to /src

import InputComponent from '../components/InputComponent'
import ReseniComponent from '../components/ReseniComponent'

export default {
  name: 'home',
  components: {
    ReseniComponent,
    InputComponent,
  },
  data() {
    return {
      reseni: null
    }
  },
  methods: {
    vyresSifru(zadani) {
      for (let i = 1; i < 26; i ++) {
        if (i === 1)
          this.reseni = i + ': ' + this.caesarShift(zadani, i);
        else
          this.reseni += i + ': ' + this.caesarShift(zadani, i);
        this.reseni += "\n";
      }
    },
    caesarShift(str, amount) {

      amount = parseInt(amount);

      // Make an output variable
      var output = '';

      // Go through each character
      for (var i = 0; i < str.length; i ++) {

        // Get the character we'll be appending
        var c = str[i];

        // If it's a letter...
        if (c.match(/[a-z]/i)) {

          // Get its code
          var code = str.charCodeAt(i);

          // Uppercase letters
          if ((code >= 65) && (code <= 90))
            c = String.fromCharCode(((code - 65 + amount) % 26) + 65);

          // Lowercase letters
          else if ((code >= 97) && (code <= 122)) {
            c = String.fromCharCode(((code - 97 + amount) % 26) + 97);
          }

        }

        // Append
        output += c;

      }

      // All done!
      return output;

    }
  }
}
</script>
