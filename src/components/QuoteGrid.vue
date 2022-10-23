<template>
  <div class="row">
    <!--DONE ToDo: Use the Quote component selector-->
    <!--RE-CHECK Loop through quotes using v-for and get quote and index-->
    <!--DONE Add a click event with .native modifier and set it equal to the deleteQuote method created below and pass index-->
    <!--RE-CHECK Display the quote inside the appQuote component, in other words pass the data object to the slot in Quote.vue-->
     <app-quote v-for="(quote, index) in quotes" :key="index" @click.native="deleteQuote(index)">
      <p slot="theQuote">{{ quote }}</p>
     </app-quote>
  </div>
</template>

<script>
// DONE ToDo: import the Quote Component
import Quote from '../components/Quote.vue'

export default {
  // DONE ToDo: Create props of quote
  props: ['quote'],

  components: {
    // ToDo: Initiate the Quote Component with a Custom Selector
    'app-quote': Quote
  },
  methods: {
    // RE-CHECK ToDo: Create a method deleteQuote that takes a paremeter of index
    // RE-CHECK $emit a custom event listener named quotesDeleted and pass index in the second parameter
    deleteQuote (index) {
      this.$emit('quotesDeleted', index)
    }
  }
}
</script>
