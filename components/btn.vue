<template>
  <button class="button" :class="[color]"><slot /></button>
</template>

<script>
export default {
  name: 'btn',
  props: {
    color: {
      type: String,
      default: 'white',
      validator(value) {
        return ['white', 'black'].includes(value)
      },
    },
  },
}
</script>

<style lang="scss" scoped>
.button {
  background: transparent;
  font-size: 18px;
  border-radius: 5px;
  padding: 16px;
  border: 2px solid white;
  outline: 0;
  text-decoration: none;
  cursor: pointer;
  white-space: nowrap;
  font-weight: bold;
  width: fit-content;
  height: fit-content;
  box-sizing: border-box;

  &.white {
    color: white;
    border-color: white;
  }

  &.black {
    color: black;
    border-color: black;
  }

  &:hover {
    color: #5fbfae;
    border-color: #5fbfae;
  }

  &:active {
    color: #468d80;
    border-color: #468d80;
  }
}
</style>
