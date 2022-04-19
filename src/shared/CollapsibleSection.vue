<template>
    <div>
        <div class="header">
            <span v-if="open" @click="open = !open" @keydown="bar">&#x25B2; Collapse</span>
            <span v-if="!open" @click="open = !open" @keydown="bar">&#x25BC; Expand</span>
        </div>
        <slot v-if="open">
            <div>DefaultContent</div>
        </slot>
    </div>
</template>

<script>
export default {
  name: 'CollapsibleSection',
  data() {
    return {
      open: true,
    };
  },
};
</script>

<style scoped>
.header {
    background-color: gray;
    padding: 3px;
    cursor: pointer;
}
</style>
