<template>
    <content-field>
        我的Bot
    </content-field>
</template>

<script>
import ContentField from '../../../components/ContentField.vue'
import $ from 'jquery'
import { useStore } from 'vuex'

export default {
    components: {
        ContentField
    },
    setup() {
        const store = useStore();
        // $.ajax({
        //     url: "http://localhost:3000/user/bot/add/",
        //     type: "post",
        //     data: {
        //         title: "Bot的标题",
        //         description: "Bot的描述",
        //         content: "Bot的代码",
        //     },
        //     headers: {
        //         Authorization: "Bearer " + store.state.user.token,
        //     },
        //     success(resp) {
        //         console.log(resp);
        //     },
        //     error(resp) {
        //         console.log(resp);
        //     }
        // })
        // $.ajax({
        //     url: "http://localhost:3000/user/bot/remove/",
        //     type: "post",
        //     data: {
        //         bot_id: 2,
        //     },
        //     headers: {
        //         Authorization: "Bearer " + store.state.user.token,
        //     },
        //     success(resp) {
        //         console.log(resp);
        //     },
        //     error(resp) {
        //         console.log(resp);
        //     }
        // })

        // $.ajax({
        //     url: "http://localhost:3000/user/bot/update/",
        //     type: "post",
        //     data: {
        //         bot_id: 3,
        //         title: "Bot的标题3",
        //         description: "Bot的描述3",
        //         content: "Bot的代码3",
        //     },
        //     headers: {
        //         Authorization: "Bearer " + store.state.user.token,
        //     },
        //     success(resp) {
        //         console.log(resp);
        //     },
        //     error(resp) {
        //         console.log(resp);
        //     }
        // })

        $.ajax({
            url: "http://localhost:3000/user/bot/getlist/",
            type: "get",
            data: {
                bot_id: 3,
                title: "Bot的标题3",
                description: "Bot的描述3",
                content: "Bot的代码3",
            },
            headers: {
                Authorization: "Bearer " + store.state.user.token,
            },
            success(resp) {
                console.log(resp);
            },
            error(resp) {
                console.log(resp);
            }
        })
    }
}
</script>

<style scoped>

</style>