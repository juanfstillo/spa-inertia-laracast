<template>
        <div>
            <Component
                v-for="link in links"
                :key="link.label"
                :is="link.url ? 'Link' : 'span'"
                :href="link.url || undefined"
                v-html="link.label"
                class="px-1"
                :class="{ 'text-gray-500': !link.url, 'font-bold': link.active }"
            />
        </div>
</template>
<script>
export default{
    props:{
        links:Array
    }
};
</script>