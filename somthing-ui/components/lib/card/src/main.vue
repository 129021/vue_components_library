<template>
  <div class="s-card" :style="width ? { width: width + 'px' } : {}">
    <div
      class="s-card-img"
      :style="imgHeight ? { height: imgHeight + 'px' } : {}"
    >
      <img :src="imgSrc" alt="img" />
    </div>
    <div v-if="summary" class="s-card-summary">
      {{ summary }}
    </div>
    <div v-else class="s-card-summary">
      <slot></slot>
    </div>
    <!-- footer插槽 -->
    <slot name="footer"></slot>
  </div>
</template>
 
<script>
export default {
  name: "Card",
  props: {
    width: {
      type: Number,
      default: 0,
    },
    imgSrc: {
      type: String,
      default: "",
    },
    imgHeight: {
      type: Number,
      default: 0,
    },
    summary: {
      type: String,
      default: "",
    },
  },
};
</script>