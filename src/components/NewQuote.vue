<template>
  <div class="row">
    <form>
      <div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3 form-group">
        <label>Quote</label>
        <!--RE-CHECK ToDo: Within the textarea use v-model that is set to quote-->
        <textarea
          class="form-control"
          rows="3"
        v-model="quote"></textarea>
      </div>
      <div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3 form-group">
        <!--RE-CHECK ToDo: Add a click event with .prevent modifier and set it equal to the createNew method created below-->
        <button class="btn btn-primary" @click.prevent="createNew">Add Quote</button>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  data () {
    return {
      // DONE ToDo: Create a data object called quote that is se to an empty string
      quote: ''
    };
  },
  methods: {
    // RE-CHECK ToDo: Create a method createNew that emits a custom event named quoteAdded that passes the quote data object above
    // RE-CHECK Set quote to an empty string
    createNew () {
      this.quote = ''
      this.$emit('quoteAdded', this.quote)
    }
  }
}
</script>
