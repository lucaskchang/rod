<template>
  <div class="p-4">
    <div class="z-0">
      <div
        :style="{ backgroundImage: 'url(\'rod.png\')', backgroundSize: `${dimensions}` }"
        class="fixed top-0 z-0 h-screen w-full blur"
      />
    </div>
    <div class="z-50 flex h-screen w-full flex-col items-center justify-center bg-transparent text-center">
      <div class="z-50 rounded-lg bg-white p-8 blur-none dark:bg-gray-950">
        <p class="z-50 text-6xl font-black md:text-9xl">
          The <span class="z-50 bg-gradient-to-r from-teal-300 via-sky-600 to-cyan-300 bg-clip-text font-sans text-transparent">Best</span> Rod
        </p>
      </div>
    </div>
    <div class="z-10 flex h-screen w-full flex-col justify-center md:flex-row">
      <div class="flex flex-col md:w-1/2">
        <img
          src="/rod.png"
          class="mx-auto size-96"
        >
      </div>
      <div class="flex flex-col p-12 pl-0 md:w-1/2">
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
    <div class="flex flex-col px-0 py-24 md:h-screen md:flex-row md:px-24">
      <div
        v-for="attribute in attributes"
        :key="attribute.name"
        class="flex h-[576px] flex-row px-0 py-4 md:w-1/3 md:px-4"
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
      <div class="z-50 mt-[50vh] rounded-lg bg-white p-8 blur-none dark:bg-gray-950">
        <p class="z-50 text-6xl font-black md:text-9xl">
          The <span class="z-50 bg-gradient-to-r from-teal-300 via-sky-600 to-cyan-300 bg-clip-text font-sans text-transparent">Best</span> Rod
        </p>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
const { width } = useWindowSize();

const dimensions = computed(() => {
  if (width.value >= 768) {
    return '250px 250px';
  }
  return '100px 100px';
});

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
