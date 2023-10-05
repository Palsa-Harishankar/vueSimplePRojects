<template>
    <h2>Step1</h2>
    <CCRLayout columns="1">
<CCRColView colSize="3">

    <CCRInputText v-model="r_name" icon="pi pi-user" label="UserName :"></CCRInputText>
</CCRColView>
    </CCRLayout>
    </template>
<script>
import { defineComponent, ref } from 'vue';

export default defineComponent({

    props:{params:String},
    setup(props) { 
        const r_name = ref();
        function onClickNext() {
            alert(props.params)
            return {
                isValid: true,
                formData: {
                    name:r_name.value
                }
            }
        }
        return {
            r_name,onClickNext
        }
    }
})
</script>