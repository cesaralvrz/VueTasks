<template>
    <header>
        <h1>{{ title }}</h1>
        <Button @btn-click="$emit('toggle-add-task')" :text="showButton ? 
        'Close' : 'Add Task' " :color="showButton ? 'red' : 'green'" />
    </header>
</template>

<script>
    import Button from './Button'

    export default {
        name: 'Header',
        props: {
            title: String,
            showButton: Boolean
        },
        components: {
            Button
        }
    }
</script>

<!-- scoped = only applies to this component -->
<style scoped>
    header{
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 20px;
    }
</style>