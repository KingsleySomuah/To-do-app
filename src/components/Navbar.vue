<template>
    <div class="flex justify-center">
        <div class="p-2 bg-gray-400 w-[80%]">
            <div class="justify-between flex items-center">
                <div class="flex items-center">
                    <img src="./../assets/icons/icons.png" alt="" width="40">
                    <p class="font-bold">To-Do List</p>
                </div>
                <div class="flex gap-4 font-semibold">
                    <span>
                        <RouterLink to="/">
                            Home
                        </RouterLink>

                    </span>
                    <span>
                        <RouterLink to="/about">
                            About
                        </RouterLink>
                    </span>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>

</script>

<style lang="scss" scoped></style>