<template src="./DropDownInPrimeVuePrac.html"></template>
<script>
import { useToast } from 'primevue/usetoast';
import { defineComponent, ref } from 'vue';

export default defineComponent({
    setup() {
        const selectedItem = ref();
        const r_d_items = [
            {name:'Hari' , code:'Hr'},
            {name:'Shankar' , code:'SH'},
            {name:'Karunakar' , code:'KR'},
            {name:'Dayanand' , code:'DA'},
        ]
        const l_items = [
            {  name: "Shivaji", code:'Hr' },
            { name: "Prashu", code:'s' },
            {  name: "Srikanth", code:'H' },
            { name: "Yadi", code:'r' },
        ];
        const mu_items = [
            { code: 1, name: "Yogi" },
            { code: 2, name: "Eshwar" },
            { code: 3, name: "Mata" },
            { code: 4, name: "Kala" },
            { code: 5, name: "Nagamani" },
        ];
        const mus=ref([])
        const l_sI=ref()
        const toast = useToast()
        const msg=()=>{toast.add({severity:'info',summary:'DropDown',detail:selectedItem.value,life:3000})}
        const listmsg=()=>{toast.add({severity:'info',summary:'ListBox',detail:l_sI.value,life:3000})}
        const multimsg=()=>{toast.add({severity:'info',summary:'MultiSelect',detail:mus.value,life:3000})}
        return {
            r_d_items, selectedItem, msg, l_items, l_sI, mu_items, mus, listmsg, multimsg
        }
    }
})
</script>