<template>
  <div class="flex flex-wrap justify-between -mt-1 md:-mt-0">
    <div
      v-scroll-reveal="{ delay: 250, distance: '10%' }"
      class="inline-flex items-start max-w-xs text-left mt-8 md:mt-12"
      :style="item.icon_opacity"
      v-for="item in iconItems"
      :key="item.icon_id"
    >
      <img
        alt="svg icon"
        class="svg w-12 md:w-16"
        :style="item.icon_color"
        :src="item.icon_svg"
      />
      <div class="ml-4 flex flex-col">
        <h3
          class="font-semibold learing-tight text-lg md:text-xl"
          :style="item.icon_color"
        >
          {{ item.icon_title }}
        </h3>
        <p class="mt-2 font-regular leading-normal text-base opacity-75">
          {{ item.icon_paragraph }}
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    iconItems: {
      type: Array
    }
  }
}
</script>
