<template>
    <input
        :type="type"
        :value="value"
        :placeholder="placeholder"
        class="inputDefault"
    >
</template>
<script>
export default {
    props: {
        placeholder: {
            required: false,
            type: String,
        },
        type: {
            required: false,
            type: String,
            default: 'text',
        }, 
        value: {
            required: false,
            type: String,
        },
    }
}
</script>