<template>
  <div class="container-main-body">
    <div class="container-component">
      <div
        class="container-full"
        :class="[props.noTop ? 'no-top' : '', props.noPad ? 'no-pad' : '', props.isDialog ? 'is-dialog' : '']"
        :style="{ marginLeft: !props.left ? 0 : `${props.left}px` }"
      >
        <div class="container-full__header">
          <slot name="header"></slot>
        </div>
        <div class="container-full__body">
          <slot />
        </div>
        <div class="container-full__footer">
          <slot name="footer"></slot>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
const props = defineProps({
  noTop: {
    type: Boolean,
    default: false,
  },
  noPad: {
    type: Boolean,
    default: false,
  },
  isDialog: {
    type: Boolean,
    default: false,
  },
  left: {
    type: Number,
    default: 0,
  },
});
</script>

<style scoped lang="scss">
.container-main-body {
  .container-component {
    height: 100%;
    .container-full {
      margin: 0;
      background-color: white;
      display: flex;
      flex-direction: column;
      &.no-top {
        top: 0 !important;
      }
      &.no-pad {
        padding: 0 !important;
        .container-full__footer {
          margin-bottom: 0;
          top: 0;
        }
        .container-full__body {
          padding: 0 !important;
          margin-bottom: 0 !important;
        }
        .container-full__header {
          background: #ffffff;

          .container {
            padding: 10px 20px;
          }
        }

        .container-full__body {
          padding: 0 20px;
          flex-grow: 1;
          overflow: auto;
          position: relative;
          margin-bottom: 130px !important;
        }
      }
    }
  }
}
</style>
