<template>
  <div>
    <h2>Child Component B</h2>
    <p>Message from Child A: {{ messageFromSibling }}</p>
  </div>
</template>

<script>
export default {
  props: ["messageFromSibling"],
};
</script>
