<template>
  <button class="garden-switch"
          @click="toggle"
          :class="{'garden-checked':value}"
          :disabled="loading ? true:disabled">
    <span><span class="garden-loadingIndicator" v-if="loading"></span></span>
    <p v-if="value" class="garden-switch-on">on</p>
    <p v-else class="garden-switch-off">off</p>
  </button>
</template>

<script lang="ts">

export default {
  props: {
    value: Boolean,
    disabled: {
      type: Boolean,
      default: false
    },
    loading: {
      type: Boolean,
      default: false
    }
  },
  setup(props, context) {
    const toggle = () => {
      context.emit('update:value', !props.value);
    };
    return {toggle};
  }
};
</script>

<style lang="scss">
$blue: #40a9ff;
$h: 22px;
$h2: $h - 4px;
.garden-switch {
  height: $h;
  width: $h*2;
  border: none;
  background: #bfbfbf;
  border-radius: $h/2;
  position: relative;

  > span {
    position: absolute;
    top: 2px;
    left: 2px;
    height: $h2;
    width: $h2;
    background: white;
    border-radius: $h2 / 2;
    transition: all 250ms;
  }

  > p {
    display: inline-block;
    width: 14px;
    height: $h;
    font-size: 14px;
    color: #fff;
    margin: 2px 7px 0 22px;
    transition: margin 250ms;

    &.garden-switch-on {
      transform: translateX(-18px);
    }
  }

  &.garden-checked {
    background: #1890ff;

    > span {
      left: calc(100% - #{$h2} - 2px);
    }
  }

  .garden-loadingIndicator {
    width: 14px;
    height: 14px;
    display: inline-block;
    margin-top: 2px;
    margin-right: 3px;
    border-radius: 8px;
    border-color: $blue $blue $blue transparent;
    border-style: solid;
    border-width: 2px;
    animation: garden-spin 1s infinite linear;
  }

  &:focus {
    outline: none;
  }

  &:active {
    > span {
      width: $h2 + 4px;
    }
  }

  &.garden-checked:active {
    > span {
      width: $h2 + 4px;
      margin-left: -4px;
    }
  }
}


</style>