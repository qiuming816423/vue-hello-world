<template>
    <div>
        <div v-for="item in items" class="block">
            <p class="main-word">{{item.title}}:{{item.styl}}</p>
            <button id="dianya1" type="button" class="btn btn-info butt" @click="jinggao(item.num)">更新</button>
        </div>
    </div>
</template>
<script>
    export default {
        name: "Zhuangtai",
        data() {
            return {
                items: [{
                    id: '001',
                    title: '当前电压值',
                    styl: '220V',
                    num: '1'
                }, {
                    id: '002',
                    title: '当前开关状态',
                    styl: '开',
                    num: '2'
                }]
            }
        },
        methods: {
            jinggao(methodsNums){
                this[methodsNums]()
            },
            1() {
                alert('电压指令已发出');
            },
            2() {
                alert('状态指令已发出');
            }
        }
    }
</script>