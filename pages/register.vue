<template>
    <div class="scrollHide h-screen w-full flex">
        <img src="/bg/bg-login.png" class="w-5/12 h-full"/>
        <div class="w-7/12 h-screen flex items-center justify-center">
            <div class="flex flex-col items-center justify-center gap-4">
            <h1 class="font-bold text-4xl">SKILL MATCH</h1>
            <h1 class="font-semibold text-lg">WELCOME</h1>
            <p class="w-1/2 text-center">Unlock Success with Skill Match
            Streamlined Connections and Endless Opportunities.
            Your Path to Career Excellence Starts Here!</p>
            <div class="w-full">
            <div class=" w-1/2 px-2 py-2 mx-auto rounded-lg bg-[#E3E3E3] flex text-base font-normal font-montserrat">
                        <div
                        :class="` transition duration-500 ${cadence === 1 ? 'font-semibold bg-[#DB4A51]' : 'hover:bg-[#E3E3E3]'} rounded-lg cursor-pointer w-1/2 text-center py-px md:py-2`"  @click="cadence = 1">
                            <p class="text-xxs md:text-base">JOB SEEKERS</p>
                        </div>
                        <div class="p-1"></div>
                        <div :class="` transition duration-500 flex items-center justify-center ${cadence === 2 ? 'font-semibold bg-[#DB4A51]' : 'hover:bg-[#E3E3E3]'} rounded-lg cursor-pointer w-1/2 text-center py-px md:py-2`"  @click="cadence = 2">
                            <p class="text-xxs md:text-base">RECRUITERS</p>
                            
                         </div>
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
            <span class="font-semibold">Email</span>
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
          <button class="focus:outline-none font-bold bg-red text-white px-14 py-2 rounded-3xl">
            SIGN UP
          </button>
        </div>
          </div>
        </div>
        </div>
    </div>
</template>

<script setup lang="ts">
    const cadence=ref(1);
</script>