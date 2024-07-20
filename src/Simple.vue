<template>
  <div class="bg-indigo-50 h-96 flex justify-center items-start pt-24">
    <div class="flex justify-center items-center text-nowrap">
      <!-- Women Dropdown -->
      <div class="relative">
        <div
          @mouseover="showWomenDropdown = true"
          @mouseleave="showWomenDropdown = false"
          class="py-2 px-4 text-xl cursor-pointer hover:underline underline-offset-4"
        >
          Women
          <div
            v-if="showWomenDropdown"
            class="absolute left-0 top-full w-fit bg-indigo-100"
          >
            <div
              @mouseover="showWomenFootwearDropdown = true"
              @mouseleave="showWomenFootwearDropdown = false"
              class="relative"
            >
              <div
                class="px-5 py-2 bg-indigo-100 hover:bg-indigo-200 cursor-pointer"
              >
                Footwear
              </div>
              <div
                v-if="showWomenFootwearDropdown"
                class="absolute left-full top-0 mt-2 w-fit bg-indigo-100"
              >
                <div
                  class="py-2 px-4 bg-indigo-100 hover:bg-indigo-200 cursor-pointer"
                >
                  Heels
                </div>
                <div
                  class="py-2 px-4 bg-indigo-100 hover:bg-indigo-200 cursor-pointer"
                >
                  Flats
                </div>
                <div
                  class="py-2 px-4 bg-indigo-100 hover:bg-indigo-200 cursor-pointer"
                >
                  Ankle Boots
                </div>
              </div>
            </div>
            <div
              @mouseover="showWomenAccessoriesDropdown = true"
              @mouseleave="showWomenAccessoriesDropdown = false"
              class="relative"
            >
              <div
                class="px-5 py-2 bg-indigo-100 hover:bg-indigo-200 cursor-pointer"
              >
                Accessories
              </div>
              <div
                v-if="showWomenAccessoriesDropdown"
                class="absolute left-full top-0 mt-2 w-fit bg-indigo-100"
              >
                <div
                  class="py-2 px-4 bg-indigo-100 hover:bg-indigo-200 cursor-pointer"
                >
                  Jewelry
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- Kids Dropdown -->
      <div class="relative">
        <div
          @mouseover="showKidsDropdown = true"
          @mouseleave="showKidsDropdown = false"
          class="py-2 px-4 text-xl cursor-pointer hover:underline underline-offset-4"
        >
          Kids
          <div
            v-if="showKidsDropdown"
            class="absolute left-0 top-full w-fit bg-indigo-100"
          >
            <!-- Boys Dropdown -->
            <div
              @mouseover="showBoysDropdown = true"
              @mouseleave="showBoysDropdown = false"
              class="relative"
            >
              <div
                class="px-5 py-2 bg-indigo-100 hover:bg-indigo-200 cursor-pointer"
              >
                Boys
              </div>
              <div
                v-if="showBoysDropdown"
                class="absolute left-full top-0 mt-2 w-fit bg-indigo-100"
              >
                <!-- Boys Topwear Dropdown -->
                <div
                  @mouseover="showBoysTopwearDropdown = true"
                  @mouseleave="showBoysTopwearDropdown = false"
                  class="relative"
                >
                  <div
                    class="px-5 py-2 bg-indigo-100 hover:bg-indigo-200 cursor-pointer"
                  >
                    Topwear
                  </div>
                  <div
                    v-if="showBoysTopwearDropdown"
                    class="absolute left-full top-0 mt-2 w-fit bg-indigo-100"
                  >
                    <div
                      class="py-2 px-4 bg-indigo-100 hover:bg-indigo-200 cursor-pointer"
                    >
                      Casual Shirts
                    </div>

                    <div
                      class="py-2 px-4 bg-indigo-100 hover:bg-indigo-200 cursor-pointer"
                    >
                      Polos
                    </div>
                    <div
                      class="py-2 px-4 bg-indigo-100 hover:bg-indigo-200 cursor-pointer"
                    >
                      Hoodies
                    </div>
                  </div>
                </div>

                <!-- Boys Footwear Dropdown -->
                <div
                  @mouseover="showBoysFootwearDropdown = true"
                  @mouseleave="showBoysFootwearDropdown = false"
                  class="relative"
                >
                  <div
                    class="px-5 py-2 bg-indigo-100 hover:bg-indigo-200 cursor-pointer"
                  >
                    Footwear
                  </div>
                  <div
                    v-if="showBoysFootwearDropdown"
                    class="absolute left-full top-0 mt-2 w-fit bg-indigo-100"
                  >
                    <div
                      class="py-2 px-4 bg-indigo-100 hover:bg-indigo-200 cursor-pointer"
                    >
                      Sneakers
                    </div>

                    <div
                      class="py-2 px-4 bg-indigo-100 hover:bg-indigo-200 cursor-pointer"
                    >
                      Boots
                    </div>
                    <div
                      class="py-2 px-4 bg-indigo-100 hover:bg-indigo-200 cursor-pointer"
                    >
                      Sandals
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";

const showWomenDropdown = ref(false);
const showKidsDropdown = ref(false);
const showWomenFootwearDropdown = ref(false);
const showWomenAccessoriesDropdown = ref(false);
const showBoysDropdown = ref(false);
const showBoysTopwearDropdown = ref(false);
const showBoysFootwearDropdown = ref(false);
</script>
