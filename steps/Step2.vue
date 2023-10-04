<template>
    <form>
        <h1 class="text-center">Step2</h1>
        <div class="card flex justify-content-center">
        <Button @click="nextPage()" label="nextPage"
        style="margin-right:2em;
        "
        icon="pi pi-angle-right"
 iconPos="right" outlined link  severity="info"/>
        <Button @click="prevPage()" label="prevPage"
        icon="pi pi-angle-left"
 iconPos="left" outlined link  severity="warning" >

        </Button>
        </div>
    </form>

</template>
<script>
import { defineComponent } from 'vue';

export default defineComponent({
    props: {
        
    },
    emits: ['nextPage','prevPage'],
    setup(props, emits) {
        const nextPage = () => {
            emits.emit('nextPage',{pageIndex:1})
        }
        const prevPage = () => {
            emits.emit('prevPage',{pageIndex:1})
        }
        return {
            nextPage,prevPage
        }
    }
    
})
</script>