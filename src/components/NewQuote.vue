<template>
  <div class="row">
    <form>
      <div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3">
        <label>Quote</label>
        <textarea></textarea>
      </div>
      <div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3">
        <button class="btn btn-primary" @click.prevent="createNew">Add Quote</button>
      </div>
    </form>
  </div>
</template>

<script>

export default {
  data: function() {
    return {
      quote: ''
    };
  },
  methods: {
    createNew() {
      //send to the parent component. quoteAdded is w.e name you want. This quote is binded with 2way binding.
      this.$emit('quoteAdded', this.quote);
      this.quote = '';
    }
  }
}
</script>

<style>
</style>
