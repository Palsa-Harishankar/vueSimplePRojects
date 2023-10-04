<script>
import Toast from 'primevue/toast';
import { useToast } from 'primevue/usetoast';
export default {
    setup() {
        const toast = useToast();
        const successMessage = () => {
            toast.add({ severity: 'success', summary: 'Success', detail: 'Severity=success', life: 3000 });
        };
        const infoMessage = () => {
            toast.add({ severity: 'info', summary: 'Info', detail: 'Severity=info', life: 3000 });
        };
        const warnMessage = () => {
            toast.add({ severity: 'warn', summary: 'Warn', detail: 'Severity=warn', life: 3000 });
        };
        const errorMessage = () => {
            toast.add({ severity: 'error', summary: 'Error', detail: 'Severity=Error', life: 3000 });
        };
        return {
            successMessage, infoMessage, errorMessage, warnMessage
        };
    },
    components: { Toast }
}
</script>
<template>

    <Toast/>
    <div class="card flex flex-wrap justify-content-center gap-6">
    <Button   severity="success" @click="successMessage" label="Success" ></Button >
    <Button   severity="info" @click="infoMessage" label="info"></Button >
    <Button severity="warning" @click="warnMessage" label="warn"></Button >
    <Button  severity="danger" @click="errorMessage" label="Error"></Button >
</div>
</template>