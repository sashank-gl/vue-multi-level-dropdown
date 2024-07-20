<template>
  <div
    class="h-screen bg-[url('https://images.unsplash.com/photo-1490481651871-ab68de25d43d?q=80&w=2070')] bg-cover bg-center"
  >
    <div
      class="flex justify-center items-center font-semibold text-nowrap pt-6"
    >
      <!-- Men Dropdown -->
      <div class="relative">
        <div
          @mouseover="showMenDropdown = true"
          @mouseleave="showMenDropdown = false"
          class="py-2 px-4 text-xl cursor-pointer hover:underline underline-offset-4"
        >
          Men
          <div
            v-if="showMenDropdown"
            class="absolute left-0 top-full w-fit bg-white/50"
          >
            <div
              @mouseover="showMenTopwearDropdown = true"
              @mouseleave="showMenTopwearDropdown = false"
              class="relative"
            >
              <div
                class="px-5 py-2 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
              >
                Topwear
                <ChevronRightIcon class="w-5 h-5 inline-block ml-2" />
              </div>
              <div
                v-if="showMenTopwearDropdown"
                class="absolute left-full top-0 mt-2 w-fit bg-white/50"
              >
                <div
                  class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                >
                  Casual Shirts
                </div>
                <div
                  class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                >
                  Dress Shirts
                </div>
                <div
                  class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                >
                  Polo Shirts
                </div>
                <div
                  class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                >
                  Hoodies
                </div>
              </div>
            </div>
            <div
              @mouseover="showMenBottomwearDropdown = true"
              @mouseleave="showMenBottomwearDropdown = false"
              class="relative"
            >
              <div
                class="px-5 py-2 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
              >
                Bottomwear
                <ChevronRightIcon class="w-5 h-5 inline-block ml-2" />
              </div>
              <div
                v-if="showMenBottomwearDropdown"
                class="absolute left-full top-0 mt-2 w-fit bg-white/50"
              >
                <div
                  class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                >
                  Jeans
                </div>
                <div
                  class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                >
                  Cargo Pants
                </div>
                <div
                  class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                >
                  Joggers
                </div>
                <div
                  class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                >
                  Shorts
                </div>
              </div>
            </div>
            <div
              @mouseover="showMenFootwearDropdown = true"
              @mouseleave="showMenFootwearDropdown = false"
              class="relative"
            >
              <div
                class="px-5 py-2 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
              >
                Footwear
                <ChevronRightIcon class="w-5 h-5 inline-block ml-2" />
              </div>
              <div
                v-if="showMenFootwearDropdown"
                class="absolute left-full top-0 mt-2 w-fit bg-white/50"
              >
                <div
                  class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                >
                  Sneakers
                </div>
                <div
                  class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                >
                  Loafers
                </div>
                <div
                  class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                >
                  Boots
                </div>
                <div
                  class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                >
                  Sandals
                </div>
              </div>
            </div>
            <div
              @mouseover="showMenAccessoriesDropdown = true"
              @mouseleave="showMenAccessoriesDropdown = false"
              class="relative"
            >
              <div
                class="px-5 py-2 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
              >
                Accessories
                <ChevronRightIcon class="w-5 h-5 inline-block ml-2" />
              </div>
              <div
                v-if="showMenAccessoriesDropdown"
                class="absolute left-full top-0 mt-2 w-fit bg-white/50"
              >
                <div
                  class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                >
                  Watches
                </div>
                <div
                  class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                >
                  Belts
                </div>
                <div
                  class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                >
                  Wallets
                </div>
                <div
                  class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                >
                  Sunglasses
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>

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
            class="absolute left-0 top-full w-fit bg-white/50"
          >
            <div
              @mouseover="showWomenTopwearDropdown = true"
              @mouseleave="showWomenTopwearDropdown = false"
              class="relative"
            >
              <div
                class="px-5 py-2 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
              >
                Topwear
                <ChevronRightIcon class="w-5 h-5 inline-block ml-2" />
              </div>
              <div
                v-if="showWomenTopwearDropdown"
                class="absolute left-full top-0 mt-2 w-fit bg-white/50"
              >
                <div
                  class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                >
                  Blouses
                </div>
                <div
                  class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                >
                  Cardigans
                </div>
                <div
                  class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                >
                  Tunics
                </div>
                <div
                  class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                >
                  Sweater Vests
                </div>
              </div>
            </div>
            <div
              @mouseover="showWomenBottomwearDropdown = true"
              @mouseleave="showWomenBottomwearDropdown = false"
              class="relative"
            >
              <div
                class="px-5 py-2 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
              >
                Bottomwear
                <ChevronRightIcon class="w-5 h-5 inline-block ml-2" />
              </div>
              <div
                v-if="showWomenBottomwearDropdown"
                class="absolute left-full top-0 mt-2 w-fit bg-white/50"
              >
                <div
                  class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                >
                  A-Line Skirts
                </div>
                <div
                  class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                >
                  Palazzo Pants
                </div>
                <div
                  class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                >
                  Capris
                </div>
                <div
                  class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                >
                  Culottes
                </div>
              </div>
            </div>
            <div
              @mouseover="showWomenFootwearDropdown = true"
              @mouseleave="showWomenFootwearDropdown = false"
              class="relative"
            >
              <div
                class="px-5 py-2 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
              >
                Footwear
                <ChevronRightIcon class="w-5 h-5 inline-block ml-2" />
              </div>
              <div
                v-if="showWomenFootwearDropdown"
                class="absolute left-full top-0 mt-2 w-fit bg-white/50"
              >
                <div
                  class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                >
                  Heels
                </div>
                <div
                  class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                >
                  Flats
                </div>
                <div
                  class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                >
                  Ankle Boots
                </div>
                <div
                  class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                >
                  Espadrilles
                </div>
              </div>
            </div>
            <div
              @mouseover="showWomenAccessoriesDropdown = true"
              @mouseleave="showWomenAccessoriesDropdown = false"
              class="relative"
            >
              <div
                class="px-5 py-2 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
              >
                Accessories
                <ChevronRightIcon class="w-5 h-5 inline-block ml-2" />
              </div>
              <div
                v-if="showWomenAccessoriesDropdown"
                class="absolute left-full top-0 mt-2 w-fit bg-white/50"
              >
                <div
                  class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                >
                  Jewelry
                </div>
                <div
                  class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                >
                  Handbags
                </div>
                <div
                  class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                >
                  Scarves
                </div>
                <div
                  class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                >
                  Hats
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
            class="absolute left-0 top-full w-fit bg-white/50"
          >
            <!-- Boys Dropdown -->
            <div
              @mouseover="showBoysDropdown = true"
              @mouseleave="showBoysDropdown = false"
              class="relative"
            >
              <div
                class="px-5 py-2 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
              >
                Boys
                <ChevronRightIcon class="w-5 h-5 inline-block ml-2" />
              </div>
              <div
                v-if="showBoysDropdown"
                class="absolute left-full top-0 mt-2 w-fit bg-white/50"
              >
                <!-- Boys Topwear Dropdown -->
                <div
                  @mouseover="showBoysTopwearDropdown = true"
                  @mouseleave="showBoysTopwearDropdown = false"
                  class="relative"
                >
                  <div
                    class="px-5 py-2 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                  >
                    Topwear
                    <ChevronRightIcon class="w-5 h-5 inline-block ml-2" />
                  </div>
                  <div
                    v-if="showBoysTopwearDropdown"
                    class="absolute left-full top-0 mt-2 w-fit bg-white/50"
                  >
                    <div
                      class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                    >
                      Casual Shirts
                    </div>
                    <div
                      class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                    >
                      Dress Shirts
                    </div>
                    <div
                      class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                    >
                      Polo Shirts
                    </div>
                    <div
                      class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                    >
                      Hoodies
                    </div>
                  </div>
                </div>
                <!-- Boys Bottomwear Dropdown -->
                <div
                  @mouseover="showBoysBottomwearDropdown = true"
                  @mouseleave="showBoysBottomwearDropdown = false"
                  class="relative"
                >
                  <div
                    class="px-5 py-2 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                  >
                    Bottomwear
                    <ChevronRightIcon class="w-5 h-5 inline-block ml-2" />
                  </div>
                  <div
                    v-if="showBoysBottomwearDropdown"
                    class="absolute left-full top-0 mt-2 w-fit bg-white/50"
                  >
                    <div
                      class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                    >
                      Jeans
                    </div>
                    <div
                      class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                    >
                      Cargo Pants
                    </div>
                    <div
                      class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                    >
                      Joggers
                    </div>
                    <div
                      class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                    >
                      Shorts
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
                    class="px-5 py-2 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                  >
                    Footwear
                    <ChevronRightIcon class="w-5 h-5 inline-block ml-2" />
                  </div>
                  <div
                    v-if="showBoysFootwearDropdown"
                    class="absolute left-full top-0 mt-2 w-fit bg-white/50"
                  >
                    <div
                      class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                    >
                      Sneakers
                    </div>
                    <div
                      class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                    >
                      Loafers
                    </div>
                    <div
                      class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                    >
                      Boots
                    </div>
                    <div
                      class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                    >
                      Sandals
                    </div>
                  </div>
                </div>
                <!-- Boys Accessories Dropdown -->
                <div
                  @mouseover="showBoysAccessoriesDropdown = true"
                  @mouseleave="showBoysAccessoriesDropdown = false"
                  class="relative"
                >
                  <div
                    class="px-5 py-2 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                  >
                    Accessories
                    <ChevronRightIcon class="w-5 h-5 inline-block ml-2" />
                  </div>
                  <div
                    v-if="showBoysAccessoriesDropdown"
                    class="absolute left-full top-0 mt-2 w-fit bg-white/50"
                  >
                    <div
                      class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                    >
                      Watches
                    </div>
                    <div
                      class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                    >
                      Belts
                    </div>
                    <div
                      class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                    >
                      Wallets
                    </div>
                    <div
                      class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                    >
                      Sunglasses
                    </div>
                  </div>
                </div>
              </div>
            </div>

            <!-- Girls Dropdown -->
            <div
              @mouseover="showGirlsDropdown = true"
              @mouseleave="showGirlsDropdown = false"
              class="relative"
            >
              <div
                class="px-5 py-2 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
              >
                Girls
                <ChevronRightIcon class="w-5 h-5 inline-block ml-2" />
              </div>
              <div
                v-if="showGirlsDropdown"
                class="absolute left-full top-0 mt-2 w-fit bg-white/50"
              >
                <!-- Girls Topwear Dropdown -->
                <div
                  @mouseover="showGirlsTopwearDropdown = true"
                  @mouseleave="showGirlsTopwearDropdown = false"
                  class="relative"
                >
                  <div
                    class="px-5 py-2 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                  >
                    Topwear
                    <ChevronRightIcon class="w-5 h-5 inline-block ml-2" />
                  </div>
                  <div
                    v-if="showGirlsTopwearDropdown"
                    class="absolute left-full top-0 mt-2 w-fit bg-white/50"
                  >
                    <div
                      class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                    >
                      Dresses
                    </div>
                    <div
                      class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                    >
                      Blouses
                    </div>
                    <div
                      class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                    >
                      Tunics
                    </div>
                    <div
                      class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                    >
                      Sweaters
                    </div>
                  </div>
                </div>
                <!-- Girls Bottomwear Dropdown -->
                <div
                  @mouseover="showGirlsBottomwearDropdown = true"
                  @mouseleave="showGirlsBottomwearDropdown = false"
                  class="relative"
                >
                  <div
                    class="px-5 py-2 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                  >
                    Bottomwear
                    <ChevronRightIcon class="w-5 h-5 inline-block ml-2" />
                  </div>
                  <div
                    v-if="showGirlsBottomwearDropdown"
                    class="absolute left-full top-0 mt-2 w-fit bg-white/50"
                  >
                    <div
                      class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                    >
                      Skirts
                    </div>
                    <div
                      class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                    >
                      Leggings
                    </div>
                    <div
                      class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                    >
                      Jeans
                    </div>
                    <div
                      class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                    >
                      Culottes
                    </div>
                  </div>
                </div>
                <!-- Girls Footwear Dropdown -->
                <div
                  @mouseover="showGirlsFootwearDropdown = true"
                  @mouseleave="showGirlsFootwearDropdown = false"
                  class="relative"
                >
                  <div
                    class="px-5 py-2 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                  >
                    Footwear
                    <ChevronRightIcon class="w-5 h-5 inline-block ml-2" />
                  </div>
                  <div
                    v-if="showGirlsFootwearDropdown"
                    class="absolute left-full top-0 mt-2 w-fit bg-white/50"
                  >
                    <div
                      class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                    >
                      Ballet Flats
                    </div>
                    <div
                      class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                    >
                      Sandals
                    </div>
                    <div
                      class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                    >
                      Boots
                    </div>
                    <div
                      class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                    >
                      Sneakers
                    </div>
                  </div>
                </div>
                <!-- Girls Accessories Dropdown -->
                <div
                  @mouseover="showGirlsAccessoriesDropdown = true"
                  @mouseleave="showGirlsAccessoriesDropdown = false"
                  class="relative"
                >
                  <div
                    class="px-5 py-2 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                  >
                    Accessories
                    <ChevronRightIcon class="w-5 h-5 inline-block ml-2" />
                  </div>
                  <div
                    v-if="showGirlsAccessoriesDropdown"
                    class="absolute left-full top-0 mt-2 w-fit bg-white/50"
                  >
                    <div
                      class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                    >
                      Headbands
                    </div>
                    <div
                      class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                    >
                      Jewelry
                    </div>
                    <div
                      class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                    >
                      Bags
                    </div>
                    <div
                      class="py-2 px-4 bg-gradient-to-r from-transparent hover:from-white/60 via-white/60 to-white/60 hover:to-transparent cursor-pointer"
                    >
                      Scarves
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
import { ChevronRightIcon } from "@heroicons/vue/24/outline";

const showMenDropdown = ref(false);
const showWomenDropdown = ref(false);
const showKidsDropdown = ref(false);
const showMenTopwearDropdown = ref(false);
const showMenBottomwearDropdown = ref(false);
const showMenFootwearDropdown = ref(false);
const showMenAccessoriesDropdown = ref(false);
const showWomenTopwearDropdown = ref(false);
const showWomenBottomwearDropdown = ref(false);
const showWomenFootwearDropdown = ref(false);
const showWomenAccessoriesDropdown = ref(false);
const showBoysDropdown = ref(false);
const showGirlsDropdown = ref(false);
const showBoysTopwearDropdown = ref(false);
const showBoysBottomwearDropdown = ref(false);
const showBoysFootwearDropdown = ref(false);
const showBoysAccessoriesDropdown = ref(false);
const showGirlsTopwearDropdown = ref(false);
const showGirlsBottomwearDropdown = ref(false);
const showGirlsFootwearDropdown = ref(false);
const showGirlsAccessoriesDropdown = ref(false);
</script>
