<template>
  <div class="col-sm-6 col-md-4 col-lg-3">
    <div class="panel panel-default">
      <div class="panel-body quote">
        <!--DONE ToDo: Add default slot tag for passing the quote-->
        <slot name="quote">Quote</slot>
      </div>
    </div>
  </div>
</template>

<script>
</script>

<style scope>
/* DONE ToDo: Create a class panel that sets the font-family to preffered font*/
/* DONE Set a specific front size to your liking*/
/* DONE Set a color of your choice*/

@font-face {
  font-family: permanentMarker;
  src: url(../assets/fonts/PermanentMarker-Regular.ttf);
}
.panel {
  font-family: 'permanentMarker', 'Arial Narrow Bold', sans-serif;
  font-weight: bold;
  font-size: 20px;
  color:rgb(172, 8, 241);
}

/* DONE ToDo: Create a class quote that sets the cursor to a pointer*/
.quote {
  cursor: pointer;
}

/* DONE ToDo: Create a hover effect on the class quote changing the background color to a color you prefer*/
.quote:hover {
  background-color: rgb(172, 8, 241);
  color: white;
}

</style>