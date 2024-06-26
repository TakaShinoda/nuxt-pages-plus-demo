<script setup lang="ts">
import { CheckIcon } from '@heroicons/vue/24/outline'
</script>

<template>
  <div class="mb-4">
    <div class="mx-auto flex h-12 w-12 items-center justify-center rounded-full bg-green-100">
      <CheckIcon class="h-6 w-6 text-green-600" aria-hidden="true" />
    </div>
    <div class="mt-3 text-center sm:mt-5">
      <h3 class="text-base font-semibold leading-6 text-gray-900">Team Member Add</h3>
      <div class="mt-2">
        <p class="text-sm text-gray-500">追加するメンバーの情報を入力してください</p>
      </div>
    </div>
  </div>
  <form class="space-y-6" action="#" method="POST">
    <div>
      <label for="name" class="block text-sm font-medium leading-6 text-gray-900">User name</label>
      <div class="mt-2">
        <input id="name" name="name" type="text" autocomplete="name" required="true" class="block w-full p-2 rounded-md border-0 py-1.5 text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-sky-600 sm:text-sm sm:leading-6" />
      </div>
    </div>
    <div>
      <label for="email" class="block text-sm font-medium leading-6 text-gray-900">Email address</label>
      <div class="mt-2">
        <input id="email" name="email" type="email" autocomplete="email" required="true" class="block w-full p-2 rounded-md border-0 py-1.5 text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-sky-600 sm:text-sm sm:leading-6" />
      </div>
    </div>
    <div>
      <button type="submit" class="flex w-full justify-center rounded-md bg-sky-600 px-3 py-1.5 text-sm font-semibold leading-6 text-white shadow-sm hover:bg-sky-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-sky-600">Add</button>
    </div>
  </form>
</template>
