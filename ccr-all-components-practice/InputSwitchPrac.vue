<template src="./InputSwitchPrac.html"></template>
<script>
import { defineComponent, ref } from 'vue';

export default defineComponent({
    setup() {
        const r_value=ref(false)
        return {
            r_value
        }
    }
})
</script>