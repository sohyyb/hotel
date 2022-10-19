<template>
  <div class="container">
    <div class="head">
      <img src="@/assets/pics/logo.png" class="brand" alt="">
      <div class="search" @click.prevent="showSearch = !showSearch">
        <div class="image">
          <icon>
            <Search />
          </icon>

          <p>search</p>
        </div>
      </div>
      <Transition>
        <div class="cont" v-if="showSearch">
          <ul class="locations">
            <li class="location">
              <label for="">Location</label>
              <input type="text" />
            </li>
            <li>Alexandia, Egypt</li>
            <li>New York, Us</li>
            <li>Riyadh, sa</li>
          </ul>
          <div class="addGusest">
            <ul>
              <li class="adults">
                <h3>Adults</h3>
                <p>Ages 13 or above</p>
                <div class="control">
                  <button @click.prevent=" adult > 1 && adult--" :disabled="adult == 1 ? true : false">-</button>
                  <span>{{adult}}</span>
                  <button @click.prevent="adult++">+</button>
                </div>
              </li>
              <li>
                <h3>Children</h3>
                <p>Ages 2 - 12</p>
                <div class="control">
                  <button @click.prevent=" children > 1 && children--"
                    :disabled="children == 1 ? true : false">-</button>
                  <span>{{children}}</span>
                  <button @click.prevent="children++">+</button>
                </div>
              </li>
            </ul>
          </div>
          <button class="search-btn" @click.prevent="showSearch = false">search</button>
          <button class="close" @click.prevent="showSearch = false">
            <icon color="#EB5757">
              <X />
            </icon>
          </button>
        </div>
      </Transition>
    </div>

    <h1>stays in Finland</h1>
    <div class="cards">
      <div class="card">
        <img src="@/assets/pics/download (1).jpg" alt="">
        <div class="desc">
          <p>SUPER HOST</p>
          <div class="rate">

            <icon color="#EB5757">
              <star />
            </icon>
            4.5
          </div>
        </div>
        <h3>cozy, peaceful and private room with...</h3>
      </div>
      <div class="card">
        <img src="@/assets/pics/download (2).jpg" alt="">
        <div class="desc">
          <p>private room</p>
          <div class="rate">

            <icon color="#EB5757">
              <star />
            </icon>
            4.5
          </div>
        </div>
        <h3>cozy, peaceful and private room with...</h3>
      </div>
      <div class="card">
        <img src="@/assets/pics/download (3).jpg" alt="">
        <div class="desc">
          <p>Entire House</p>
          <div class="rate">

            <icon color="#EB5757">
              <star />
            </icon>
            4.5
          </div>
        </div>
        <h3>cozy, peaceful and private room with...</h3>
      </div>
      <div class="card">
        <img src="@/assets/pics/download (4).jpg" alt="">
        <div class="desc">
          <p>SUPER HOST</p>
          <div class="rate">

            <icon color="#EB5757">
              <star />
            </icon>
            4.5
          </div>
        </div>
        <h3>cozy, peaceful and private room with...</h3>
      </div>
      <div class="card">
        <img src="@/assets/pics/download.jpg" alt="">
        <div class="desc">
          <p>private room</p>
          <div class="rate">

            <icon color="#EB5757">
              <star />
            </icon>
            4.5
          </div>
        </div>
        <h3>cozy, peaceful and private room with...</h3>
      </div>
      <div class="card">
        <img src="@/assets/pics/hotel-room-300x300.jpg" alt="">
        <div class="desc">
          <p>Entire House</p>
          <div class="rate">

            <icon color="#EB5757">
              <star />
            </icon>
            4.5
          </div>
        </div>
        <h3>cozy, peaceful and private room with...</h3>
      </div>
    </div>

  </div>
</template>
<script setup>
import { Star, Search, X } from '@vicons/tabler';
import { Icon } from '@vicons/utils'
import { ref } from 'vue';
const showSearch = ref(false)
const adult = ref(1)
const children = ref(1) 
</script>
<style>
.v-enter-active,
.v-leave-active {
  transition: opacity 0.3s ease;
}

.v-enter-from,
.v-leave-to {
  opacity: 0;
}
</style>