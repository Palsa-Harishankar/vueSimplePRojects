<template src="./CheckBoxPrac.html"></template>
<script>
import { defineComponent, ref } from 'vue';

export default defineComponent({
    setup() {
        const value = ref('')
        const r_selectedValues=ref([''])
        const values = ref([
            'java',
            'HTML',
            'CSS',
            'Vue.js'
        ])
        const label = ref([
         'java',
         'HTML',
          'CSS',
         'Vue.js'
        ])
        return {
            value,values,label,r_selectedValues
        }
    }
})
</script>