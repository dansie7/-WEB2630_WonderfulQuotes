<template>
  <div class="container">
    <!--DONE ToDo: Use the Header component selector-->
    <!--DONE Bind data props quoteCount and set it equal to the quote length-->
    <!--DONE Bind data props maxQuotes and set it equal to the maxQuotes created below-->
    <app-header :quoteCount="quoteCount = quotes.length" :maxQuotes="maxQuotes = maxQuotes"></app-header>

    <!--DONE ToDo: Use the NewQuote component selector-->
    <!--DONE Call @quoteAdded that is emitted from the NewQuote Component and pass the newQuote method created below-->
    <app-new-quote @quoteAdded="newQuote($event)"></app-new-quote>

    <!--DONE ToDo: Use the QuoteGrid component selector-->
    <!--DONE Bind data props quotes and set it equal to the quotes array created below-->
    <!--DONE Call @quoteDeleted that is emitted from the QuoteGrid Component and pass the deleteQuote method created below-->
    <app-quote-grid :quote="quotes" @quotesDeleted="deleteQuote($event)"></app-quote-grid>
    <div class="row">
      <div class="col-sm-12 text-center">
        <div class="alert alert-info">Info: Click on a Quote to delete it!</div>
      </div>
    </div>
  </div>
</template>

<script>
//  DONE Todo: Import QuoteGrid, NewQuote, and Header Components
import Header from './components/Header.vue'
import QuoteGrid from './components/QuoteGrid.vue'
import NewQuote from './components/NewQuote.vue'

export default {
  data () {
    return {
      // DONE ToDo: Create an array called quotes
      //DONE Have at least one string by default
      quotes: ['Quote even if by default.'],

      // DONE ToDo: Create maxQuotes that is set to 10
      maxQuotes: 10
    }
  },
  methods: {
    // DONE ToDo: Create a method called newQuote that takes the parameter quote.
    // DONE This method will check if the quotes length is greater than or equal to the maxQuotes
    // DONE If it is return an alert telling the user to delete a quote
     // DONE Outside of conditional, push quote (method parameter) to the quotes array

    newQuote (quote) {
      if ( this.quotes.length > 10 || this.quotes.length === this.maxQuotes ) {
        return alert('You have exceeded the Quote max, please delete a quote.')
      }
      this.quotes.push(quote)
    },
   
    // DONE ToDo: Create a method called deleteQuote that takes in a parameter of index
    // DONE This method will splice the quotes array by (index, 1)
    deleteQuote (index) {
      this.quotes.splice(index, 1)
    }
  },
  components: {
    // DONE ToDo: Initiate the QuoteGrid, NewQuote, and Header Components with Custom Selectors
    'app-quote-grid': QuoteGrid,
    'app-new-quote' : NewQuote,
    'app-header': Header
  }

}
</script>

<style></style>
