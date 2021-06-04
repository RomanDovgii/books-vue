<template>
  <a class="logo">
    <p class="logo__heading">Мои Книги</p>
  </a>
</template>

<script>
export default {
  name: 'Logo',
};
</script>

<style lang="scss">
.logo {
  display: flex;
  align-items: center;
}

.logo__heading {
  color: #F4F1DE;
  font-size: 4rem;
  padding-top: 20px;
  padding-bottom: 20px;
  font-weight: 700;
}
</style>
