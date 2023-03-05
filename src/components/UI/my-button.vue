<template>
  <button type="button" class="btn d-flex align-items-center" :class="classBtn" :style="style">
    <slot></slot>
  </button>
</template>

<script>
export default {
  name: "my-button",
  props: {classBtn: String, colorBtn: String, hoverColorBtn: String},
  data() {
    return {
      style: {
        '--color': this.colorBtn,
        '--hovercolor': this.hoverColorBtn,
      }
    }
  }
}
</script>

<style scoped>
button {
  background: var(--color);
  border-color: var(--color);
  font-size: 0.875rem;
}

button:hover {
  background: var(--hovercolor);
  border-color: var(--hovercolor);
}
</style>