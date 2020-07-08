<script>
import './_Input.scss';

export default {
  name: 'Input',
  props: {
    error: {
      type: Boolean,
      default: false,
    },
    disabled: {
      type: Boolean,
      default: false,
    },
    readonly: {
      type: Boolean,
      default: false,
    },
    multiline: {
      type: Boolean,
      default: false,
    },
    row: {
      type: String,
      default: '2',
    },
    size: {
      type: String,
      validator(value) {
        return ['sm', 'md'].includes(value);
      },
    },
    label: {
      type: String,
    },
    placeholder: {
      type: String,
    },
    helperText: {
      type: String,
    },
    type: {
      type: String,
      default: 'text',
    },
    startIcon: {
      type: String,
    },
    endIcon: {
      type: String,
    },
    value: {
      type: String,
    },
  },
  methods: {
    updateValue(value) {
      this.$emit('input', value);
    },
  },
};
</script>

<template>
  <label class="input" :class="{
    'input--error': error,
    'input--disabled': disabled
  }">
    <span class="input__wrap" :class="{[`input__wrap--${size}`]: size}">
      <i v-if="startIcon" class="material-icons material-icons--start">
        {{startIcon}}
      </i>

      <input
        v-if="!multiline"
        class="input__field"
        :type="type"
        :placeholder="placeholder"
        :disabled="disabled"
        :readonly="readonly"
        :tabindex="disabled ? -1 : null"
        :value="value"
        @input="updateValue($event.target.value)"
      >

      <textarea
        v-if="multiline"
        :rows="row"
        class="input__field"
        :placeholder="placeholder"
        :disabled="disabled"
        :readonly="readonly"
        :tabindex="disabled ? -1 : null"
        :value="value"
        @input="updateValue($event.target.value)"
      />

      <i v-if="endIcon" class="material-icons material-icons--end">
        {{endIcon}}
      </i>
    </span>

    <span class="input__label" v-if="label">{{label}}</span>
    <span class="input__helper-text" v-if="helperText">{{helperText}}</span>
  </label>
</template>
