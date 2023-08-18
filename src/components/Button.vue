<template>
    <button :type="type" class="transition-color flex duration-100 items-center w-full justify-center gap-x-1.5 rounded-md bg-gray-100 px-3 py-1.5 text-sm font-semibold text-gray-700 hover:bg-gray-400 hover:text-white" :class="left? 'flex-row-reverse':''">
        <slot />
        <component :is="icon" v-if="icon" class="w-4 h-4 stroke-2"></component>
    </button>
</template>
<script>
export default {
    props: {
        icon: {
            required: false,
            type: Object,
        },
        type: {
            required: false,
            type: String,
            default: 'submit',
        }, 
        left: {
            required: false,
            type: Boolean,
        },
    }
}
</script>
