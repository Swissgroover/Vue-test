<template>
  <div class="w-full p-10 lg:p-20">
    <RadioGroup v-model="selected">
      <RadioGroupLabel class="sr-only"> Server size </RadioGroupLabel>
      <div class="space-y-4">
        <RadioGroupOption as="template" v-for="plan in plans" :key="plan.name" :value="plan" v-slot="{ checked, active }">
          <div :class="[checked ? 'border-transparent' : 'border-gray-300', active ? 'border-indigo-500 ring-2 ring-indigo-500' : '', 'relative block cursor-pointer rounded-lg border bg-white px-6 py-4 shadow-sm focus:outline-none sm:flex sm:justify-between']">
            <span class="flex items-center">
              <span class="flex flex-col text-sm">
                <RadioGroupLabel as="span" class="font-medium text-gray-900">{{ plan.name }}</RadioGroupLabel>
                <RadioGroupDescription as="span" class="text-gray-500">
                  <span class="block sm:inline">{{ plan.ram }} </span>
                </RadioGroupDescription>
              </span>
            </span>
            <RadioGroupDescription as="span" class="mt-2 flex text-sm sm:mt-0 sm:ml-4 sm:flex-col sm:text-right">
              <span class="font-medium text-gray-900">{{ plan.price }}</span>
              <span class="ml-1 text-gray-500 sm:ml-0">/month</span>
            </RadioGroupDescription>
            <span :class="[active ? 'border' : 'border-2', checked ? 'border-indigo-500' : 'border-transparent', 'pointer-events-none absolute -inset-px rounded-lg']" aria-hidden="true" />
          </div>
        </RadioGroupOption>
      </div>
    </RadioGroup>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import { RadioGroup, RadioGroupDescription, RadioGroupLabel, RadioGroupOption } from '@headlessui/vue'

const plans = [
  { name: 'Hobby', ram: '8GB', price: '$40' },
  { name: 'Startup', ram: '12GB', price: '$80' },
  { name: 'Business', ram: '16GB', price: '$160' },
  { name: 'Enterprise', ram: '32GB', price: '$240' },
  { name: 'Enterprise', ram: '32GB', price: '$240' },
  { name: 'Enterprise', ram: '32GB', price: '$240' },
  { name: 'Enterprise', ram: '32GB', price: '$240' },
]

const selected = ref(plans[0])
</script>