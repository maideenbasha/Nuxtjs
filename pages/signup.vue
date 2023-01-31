<template>
    <div>
  <b-form @submit.stop.prevent>
    <label for="userName">UserName</label>
    <b-form-input class="form-control input" type="text" v-model="userName" v-bind:class="{error:$v.userName.$error,valid: $v.userName.$dirty && !$v.userName.$invalid }"/>   
    <div v-if="$v.userName.$dirty">
      <p class="error-message" v-if="!$v.userName.required">UserName is required</p>
               </div>
    <label for="email">Email</label>
    <b-form-input class="form-control input" type="email"  v-model="email" v-bind:class="{error:$v.email.$error,valid: $v.email.$dirty && !$v.email.$invalid }"/>
    <div  v-if="$v.email.$dirty">
              <p class="error-message" v-if="!$v.email.required">Email is required</p>
              <p class="error-message" v-if="$v.email.required && !$v.email.email">Enter Validate Email</p>   
            </div>
    <label for="password">Password</label>
    <b-form-input class="form-control input" type="password" v-model="password" v-bind:class="{error:$v.password.$error,valid: $v.password.$dirty && !$v.password.$invalid }"/>   
    <div v-if="$v.password.$dirty">
      <p class="error-message" v-if="!$v.password.required">Password is required</p>
      <p class="error-message" v-if="!$v.password.minLength">Password Length is 8 letters above</p>
               </div>
    </b-form><br>
   <b-button @click="submit()">submit</b-button>

  
</div>
</template>
<script>
import NavBar from '~/components/NavBar.vue'
import { required,minLength,email,maxLength } from 'vuelidate/lib/validators'

export default {
    components:{
        NavBar
    },
     data() {
    return {
      userName:'',  
      email: '',
      password: '',
      submitStatus: null
    }
  },
   validations: {
    userName:{
        required
    },
    email: {
      required,
      email
    },
    password: {
      required,
      minLength: minLength(8)
    }
  },
   methods: {
    submit() {
      console.log('submit')
      this.$v.$touch()
      if (this.$v.$invalid) {
        this.submitStatus = 'ERROR'
      } else {
        // do your submit logic here
        this.submitStatus = 'PENDING'
        setTimeout(() => {
          this.submitStatus = 'OK'
        }, 500)
      }
    }
  }
}
</script>



  