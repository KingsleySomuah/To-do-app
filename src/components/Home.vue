<template>
  <div class="container mx-auto mt-10 px-5 py-10">
    <form action="" class="flex items-center gap-3" @submit.prevent="addTask">
      <div class="p-5 ">
        <input type="text" placeholder="I need it"
          class="px-4 py-2 shadow-sm border border-gray-300 rounded-md placeholder-gray-400 " v-model="taskName">
      </div>
      <button type="submit"
        class="bg-yellow-200 text-black px-4 py-2 rounded-md shadow-sm hover:bg-yellow-400 transition-all">Add
        item</button>
    </form>

    <div class="justify-between flex">
      <div class="px-4 font-semibold text-gray-600">
        <p>You Have 2 Tasks to Complete</p>
      </div>
      <div class="mx-4 space-x-3">
        <button class="bg-green-300 px-3 py-1 rounded-md">All</button>
        <button class="bg-gray-600 px-3 py-1 rounded-md text-white">Favourite</button>
      </div>

    </div>

    <div class="flex justify-between items-center shadow-sm shadow-gray-400 px-3 py-3 mx-4 my-4" v-for="task in tasks"
      :key="task.id">
      <div>
        <p>{{ task.title }}</p>
      </div>
      <div class="flex gap-3">
        <i class="material-icons text-black cursor-pointer">edit</i>
        <i class="material-icons text-black cursor-pointer" @click="deleteTask(task.id)">delete</i>
        <i class="material-icons text-gray-300 cursor-pointer" :class="{ favourite: task.isFavourite === true }"
          @click="togglerFavourite(task.id)">favorite</i>
      </div>
    </div>
    <button type="submit" class="bg-orange-500 font-semibold rounded-md px-4 py-2 mx-4">Reset Tasks</button>




  </div>
</template>

<script setup>
import { ref } from 'vue';
const tasks = ref([
  { title: 'Eating', id: 1, isFavourite: false },
  { title: 'teaching', id: 2, isFavourite: false }
])

const taskName = ref('')

const addTask = () => {
  const data = {
    title: taskName.value,
    id: Math.floor(Math.random() * 1000) + 1,
    isFavourite: false
  }

  tasks.value.push(data)
  taskName.value = ''

}

const deleteTask = (id) => {
  if (window.confirm('Are you sure you want to delete')) {
    tasks.value = tasks.value.filter((task) => {
      return task.id != id
    })
  }
}

const togglerFavourite = (id) => {
  tasks.value.forEach((task) => {
    if (task.id === id) {
      task.isFavourite = !task.isFavourite
    }
  }

  )
}

















// const deleteTask = (id) => {
//   if (window.confirm("Are you sure you want to Delete?")) {
//     tasks.value = tasks.value.filter((task) => {
//       return task.id != id;
//     })
//   }
// }

// const togglerFavourite = (id) => {
//   tasks.value.forEach((task) => {
//     if (task.id === id) {
//       task.isFavourite = !task.isFavourite
//     }
//   })
// }


</script>

<style scoped>
.favourite {
  color: red
}
</style>
