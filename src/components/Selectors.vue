<template>
  <section class="selectors">
    <div class="selectors__wr">
      <h2 class="selectors__heading">Сортировка по жанрам:</h2>
      <ul class="selectors__list">
        <li class="selectors__el">
          <Selector/>
        </li>
      </ul>
    </div>
  </section>
</template>

<script>
import Selector from './Selector.vue';

export default {
  name: 'Selectors',
  components: {
    Selector,
  },
};
</script>

<style lang="scss">
.selectors {
  background-color: rgba(#E07A5F, 1.0);
  display: flex;
  justify-content: center;
  padding-top: 20px;
  padding-bottom: 20px;
}

.selectors__wr {
  max-width: 1440px;
  width: 100%;
  display: flex;
  align-items: center;
}

.selectors__heading {
  font-size: 3rem;
  color: #F4F1DE;
  font-weight: 300;
}

.selectors__list {
  list-style: none;
  align-self: flex-end;
}
</style>
