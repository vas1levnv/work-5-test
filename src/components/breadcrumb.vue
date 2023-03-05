<template>
  <nav class="mt-3" style="--bs-breadcrumb-divider: '>';" aria-label="breadcrumb">
    <ol class="breadcrumb">
      <li class="breadcrumb-item"><a href="#">Главная</a></li>
      <li class="breadcrumb-item active" aria-current="page">Мои магазины</li>
    </ol>
  </nav>
</template>

<script>
export default {
  name: "bread-crumb"
}
</script>

<style scoped>
.breadcrumb-item a{
  color: #7D7D7D;
  text-decoration: none;
}
</style>