<template>
  <div
    class="h-screen bg-[url('https://images.unsplash.com/photo-1490481651871-ab68de25d43d?q=80&w=2070')] bg-cover bg-center"
  >
    <div
      class="flex justify-center items-center font-semibold text-nowrap pt-6"
    >
      <ul class="flex justify-center items-center">
        <li
          v-for="category in data"
          :key="category.label"
          @mouseover="showSubDropdown(category.label)"
          @mouseleave="hideSubDropdown(category.label)"
          class="relative py-2 px-4 text-xl cursor-pointer hover:underline underline-offset-4"
        >
          {{ category.label }}
          <div
            v-if="subDropdowns[category.label]"
            class="absolute left-0 top-full w-fit bg-white/50"
          >
            <ul>
              <li
                v-for="subcategory in category.dropdown"
                :key="subcategory.label"
                @mouseover="showItemDropdown(subcategory.label)"
                @mouseleave="hideItemDropdown(subcategory.label)"
                class="relative px-5 py-2 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
              >
                {{ subcategory.label }}
                <ChevronRightIcon class="w-5 h-5 inline-block ml-2" />

                <div
                  v-if="itemDropdowns[subcategory.label]"
                  class="absolute left-full top-0 mt-2 w-fit bg-white/50"
                >
                  <ul
                    v-if="
                      subcategory.dropdown &&
                      subcategory.dropdown.length > 0 &&
                      subcategory.dropdown[0].label
                    "
                  >
                    <li
                      v-for="item in subcategory.dropdown"
                      :key="item.label"
                      @mouseover="showSubItemDropdown(item.label)"
                      @mouseleave="hideSubItemDropdown(item.label)"
                      class="relative py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                    >
                      {{ item.label }}
                      <ChevronRightIcon class="w-5 h-5 inline-block ml-2" />

                      <div
                        v-if="
                          item.dropdown &&
                          item.dropdown.length > 0 &&
                          subItemDropdowns[item.label]
                        "
                        class="absolute left-full top-0 mt-2 w-fit bg-white/50"
                      >
                        <ul>
                          <li
                            v-for="subItem in item.dropdown"
                            :key="subItem"
                            class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                          >
                            {{ subItem }}
                          </li>
                        </ul>
                      </div>
                    </li>
                  </ul>
                  <ul v-else>
                    <li
                      v-for="item in subcategory.dropdown"
                      :key="item"
                      class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                    >
                      {{ item }}
                    </li>
                  </ul>
                </div>
              </li>
            </ul>
          </div>
        </li>
      </ul>
    </div>
  </div>
</template>

<script setup>
import { ChevronRightIcon } from "@heroicons/vue/24/outline";
import { ref } from "vue";

const subDropdowns = ref({});
const itemDropdowns = ref({});
const subItemDropdowns = ref({});

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

function showSubDropdown(label) {
  subDropdowns.value[label] = true;
}

function hideSubDropdown(label) {
  subDropdowns.value[label] = false;
}

function showItemDropdown(label) {
  itemDropdowns.value[label] = true;
}

function hideItemDropdown(label) {
  itemDropdowns.value[label] = false;
}

function showSubItemDropdown(label) {
  subItemDropdowns.value[label] = true;
}

function hideSubItemDropdown(label) {
  subItemDropdowns.value[label] = false;
}
</script>
