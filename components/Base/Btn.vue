<script setup lang="ts">
import type { HeaderAction } from "~/types";

const { $viewport } = useNuxtApp();

const attr = ({
  isMenu = false,
  isPopover = false,
}: {
  isMenu?: boolean;
  isPopover?: boolean;
}) =>
  (isMenu || isPopover) && $viewport.isGreaterOrEquals("tablet") ? "" : "to";

const props = defineProps<{ btnOptions: HeaderAction; isMenuOpen?: boolean }>();
props.btnOptions.icon = props.btnOptions.icon ?? "mdi-home";

const TRoute = useRoute();

const {
  icon,
  route,
  title,
  category,
  color,
  hasChip,
  isMenu,
  mobile,
  isPopover,
} = props.btnOptions;
</script>

<template>
  <!-- :to="route" -->
  <UButton
    v-bind:[attr({isMenu,isPopover})]="route"
    size="lg"
    square
    color="gray"
    class="relative flex h-full items-center justify-center rounded-none text-black/70 transition-colors hover:bg-black/10 dark:hover:bg-white/10 md:h-auto md:rounded-full"
    :class="{
      'flex md:hidden': mobile,
      'hidden md:flex': mobile === false,
      'bg-black/10 dark:bg-white/10': isMenuOpen,
    }"
    variant="ghost"
  >
    <span
      class="absolute left-0 top-0 block h-full w-full rounded-none md:hidden md:rounded-full"
      :class="{ '!bg-blue-600 !text-white': TRoute.path === route }"
    />
    <!-- {{ hasChip }} -->
    <!-- icon -->
    <UChip
      :show="hasChip === true"
      :color="color"
      class=""
      :ui="{ base: 'dark:text-white' }"
      text="3"
      size="2xl"
    >
      <div
        class="btn-content flex flex-col items-center justify-center"
        :class="{
          'text-white dark:text-white/70 md:text-black/70':
            TRoute.path === route,
        }"
      >
        <UIcon
          :name="icon"
          size="20"
          :class="{ 'mr-[1px] mt-[1px]': hasChip === true }"
        />
        <span v-text="title" class="text-[10px] capitalize md:hidden" />
      </div>
    </UChip>
  </UButton>
</template>
