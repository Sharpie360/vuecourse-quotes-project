<template>
  <div class="col-sm-6 col-md-4 col-lg-3">
    <div class="card">
      <div class="card-body quote">
        <slot></slot>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
.card-body {
  font-family: Cursive;
  font-size: 24px;
  padding: 0.5rem 1rem;
}
.quote {
  cursor: pointer;
}
.quote:hover {
  background-color: rgba(40, 213, 200, 0.3);
}
</style>
