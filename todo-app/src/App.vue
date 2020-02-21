<template>
  <div id="app">
    <TodoHeader></TodoHeader>
    <TodoInput></TodoInput>
    <TodoList></TodoList>
    <TodoFooter></TodoFooter>
  </div>
</template>

<script>
  import TodoHeader from './components/TodoHeader';
  import TodoFooter from './components/TodoFooter';
  import TodoInput from './components/TodoInput';
  import TodoList from './components/TodoList';

  export default {
    components: {
      'TodoHeader': TodoHeader,
      'TodoFooter': TodoFooter,
      'TodoInput': TodoInput,
      'TodoList': TodoList
    }
  }
</script>

<style>
</style>
