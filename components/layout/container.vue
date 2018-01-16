<template>
  <section :class="$style.container">
    <slot></slot>
  </section>
</template>

<style lang="scss" module>
  .container {
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    flex-wrap: wrap;
    flex-direction: column;
    margin: 50px 0;
  }
</style>
