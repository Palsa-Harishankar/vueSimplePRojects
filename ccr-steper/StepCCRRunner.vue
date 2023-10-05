<template>

    <h2>Stepper Component</h2>

    

 <CCRLayout columns="1">
  <CCRColview colSize="12">
    <CCRStepper :items="r_stepItems" ref="r_nextRef" @onBeforeNext="onClkNext($event)"  @onClickFinish="finsh($event)" 
></CCRStepper>
</CCRColview>
 </CCRLayout>
    </template>
    
    <script lang="ts">
    import { defineComponent, ref } from "vue";
  
    import StepA from "./StepA.vue"
    import StepB from "./StepB.vue"
    import StepC from "./StepC.vue"
    
    export default defineComponent({
       
      
    setup() {
            const formData=ref({})
            const r_nextRef = ref()
            const stepData1 = ref({"stepname": "step-1"})
            const stepData2 = ref({ "stepname": 'Step-2' })
            const stepData3=ref({  "stepname":'Step-3'})
            const r_stepItems = ref([
      {
        label:"Step1",
        content: StepA,
        params: stepData1.value
        
       
      },
      {
        label: 'Step2',
        content: StepB,
        params: stepData2.value
       
      },
      {
        label: 'Step3',
        content: StepC,
        params: stepData3.value
       
      },
            ]);
            function onClkNext(calBack) {
            
            
              let objActiveStepResp = calBack.compRef.onClickNexst();
                  if (objActiveStepResp && objActiveStepResp.isValid) {
                    formData.value[calBack.pageIndex] = objActiveStepResp.formData;

                    r_nextRef.value.nextPage(true)
                  }

            }
            function finsh(callback){
                  // alert("Thank you  sir")
                  alert(JSON.stringify(formData.value))
                }
   
           
 
        return {
            r_stepItems,r_nextRef,onClkNext,finsh
        
               
        };
    },
   
})
    </script>