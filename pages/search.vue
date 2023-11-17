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
                            <TagSearch />
                        </div>
                        <div class="w-1/2 flex gap-2 items-center">
                            <SvgLocation class="text-black/60 scale-125" />
                            <input
                                placeholder="Search for Location"
                                type="text"
                                class="focus:outline-none h-8 w-full bg-transparent px-2 rounded"
                            />
                        </div>
                </div>
                <div class="flex gap-2 items-center">
                    <div class="py-2 px-4 rounded h-fit flex gap-2 transition-all ease-in-out duration-300 border border-white bg-white/30 hover:bg-white cursor-pointer">
                        <SvgFilter class="text-black/60" />
                        <span>Filters</span>
                    </div>
                    <div class="py-2 px-6 rounded text-white bg-blue-700 border border-blue-700 h-fit cursor-pointer">Search</div>
                </div>
            </div>
        </div>
        <div clas="container mx-auto">

        </div>
    </div>
</template>