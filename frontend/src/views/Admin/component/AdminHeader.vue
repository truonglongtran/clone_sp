<template>
  <header class="bg-white shadow p-4 flex justify-between items-center w-full">
    <h1 class="text-xl font-bold">Bảng điều khiển Admin</h1>
    <div>{{ currentRole }}</div>
  </header>
</template>

<script>
export default {
  name: 'AdminHeader',
  computed: {
    currentRole() {
      const role = localStorage.getItem('role') || 'Unknown';
      return role.charAt(0).toUpperCase() + role.slice(1);
    },
  },
};
</script>
  