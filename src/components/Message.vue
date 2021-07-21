<template>
  <div class="message">
   <p>{{ message }}
   <slot name="content"></slot>
   </p>
  </div>
</template>
<script>
export default {
  name: 'messages',
  props: {
    message: String,
  },
  data: {
  }
}
</script>

<style scoped>
.message {
  min-width: 60%;
  max-width: 80%;
  padding: 0.1em;
  text-align: left;
  padding-left: 1em;
  margin-bottom: 1em;
  margin-left: 10px;
}
.question {
  background: #F1F0F0;
  color: #000000;
  border-radius: 0.8rem 0.8rem 0.8rem 0 ;
  float:left;
  margin-left: 10px;
} 
.user-answer {
  background-color: #083045;
  color: #FFF;
  border-radius: 0.8rem 0.8rem 0 0.8rem;
  float: right;
  margin-right: 10px;
} 
</style>