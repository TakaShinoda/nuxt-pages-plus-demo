<script setup lang="ts">
import {
  BellIcon,
  FingerPrintIcon,
  UserCircleIcon,
  UsersIcon,
} from '@heroicons/vue/24/outline'

const secondaryNavigation = [
  { name: 'General', href: '#', icon: UserCircleIcon, current: false },
  { name: 'Security', href: '#', icon: FingerPrintIcon, current: false },
  { name: 'Notifications', href: '#', icon: BellIcon, current: false },
  { name: 'Team', href: '#', icon: UsersIcon, current: true },
] as const
</script>

<template>
  <aside class="flex overflow-x-auto border-b border-gray-900/5 py-4 lg:block lg:w-64 lg:flex-none lg:border-0 lg:py-20">
    <nav class="flex-none px-4 sm:px-6 lg:px-0">
      <ul role="list" class="flex gap-x-3 gap-y-1 whitespace-nowrap lg:flex-col">
        <li v-for="item in secondaryNavigation" :key="item.name">
          <a :href="item.href" :class="[item.current ? 'bg-gray-50 text-sky-600' : 'text-gray-700 hover:bg-gray-50 hover:text-sky-600', 'group flex gap-x-3 rounded-md py-2 pl-2 pr-3 text-sm font-semibold leading-6']">
            <component :is="item.icon" :class="[item.current ? 'text-sky-600' : 'text-gray-400 group-hover:text-sky-600', 'h-6 w-6 shrink-0']" aria-hidden="true" />
            {{ item.name }}
          </a>
        </li>
      </ul>
    </nav>
  </aside>
</template>
