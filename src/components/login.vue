<template>
  <div class="login-page">
    <div class="login-wrapper">
      <div class="kutia">
        <div class="emri-wrapper">
          <div class="svg-holder">
            <svg version="1.0" id="Layer_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
             viewBox="0 0 300 300" enable-background="new 0 0 300 300" xml:space="preserve" >
            <path fill="#707487" d="M262.7,243.2v50.4c0,3.6-2.9,6.5-6.5,6.5H43.8c-3.6,0-6.5-2.9-6.5-6.5v-50.4c0-50.2,33.3-93.1,78.9-107.5
              c-22.8-12.2-38.5-35.8-38.5-63.4c0-41.2,34.4-74.2,76-72.1c36.4,1.9,66,31.1,68.3,67.5c1.9,29.6-14.3,55.3-38.3,68.1
              C229.4,150.1,262.7,192.9,262.7,243.2z"/>
          </svg>
          </div>
         <input type="text" placeholder="Username" v-model="message">
          <span class="form-group__message" v-if="$v.message.$error">Field is required</span>
        </div>
        <div class="emri-wrapper">
          <div class="svg-holder">
            <svg version="1.0" id="Layer_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
             viewBox="0 0 300 300" enable-background="new 0 0 300 300" xml:space="preserve">
          <path fill="#707487" d="M244.5,99.2h-18.3V76.3C226.3,34.3,192,0,149.9,0c-42.1,0-76.3,34.3-76.3,76.3v22.9H55.3
            c-14.3,0-26,11.7-26,25.9v148.6c0,14.5,11.7,26.2,26,26.2h189.3c14.5,0,26.3-11.7,26.3-26.2V125.2C270.8,110.9,259,99.2,244.5,99.2z
             M108.1,76.3c0-23,18.8-41.8,41.8-41.8c23.1,0,41.8,18.8,41.8,41.8v22.9h-83.7V76.3z M164,231.2v37.9c0,1.6-1.4,2.8-3,2.8h-18.2
            c-1.4,0-2.7-1.2-2.7-2.8v-37.9c-12.4-4.8-21.4-16.8-21.4-31.1c0-18.4,14.9-33.3,33.4-33.3c18.4,0,33.3,14.9,33.3,33.3
            C185.4,214.4,176.4,226.4,164,231.2z"/>
          </svg>
          </div>
          <input type="password" placeholder="Password" v-model="password">
        </div>
        <button @click="login" >LOGIN</button>
      </div>
      <div class=" footer-wrapper">
        <div class="footer">
          <input type="checkbox"  checked>
        </div>
        <div class="kujtome">
          <h6> REMEMBER ME </h6>
        </div>
        <h6> FORGOT PASSWORD? </h6>
      </div>
    </div>
  </div>
</template>

<script type="text/babel">
  import { required } from 'vuelidate/lib/validators'
  export default {
    data () {
      return {
        message: '',
        password: ''
      }
    },
    methods: {
      login () {
        this.$v.message.$touch()
        // setTimeout(() => {
        //   this.$router.push({name: 'dashboard'})
        // }, 300)
        console.log(this.$v.message)
      }
    },
    validations: {
      message: {
        required
      }
    }
  }
</script>
