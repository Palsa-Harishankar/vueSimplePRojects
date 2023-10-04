<template src="./RadioPrac.html"></template>
<script lang="ts">
import { defineComponent, ref } from 'vue';

import Toast from 'primevue/toast';
import { useToast } from 'primevue/usetoast';


export default defineComponent({
    components: {
        Toast
    },
    setup() {
        const value = ref()
        const values: String[] = ['male', 'female', 'trans']

        const labels = [('male'), ('female'), ('trans')];
        const toast = useToast()
        const calling = () => {
            // alert(value.value)
            toast.add({ severity: 'info', summary: 'CCRRadioButton component', detail: value.value, life: 3000 })
        }

        return {
            labels, values, value, calling
        }
    }
})
</script>