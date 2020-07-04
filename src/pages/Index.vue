<template>
  <q-page class="flex flex-center">
     <q-card flat bordered class="my-card text-center">
      <q-card-section>
       <q-input outlined v-model="text" label="Email or Phone Number" />
      <q-input outlined v-model="text" label="Password" class="q-mt-sm" />
       <q-btn color="blue-10" label="Login" class="q-mt-sm full-width" no-caps />
       <a href="#" style="font-size:10px;text-decoration:none">Forgot account?</a>
      </q-card-section>

      <q-separator inset />

      <q-card-section>
<q-btn color="green-7" label="Create New Account" style="padding:0" no-caps></q-btn>
      </q-card-section>
    </q-card>
  </q-page>
</template>

<script>
export default {
  name: 'PageIndex'
}
</script>

<style>
</style>
