<template>
  <div>
    <form action="" :class="form_values.age == '0' ? 'my_border' : ''">
      <label for="name">Name</label><br>
      <input type="text" name="" id="name" v-model="form_values.name"><br>
      <label for="age">Age</label><br>
      <input type="text" name="" id="age" v-model="form_values.age"><br>
      <label for="choices">Choices</label><br>
      <select name="" id="choices" multiple v-model="form_values.choices">
        <option value="car">car</option>
        <option value="a">a</option>
        <option value="b">b</option>
        <option value="c">c</option>
      </select>
      <h2 v-for="(name, ind) in form_values.choices" :key="name">{{ ind + 1 }} {{ name }}</h2>
      <button @click="show_data($event)">Display values</button>
      <h2 v-for="(obj, ind) in my_objs" :key="obj">{{ ind + 1 }} {{ obj.name }}</h2>

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
        age: 0,
        choices: []
      },
      my_objs: [
        {name: 'Foster', age: 21},
        {name: 'Asante', age: 3},
        {name: 'Amponsah', age: 90}
      ]
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
