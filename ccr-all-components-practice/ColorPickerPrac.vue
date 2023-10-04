<template src="./ColorPickerPrac.html"></template>
<script>
import { useToast } from 'primevue/usetoast';
import { defineComponent, ref } from 'vue';

export default defineComponent({
    setup() {
        const colorV = ref()
        const toast=useToast()
        const fun = () => {
            toast.add({
                severity: 'info', summary: 'Color Picker',life:3000, detail:colorV.value
          
            })
        }
        return {
            colorV,fun
        }
    }
})
</script>