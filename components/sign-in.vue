<template>
  <div class="flex flex-col justify-center items-center h-screen text-[#333]">
    <NuxtLink to="/" class="rounded-full p-3 bg-white/20 hover:bg-white/50">
      <Icon class="text-[24px]" name="uil:home" />
    </NuxtLink> 

    <h2 class="text-[40px] tracking-[2px]">Welcome</h2>
    <h4 class="text-[18px] font-light mb-10">Sign in/Log in</h4>
    <br />
      <label for="email">Enter email</label>
      <input
        v-model="login.email"
        type="email"
        placeholder="abc@gmaii.com"
        class="custom-input bg-black/50 backdrop-blur-md"
      />
      <label for="password">Enter password</label>
      <input
        v-model="login.password"
        type="password"
        placeholder="*********"
        class="custom-input bg-black/50 backdrop-blur-md"
      />
      <div class="text-[11px]">
        Don't have an account with us -
        <NuxtLink to="/signUpPage">
          <span class="underline">Go back to sign up</span>
        </NuxtLink>
      </div>
      <br />

      <button @click="submitBtn" class="login-btn">continue</button>
  </div>
</template>

<script>
export default ({
    data() {
       return{
        login:{
            email: '',
            password: '',
        }
       } 
    },
    methods: {
      submitBtn(){
         if (this.login.email.trim() === 'renelanglois43@yahoo.ca' && this.login.password.trim() === 'renelangentry123') {
          this.$router.push("/dashboard")
         console.log('here')
        } else {
           alert('Incorrect Details')
        } 
      }
    }
})
</script>


<style>
label {
  font-weight: 600;
  font-size: 12px;
  text-align: center;
}
</style>