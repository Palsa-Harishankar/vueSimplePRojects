<template src="./TextAreaDemo.html"></template>
<script>
import { useToast } from 'primevue/usetoast';
import { defineComponent, ref } from 'vue';

export default defineComponent({
    setup() {
        const textAreaContent = ref()
        const toast = useToast();
        const textMessage = () => {
            toast.add({ severity: 'success', summary: 'Textarea Component', detail: textAreaContent.value, life: 2000 });
        }
        return {
            textAreaContent,textMessage
        }
    }
})
</script>