<template>
  <div>
    <div class="card">
      <div id="card-header">
        <slot name="header"></slot>
      </div>

      <div id="card-content">
        <slot>Default content</slot>
      </div>

      <div id="card-footer">
        <slot name="footer"></slot>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "CardVue",
};
</script>

<style>
.card {
  border: 1px solid black;
  padding: 10px;
  margin: 10px;
  width: 200px;
}
</style>
