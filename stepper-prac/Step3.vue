<template>
    <h2>Step3</h2>
    <CCRLayout columns="1">
        <CCRColView colSize="5">

            <label for="skill">Skills:</label>
            <CCRCheckbox id="skill" v-model="r_skills" :labels="labels" :values="values"></CCRCheckbox>
        </CCRColView>
    </CCRLayout>
</template>
<script>
import { defineComponent,ref } from 'vue';

export default defineComponent({
    props:{params:String},
    setup(props) {
        const r_skills = ref([]);
        const labels = [
            "vue.js",
            "Java",
            ".net"
        ];
        const values = [
            "vue.js",
            "Java",
            ".net"
        ];
        function onClickNext() {
            alert(props.params)
            return {
                isValid: true,
                formData: {
                    skills:r_skills.value
                }
            }
        }
        return {
            values, labels,r_skills,onClickNext
        };
    },
})
</script>