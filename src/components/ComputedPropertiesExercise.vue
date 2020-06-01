<template>
  <div class="computed-properties-exercise container">
    <div class="row">
      <div class="col-12">
        <div class="border p-1">
          <div class="reverse-message">
            <p>Original Message: {{ message }}</p>
            <p>Computed Reversed Message: {{ reversedMessage }}</p>
            <p>Comuter All Caps Message: {{ allCapsMessage }}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "computed-properties-exercise",
  data() {
    return {
      message: "Hello World!",
    };
  },
  computed: {
    reversedMessage() {
      return this.message
        .split("")
        .reverse()
        .join("");
    },
    allCapsMessage() {
      return this.message.toUpperCase();
    },
  },
};
</script>

<style scoped></style>
