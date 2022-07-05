<template>
  <div class="hello">

    <h1>{{ msg }}</h1>

    <h2>Net-Ninja Project</h2>

  </div>
  <div id="app">

    <div v-if="showBooks">
    <p>{{title}} - {{author}} - {{age}}</p>

    </div>
    <button @click="toggleShowBooks">
    <span v-if="showBooks">Gizle</span>
    <span v-else>Göster</span>

    </button>
    <div v-show="showBooks">Şuan Gösteriliyor</div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String,
  },
  data() {
    return {
      showBooks: true,
      title: 'Never Say Never',
      author: 'Tom Cruise',
      age: 25,
    };
  },
  methods: {
    toggleShowBooks() {
      this.showBooks = !this.showBooks;
    },

  },
};

</script>
