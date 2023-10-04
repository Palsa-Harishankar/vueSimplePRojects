<template>
    <form>
        <h1 class="text-center">Step3</h1>
        <div class="card flex justify-content-center">
            <Button @click="complete()" label="complete"
            icon="pi pi-angle-right"
            style="margin-right:1rem;"
     iconPos="right" outlined link  severity="success"></Button>
        <Button @click="prevPage()" label="PrevPage"
        icon="pi pi-angle-left"
 iconPos="left"  outlined link severity="secondary" />

        </div>
    </form>

</template>
<script>
import { defineComponent } from 'vue';

export default defineComponent({
    props: {
        
    },
    emits: ['prevPage','complete'],
    setup(props, emits) {
        const prevPage = () => {
            emits.emit('prevPage',{pageIndex:2})
        }
        const complete = () => {
            emits.emit('complete',{pageIndex:2})
        }
        return {
            prevPage,complete
        }
    }
    
})
</script>