<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <div>
    <h1>Parent Component</h1>
    <p>Message from Child A: {{ messageFromChildA }}</p>
    <ChildComponentA
      @message-from-childA="handleMessageFromChildA"
      message="Hello From Parent"
    />
    <ChildComponentB
      @message-from-child="handleMessageFromChildB"
      :messageFromSibling="messageFromChildA"
    />
  </div>
</template>

<script>
import ChildComponentA from "./ChildComponentA.vue";
import ChildComponentB from "./ChildComponentB.vue";

export default {
  components: {
    ChildComponentA,
    ChildComponentB,
  },
  data() {
    return {
      messageFromParent: "Hello From Parent",
      messageFromChildA: "",
    };
  },
  methods: {
    handleMessageFromChildA(message) {
      this.messageFromChildA = message;
    },
    handleMessageFromChildB(message) {
      this.messageFromChildB = message;
    },
  },
};
</script>
