<script>
export default {
  name: 'Test',
  data () {
    return {
      titulo: 'Welcome to Your Vue.js App',
      user: {
        firstName: 'John',
        lastName: 'Doe'
      },
      myhtml: '<h3>una etiquera</h3>',
      showName: true,
      tasks: [
        {title: 'comer'},
        {title: 'dormir'}
      ]
    }
  },
  methods: {
    saludar(name) {
        alert('hello! ' + name);
    },
    tipedEnter(e){
        alert('enter!');
    }
  },
  computed: {
    fullName(){
      return this.user.firstName + ' ' + this.user.lastName;  
    }
  },
  props: {
    msg: {
      type: String,
      default: 'Mensaje por defecto'

    }
  }
}
</script>

<template>
    <div>
        <span v-html="myhtml"></span>
        <div v-if="showName">
            <p>{{ user.firstName }}&nbsp;{{ user.lastName }}</p>
        </div>
        <div v-else="showName">
            <p>No puedo mostrar el nombre</p>
        </div>
        <hr>
        <ul>
            <li v-for="task in tasks">
                {{ task.title }}
            </li>
        </ul>
        <hr>
        <input type="text" v-on:keyup.enter="tipedEnter">
        <input type="text" v-model="user.firstName">
        <button type="button" v-on:click="saludar(user.firstName)">
            CLICK ME
        </button>
        <hr>
        <p>{{ fullName }}</p>
        <hr>
        <p><strong>{{ msg }}</strong></p>
    </div>
</template>


<style>
</style>