<template>
  <q-page class="flex flex-center">
     <q-card class="my-card">
      <q-card-section>
        <div class="row">
         <q-input filled v-model="User.Name" label="Name" />
          <q-input filled v-model="User.Surname" label="Surname" class="q-ml-sm"/>
          </div>
           <q-input filled v-model="User.Email" label="E-mail" class="q-mt-md"/>
           <q-input filled v-model="User.Confirm_Email" label="Confirm E-mail" class="q-mt-xs"/>
            <q-input filled v-model="User.Password" label="Password" class="q-mt-md" type="password"/>
             <q-input filled v-model="User.Confirm_Password" label="Confirm Password" class="q-mt-xs" type="password" />
              <q-btn color="green-8" v-on:click="register" text-color="white" label="Register" class="q-mt-md full-width"  />
      </q-card-section>
    </q-card>

      </q-page>
</template>
<script>
export default {
  name: 'register',
  data () {
    return {
      User: {
        Name: '',
        Surname: '',
        Email: '',
        Confirm_Email: '',
        Password: '',
        Confirm_Password: ''
      }
    }
  },
  methods: {
    register () {
      this.$axios.post('https://reqres.in/api/users', this.User)
        .then(response => {
          console.log(response)
        })
    }
  }

}
</script>

<style>
</style>
