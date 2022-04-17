<template>
  <div id="home">
    <Header />

    <div class="container">
      <div class="col">
        <h3>Tasks</h3>
        <hr>
        <div v-for="lista in listas" :key="lista.id">
          <Tasks :lista="lista" />
        </div>
        <a href="/about" class="btn btn-success">
          Adicionar
        </a>
      </div>
    </div>
  </div>
</template>

<script>
import Header from '@/components/Header.vue';
import Tasks from '@/components/Tasks.vue';

export default {
  name: 'home-page',
  components: {
    Header,
    Tasks,
  },
  data() {
    return {
      listas: [
        {
          id: 1,
          name: 'testandooo ',
        },
        {
          id: 2,
          name: 'Viuva Negra',
        },
      ],
    };
  },
};
</script>
