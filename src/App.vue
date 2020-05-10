<template>
  <div class="container">
    <NewQuote @quoteAdded="newQuote"></NewQuote>
    <QuoteGrid :quotes="quotes"></QuoteGrid>
    <div class="row">
      <div class="col-sm-12 text-center">
        <div class="alert alert-info">Info: Click on a Quote to delete it!</div>
      </div>
    </div>
  </div>
</template>

<script>
import QuoteGrid from "./components/QuoteGrid";
import NewQuote from "./components/NewQuote";
export default {
  data() {
    return {
      quotes: ["Just a quote to see something"],
      maxQuotes: 10
    };
  },
  methods: {
    newQuote(quote) {
      this.quotes.push(quote);
    }
  },
  components: {
    QuoteGrid,
    NewQuote
  }
};
</script>

<style></style>
