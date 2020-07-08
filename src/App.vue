<template>
  <div id="app">
    <Input
      helperText="Hello"
      type="password"
      placeholder="Placeholder"
      startIcon="3d_rotation"
      size="sm"
    />
    <Input
      multiline
      row="4"
      helperText="Hello"
      type="password"
      placeholder="Placeholder"
      startIcon="3d_rotation"
      size="sm"
    />
    <Input error label="Hello" endIcon="3d_rotation" placeholder="Placeholder" value="123" />
    <Input disabled />

    {{val}}
  </div>
</template>

<script>
import Input from '@/components/Input.vue';

export default {
  name: 'App',
  components: {
    Input,
  },
};
</script>

<style lang="scss">
  body {
    background-color: white;
    color: black;
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI",
                  Roboto, Helvetica, Arial, sans-serif, "Apple Color Emoji",
                  "Segoe UI Emoji", "Segoe UI Symbol";
  }

  .component-title {
    font-size: 2em;
  }
</style>
