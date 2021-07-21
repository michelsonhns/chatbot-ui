<template>
  <div id="app" class="chat-box">
    <div class="chat-log">
      <Message class="question" message="ola"/>

      <Message class="user-answer" message="ola"/>

      <Message class="question" message="Quelle genre vous vous identifiez ?"/>

      <Message class="user-answer">
        <template slot="content">
          <RadioField/>
        </template>
      </Message>
      <Message class="question" message="Quelle est votre activité principale ?"/>

      <Message class="user-answer">
        <template  slot="content">
          <CheckBox/>
        </template>
      </Message>
    </div>
     <div class="chat-input">      
      <form>
        <input type="text" placeholder="envoyer un message..."/>
        <button type="submit"><i class="material-icons">send</i></button>
      </form>  
    </div>
   
  </div>
</template>

<script>
import RatingStars from './components/RatingStars.vue'
import Message from './components/Message.vue'
import RadioField from './components/RadioField.vue'
import CheckBox from './components/CheckBox.vue'


export default {
  name: 'App',
  components: {
    RatingStars,
    Message,
    RadioField,
    CheckBox,
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  width: 50%;
}
.chat-box {
  position:fixed;
  right:30px;
  bottom:50px;
  max-height:90vh;
  padding-top: 1em;
  overflow: scroll;
  border-radius:5px;
  box-shadow: 0px 5px 35px 9px #ccc;
}


.chat-input input {
  background: #f4f7f9;
  width:98%;
  position:relative;
  height: 50px;
  padding: 1%;
  border:none;
  outline:none;
  color:#888;
  border-top:none;
  border-bottom-right-radius:5px;
  border-bottom-left-radius:5px;
  overflow:hidden;  
}


.chat-input button {  
  position:absolute;
  bottom:10px;
  right:10px;
  background: transparent;
  border:none;
  border-radius:50%;
  color:#083045;
  width:35px;
  height:35px;
}
</style>
