<template>
  <div class="row">
    <!--ToDo: Use the Quote component selector-->
    <!--Loop through quotes using v-for and get quote and index-->
    <!--Add a click event with .native modifier and set it equal to the deleteQuote method created below and pass index-->
    <!--Display the quote inside the appQuote component, in other words pass the data object to the slot in Quote.vue-->
  </div>
</template>

<script>
// ToDo: import the Quote Component

export default {
  // ToDo: Create props of quote

  components: {
    // ToDo: Initiate the Quote Component with a Custom Selector
  },
  methods: {
    // ToDo: Create a method deleteQuote that takes a paremeter of index
    // $emit a custom event listener named quotesDeleted and pass index in the second parameter
  }
}
</script>
