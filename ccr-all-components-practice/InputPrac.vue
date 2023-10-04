<template src="./InputPrac.html"></template>
<script lang="ts">
import { useToast } from 'primevue/usetoast';
import { defineComponent, ref } from 'vue';

export default defineComponent({
    setup() {
        const inputValue = ref('')
        const toast = useToast();
        const msg = () => {
            toast.add({
                severity: 'info',
                summary: 'InputText Component',
                detail: inputValue.value,
                life:3000
            })
        }
        return {
            inputValue,msg
        }
    }

})
</script>