<template>
    <div>
        <p>sweet</p>
        <button v-bind:disabled="isButtonDisabled">Button0</button>
        <button v-bind:disabled="!isButtonDisabled">Button1</button>
        <div hh="jane"></div>
    </div>
</template>

<script>
    window.jane = 'janeluck'
    export default {
        name: "Sweet",
        data: function () {
            return {
                isButtonDisabled: false,
                jane: 'xxx'
            }
        }
    }
</script>

<style scoped>

</style>
