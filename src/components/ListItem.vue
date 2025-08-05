<script lang="ts" setup>
interface CheckBoxCheck {
  isChecked: boolean | false
}

defineProps<CheckBoxCheck>()
</script>

<template>
  <label :class="{ checked: isChecked }">
    <input type="checkbox" :checked="isChecked" />
    <slot></slot>
  </label>
</template>

<style scoped>
label {
  cursor: pointer;
}

.checked {
  text-decoration: line-through;
}
</style>
