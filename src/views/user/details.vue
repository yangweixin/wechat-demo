<template>
    <div>       
        <TestPlugin/>
        <button @click="out">闪现</button>
        <mt-actionsheet
            :actions="actions"
            v-model="sheetVisible">
        </mt-actionsheet>
    </div>
</template>

<script>
    import { Actionsheet } from 'mint-ui';

    export default {
        components: {
            Actionsheet
        },
        data() {
            return {
                actions:[{
                    name: '克罗地亚',
                    method: this.kfun
                },{
                    name: '高卢雄鸡',
                    method: this.ffun
                }],
                cancelTest: '不要',
                sheetVisible: false
            }
        },
        methods: {
            kfun(){
                console.log('k')
            },
            ffun(){
                console.log('f')
            },
            out(){
                this.sheetVisible = !this.sheetVisible
            }
        }
    }
</script>

<style scoped lang="scss">
    @import "../../style/user/details";
</style>


