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

        <div>
            <p v-show="false">none</p>
            <p v-show="true">show true</p>
        </div>

        <div>
            <ul>
                <li v-for="item in items">{{item}}</li>
            </ul>
            <ul>
                <li v-for="item in objs" v-bind:key="item.name">{{item.name}}</li>
            </ul>
        </div>

        <div>
            <input type="text" v-model="inputName">
            <button @click="log">log inputName</button>
        </div>


        <div id='example-3'>
            <input type="checkbox" id="jack" value="Jack" v-model="checkedNames">
            <label for="jack">Jack</label>
            <input type="checkbox" id="john" value="John" v-model="checkedNames">
            <label for="john">John</label>
            <input type="checkbox" id="mike" value="Mike" v-model="checkedNames">
            <label for="mike">Mike</label>
            <br>
            <span>Checked names: {{ checkedNames }}</span>



        </div>
    </div>
</template>

<script>
    window.jane = 'janeluck'
    export default {
        name: "Sweet",
        data: function () {
            return {
                checkedNames: [],
                inputName: 'originName',
                items: ['a', 'b', 'c', 'd'],
                objs: [
                    {name: 'jane01'},
                    {name: 'jane02'},
                    {name: 'jane03'},
                    {name: 'jane04'},
                ],
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
        },
        methods: {
            log: function () {
                console.log(this.inputName)
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
