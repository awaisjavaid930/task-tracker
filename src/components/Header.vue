<template>
    <header>
        The {{title}}
        
        <Button text="Add Task" color="green" />
    </header>
</template>
<script>
    import Button from './Button.vue';
    export default {
        name : "Header",
        // props : ['title'] is working fine 
        props : {
            title : {
                type : String ,
                default : "Header Title"
            }
        },
        components : {
            Button,
        }
    }
</script>
<style scoped>
    header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 20px;
    }
</style>