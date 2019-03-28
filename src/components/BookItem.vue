<template>
  <li>
    {{book.title}} : {{book.author}}
    <span v-if="book.finishedReading">- Read</span>
    <span v-else>- Not Read</span>
    <span v-if="book.ownership === 'borrowed'">- Borrowed</span>
    <span v-else>- Bought</span>
  </li>
</template>

<script>
export default {
  name: 'BookItem',
  props: ['book'],
};
</script>

<style>
li {
  display: block;
  margin: 0 10px;
}
</style>