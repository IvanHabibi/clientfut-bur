<template lang="html">

  <div class="valign-wrapper row login-box" id="login">
    <div class="col card hoverable s10 pull-s1 m6 pull-m3 l4 pull-l4">
      <form>
        <div class="card-content">
          <span class="card-title">Enter credentials</span>
          <div class="row">
            <div class="input-field col s12">
              <label for="username">Username</label>
              <input type="text" class="validate" name="username" id="username" v-model="username" />
            </div>
            <div class="input-field col s12">
              <label for="password">Password </label>
              <input type="password" class="validate" name="password" id="password" v-model="password"/>
            </div>
            <a @click="fungsiLogin" class="btn green waves-effect waves-light" to="/" >log In</a> or
            <a class="btn green waves-effect waves-light" >Sign Up</a>

          </div>
        </div>
        <div class="card-action center-align">
          <a  class="btn indigo darken-4 waves-effect waves-light">Facebook</a>
        </div>

      </form>
    </div>
  </div>
</template>
<script>
export default {
  name: 'login',
  data(){
    return {
      username:'',
      password:''
    }

  },
  methods:{

    fungsiLogin: function() {
      console.log(this.username);
      console.log(this.password);
        axios.post('http://localhost:3000/signin', {
                username: this.username,
                password: this.password
            })
            .then(function(response) {

                window.localStorage.setItem('token', JSON.stringify(response.data.token))
                console.log(response.data.token);
            });
    }
  }
}
</script>

<style lang="css" scoped>
#login{
  margin-top:60px

}





</style>
