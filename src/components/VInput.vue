<template>
    <input
      :value="modelValue"
      name="search"
      placeholder="Arama Yapin..."
      @input="onInput"
    />
</template>

<script>
  export default {
    name: 'VInput',
    props: {
      modelValue: {
        type: String,
        default: '',
      },
    },
    methods: {
      onInput(event) {
        const { value } = event.target;

        this.$emit('update:modelValue', value);
      }
    }
  }
</script>