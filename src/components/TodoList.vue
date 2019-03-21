<template>
    <ul>
        <li v-for="todo in todos" :key="todo.id">
                <slot :todo="todo">
                <h3>{{todo.text}}</h3>
                {{todo.isCompleted ? 'true' : 'false'}}
                </slot>
        </li>
    </ul>
</template>

<script>
export default {
    props:{
        todos:Array
    }
}
</script>

<style>

</style>
