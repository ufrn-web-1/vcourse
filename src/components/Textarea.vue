<script setup lang="ts">
const props = defineProps({
  icon: {
    type: String,
    default: 'io-person-sharp',
    validator(value: string, _) {
      return value.startsWith('io')
    },
  },
})
</script>

<template>
  <label
    class="flex shadow-md overflow-hidden rounded-lg flex-col gap-1 w-full ring-green-600 focus-within:ring-2"
  >
    <div class="flex flex-row w-full">
      <div class="flex w-10 h-full min-w-10 flex-col bg-green-400">
        <div class="flex justify-center items-center h-10 w-10 min-h-10 min-w-10 bg-green-500">
          <v-icon v-bind:name="props.icon" />
        </div>
      </div>

      <textarea class="bg-zinc-200 outline-none px-4 py-2 w-full" v-bind="$attrs" />
    </div>
  </label>
</template>
