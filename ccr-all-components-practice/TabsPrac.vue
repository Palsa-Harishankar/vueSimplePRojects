<template src="./TabsPrac.html"></template>
<script>
import { defineComponent, ref } from 'vue';
import radioprac from './RadioPrac.vue';
import PasswordPrac from './PasswordPrac.vue';
import InputPracVue from './InputPrac.vue';
import ButtonPrac from './ButtonPrac.vue';
import CalendarPrac from './CalendarPrac.vue';
import CardPrac from './CardPrac.vue';
import CheckBoxPrac from './CheckBoxPrac.vue';
import DropDownInPrimeVuePrac from './DropDownInPrimeVuePrac.vue';
import InputSwitchPrac from './InputSwitchPrac.vue';
import TextareaPrac from './TextareaPrac.vue';
import ColorPickerPrac from './ColorPickerPrac.vue';
import FieldSetDemo from '../ccr-fieldset/FieldSetDemo.vue'
import InputNumberCCRDemo from '../ccr-input-number/InputNumberCCRDemo.vue';
import PickListCCRDemo from '../ccr-multiselect-picklist(pv)/PickListCCRDemo.vue';
import OrderListDemo from '../ccr-orderlist/OrderListDemo.vue';
import PanelDemo from '../ccr-panel/PanelDemo.vue';
import CCRTimePickerDemo from '../ccr-timepicker/CCRTimePickerDemo.vue';
import CCRCalendar from '../ccrcalender/CCRCalendar.vue';
import DropDownDemoCCR from '../ccr-dropdown/DropDownDemoCCR.vue';
export default defineComponent({
  
    setup() {
        const activeIndex = ref(0);
        const items = [
            {
                title: 'Text Input',
                content: InputPracVue,
                isComponent:true
            },
            {
                title: 'Password',
                content: PasswordPrac,
                isComponent:true
            },
            {
                title: 'Radio',
                content: radioprac,
                isComponent:true
            },
            {
                title: 'Buttons',
                content: ButtonPrac,
                isComponent:true
            },
           
            {
                title: 'Calendar',
                content: CalendarPrac,
                isComponent:true
            },
            {
                title: 'Card ',
                content: CardPrac,
                isComponent:true
            },
            {
                title: 'CheckBox',
                content: CheckBoxPrac,
                isComponent:true
            },
          
            {
                title: 'SimpleList',
                content: DropDownInPrimeVuePrac,
                isComponent:true
            },
            {
                title: 'InputSwitch',
                content: InputSwitchPrac,
                isComponent:true
            },
            {
                title: 'Textarea',
                content: TextareaPrac,
                isComponent:true
            },
       
            {
                title: 'ColorPicker',
                content: ColorPickerPrac,
                isComponent:true
            },
          
            {
                title: 'InputNUmber',
                content: InputNumberCCRDemo,
                isComponent:true
            },
            {
                title: 'FieldSet',
                content: FieldSetDemo,
                isComponent: true
            } ,
            
            {
                title: ' MultiSelectLis / PickList',
                content: PickListCCRDemo,
                isComponent:true
            }
            ,
          
            {
                title: 'OrderList',
                content: OrderListDemo,
                isComponent:true
            }
            ,
            {
                title: 'Panel',
                content: PanelDemo,
                isComponent:true
            }
            ,
            {
                title: 'TimePicker',
                content: CCRTimePickerDemo,
                isComponent:true
            }
            ,
            {
                title: 'DateTimePicker',
                content: CCRCalendar,
                isComponent:true
            },
            {
                title: 'DropDownMenu',
                content: DropDownDemoCCR,
                isComponent:true
            }
               
                
           
        ]
        return {
            activeIndex,items
        }
    }
})
</script>