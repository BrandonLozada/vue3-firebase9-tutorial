<template>
  <div class="brand-todo">
    <div class="title has-text-centered">Brand Todo</div>

    <div class="field is-grouped mb-5">
      <p class="control is-expanded">
        <input class="input" type="text" placeholder="Add a todo" />
      </p>
      <p class="control">
        <a class="button is-info"> Add </a>
      </p>
    </div>

    <div v-for="todo in todos" class="card mb-5">
      <div class="card-content">
        <div class="content">
          <div class="columns is-mobile is-vcentered">
            <div class="column">
              {{ todo.content }}
            </div>
            <div class="column is-5 has-text-right">
              <button class="button is-light">&check;</button>
              <button class="button is-danger ml-2">&cross;</button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
/*
  imports
*/
import { ref } from "vue";

/*
  todos
*/
const todos = ref([
  {
    id: "id1",
    content: "Resurar mi trasero",
    done: false,
  },
  {
    id: "id2",
    content: "Rasurar la barba",
    done: false,
  }
]);
</script>

<style>
@import "node_modules\bulma\css\bulma.min.css";

.brand-todo {
  max-width: 400px;
  padding: 20px;
  margin: 0 auto;
}
</style>
