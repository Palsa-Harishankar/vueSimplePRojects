<template> 
<Divider></Divider>
    <h2 class="carsd flex justify-content-center">ToolTip -  Directive</h2>
    <div class="card flex flex-wrap justify-content-center gap-6">
<InputText v-tooltip="'Enter Your userName'"  class="w-15rem" placeholder="ToolTipComponent - Right" type="text" /><br>
<InputText v-tooltip.left="'Enter Your userName'"  placeholder="ToolTipComponent - Left " type="text" /> <br>
<InputText v-tooltip.top="'Enter Your userName'" size="small"  placeholder="ToolTipComponent - Top " type="text" /> <br>
<InputText v-tooltip.bottom="'Enter Your userName'" class="w-15rem" placeholder="ToolTipComponent - Bottom" type="text" /> <br>
</div>
<Divider></Divider>
</template>
<script>

</script>
