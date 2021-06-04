<template>
  <header class="header">
    <div class="header__wr">
      <Logo/>
    </div>
  </header>
</template>

<script>
import Logo from './Logo.vue';

export default {
  name: 'Header',
  components: {
    Logo,
  },
};
</script>

<style lang="scss">
.header {
  background-color: #F2CC8F;

  display: flex;
  justify-content: center;

  min-height: 50px;
}

.header__wr {
  max-width: 1440px;
  width: 100%;
  display: flex;
  align-items: center;
}
</style>
