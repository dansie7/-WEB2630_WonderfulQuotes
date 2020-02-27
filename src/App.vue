<template>
  <div class="container">
    <!--ToDo: Use the Header component selector-->
    <!--Bind data props quoteCount and set it equal to the quote length-->
    <!--Bind data props maxQuotes and set it equal to the maxQuotes created below-->

    <!--ToDo: Use the NewQuote component selector-->
    <!--Call @quoteAdded that is emitted from the NewQuote Component and pass the newQuote method created below-->

    <!--ToDo: Use the QuoteGrid component selector-->
    <!--Bind data props quotes and set it equal to the quotes array created below-->
    <!--Call @quoteDeleted that is emitted from the QuoteGrid Component and pass the deleteQuote method created below-->
    <div class="row">
      <div class="col-sm-12 text-center">
        <div class="alert alert-info">Info: Click on a Quote to delete it!</div>
      </div>
    </div>
  </div>
</template>

<script>
//  Todo: Import QuoteGrid, NewQuote, and Header Components
export default {
  data () {
    return {
      // ToDo: Create an array called quotes
      // Have at least one string by default

      // ToDo: Create maxQuotes that is set to 10
    }
  },
  methods: {
    // ToDo: Create a method called newQuote that takes the parameter quote.
    // This method will check if the quotes length is greater than or equal to the maxQuotes
    // If it is return an alert telling the user to delete a quote
    // Outside of conditional, push quote (method parameter) to the quotes array

    // ToDo: Create a method called deleteQuote that takes in a parameter of index
    // This method will splice the quotes array by (index, 1)
  },
  components: {
    // ToDo: Initiate the QuoteGrid, NewQuote, and Header Components with Custom Selectors
  }

}
</script>

<style></style>
