
  <template>
    <div id="app">
      <Messagist :messages="messages"></Messagist>
    </div>

      </template>


      <script>
import Message from "./Message.vue";
import Choice from "./Choice.vue";
import Messagist from "./MessagistWrapper";

export default {
  name: "App",

  components: {
    Messagist: Messagist
  },

  data: function () {

    return { messages: {
      init: {
        content: ["Hello", "I am Messagist, and will be your new best friend!"],
        choices: {
          accept: "Okay Messagist, I accept that ♥️"
        }
      },
      accept: {
        content: "🎉🎉🎉 That makes me happy"
      }
    }
   }
  }
};
</script>



<style scoped>
.Survey {
  max-width: 640px;
  margin: 0 auto;
}

label {
  display: block;
}

input {
  width: 100%;
  display: block;
  height: 2rem;
  font-size: 1rem;
  padding: 0 0.5rem;
  margin: 0.5rem 0;
  box-sizing: border-box;
}

button {
  float: right;
  padding: 10px 20px;
  background: darkseagreen;
  color: #fff;
  font-weight: bold;
  border: 1px solid forestgreen;
  border-radius: 0.5rem;
}
</style>
