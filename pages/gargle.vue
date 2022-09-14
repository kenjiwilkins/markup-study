<template>
  <div class="flex flex-col items-stretch min-h-screen">
    <header class="flex-grow">
      <div class="flex space-x-4 float-right px-6 py-4">
        <div class="flex space-x-3">
          <a>mail</a>
          <a>image</a>
        </div>
        <div class="flex space-x-3">
          <a>app</a>
          <a>user</a>
        </div>
      </div>
    </header>
    <main class="flex-grow flex-shrink-0">
      <div class="flex flex-col items-center max-h-72 flex-shrink-0 box-border" style="height:calc(100% - 560px)">
        <div class="max-h-24 h-full relative mt-auto">
          <img class="w-auto h-24" src="../assets/img/gargle.png" alt="Gargle">
        </div>
      </div>
      <form id="searchForm" @submit.prevent="search">
        <div>
          <div>
            <div
              class="flex z-10 h-11 bg-white border-solid border-gray-200 border rounded-3xl w-auto max-w-screen-sm mx-auto">
              <div class="flex flex-grow flex-shrink pt-1 pb-0 pr-2 pl-3">
                <div class="flex items-center pr-3 -mt-1">
                  <div class="m-auto">
                    <span class="h-5 leading-5 w-5 fill-current inline-block mt-1 relative">
                      <svg focusable="false" xmlns="http://www.w3.org/2000/svg">
                        <path
                          d="M15.5 14h-.79l-.28-.27A6.471 6.471 0 0 0 16 9.5 6.5 6.5 0 1 0 9.5 16c1.61 0 3.09-.59 4.23-1.57l.27.28v.79l5 4.99L20.49 19l-4.99-5zm-6 0C7.01 14 5 11.99 5 9.5S7.01 5 9.5 5 14 7.01 14 9.5 11.99 14 9.5 14z">
                        </path>
                      </svg>
                    </span>
                  </div>
                </div>
                <div class="flex flex-grow flex-shrink flex-wrap">
                  <input class="bg-transparent border-none m-0 p-0 break-words outline-none flex" id="query" type="text"
                    maxlength="2048" name="query" aria-autocomplete="both" aria-haspopup="false" autocapitalize="off"
                    autocomplete="off" autofocus role="combobox" spellcheck="false" title="search" v-model="query"
                    aria-label="Query">
                </div>
                <div class="flex items-center pr-3 -mt-1">
                  <div class="m-auto">
                    <span class="h-5 leading-5 w-5 fill-current inline-block mt-1 relative">
                      <svg focusable="false" xmlns="http://www.w3.org/2000/svg">
                        <path
                          d="m12 15c1.66 0 3-1.31 3-2.97v-7.02c0-1.66-1.34-3.01-3-3.01s-3 1.34-3 3.01v7.02c0 1.66 1.34 2.97 3 2.97z">
                        </path>
                        <path d="m11 18.08h2v3.92h-2z"></path>
                        <path
                          d="m7.05 16.87c-1.27-1.33-2.05-2.83-2.05-4.87h2c0 1.45 0.56 2.42 1.47 3.38v0.32l-1.15 1.18z">
                        </path>
                        <path
                          d="m12 16.93a4.97 5.25 0 0 1 -3.54 -1.55l-1.41 1.49c1.26 1.34 3.02 2.13 4.95 2.13 3.87 0 6.99-2.92 6.99-7h-1.99c0 2.92-2.24 4.93-5 4.93z">
                        </path>
                      </svg>
                    </span>
                  </div>
                </div>
              </div>
            </div>
            <div class="h-20 pt-4 block">
              <div class="flex justify-center h-20">
                <input class="bg-gray-100 border border-solid border-gray-100 rounded my-4 mx-1 py-0 px-4"
                  value="find Gargle" @click="search" aria-label="find Gargle" name="btnfind" role="button"
                  type="submit" tabindex="0">
                <input class="bg-gray-100 border border-solid border-gray-100 rounded my-4 mx-1 py-0 px-4"
                  value="I'm Feeling Wonderful" aria-label="I'm Feeling Wonderful" name="btnwonder" role="button"
                  type="submit">
              </div>
            </div>
          </div>
        </div>
      </form>
      <div class="flex-grow flex-shrink-0 box-border">
        <div class="text-sm mb-6 text-center">
          <div class="inline-block text-gray-800 leading-7">You can find something you want in other
            languages:<a>日本語</a></div>
        </div>
      </div>
    </main>
    <footer class="flex-shrink-0 w-full">
      <div class=" bg-slate-400">
        <div class="justify-evenly flex flex-wrap px-5 py-0">
          <div class="justify-evenly flex flex-wrap">
            <a class="text-gray-500 block p-4 whitespace-nowrap no-underline">About K</a>
            <a class="text-gray-500 block p-4 whitespace-nowrap no-underline">Ads</a>
            <a class="text-gray-500 block p-4 whitespace-nowrap no-underline">business</a>
            <a class="text-gray-500 block p-4 whitespace-nowrap no-underline">how2</a>
          </div>
          <div class="justify-evenly flex flex-wrap">
            <a class="text-gray-500 block p-4 whitespace-nowrap no-underline">privacy</a>
            <a class="text-gray-500 block p-4 whitespace-nowrap no-underline">T&C</a>
            <a class="text-gray-500 block p-4 whitespace-nowrap no-underline">Settings</a>
          </div>
        </div>
      </div>
    </footer>
  </div>
</template>
<script lang="ts">
import { defineComponent } from 'vue'
export default defineComponent({
  name: 'Gargle',
  data() {
    return {
      query: ''
    }
  },
  methods: {
    search() {
      window.location.href = `https://www.google.com/search?q=${this.query}`
    }
  }
})
</script>