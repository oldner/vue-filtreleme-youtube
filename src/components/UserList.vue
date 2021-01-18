<template>
  <div>
    <input type="text" @input="sendData" />
    <Card>
      <p v-for="i in filteredList" :key="i">{{ i }}</p>
    </Card>
  </div>
</template>

<script>
import Card from "./Card.vue";
export default {
  props: {
    list: Array,
  },
  components: { Card },
  data() {
    return {
      filteredList: this.list,
    };
  },
  methods: {
    sendData(e) {
      this.filteredList = this.list.filter((item) =>
        item.startsWith(e.target.value)
      );
    },
  },
};
</script>

<style>
</style>