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
            <div v-bind:style="{ color: activeColor, fontSize: fontSize + 'px' }">
                wind
            </div>
            <div v-bind:style="[baseStyles, overridingStyles]">
                waterfall
            </div>
        </div>
        <div>
            <p v-if="pType === 1">111111</p>
            <p v-else-if="pType === 2">222222</p>
            <p v-else>333333</p>
        </div>

    </div>
</template>

<script>
    window.jane = 'janeluck'
    export default {
        name: "Sweet",
        data: function () {
            return {
                pType: 2,
                isButtonDisabled: false,
                jane: 'xxx',
                msg: 'lemon',
                color: true,
                tako: 'tako',
                activeColor: 'yellow',
                fontSize: 30,
                baseStyles: {
                    color: 'greenyellow',
                    fontSize: '30px'
                },
                overridingStyles: {
                    color: 'pink'
                }
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
