<script setup lang="ts">
import { ref } from 'vue'

const open = ref(false)
const handleClick = () => {
  console.log('handleClick')
  open.value = true
}
</script>

<template>
  <!-- <h1 class="sr-only">Team Settings</h1> -->
  <h1 class="sr-only">Notifications Settings (legacy)</h1>
  <LegacyDialog v-model="open" />
  <div class="mx-auto max-w-2xl space-y-16 sm:space-y-20 lg:mx-0 lg:max-w-none">
    <div>
      <!-- <h2 class="text-base font-semibold leading-7 text-gray-900">Team Members</h2> -->
      <h2 class="text-base font-semibold leading-7 text-gray-900">Notifications</h2>
      <dl class="mt-6 space-y-6 divide-y divide-gray-100 border-t border-gray-200 text-sm leading-6">
        <div class="pt-6 sm:flex">
          <dt class="font-medium text-gray-900 sm:w-64 sm:flex-none sm:pr-6">メンバー追加</dt>
          <dd class="mt-1 flex justify-between gap-x-6 sm:mt-0 sm:flex-auto">
            <div class="text-gray-900">チームメンバーを追加します</div>
            <button @click="handleClick" type="button" class="font-semibold text-sky-600 hover:text-sky-500">Add</button>
          </dd>
        </div>
        <div class="pt-6 sm:flex">
          <dt class="font-medium text-gray-900 sm:w-64 sm:flex-none sm:pr-6">メンバー編集</dt>
          <dd class="mt-1 flex justify-between gap-x-6 sm:mt-0 sm:flex-auto">
            <div class="text-gray-900">チームメンバーを編集します</div>
            <button type="button" class="font-semibold text-sky-600 hover:text-sky-500">Edit</button>
          </dd>
        </div>
        <div class="pt-6 sm:flex">
          <dt class="font-medium text-gray-900 sm:w-64 sm:flex-none sm:pr-6">メンバー削除</dt>
          <dd class="mt-1 flex justify-between gap-x-6 sm:mt-0 sm:flex-auto">
            <div class="text-gray-900">チームメンバーを削除します</div>
            <button type="button" class="font-semibold text-red-600 hover:text-red-500">Delete</button>
          </dd>
        </div>
      </dl>
    </div>
  </div>
</template>
