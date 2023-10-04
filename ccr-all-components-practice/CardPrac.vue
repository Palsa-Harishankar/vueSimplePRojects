<template src="./CardPrac.html"></template>
<script>
import { useToast } from 'primevue/usetoast';
import { defineComponent } from 'vue';

export default defineComponent({
    setup() {
        const toast = useToast()

const successMessage = () => {
    toast.add({ severity: 'success', summary: 'Card', detail: 'submit sucsess', life: 3000 });
        };
        const errorMessage = () => {
    toast.add({ severity: 'error', summary: 'Card', detail: 'canceled', life: 3000 });
};
        return {
            successMessage,errorMessage
        }
    }
})
</script>