<template>
  <BDropdownItemButton
    :button-class="[
      'd-flex justify-content-between text-nowrap',
      {[`text-${variant}`]: variant}
    ]"
    v-on="$listeners"
  >
    <slot>
      {{ text }}
    </slot>
    <Icon v-if="icon" :icon="icon" class="ml-4" />
  </BDropdownItemButton>
</template>
<script lang="ts">
  import { defineComponent } from '@vue/composition-api'

  export default defineComponent({
    props: {
      text: { type: String, default: '' },
      icon: { type: String, default: null },
      variant: { type: String, default: '' },
    }
  })
</script>
