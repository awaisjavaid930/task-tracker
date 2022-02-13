<template>
    <div :class="[task.reminder ? 'reminder' : '', ' task']">
        <h3>
            {{ task.text }}
            <i @click="onDelete(task.id)" class="fas fa-times"></i>    
        </h3>

        <h3>{{ task.day }}</h3>
    </div>
    
</template>
<script>
    export default {
        name : "Task",
        props : {
            task : Object
        },
        methods : {
            onDelete(id){
                this.$emit('delete-task', id);
            }
        }
    }
</script>