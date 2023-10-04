<template src="./CalendarPrac.html"></template>
<script>
import { useToast } from 'primevue/usetoast';
import { defineComponent, ref } from 'vue';

export default defineComponent({
    setup() {
        const selectionMode = 'multiple';
        const inline = true;
        const showButtonBar = true;
        const showIcon = false;
        const view = 'date';
        const date = ref('')
        const toast=useToast()
        const sub = () => {
            toast.add({severity:'info',summary:'CCRDatePicker Component', detail:date.value, life:3000})
        }

        return {
            selectionMode,inline,showButtonBar,showIcon,view,date,sub
            
        }
    }
})
</script>