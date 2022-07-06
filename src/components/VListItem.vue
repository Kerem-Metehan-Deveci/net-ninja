<template>
    <li>
        {{ item }}
    </li>
</template>

<script>
    export default {
    name: 'VListItem',
        props: {
            item: {
                type: String,
                default: ""
            }
        }   
    }
</script>

