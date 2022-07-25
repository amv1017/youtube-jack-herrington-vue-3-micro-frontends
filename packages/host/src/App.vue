<template>
  <div class="mt-10 text-3xl mx-auto max-w-6xl">
    <Header />
    <div class="mt-10">Count: {{count}}</div>
    <div>
      <button
        @click="addOne"
        class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded"
      >
        AddOne
      </button>
    </div>
  </div>
</template>

<script>
import Header from "remote/Header"
export default {
  components: {
    Header
  },
  computed: {
    count() {
      return this.$store.state.count
    }
  },
  methods: {
    addOne() {
      this.$store.commit('addOne')
    }
  }
}
</script>
