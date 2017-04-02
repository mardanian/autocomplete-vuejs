<template>
  <div class="container">
    <autocomplete :suggestions="cities" @selected="valueSelected"></autocomplete>
    <br>
    {{ value }}
  </div>
</template>

<script>
import AutoComplete from './AutoComplete.vue';

export default {
  components: {
    'autocomplete': AutoComplete
  },
  data() {
    return {
      cities: [ 'Bangalore','Chennai','Cochin','Delhi','Kolkata','Mumbai' ],
      value: ''
    }
  },
  methods: {
    valueSelected(value) {
      this.value = value;
    }
  }
}
</script>
