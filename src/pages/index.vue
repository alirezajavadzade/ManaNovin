<template>
  <v-container>
    <v-row v-if="loading == false">
      <v-col cols="12" md="4" lg="3" v-for="(item, i) in User" :key="i">
        <DialogComponent :user="item"/>
      </v-col>
    </v-row>
    <v-row v-else>
      <v-col>
        <div class="text-center">
          <v-progress-circular color="#000" indeterminate></v-progress-circular>
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>

<script lang="ts" setup>

import { ref, onMounted } from 'vue';
import DialogComponent from '../components/DialogComponent.vue';

interface UserItem {
  id: number;
  login: string;
}

const User = ref<UserItem[]>([]);
const loading = ref<boolean>(false);



async function FetchData() {
  loading.value = true;
  try {
    const response = await fetch('https://api.github.com/users');
    if (!response.ok) {
      console.log('error')
    }
    const data = await response.json();
    User.value = data.filter((item: UserItem) => item.id < 15).map((item: UserItem) => ({ id: item.id, login: item.login }));
  } catch (error) {
    console.log(error);
  }
  loading.value = false;
}

onMounted(() => {
  FetchData();
});

</script>

<style>
.modal-btn {
  min-height: 6rem;
}
</style>
