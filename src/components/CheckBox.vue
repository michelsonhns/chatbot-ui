<template>
  <div>
    <label for="" v-for="option in options" :key="option.id">
      <input type="checkbox" :name="option.name" :value="option.value">
          {{option.text}}
       <slot></slot>
    </label>
  </div>
</template>

<script>
export default {
  data () {
    return {
      options: [
        { text: 'Cinéma', value: 'movie', name: 'interest' },
        { text: 'Sports', value: 'sport', name: 'interest'  },
        { text: 'Voyage', value: 'travel', name: 'interest'  },
        { text: 'Théâtre', value: 'theater', name: 'interest'  },
        { text: 'Concert', value: 'concert', name: 'interest' }
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
</style>