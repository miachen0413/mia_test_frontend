<template>
  <div class="container">
    <table class="table">
      <thead>
      <tr>
        <th scope="col">id</th>
        <th scope="col">名字</th>
        <th scope="col">年齡</th>
        <th scope="col">操作</th>
      </tr>
      </thead>
      <tbody>
      <tr v-for="(v,i) in users" :key="`user_${i}`">
        <th scope="row">{{ v.id }}</th>
        <td>{{ v.name }}</td>
        <td>{{ v.age }}</td>
        <td class="d-flex gap-1">
          <button class="btn btn-success">修改</button>
          <button class="btn btn-danger">刪除</button>
        </td>
      </tr>
      </tbody>
    </table>

    <div>
<!--      <b-form-controls v-model="selectUser?.id"/>-->
<!--      <b-form-controls v-model="selectUser?.name"/>-->
<!--      <b-form-controls v-model="selectUser?.age"/>-->
    </div>
  </div>
</template>

<script setup lang="ts">
import axios from 'axios'
import {onMounted, ref} from 'vue';

interface User{
  id: number;
  name: string;
  age: number;
}

const users = ref<User[]>([])
const selectUser = ref<User>({
  id: 0,
  name: '',
  age: 0,
})

const baseUrl = ''

const setupPage = () => {
  axios({
    method: 'get',
    url: baseUrl + '/api/user',
  }).then(res => {
    const {data} = res.data
    users.value = data
  })
}

onMounted(setupPage)
</script>

<style scoped>

</style>