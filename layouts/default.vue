<template>
  <div class="nav-header">
    <TheHeader/>
    <main class="content-holder">
      <nuxt/>
    </main>    
  </div>
</template>
<script>
import TheHeader from '@/components/TheHeader/TheHeader'
export default {
  components:{
    TheHeader
  }
}
</script>

<style>
html {
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}
.content-holder{
  margin-top: 20px;
}

</style>
