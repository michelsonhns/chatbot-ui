<template>
<div class="radio">
  <label v-for="option in options" :key="option.id">
      <input type="radio" :value="option.value" :name="option.name"/>
      {{option.text}}
  </label>
</div>
</template>

<script>
  export default {
    data () {
      return {
       options: [
          { text: 'Femme', value: 'female', name: 'gender' },
          { text: 'Homme', value: 'male', name: 'gender'  },
          { text: 'Non-binaire', value: 'non-binary', name: 'gender'  },
          { text: 'Autre', value: 'other', name: 'gender'  },
          { text: 'Je ne souhaite pas informer', value: 'dont-want-inform', name: 'gender' }
      ]
      }
    },
  }
</script>

<style scoped>
label {
  display: block;
  text-align: left !important;
}
.radio {

}
</style>