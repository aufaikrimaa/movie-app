<template>
  <div>
    <div
      class="base absolute flex justify-end right-0 lg:justify-center z-20 text-white lg:left-1/2 lg:right-1/2 top-2 sm:top-4 md:top-8"
    >
      <nuxt-link to="/"> <Logo /></nuxt-link>
    </div>
    <div
      class="base absolute flex justify-end z-20 text-white hidden lg:block text-3xl right-0 top-7 gap-2"
    >
      <input
        type="text"
        placeholder="Type something..."
        class="bg-transparent h-8 self-center px-3 py-1 text-xs rounded-full w-9/10 w-[20rem] border border-white focus:outline-none focus:ring focus:ring-red-500 focus:ring-opacity-50"
      />
      <Icon
        name="uil:search"
        style="color: white"
        class="absolute top-6 right-2 transform -translate-y-1/2 h-6 pointer-events-none"
      />
    </div>

    <nav class="hidden lg:block absolute base z-20 top-8">
      <div class="text-white text-2xl flex gap-2 font-bold">
        <div class="relative py-1 px-6 rounded-full overflow-hidden group">
          <nuxt-link to="/"
            ><div class="relative z-10">Home</div>
            <div
              class="absolute inset-0 bg-gray-300/20 transition-transform duration-300 ease-in-out rounded-full"
              :class="{
                'scale-100': $route.path === '/',
                'scale-0 group-hover:scale-100': $route.path !== '/',
              }"
            ></div>
          </nuxt-link>
        </div>
        <div class="relative py-1 px-6 rounded-full overflow-hidden group">
          <nuxt-link to="/movie"
            ><div class="relative z-10">Movies</div>
            <div
              class="absolute inset-0 bg-gray-300/20 transition-transform duration-300 ease-in-out rounded-full"
              :class="{
                'scale-100': $route.path === '/movie',
                'scale-0 group-hover:scale-100': $route.path !== '/movie',
              }"
            ></div>
          </nuxt-link>
        </div>
        <div class="relative py-1 px-6 rounded-full overflow-hidden group">
          <nuxt-link to="/tv"
            ><div class="relative z-10">TV Shows</div>
            <div
              class="absolute inset-0 bg-gray-300/20 transition-transform duration-300 ease-in-out rounded-full"
              :class="{
                'scale-100': $route.path === '/tv',
                'scale-0 group-hover:scale-100': $route.path !== '/tv',
              }"
            ></div>
          </nuxt-link>
        </div>
      </div>
    </nav>

    <nav
      class="block lg:hidden w-4/5 fixed bottom-0 left-1/2 transform -translate-x-1/2 z-20"
    >
      <div
        class="nav-menu bg-gray-300/50 rounded-2xl flex justify-around mb-4 h-8 sm:h-10 md:h-12"
      >
        <div class="flex items-center">
          <nuxt-link to="/" class="flex items-center justify-center">
            <Icon
              name="mdi:home"
              class="text-2xl sm:text-3xl md:text-4xl"
              :class="{
                'text-white': $route.path === '/',
                'text-white/60': $route.path !== '/',
              }"
            />
          </nuxt-link>
        </div>
        <div class="flex items-center">
          <nuxt-link to="/movie" class="flex items-center justify-center">
            <Icon
              name="mdi:movie-play"
              class="text-2xl sm:text-3xl md:text-4xl"
              :class="{
                'text-white': $route.path === '/movie',
                'text-white/60': $route.path !== '/movie',
              }"
            />
          </nuxt-link>
        </div>
        <div class="flex items-center">
          <nuxt-link to="/tv" class="flex items-center justify-center">
            <Icon
              name="mdi:tv-classic"
              class="text-2xl sm:text-3xl md:text-4xl"
              :class="{
                'text-white': $route.path === '/tv',
                'text-white/60': $route.path !== '/tv',
              }"
            />
          </nuxt-link>
        </div>
        <div class="flex items-center">
          <nuxt-link to="/" class="flex items-center justify-center">
            <Icon
              name="mdi:search"
              class="text-2xl sm:text-3xl md:text-4xl"
              :class="{
                'text-white': $route.path === '/search',
                'text-white/60': $route.path !== '/search',
              }"
            />
          </nuxt-link>
        </div>
      </div>
    </nav>
  </div>
</template>

<script setup></script>

<style scoped>
.text-shadow {
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
}
</style>
