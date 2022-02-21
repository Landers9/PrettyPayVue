<template>
  <div class="login">
    <FormLogin/>
  </div>
</template>

<script>
// @ is an alias to /src
import FormLogin from '@/components/FormLogin.vue'

export default {
  name: 'Login',
  components: {
    FormLogin
  }
}
</script>
