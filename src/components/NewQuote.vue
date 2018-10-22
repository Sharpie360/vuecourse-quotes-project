<template>
  <div class="row">
    <form class="form-group">
      <div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3">
        <label>Quote</label>
        <textarea class="form-control" rows="3" v-model="quote"></textarea>
      </div>
      <div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3">
        <button class="btn btn-success" @click.prevent="createNewQuote">Add New Quote</button>
      </div>
    </form>
  </div>
</template>

<script>
import eventBus from '../main.js'
export default {
  data() {
    return {
      quote: ""
    }
  },
  methods: {
    createNewQuote(){
      this.$emit('quoteAdded', this.quote)
      this.quote = ''
    }
  }
};
</script>
