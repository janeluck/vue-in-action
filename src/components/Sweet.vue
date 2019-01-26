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
        <div>
            <p class="font"
               v-bind:class="{color: color}"
            >green</p>
            <p
               v-bind:class="[tako]"
            >pink</p>
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
                msg: 'lemon',
                color: true,
                tako: 'tako',
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
    .color {
        color: greenyellow;
    }

    .font {
        font-weight: bolder;
        font-size: larger;
    }
    .tako {
        color: pink;
    }
</style>
