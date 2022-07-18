<template>
  <hr />
  <input v-model="inputak" />
</template>

<script>
export default {
  name: 'Formik2',
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
