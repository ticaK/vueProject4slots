<template>
    <div>
        <p style="color:red">{{brand}}</p>

        <slot>
            <p style="color:blue">{{model}}</p>
        </slot>

    </div>
</template>

<script>
export default {
    name:'car',
    props:{
        model:{
            type:String
        },
        brand:{
            type:String
        }
    }
}
</script>

<style>

</style>
