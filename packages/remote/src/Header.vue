<template>
  <div class="text-3xl bg-blue-900 text-white p-5 flex">
    <div class="font-bold flex-grow">
      Header
    </div>
    <div>{{count}}</div>
  </div>
</template>

<script>
export default {
  computed: {
    count() {
      return this.$store?.state?.count ?? 0
    }
  }
}
</script>
