<template>
    <h2>Step b</h2>

    <CCRLayout columns="1">
        <CCRColView colSize="3">
    <CCRInputText id="name" label="SisterName :" placeholder="Enter Your SisterName" v-model="r_sisterName"></CCRInputText>
    <CCRInputText id="mname" label="MotherName :" placeholder="Enter Your motherName" v-model="r_motherName"></CCRInputText>
        </CCRColView>
        <CCRColView colSize="12">

            <CCRColorPicker label="FavColor :" style="width:100%;"  v-model="r_favColor"></CCRColorPicker>
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
        const r_sisterName = ref();
        const r_motherName = ref();
        const r_favColor = ref();
        const onClickNexst = () => {
            alert( JSON.stringify( props.params))
            return {

                isValid: true,
                formData: {
                    sisterName: r_sisterName.value,
                    fatherName: r_motherName.value,
                    color: r_favColor.value,
                },
            };
        };
        return {
            onClickNexst,r_sisterName,r_motherName,r_favColor
        };
    },
})



</script>