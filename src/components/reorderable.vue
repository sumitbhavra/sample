<template>
  <div>
    <div>
      <ul>
        <li v-for="(item, idx) in data" :key="idx" @click="reorder(item)">
          {{ item }}
        </li>
      </ul>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      data: this.items || [],
    };
  },
  props: {
    items: {
      required: true,
      type: Array,
    },
  },
  methods: {
    reorder(i) {
      const idx = this.data.indexOf(i);
      console.log('reorder -> idx', idx);
      if (idx !== 0) {
        const temp = this.data[0];
        this.data[0] = this.data[idx];
        this.data[idx] = temp;
      }
      this.data = this.data.slice();
    },
  },
};
</script>
