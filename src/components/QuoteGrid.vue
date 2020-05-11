<template>
  <div class="row">
    <Quote
      v-for="(quote, index) in quotes"
      :key="quote"
      @click.native="deleteQuote(index)"
      >{{ quote }}</Quote
    >
  </div>
</template>

<script>
import Quote from "./Quote";

export default {
  props: ["quotes"],
  methods: {
    deleteQuote(index) {
      this.$emit("quoteDeleted", index);
    }
  },
  components: { Quote }
};
</script>

<style></style>
