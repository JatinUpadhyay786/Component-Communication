<template>
  <div>
    <h2>Child Component A</h2>
    <p>Message From Parent: {{ message }}</p>
    <button @click="sendMessageToParent">Send Message to Parent</button>
  </div>
</template>

<script>
export default {
  props: ["message"],
  methods: {
    sendMessageToParent() {
      this.$emit("message-from-childA", "Hello from Child A!");
    },
  },
};
</script>
