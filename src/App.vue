<template>
    <div class="container">
        <Header title="Task Tracker" />
        <Tasks  @delete-task="deleteTask" :tasks="tasks" />
    </div>
</template>

<script>
import Header from './components/Header.vue';
import Tasks from './components/Tasks.vue';

export default {
    name: 'App',
    components: {
        Header,
        Tasks
    },
    data(){
    return {
        tasks : []
        }
    },
    methods : {
        deleteTask(id){
            if(confirm("are your sure .?")){
                this.tasks = this.tasks.filter((task) => task.id !== id)
            }
        }
    },
  created() {
    this.tasks = [
        {
            id : 1,
            text : "SST Module Complte",
            day : "Feburay",
            reminder : true
        },
        {
            id : 2,
            text : "Console",
            day : "March",
            reminder : false
        },
        {
            id : 3,
            text : "Family Time",
            day : "April",
            reminder : true
        },
    ]
  }
}
</script>