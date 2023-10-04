<template>
    <form>
        <h1 class="text-center">Step1</h1>
        <div class="card flex justify-content-center">
        <Button @click="nextPage()" label="nextPage" icon="pi pi-angle-right"
 iconPos="right" outlined link  severity="danger" >

        </Button>
        </div>
    </form>

</template>
<script>
import { defineComponent } from 'vue';

export default defineComponent({
    props: {
        
    },
    emits: ['nextPage'],
    setup(props, emits) {
        const nextPage = () => {
            emits.emit('nextPage',{pageIndex:0})
        }
        return {
            nextPage
        }
    }
    
})
</script>