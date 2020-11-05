<template>
    <div class="sign-up">
        <h1>Crie uma nova conta</h1>
        <input 
          type="text" 
          placeholder="Email"
          v-model="email"
        />
        <br/>
        <input
          type="password" 
          placeholder="Password"
          v-model="password"
        />
        <br/>
        <div>
            <button @click="signUp">Registrar</button>
        </div>
       <span>
           ou retorne ao 
           <router-link to="/login">login.</router-link>
       </span>
    </div>
</template>

<script>
import  firebase from "firebase";

export default {
    name: "signup",
    data(){
        return {
          email: '',
          password: ''
        };
    },
    methods: {
      signUp(){
        firebase.auth().createUserWithEmailAndPassword(this.email, this.password).then(
          (user) => {
            this.$router.replace('/');
          },
          (err) =>{
            alert('Aconteceu algo inesperado.' + err.message);
          }
        )
      }
    }
}
</script>

<style scoped>
.sign-up {
  margin-top: 40px;
}
input {
  margin: 10px 0;
  width: 20%;
  padding: 15px;
}
button {
  font-family: "Roboto", sans-serif;
  text-transform: uppercase;
  outline: 0;
  background: #1606f3;
  border: 0;
  padding: 15px;
  color: #ffffff;
  font-size: 14px;
  -webkit-transition: all 0.3 ease;
  transition: all 0.3 ease;
  cursor: pointer;
}
span {
  display: block;
  margin-top: 20px;
  font-size: 11px;
}
</style>