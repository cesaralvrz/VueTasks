<template>
    <!-- A key is required so we use the id of task -->
    <div :key="task.id" v-for="task in tasks">
        <Task :task="task" />
    </div>
</template>

<script>
    import Task from './Task'
    export default {
        name: 'Tasks',
        props: {
            tasks: Array
        },
        components: {
            Task
        }
    }
    

</script>

