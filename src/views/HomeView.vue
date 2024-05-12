<script>
export default {
  data() {
    return {
      searchQuery: "",
    };
  },
  methods: {
    handleSearchInput() {
      if (this.searchQuery.toLowerCase() === "bahirdar") {
        this.$router.push({ name: "about" });
      } else {
        this.$router.push({ name: "Notf" });
      }
    },
  },
};
</script>

<template>
  <div>
    <div
      class="flex flex-row items-center float-right text-sm text-gray-700 mt-5"
    >
      <p href="" class="p-3">Gmail</p>
      <a href="" class="p-3">Images</a>
      <button class="bg-blue-600 text-white w-24 h-8 mr-8">Log in</button>
    </div>

    <div class="flex flex-col justify-center items-center h-screen">
      <div class="flex flex-col justify-center items-center h-screen">
        <label>
          <span class="text-blue-500 text-8xl">G</span>
          <span class="text-red-500 text-8xl">o</span>
          <span class="text-yellow-500 text-8xl">o</span>
          <span class="text-blue-500 text-8xl">g</span>
          <span class="text-green-500 text-8xl">l</span>
          <span class="text-red-500 text-8xl">e</span>
        </label>

        <div class="mb-5 mt-7 items-center relative">
          <i
            class="absolute inset-y-0 left-5 flex items-center pl-3 fas fa-search text-gray-400"
          ></i>
          <input
            v-model="searchQuery"
            @keyup.enter="handleSearchInput"
            class="m-4 shadow-lg border rounded-3xl w-[650px] py-2 px-3 text-gray-700 pl-10"
            type="text"
            placeholder="search Google"
          />
          <div class="absolute inset-y-0 right-5 flex items-center pr-3">
            <i class="mr-3 fas fa-keyboard text-gray-400"></i>
            <i class="fas fa-microphone text-gray-400"></i>
          </div>
        </div>

        <div class="mb-10 flex items-center justify-center">
          <button class="bg-gray-100 py-2 px-4 ml-4">Google Search</button>
          <button class="bg-gray-100 py-2 px-4 ml-4">I'm Feeling Lucky</button>
        </div>
        <div class="inline">
          Google offered in :<span class="text-blue-600">
            Amharic Tigirigna Somaalli</span
          >
        </div>
      </div>
    </div>
  </div>
</template>
