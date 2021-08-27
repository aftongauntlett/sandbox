<template>
    <ul class="skip-links">
        <li>
            <a href="#main" ref="skipLink" class="skip-link">Skip to main content</a>
        </li>
    </ul>
</template>

<script>
export default {
  watch: {
    $route() {
      this.$refs.skipLink.focus();
    }
  }
};
</script>

<style scoped lang="css">
.skip-link {
  white-space: nowrap;
  margin: 1em auto;
  top: 0;
  position: fixed;
  left: 50%;
  margin-left: -72px;
  opacity: 0;
  z-index: 1000;
}
.skip-link:focus {
  opacity: 1;
  background-color: white;
  padding: .5em;
  border: 1px solid black;
}
</style>