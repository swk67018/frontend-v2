<template>
  <v-tooltip
    bottom
    :open-delay="0"
    transition="slide-y-transition"
  >
    <template #activator="{ on, attrs }">
      <v-btn
        v-haptic
        v-bind="{...$attrs, ...attrs}"
        :style="{'top': top}"
        v-on="{...$listeners, ...on}"
      >
        <slot />
      </v-btn>
    </template>
    <span>
      {{ tip }}
    </span>
  </v-tooltip>
</template>

<script>
export default {
  name: 'TooltipBtn',
  props: {
    tip: {
      type: String,
      default () {
        return ''
      }
    },
    top: {
      type: String,
      default () {
        return ''
      }
    }
  }
}
</script>

<style scoped>

</style>
