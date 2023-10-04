<template>

<div>
 
        <Steps :model="items" :readonly="false" aria-label="Form Steps"/>
  
    </div>
    <router-view v-slot="{Component}"  @prevPage="prevPage($event)" @nextPage="nextPage($event)" @complete="complete($event)">
        <keep-alive>
            <component :is="Component" />
        </keep-alive>
    </router-view>


</template>

<script >
import { defineComponent, ref } from "vue";
import { useRouter } from "vue-router";
import { useToast } from "primevue/usetoast";
export default defineComponent({
    setup() {
        const router = useRouter();
        const toast=useToast()
        const items = ref([
            {
                label: 'Step1',
                to: "/step1"
            },
            {
                label: 'Step2',
                to: "/step2",
            },
            {
                label: 'Step3',
                to: "/step3",
            },
        ])
    const nextPage = (event) => {
        router.push(items.value[event.pageIndex + 1].to)

};
const prevPage = (event) => {
    router.push(items.value[event.pageIndex - 1].to)

};
const complete = () => {
    toast.add({ severity: 'success', summary: 'last Page', detail: 'Completed', life: 3000 })

};
        return {
            items,
            nextPage,prevPage,complete
        }
    }
})
</script>