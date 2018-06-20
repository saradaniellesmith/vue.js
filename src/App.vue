<template>
  <div id="app">
   <h1> Hello</h1>
   <h2> Welcome to our Website {{ user.username }}! </h2>
   
    <div>
     Username: <input type="text" v-model="user.username"> <br>
     First Name: <input type="text" v-model="user.firstname"> <br>
     Last Name <input type="text" v-model="user.lastname"> <br>
    </div>

     <br>

     <div>
       Email: <input type="text" v-model="user.email"> 
       Password: <input type="text" v-model="user.password"> 
     </div>

     <p>
       Display Boolean value: {{myBoolean}}
     </p>

     <div>
       <button v-on:click="toggleBoolean">
         Show Paragraph
       </button>
     </div>

     <p v-if="myBoolean">
       Hello {{ user.firstname }}, you are now logged in as {{ user.username }}! 
       We are stoked to have you here - let's get started!
     </p>

 
  </div>
</template>

<script>
export default {
  data() {
    return {
      user : {
        username: '',
        firstname: '',
        lastname: '',
        email: '',
        password: ''
      },
      myBoolean: true
    }
  },
  methods: {
   toggleBoolean() {
     this.myBoolean = !this.myBoolean
    }
  }
}
</script>

<style>

#app {
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
  font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
}
</style>
