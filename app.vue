<template>
  <div>
    <UContainer>
      <UAccordion :items="items" size="xl" />
      <UDivider label="OR" />


      <div>
        <UButton label="Open" @click="isOpen = true" />

        <USlideover v-model="isOpen">
          <div class="p-4 flex-1">
            <UVerticalNavigation :links="links" />
          </div>
        </USlideover>
      </div>
    </UContainer>
  </div>
</template>
<script setup>
const isOpen = ref(false);
const items = [
  {
    label: "Getting Started",
    icon: "i-heroicons-information-circle",
    defaultOpen: true,
    content:
      "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed neque elit, tristique placerat feugiat ac, facilisis vitae arcu. Proin eget egestas augue. Praesent ut sem nec arcu pellentesque aliquet. Duis dapibus diam vel metus tempus vulputate.",
  },
  {
    label: "Installation",
    icon: "i-heroicons-arrow-down-tray",
    disabled: true,
    content:
      "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed neque elit, tristique placerat feugiat ac, facilisis vitae arcu. Proin eget egestas augue. Praesent ut sem nec arcu pellentesque aliquet. Duis dapibus diam vel metus tempus vulputate.",
  },
  {
    label: "Theming",
    icon: "i-heroicons-eye-dropper",
    content:
      "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed neque elit, tristique placerat feugiat ac, facilisis vitae arcu. Proin eget egestas augue. Praesent ut sem nec arcu pellentesque aliquet. Duis dapibus diam vel metus tempus vulputate.",
  },
  {
    label: "Layouts",
    icon: "i-heroicons-rectangle-group",
    content:
      "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed neque elit, tristique placerat feugiat ac, facilisis vitae arcu. Proin eget egestas augue. Praesent ut sem nec arcu pellentesque aliquet. Duis dapibus diam vel metus tempus vulputate.",
  },
  {
    label: "Components",
    icon: "i-heroicons-square-3-stack-3d",
    content:
      "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed neque elit, tristique placerat feugiat ac, facilisis vitae arcu. Proin eget egestas augue. Praesent ut sem nec arcu pellentesque aliquet. Duis dapibus diam vel metus tempus vulputate.",
  },
  {
    label: "Utilities",
    icon: "i-heroicons-wrench-screwdriver",
    content:
      "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed neque elit, tristique placerat feugiat ac, facilisis vitae arcu. Proin eget egestas augue. Praesent ut sem nec arcu pellentesque aliquet. Duis dapibus diam vel metus tempus vulputate.",
  },
];
const links = [
  {
    label: "Profile",
    avatar: {
      src: "https://avatars.githubusercontent.com/u/739984?v=4",
    },
    badge: 100,
  },
  {
    label: "Installation",
    icon: "i-heroicons-home",
    to: "https://www.yazilimkodlama.com/teknoloji/kare-isareti-nasil-yapilir-hash-diyez-kare-isareti/",
    target: '_blank'
  },
  {
    label: "Vertical Navigation",
    icon: "i-heroicons-chart-bar",
    to: "/navigation/vertical-navigation",
  },
  {
    label: "Command Palette",
    icon: "i-heroicons-command-line",
    to: "#headlessui-disclosure-button-65",
  },
];
</script>
