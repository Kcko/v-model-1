<template>
  <!-- 1 zpusob -->
  <input
    type="text"
    :value="modelValue"
    @input="$emit('update:modelValue', $event.target.value)"
  />
  <!-- 2 zpusob -->
  <input v-model="inputak" />

  <br />Data z child {{ modelValue }}

  <Formik2 v-model="inputak" />
</template>

<script>
import Formik2 from './Formik2.vue';

export default {
  name: 'Formik',
  components: {
    Formik2,
  },
  props: ['modelValue'],
  data() {
    return {};
  },
  computed: {
    inputak: {
      get() {
        return this.modelValue;
      },
      set() {
        this.$emit('update:modelValue', event.target.value);
      },
    },
  },
};
</script>
