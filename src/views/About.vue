<template>
  <div class="about">
    <h1>This is an about page {{zeName}}</h1>
  </div>
</template>
<script>
  export default {
    props: {
      zeName: String
    }
  }
</script>
