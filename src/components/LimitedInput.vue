<template>
      <div class="p-3 rounded-md bg-gray-200 inline-block">
    <input
      class="border px-2"
      :class="isTextTooLong ? 'border-red-500 bg-red-200' : undefined"
      v-model="val"
    />
    <p v-if="isTextTooLong" class="text-red-600 text-xs">
      Limited to {{ limit }} chars.
    </p>
  </div>
</template>

<script setup>
import { ref, computed } from 'vue';
    const props = defineProps({
        disabled: {
      type: Boolean,
      default: false,
    },
    limit: {
      type: Number,
      default: 12,
    },
    value: {
      type: String,
      default: "",
    },
    })
    const val = ref(props.value)
    const isTextTooLong = computed(() => val.value.length > props.limit)
</script>
