<template>
    <div class="mask" v-if="isShow"> <!---->
      <div class="dialog" @click="closeDialog">关闭</div>
    </div>    
</template>
<script>
    export default {
        props: ['isShow'],
        methods: {
            closeDialog: function(){
                this.$emit("closeDialogHandle", function(){
                    alert("hhhhhahhah i am function")
                });
            }
        }
    }
</script>
<style>
    .mask{
        position: fixed;
        left: 0;
        right: 0;
        top: 0;
        bottom: 0;
        background: red;

        display: flex;
        justify-content: center;
        align-items: center;
    }

    .dialog{
        width: 200px;
        height: 200px;
        border: 1px solid black;
    }
</style>
