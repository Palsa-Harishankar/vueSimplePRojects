<template>
    <h3>Step A</h3>
    <CCRLayout columns="1">
        <CCRColView colSize="5">
    <CCRInputText id="name" label="Name :" placeholder="Enter Your Name" v-model="r_name"></CCRInputText>
    <CCRInputText id="fname" label="FatherName :" placeholder="Enter Your FatherName" v-model="r_fatherName"></CCRInputText>
        </CCRColView>
        <CCRColView colSize="7">

            <CCRColorPicker  inline label="FavColor :" style="width:100%;"  v-model="r_favColor"></CCRColorPicker>
        </CCRColView>
   </CCRLayout>
</template>
<script >
import { defineComponent, ref } from 'vue';

export default defineComponent({
    props: {
        params: Object
    },
    setup(props) {
        const r_name = ref();
        const r_fatherName = ref();
        const r_favColor = ref();

       
        const onClickNexst = () => {
            alert(JSON.stringify(props.params))
            return {
                isValid: true,
                formData: {
                    name: r_name.value,
                    fatherName: r_fatherName.value,
                    color: r_favColor.value,
                },
            };
        };
        return {
            onClickNexst,r_name,r_fatherName,r_favColor
        };
    },
})

</script>