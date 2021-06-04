<template>
  <footer class="footer">
    <div class="footer__wr">
      <Developer/>
      <Logo/>
    </div>
  </footer>
</template>

<script>
import Logo from './Logo.vue';
import Developer from './Developer.vue';

export default {
  name: 'Footer',
  components: {
    Logo,
    Developer,
  },
};
</script>

<style lang="scss">
.footer {
  background-color: #F2CC8F;

  display: flex;
  justify-content: center;

  min-height: 50px;
}

.footer__wr {
  max-width: 1440px;
  width: 100%;
  display: flex;
  justify-content: space-between;
}
</style>
