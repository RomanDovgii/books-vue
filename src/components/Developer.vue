<template>
  <div
    class="developer"
    :class="isDark ? `developer--dark`: ``"
  >
    <h3 class="developer__name">Довгий Роман Олегович</h3>
    <p class="developer__date">06-04-2021</p>
    <p class="developer__group">201-321</p>
  </div>
</template>

<script>
export default {
  name: 'Developer',
  props: {
    isDark: {
      type: Boolean,
    },
  },
};
</script>

<style lang="scss">
.developer {
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding-top: 10px;
  padding-bottom: 10px;
}

.developer :where(h3, p) {
  color: #3D405B;
  transition: color 0.3s;
}

.developer--dark :where(h3, p) {
  color: #F4F1DE;
}

.developer__name {
  font-size: 3rem;
}

.developer p {
  font-size: 2rem;
}
</style>
