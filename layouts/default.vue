<template>
    <div class="container mx-auto max-w-4xl">
        <header class="flex justify-between items-start md:items-center mt-5">
            <div class="flex items-center md:space-x-12">
                <div>
                    <NuxtLink to="/" class="hidden md:block text-xl font-semibold p-2 hover:bg-gray-200 dark:hover:bg-gray-800">Min Khant Naung</NuxtLink>
                </div>

                <Menu />
            </div>

            <ClientOnly>
                <color-mode-selector />
            </ClientOnly>
        </header>

        <main class="p-2 mt-10">
            <slot />
        </main>
    </div>
</template>

<script setup>
useHead({
    // as a string,
    // where `%s` is replaced with the title
    titleTemplate: '%s - Min Khant Naung',
})
</script>

<style>
body {
    @apply bg-white dark:bg-gray-900 text-gray-700 dark:text-gray-300;
}
</style>