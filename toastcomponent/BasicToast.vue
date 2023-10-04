<template>
    <Toast/>
    <div class="flex flex-wrap justify-content-center">
    <Button @click="check" label="Check"></Button>
    </div>
</template>
<script>
import { useToast } from 'primevue/usetoast';
import { defineComponent } from 'vue';

export default defineComponent({
    setup() {
        const toast = useToast()
        const check = () => {
            toast.add({ severity:'info' , summary:'Info' , detail:'Demo Toast' ,life:2000})
        }
        return {
            check
        }
    }
})
</script>