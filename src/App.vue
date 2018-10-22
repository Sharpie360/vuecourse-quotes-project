<template>
  <div class="container">
    <app-header></app-header>
    <app-quote-grid :quotes="quotes" @quoteDeleted="deleteQuote"></app-quote-grid>
    <app-new-quote @quoteAdded="addQuote"></app-new-quote>
    <div class="row">
      <div class="alert alert-info">
        Click on a Quote to delete it
      </div>
    </div>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import QuoteGrid from "./components/QuoteGrid.vue";
import NewQuote from "./components/NewQuote.vue";

import eventBus from "./main.js";

export default {
  data() {
    return {
      maxQuotes: 10,
      quotes: ["just a quote to see something"]
    };
  },
  components: {
    "app-header": Header,
    "app-quote-grid": QuoteGrid,
    "app-new-quote": NewQuote
  },
  methods: {
    addQuote(quote) {
      this.quotes.push(quote);
    },
    deleteQuote(i) {
      this.quotes.splice(i, 1);
    }
  }
};
</script>

<style>
</style>
