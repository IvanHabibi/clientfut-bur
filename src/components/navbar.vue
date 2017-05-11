<template lang="html">
  <nav>
    <div class="nav-wrapper" >
      <a href="#" class="brand-logo">Logo</a>
      <ul id="nav-mobile" class="right hide-on-med-and-down">
        <li><a href="sass.html">Sass</a></li>
        <li><a href="badges.html">Components</a></li>
        <li><router-link to="/Login">Sign in</router-link></li>
      </ul>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'navbar'
}
</script>

<style lang="css">
#navbar{
    margin-top:60px
}
</style>
