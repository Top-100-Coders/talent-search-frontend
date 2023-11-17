
import { FilterBar } from '#build/components';
<template>
    <div class="h-full w-full">
        <div class="container mx-auto flex flex-col items-center justify-center mt-16">
            <div class="flex flex-col items-center leading-[80px]">
                <span class="font-medium text-[64px] capitalize">Find the right</span>
                <div class="flex gap-4">
                    <span class="font-medium text-[64px] capitalize text-blue-700">candidate</span>
                    <span class="font-medium text-[64px] capitalize">for the job</span>
                </div>
            </div>
            <div class="w-full p-2 bg-gray-200 mt-8 flex rounded">
                <div class="flex-1 flex items-center gap-4">
                        <div class="w-1/2 flex gap-2 border-r-2 border-black/30">
                            <SvgSearch class="text-black/60" />
                            <TagSearch ref="tags" />
                        </div>
                        <div class="w-1/2 flex gap-2 items-center">
                            <SvgLocation class="text-black/60 scale-125" />
                            <input
                                v-model="location"
                                placeholder="Search for Location"
                                type="text"
                                class="focus:outline-none h-8 w-full bg-transparent px-2 rounded"
                            />
                        </div>
                </div>
                <div class="flex gap-2 items-center">
                    <div class="py-2 px-4 rounded h-fit flex gap-2 transition-all ease-in-out duration-300 border border-white bg-white/30 hover:bg-white cursor-pointer" 
                    @click="filterRef.toggleView()">
                        <SvgFilter class="text-black/60" />
                        <span>Filters</span>
                    </div>
                    <div class="py-2 px-6 rounded text-white bg-blue-700/80 hover:bg-blue-700 border border-blue-700/80 hover:border-blue-700 h-fit cursor-pointer" @click="search">Search</div>
                </div>
            </div>
        </div>
        <div v-if="viewResults" class="container mx-auto mt-16 flex flex-col">
            <span class="mb-8">{{ data.length }} candidates found</span>
            <div class="flex flex-col gap-4">
                <div v-for="(item, i) in data" :key="i" class="px-6 gap-4 py-4 border-2 border-grey-200 rounded-lg flex items-center">
                    <div class="h-16 w-16 bg-center rounded" :style="`background-image: url('${item.image}');`"></div>
                    <div class="flex flex-col">
                        <span class="font-semibold text-xl"> {{ item.name }}</span>
                        <span> {{ item.job }}</span>
                    </div>
                </div>
            </div>
        </div>
        <FilterBar ref="filterRef"/>
    </div>
</template>
<script setup>
    const filterRef = ref(null);
    const location = ref(null);
    const tags = ref(null);

    const data = ref([{
        name: "Josh Bennet",
        job: "Full-Stack Developer",
        image: 'https://images.pexels.com/photos/4195342/pexels-photo-4195342.jpeg?auto=compress&cs=tinysrgb&w=64&h=35&dpr=2'
    },{
        name: "Veronica Sals",
        job: "Software Architect",
        image: 'https://images.pexels.com/photos/16115837/pexels-photo-16115837/free-photo-of-young-elegant-woman-in-a-brown-coat-and-a-hat-posing-in-city.jpeg?auto=compress&cs=tinysrgb&w=1200'
    },{
        name: "Richard Bill",
        job: "Hourly UI Designer",
        image: 'https://images.pexels.com/photos/3206171/pexels-photo-3206171.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2'
    }])

    const viewResults = ref(false);

    function search(){
        console.log(tags.value.items, location.value);
        viewResults.value = true;
    }

</script>
