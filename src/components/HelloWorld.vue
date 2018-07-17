<template>
<ul>
<li >
  {{ todos.ok }}
</li>
</ul>
</template>

<script>

export default {
  name: 'HelloWorld',
  props: {
    msg: String,
    ok: String
  },
  data() {
            return {
                todos: []
            }
        },
        created: function() { // get todo items and start listening to events once component is created
            this.fetchTodo();
        },
        methods: {
            fetchTodo() {
                let uri = 'http://localhost:8000/api';
                this.$http.get(uri).then(response => {

                  console.log(response.body);
                  this.todos = response.body;

                });

            }
        }
    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
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
