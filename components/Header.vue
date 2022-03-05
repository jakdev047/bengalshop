<template>
  <div>
    <div class="container">
      <div class="py-6 flex justify-between items-center">
        <!-- logo -->
        <Logo />

        <!-- search input -->
        <div class="w-96">
          <div class="border border-gray-100 p-1 flex rounded-full items-center">
            <div class="min-w-max px-3">
              <img src="~/assets/img/search.png" alt="">
            </div>
            <input class="w-full px-3 pxy-1 focus:outline-none" type="search" placeholder="Search here ...">

            <button class="bg-gray bs-button-bg px-6 rounded-full py-2 text-white" type="submit">Search</button>
          </div>
        </div>

        <!-- cart-icon -->
        <div class="min-w-max flex items-center">
          <nuxt-link to="/wishlist">
              <span class="bs-icon-box rounded-full hover:bg-gray-200 inline-block flex items-center justify-center">
                <img src="~/assets/img/heart.png" alt="wishlist">
            </span>
          </nuxt-link>
          <nuxt-link class="relative mx-4" to="/cart">
            <span class="bs-icon-box rounded-full hover:bg-gray-200 inline-block flex items-center justify-center">
              <img src="~/assets/img/u_shopping-bag.png" alt="user">
            </span>
            <span class="absolute bg-red-600 px-1 h-4 top-0 right-0 rounded-full text-xs flex justify-center items-center text-white">{{ count }}</span>
          </nuxt-link>
          <nuxt-link to="/my-account" class="flex items-center">
            <span class="bs-icon-box rounded-full hover:bg-gray-200 inline-block flex items-center justify-center">
              <img src="~/assets/img/user.png" alt="user">
            </span>
            <span>Account</span>
          </nuxt-link>
        </div>

      </div>
    </div>
  </div>
</template>

<script>
  import Logo from "./Logo";
  export default {
    name: 'Header',
    components: {Logo},
    data() {
      return {
        allCategoryMenu: false,
        count: 0
      }
    },
  }
</script>