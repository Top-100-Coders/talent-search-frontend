<template>
     <div class=" flex items-center justify-center bg-red w-screen h-screen">
      <div class="p-12 gap-12 bg-white rounded-lg flex flex-col items-center justify-center">
        <div class="flex flex-col items-center justify-center gap-3">
            <h1 class="font-bold text-4xl">SKILL MATCH</h1>
            <h1 class="font-semibold text-lg">WELCOME BACK</h1>
        </div>
        <div class="flex flex-col items-center justify-center gap-3 p-6">
          <div class="flex flex-col">
            <span class="font-semibold">Username</span>
          <input
            placeholder=""
            type="text"
            class="focus:outline-none bg-grey px-16 py-3 rounded-full"
          />
          </div>
          <div class="flex flex-col">
            <span class="font-semibold">Password</span>
          <input
            placeholder=""
            type="text"
            class="focus:outline-none bg-grey px-16 py-3 rounded-full"
          />
          </div>
          <div class="flex gap-2">
            <input type="checkbox">
            <span>Remember me</span>
          </div>
          <button class="focus:outline-none font-bold bg-red text-white px-14 py-2 rounded-3xl">
            LOGIN
          </button>
        </div>
      </div>
    </div>
</template>