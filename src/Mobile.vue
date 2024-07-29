<template>
  <div
    class="h-screen bg-[url('https://images.unsplash.com/photo-1490481651871-ab68de25d43d?q=80&w=2070')] bg-cover bg-center"
  >
    <div class="w-full flex justify-end">
      <div class="relative p-4">
        <Bars3Icon @click="openMenu" class="size-8 p-1 bg-white/50 rounded" />

        <div
          v-if="menuOpen"
          class="fixed inset-0 z-40 bg-black/50"
          @click="closeMenu"
        ></div>

        <div
          v-if="menuOpen"
          class="fixed inset-y-0 right-0 z-50 w-5/6 bg-white"
        >
          <div v-if="currentMenu === 'main'">
            <div class="flex items-center justify-between p-4">
              <div class="text-xl text-amber-600 font-bold italic uppercase">
                Urban Canvas
              </div>
              <XMarkIcon @click="closeMenu" class="size-6" />
            </div>

            <ul>
              <li
                v-for="category in data"
                :key="category.label"
                @click="openSubMenu(category)"
                class="p-4 active:bg-amber-100 cursor-pointer"
              >
                {{ category.label }}
              </li>
            </ul>
          </div>

          <div v-else-if="currentMenu === 'sub'">
            <div class="flex items-center p-4 gap-2">
              <ArrowLeftIcon @click="goBack" class="size-6 cursor-pointer" />
              <div class="text-xl font-semibold mb-1">
                {{ currentCategory.label }}
              </div>
            </div>
            <ul>
              <li
                v-for="subcategory in currentCategory.dropdown"
                :key="subcategory.label || subcategory"
                @click="openItemMenu(subcategory)"
                class="p-4 active:bg-amber-100 cursor-pointer"
              >
                {{ subcategory.label || subcategory }}
              </li>
            </ul>
          </div>

          <div v-else-if="currentMenu === 'item'">
            <div class="flex items-center gap-2 p-4">
              <ArrowLeftIcon @click="goBack" class="size-6 cursor-pointer" />
              <div class="text-xl font-semibold mb-1">
                {{ currentSubCategory.label }}
              </div>
            </div>
            <ul>
              <li
                v-for="item in currentSubCategory.dropdown"
                :key="item.label || item"
                @click="item.dropdown ? openFinalMenu(item) : null"
                :class="item.dropdown ? 'cursor-pointer' : ''"
                class="p-4 active:bg-amber-100"
              >
                {{ item.label || item }}
              </li>
            </ul>
          </div>

          <div v-else-if="currentMenu === 'final'">
            <div class="flex items-center gap-2 p-4">
              <ArrowLeftIcon @click="goBack" class="size-6 cursor-pointer" />
              <div class="text-xl font-semibold mb-1">
                {{ currentFinalCategory.label }}
              </div>
            </div>
            <ul>
              <li
                v-for="finalItem in currentFinalCategory.dropdown"
                :key="finalItem"
                class="p-4 active:bg-amber-100 cursor-pointer"
              >
                {{ finalItem }}
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";
import { Bars3Icon, ArrowLeftIcon, XMarkIcon } from "@heroicons/vue/24/outline";

const menuOpen = ref(false);
const currentMenu = ref("main");
const menuHistory = ref([]);
const currentCategory = ref({});
const currentSubCategory = ref({});
const currentFinalCategory = ref({});

const data = [
  {
    label: "Men",
    dropdown: [
      {
        label: "Topwear",
        dropdown: ["Shirts", "Polos", "Jackets", "T-Shirts", "Sweaters"],
      },
      {
        label: "Bottomwear",
        dropdown: ["Jeans", "Shorts", "Trousers", "Chinos", "Joggers"],
      },
      {
        label: "Accessories",
        dropdown: ["Belts", "Watches", "Sunglasses", "Hats", "Wallets"],
      },
      {
        label: "Shoes",
        dropdown: ["Sneakers", "Loafers", "Boots", "Formal Shoes", "Sandals"],
      },
    ],
  },
  {
    label: "Women",
    dropdown: [
      {
        label: "Topwear",
        dropdown: ["Tops", "Blouses", "Dresses", "Sweaters", "Jackets"],
      },
      {
        label: "Bottomwear",
        dropdown: ["Jeans", "Leggings", "Skirts", "Shorts", "Trousers"],
      },
      {
        label: "Accessories",
        dropdown: [
          "Jewelry",
          "Belts",
          "Scarves",
          "Handbags",
          "Hair Accessories",
        ],
      },
      {
        label: "Shoes",
        dropdown: ["Sneakers", "Flats", "Boots", "Heels", "Sandals"],
      },
    ],
  },
  {
    label: "Kids",
    dropdown: [
      {
        label: "Boys",
        dropdown: [
          {
            label: "Topwear",
            dropdown: [
              "Shirts",
              "Polos",
              "Formals",
              "T-Shirts",
              "Sweaters",
              "Jackets",
            ],
          },
          {
            label: "Bottomwear",
            dropdown: [
              "Jeans",
              "Shorts",
              "Trousers",
              "Sweatpants",
              "Cargo Pants",
            ],
          },
          {
            label: "Accessories",
            dropdown: ["Hats", "Belts", "Sunglasses", "Watches", "Backpacks"],
          },
          {
            label: "Shoes",
            dropdown: [
              "Sneakers",
              "Sandals",
              "Formal Shoes",
              "Boots",
              "Loafers",
            ],
          },
        ],
      },
      {
        label: "Girls",
        dropdown: [
          {
            label: "Topwear",
            dropdown: ["Tops", "Blouses", "Dresses", "Sweaters", "Jackets"],
          },
          {
            label: "Bottomwear",
            dropdown: ["Jeans", "Leggings", "Skirts", "Shorts", "Trousers"],
          },
          {
            label: "Accessories",
            dropdown: ["Hairbands", "Jewelry", "Belts", "Bags", "Scarves"],
          },
          {
            label: "Shoes",
            dropdown: ["Sneakers", "Sandals", "Flats", "Boots", "Formal Shoes"],
          },
        ],
      },
    ],
  },
];

function openMenu() {
  menuOpen.value = true;
}
function closeMenu() {
  menuOpen.value = false;
}

function openSubMenu(category) {
  menuHistory.value.push({
    menu: currentMenu.value,
    category: currentCategory.value,
    subCategory: currentSubCategory.value,
    finalCategory: currentFinalCategory.value,
  });
  currentCategory.value = category;
  currentMenu.value = "sub";
}

function openItemMenu(subcategory) {
  menuHistory.value.push({
    menu: currentMenu.value,
    category: currentCategory.value,
    subCategory: currentSubCategory.value,
    finalCategory: currentFinalCategory.value,
  });
  currentSubCategory.value = subcategory;
  currentMenu.value = "item";
}

function openFinalMenu(item) {
  menuHistory.value.push({
    menu: currentMenu.value,
    category: currentCategory.value,
    subCategory: currentSubCategory.value,
    finalCategory: currentFinalCategory.value,
  });
  currentFinalCategory.value = item;
  currentMenu.value = "final";
}

function goBack() {
  const lastState = menuHistory.value.pop();
  if (lastState) {
    currentMenu.value = lastState.menu;
    currentCategory.value = lastState.category;
    currentSubCategory.value = lastState.subCategory;
    currentFinalCategory.value = lastState.finalCategory;
  } else {
    currentMenu.value = "main";
  }
}
</script>
