<template src="./PasswordPrac.html"></template>
<script>
import { useToast } from 'primevue/usetoast';
import { defineComponent, ref } from 'vue';
import Toast from 'primevue/toast';

export default defineComponent({
    components: {
      Toast  
    },
    setup() {
        const r_pass = ref('')
        const suggest = [
        "At least one lowercase",
          "At least one uppercase",
          "At least one numeric",
          "Minimum 8 characters",
        ]
        const toast=useToast()
        const dum = () => {
          //  alert(r_pass.value)
            toast.add({severity:'info' ,summary:'CCRInputPassword component', detail:'Password :'+r_pass.value ,life:3000} )
        }
        return {
            r_pass,suggest , dum
        }
    }
})
</script>