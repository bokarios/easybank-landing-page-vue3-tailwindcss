<script setup lang="ts">
const features = [
  {
    id: 1,
    title: 'Online Banking',
    content:
      'Our modern web and mobile applications allow you to keep track of your finances wherever you are in the world.',
    icon: 'icon-online.svg',
  },
  {
    id: 2,
    title: 'Simple Budgeting',
    content:
      "See exactly where you money goes each month. Receive notifications when you're close to hitting your limits.",
    icon: 'icon-budgeting.svg',
  },
  {
    id: 3,
    title: 'Fast Onboarding',
    content:
      "We don't do branches. Open your account in minutes online and start taking control of your finances right away.",
    icon: 'icon-onboarding.svg',
  },
  {
    id: 4,
    title: 'Open API',
    content:
      'Manage your savings, investments, pension, and more much from one account. Tracking your money has never been easier.',
    icon: 'icon-api.svg',
  },
]
</script>

<template>
  <section class="w-full bg-brand-light-grayish-blue relative -z-20">
    <div
      class="w-full px-6 md:px-20 xl:px-40 py-16 lg:py-24 max-w-[1440px] mx-auto"
    >
      <h3
        class="text-[34px] lg:text-[42px] text-brand-dark-blue text-center lg:text-left leading-tight mb-5"
      >
        Why choose Easybank?
      </h3>
      <p
        class="text-md lg:text-body text-brand-grayish-blue font-normal text-center lg:text-left mb-14 lg:mb-20"
      >
        We leverage Open Banking to turn your account into your financial hub.
        <br />
        Control your finances like never before.
      </p>
      <div
        class="flex flex-col lg:flex-row lg:justify-items-auto gap-10 w-full"
      >
        <div
          v-for="feature in features"
          :key="feature.id"
          class="flex flex-col items-center lg:items-start text-center lg:text-left w-full lg:w-3/12"
        >
          <img :src="`/images/${feature.icon}`" class="mb-8" alt="online" />
          <h4
            class="text-xl xl:text-2xl font-normal text-brand-dark-blue mb-4 lg:mb-6"
          >
            {{ feature.title }}
          </h4>
          <p class="text-brand-grayish-blue font-normal">
            {{ feature.content }}
          </p>
        </div>
      </div>
    </div>
  </section>
</template>
