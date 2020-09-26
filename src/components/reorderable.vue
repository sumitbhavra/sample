<template>
  <div>
    <div>
      <ul>
        <li v-for="(item,idx) in items" :key="idx" @click="reorder(item)">
          {{ item }}
        </li>
      </ul>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    items: {
      required: true,
      type: Array,
    },
  },
  methods: {
    reorder(i) {
      const idx = this.items.indexOf(i);
      if (idx !== 0) {
        const temp = this.items[0];
        this.items[0] = this.items[idx];
        this.items[idx] = temp;
      }

      console.log(this.items);
    },
  },
};
</script>
