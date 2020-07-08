<template>
  <div id="app">
    <h5 class="component-title">Input default</h5>
    <Input />
    <Input label="Label" />
    <Input label="Password" type="password" startIcon="https" />
    <Input label="Label" placeholder="Placeholder" value="Value text" />
    <Input label="Label" placeholder="Placeholder" helperText="Some text" />

    <h5 class="component-title">Input error</h5>
    <Input error />
    <Input error label="Label" />
    <Input error label="Label" placeholder="Placeholder" />
    <Input error label="Label" placeholder="Placeholder" helperText="Some text" />

    <h5 class="component-title">Input icon</h5>
    <Input startIcon="3d_rotation" />
    <Input label="Label" placeholder="Placeholder" startIcon="3d_rotation" />
    <Input label="Label" placeholder="Placeholder" endIcon="3d_rotation" />

    <h5 class="component-title">Input disabled</h5>
    <Input startIcon="3d_rotation" disabled />
    <Input error label="Label" disabled />

    <h5 class="component-title">Input sizes</h5>
    <Input label="Password" type="password" helperText="Some text" startIcon="https" size="sm" />
    <Input label="Text" type="text" helperText="Some text" size="md" />

    <h5 class="component-title">Input multiline</h5>
    <Input
      multiline
      row="4"
      helperText="Hello"
      placeholder="Placeholder"
      startIcon="3d_rotation"
      size="sm"
    />
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
