<template>
     <div class=" flex items-center justify-center bg-white w-screen h-screen">
      <div class="p-12 gap-12 bg-white border border-black rounded-lg flex flex-col items-center justify-center">
        <div class="flex flex-col items-center justify-center gap-3">
            <h1 class="font-bold text-4xl">SKILL MATCH</h1>
            <h1 class="font-semibold text-lg">WELCOME BACK</h1>
        </div>
        <div class="flex flex-col items-center justify-center gap-3 p-6">
          <input
            placeholder="USERNAME/EMAIL"
            type="text"
            class="focus:outline-none border border-black px-16 py-3 rounded-full"
          />
          <input
            placeholder="PASSWORD"
            type="text"
            class="focus:outline-none border border-black px-16 py-3 rounded-full"
          />
          <div class="flex gap-2">
            <input type="radio">
            <span>Remember me</span>
          </div>
          <button class="focus:outline-none font-bold border border-black px-14 py-2 rounded-3xl">
            LOGIN
          </button>
        </div>
      </div>
    </div>
</template>