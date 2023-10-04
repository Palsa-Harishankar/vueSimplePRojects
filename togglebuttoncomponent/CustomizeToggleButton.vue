<template src="./CustomizedToggleButton.html"></template>
<script>
import { defineComponent, ref } from 'vue';

export default defineComponent({
    setup() {
        const toggle = ref(false)
        return {
            toggle
        }
    }
})
</script>