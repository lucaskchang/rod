<template>
  <div>
    <div class="z-0">
      <div
        :style="{ backgroundImage: 'url(\'rod.png\')', backgroundSize: '250px 250px' }"
        class="fixed top-0 z-0 h-screen w-full blur"
      />
    </div>
    <div class="z-50 flex h-screen w-full flex-col items-center justify-center bg-transparent text-center">
      <div class="z-50 rounded-lg bg-white p-8 blur-none">
        <p class="z-50 text-9xl font-black">
          The <span class="z-50 bg-gradient-to-r from-teal-300 via-sky-600 to-cyan-300 bg-clip-text font-sans text-transparent">Best</span> Rod
        </p>
      </div>
    </div>
    <div class="z-10 flex h-screen w-full flex-row justify-center">
      <div class="flex w-1/2 flex-col">
        <img
          src="/rod.png"
          class="mx-auto size-96"
        >
      </div>
      <div class="flex w-1/2 flex-col p-12 pl-0">
        <p class="text-5xl font-bold">
          Rod <span class="text-4xl text-gray-500 dark:text-gray-300">/rŏd/</span>
        </p>
        <p class="text-2xl">
          noun
        </p>
        <p class="text-2xl">
          A thin straight piece or bar of material, such as metal or wood
        </p>
      </div>
    </div>
    <div class="flex h-screen flex-row p-24">
      <div
        v-for="attribute in attributes"
        :key="attribute.name"
        class="flex h-[576px] flex-col p-4 md:w-1/3 md:flex-row"
      >
        <img
          src="/up.png"
          class="h-full"
        >
        <div class="flex flex-col">
          <img
            src="/straight.png"
            class="w-full"
          >
          <div class="z-50 h-[540px] rounded-lg bg-white p-4 dark:bg-gray-950">
            <p class="text-2xl font-bold">
              {{ attribute.name }}
            </p>
            <p class="mt-4 text-lg">
              {{ attribute.description }}
            </p>
          </div>
          <img
            src="/straight.png"
            class="w-full"
          >
        </div>
        <img
          src="/up.png"
          class="h-full"
        >
      </div>
    </div>
    <ColorMode />
    <div
      :style="{ backgroundImage: 'url(\'rod.png\')', backgroundSize: '250px 250px' }"
      class="z-50 flex h-[1000vh] w-full flex-col items-center  text-center"
    >
      <div class="z-50 mt-[50vh] rounded-lg bg-white p-8 blur-none">
        <p class="z-50 text-9xl font-black">
          The <span class="z-50 bg-gradient-to-r from-teal-300 via-sky-600 to-cyan-300 bg-clip-text font-sans text-transparent">Best</span> Rod
        </p>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
const attributes = [
  {
    name: 'Legality',
    description: 'This rod was stolen from my roommate who is currently out of town.',
  },
  {
    name: 'Grip',
    description: 'This rod is equipped with a comfortable grip thanks to tape.',
  },
  {
    name: 'Material',
    description: 'This rod is made of aluminum making it lightweight and durable.',
  },
];
</script>
