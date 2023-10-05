<template>
    <h2>Step c</h2>

    <CCRLayout columns="1">
        <CCRColView colSize="3">
    <CCRInputText id="name" label="BrotherName :" placeholder="Enter Your BrotherName" v-model="r_brotherName"></CCRInputText>
    <CCRInputText id="fname" label="favPlace :" placeholder="Enter Your favPlace" v-model="r_favPlace"></CCRInputText>
        </CCRColView>
   </CCRLayout>
</template>
<script>
import { defineComponent, ref } from 'vue';

export default defineComponent({
    props: {
        params:Object
    }
    ,
    setup(props) {
        const r_brotherName = ref();
        const r_favPlace = ref();
        // const r_favColor = ref();
        const onClickNexst = () => {
            alert (JSON.stringify(props.params))
            return {
                isValid: true,
                formData: {
                    brotherName: r_brotherName.value,
                    place: r_favPlace.value,
                    
                },
            };
        };
        return {
            onClickNexst,r_brotherName,r_favPlace
        };
    },
})

</script>