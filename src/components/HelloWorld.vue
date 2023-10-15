<template>
  <div>
    <form action="" :class="form_values.age == '0' ? 'my_border' : ''">
      <label for="name">Name</label>
      <input type="text" name="" id="name" v-model="form_values.name">
      <label for="age">Age</label>
      <input type="text" name="" id="age" v-model="form_values.age">
      <button @click="show_data($event)">Display values</button>
    </form>
    <div v-show="form_values.age == 8">
      <h2>cart</h2>
    </div>
    <div v-if="form_values.age == 0">
      <h2>Basket</h2>
    </div>
  </div>
</template>

<script>
export default {
  name: 'abcdM',
  props: {
    msg: String
  },
  data(){
    return {
      form_values: {
        name: '',
        age: 0
      }
    }
  },
  methods: {
    show_data(event){
      event.preventDefault();
      console.log(this.form_values);
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.my_border{
  border: 1px solid red;
}
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
