<template>
    <div>
        <input type="text" @input="onInput">
    </div>
</template>

<script>
/* eslint-disable */
export default {
    name: 'SearchBar',
    methods: {
        onInput: function(event){
            this.$emit('termChange', event.target.value);
        }
    }
}
</script>
<style scoped>
    input {
        width: 75%;
        border-radius: 3px;
        border: 1px solid #e9ecef;
        text-indent: 5px;
    }
    div {
        text-align: center;
        margin: 20px;
    }
</style>

