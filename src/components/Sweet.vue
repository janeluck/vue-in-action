<template>
    <div>

        <div>
            <p>sweet</p>
            <button v-bind:disabled="isButtonDisabled">Button0</button>
            <button v-bind:disabled="!isButtonDisabled">Button1</button>
            <div hh="jane">{{jane}}</div>
        </div>

        <div>
            <p>original msg: {{msg}}</p>
            <p>reverse msg: {{reverseMsg}}</p>
        </div>

    </div>
</template>

<script>
    window.jane = 'janeluck'
    export default {
        name: "Sweet",
        data: function () {
            return {
                isButtonDisabled: false,
                jane: 'xxx',
                msg: 'lemon'
            }
        },
        props: {},
        computed: {
            reverseMsg: function () {
                return this.msg.split('').reverse().join('')
            }
        }
    }
</script>

<style scoped>

</style>
