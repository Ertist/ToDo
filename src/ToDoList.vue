<template>
 <div>
   <h1>todolist</h1>
   <input type="text" v-model="listMsg" />
   <button @click = "addList">add</button>
   <ul>
       <todo-item v-for="(item, index) of list" :key="index" :content="item" :index="index" @itemDelete="deleteList"></todo-item>
   </ul>
 </div>
</template>

<script>
import listItem from './components/listItem.vue'
export default {
  components: {
    'todo-item': listItem
  },
  data () {
    return {
      listMsg: '',
      list: []
    }
  },
  methods: {
    addList: function () {
      this.list.push(this.listMsg)
      this.listMsg = ''
    },
    deleteList: function (index) {
      this.list.splice(index, 1)
    }
  }
}
</script>

<style>

</style>
