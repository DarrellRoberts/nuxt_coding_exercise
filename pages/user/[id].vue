<template>
  <article v-if=!pending>
    <h1>User profile: {{ user?.username }}</h1>
    <h3>Name: {{ user?.name }}</h3>
    <h3>Email: {{ user?.email }}</h3>
    <h3>Address:</h3>
    <ul>
      <li>Street: {{ user?.address?.street }}</li>
      <li>Suite: {{ user?.address?.suite }}</li>
      <li>City: {{ user?.address?.city }}</li>
      <li>Zipcode: {{ user?.address?.zipcode }}</li>
    </ul>
    <h3>Website: {{ user?.website}}</h3>
  </article>
  <article v-else>
    <h1>Loading...</h1>
  </article>
</template>

<script setup>
// Fetch user data
import { useLazyAsyncData, useRoute } from 'nuxt/app';

const route = useRoute();

const userId = route.params.id;

const { data: user, pending } = useLazyAsyncData(() => {
  try {
    return fetch(`https://jsonplaceholder.typicode.com/users/${userId}`).then((res) => res.json())
  } catch(error) {
    console.error(error);
  }
});
</script>