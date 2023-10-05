<template>
    <h2>Step2</h2>
    <CCRLayout colmuns="1">
        <CCRColView colSize="3">
        <CCRInputNumber  v-model="r_rollNumber"  label="RollNumber :" placeholder="Enter RollNumber "></CCRInputNumber>
   </CCRColView>
   </CCRLayout>
</template>
<script>
import { defineComponent, ref } from 'vue';

export default defineComponent({
    
    props:{params:String},
    setup(props) {
        const r_rollNumber = ref()
        function onClickNext() {
            alert(props.params)
            return {
                isValid: true,
                formData: {
                  roll:  r_rollNumber.value
                }
            }
        }
        return {
            r_rollNumber,onClickNext
        }
    }
})
</script>