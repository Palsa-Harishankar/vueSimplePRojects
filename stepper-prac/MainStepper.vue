<template>
    <CCRStepper :items="items"
      @onBeforeNext="onClickNext"
    
      @onClickFinish="finish"
      ref="r_nextRef"></CCRStepper>
</template>
<script>
import { defineComponent, ref } from 'vue';
import Step1 from "./Step1.vue"
import Step2 from "./Step2.vue"
import Step3 from "./Step3.vue"
export default defineComponent({
    setup() {
        const  formData=ref({})
        const r_nextRef = ref();
        const step1Param="This is Step1"
        const step2Param="This is Step2"
        const step3Param="This is Step3"
        const items = [
            {
                label: 'Step1',
                content: Step1,
                params:step1Param
            }
            ,
            {
                label: 'Step2',
                content: Step2,
                params:step2Param
            },
            
            {
                label: 'Step3',
                content: Step3,
                params:step3Param
            },
        ];
        const onClickNext = (obj) => { 
            let data = obj.compRef.onClickNext();
            if (data && data.isValid) {
                formData.value[obj.pageIndex]=data.formData
                r_nextRef.value.nextPage(true)
            }
        };
        const finish = () => {
            alert(JSON.stringify(formData.value))            
        }
        return {items , onClickNext,r_nextRef,finish};
    },
})
</script>