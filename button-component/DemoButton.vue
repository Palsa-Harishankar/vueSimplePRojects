<template src="./DemoButton.html"></template>
<script>
import { defineComponent } from 'vue';
import { useToast } from 'primevue/usetoast';
export default defineComponent({
    setup() {
        const toast = useToast();

        const successMessage = () => {
            toast.add({ severity: 'success', summary: 'Success', detail: 'success', life: 3000 });
        };
        const infoMessage = () => {
            toast.add({ severity: 'info', summary: 'Info', detail: 'info', life: 3000 });
        };
        const warnMessage = () => {
            toast.add({ severity: 'warn', summary: 'Warn', detail: 'warn', life: 3000 });
        };
        const errorMessage = () => {
            toast.add({ severity: 'error', summary: 'Error', detail: 'Error', life: 3000 });
        };
        return {
            successMessage, infoMessage, errorMessage, warnMessage
        };
    }
})
</script>