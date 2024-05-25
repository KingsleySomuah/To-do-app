<template>
    <div class="flex justify-center">
        <div class="p-4 bg-gray-100 w-[80%]">
            <div class="justify-between flex">
                <div class="flex">
                    <img src="./../assets/icons/logo.svg" alt="" width="30">
                    <p>To-Do List</p>
                </div>
                <div class="flex gap-4">
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

<style lang="scss" scoped>

</style>