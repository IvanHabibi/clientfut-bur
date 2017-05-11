<template lang="html">
  <div class="valign-wrapper row login-box">
    <div class="col card hoverable s10 pull-s1 m6 pull-m3 l4 pull-l4">
      <form>
        <div class="card-content">
          <span class="card-title">Sign Up</span>
          <div class="row">
            <div class="input-field col s12">
              <label for="username">Username</label>
              <input type="text" class="validate" name="username" id="username" />
            </div>
            <div class="input-field col s12">
              <label for="password">Password </label>
              <input type="password" class="validate" name="password" id="password" />
            </div>
            <div class="input-field col s12">
              <label for="password">Email </label>
              <input type="email" class="validate" name="password" id="password" />
            </div>
            <div class="input-field col s12">
              <label for="password">Phone </label>
              <input type="text" class="validate" name="password" id="password" />
            </div>
            <a router-link to="/Register" class="btn green waves-effect waves-light">Sign Up </a>
          </div>
        </div>
      </form>
    </div>
  </div>
</template>
<script>
export default {
  name: 'register'
}
</script>

<style lang="css" scoped>






</style>
