<template>
    <div class="container p-10">
        <div class="flex items center gap-4">
            <div
                class=" text-gray-400 bg-white w-[20%] p-1 h-[7vh] font-semibold shadow-sm shadow-gray-500 rounded-md flex items-center">
                <p class="items-center">I need to ..</p>
            </div>
            <div class="bg-yellow-300 font-semibold text-center w-[10%] h-[7vh] p-1 rounded-md">
                <p>Add</p>
            </div>
        </div>

        <div class="justify-between flex pt-10 pb-5">
            <div class="font-bold">
                <p>You have 2 tasks to complete</p>
            </div>
            <div class="flex gap-4">
                <div class="bg-green-400 w-10 text-center">All</div>
                <div class="bg-gray-800 text-white text-center w-20 h-8">Favourite</div>
            </div>
        </div>


        <div class="flex justify-between p-3 bg-white shadow-sm shadow-gray-800">
                <div>
                    <p>Finish Data Structures assignment</p>
                </div>
                <div class="flex gap-3">
                    <img src="./../assets/icons/trash-solid.svg" alt="" width="15">
                    <img src="./../assets/icons/heart.svg" alt="" width="20">
                </div>
        </div>
        <div class="flex justify-between bg-white shadow-sm shadow-gray-800 p-3 mt-5 ">
                    <div>
                        <p>Finish Data Structures assignment</p>
                    </div>
                    <div class="flex gap-3">
                        <img src="./../assets/icons/trash-solid.svg" alt="" width="15">
                        <img src="./../assets/icons/heart.svg" alt="" width="20">
                    </div>
        </div>
        <div class="bg-orange-600 font-semibold mt-5 w-[15%] p-2 text-center rounded-lg ">
            <p>Reset Tasks</p>
        </div>
    </div>


</template>

<script setup>

</script>

<style lang="scss" scoped></style>