<template>
  <div>
    <div class="header">
      <span v-if="open" @click="open = !open">Collapse</span>
      <span v-if="!open" @click="open = !open">Expend</span>
    </div>
    <slot v-if="open">
      <div>Default content</div>
    </slot>
  </div>
</template>
<script>
export default {
  name: 'CllapsibleSection',
  data() {
    return {
      open: true,
    };
  },
};
</script>
<style lang="scss" scoped>
.header {
  background-color: grey;
  padding: 3px;
  cursor: pointer;
}
</style>
