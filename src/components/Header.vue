<template>
  <div class="row">
    <div class="col-sm-12">
      <h3>Quotes Added</h3>
      <div class="progress">
        <div class="progress">
          <!-- DONE ToDo: Div with class="progress-bar" - Bind the style tag that adjusts the style width using quoteCount / maxQuotes-->
          <!-- DONE Remember to multiple the the divided total by 100 and adding the '%' to get a percentage-->
          <div
            class="progress-bar"
            role="progressbar"
            aria-valuenow="60"
            aria-valuemin="0"
            aria-valuemax="100" :style="{width: (quoteCount / maxQuotes) * 100 + '%'}"
          >
            <!--ToDo: Output quoteCount and maxQuotes-->
            <p>Quote Count: {{quoteCount}} Quote Max: {{maxQuotes}}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  // DONE ToDo: Create props that are being passed in App.vue (quoteCount & maxQuotes)
  // DONE Note: use normal array syntax, to pass more then 1 separate by comma
  props: ['quoteCount', 'maxQuotes']
}
</script>
