<script>
export default {
    name:'MainApp'
}
</script>


<template>
  <div>
    <p>--------> CONTENT GOES HERE </p>
  </div>
</template>



<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;
    div {
        color: white;
        background-color: #1C1C1C;
        height: 200px;
        @include centerFlex;
    }
</style>