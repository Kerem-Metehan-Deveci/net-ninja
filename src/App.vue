<template>
  <div class="app">
    <h1>Kerem'in Listesi </h1>

    <v-input
      v-model="searchText"
      name="search"
      placeholder="Arama Yapin..."
    />

    <v-list :items="filteredItems"/>
  </div>
</template>

<script>
import VTest from "@/components/VTest.vue";
import VInput from "@/components/VInput.vue";
import VList from "@/components/VList.vue";

export default {
  name: 'App',
  components: {
    VInput,
    VList,
  },
  data() {
    return {
      searchText: '',
      list: [
        "Muz",
        "Elma",
        "Armut",
        "Karpuz"
      ]
    };
  },
  computed: {
    filteredItems() {
      return this.list.filter((item) => item.includes(this.searchText));
    }
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.app {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}

app h1 {
  margin-bottom: 12px;
}

.list {
  list-style-type: none;
}

.list li {
  padding: 8px;
  font-weight: bold;
}
</style>
