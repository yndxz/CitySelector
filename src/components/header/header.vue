<template>
    <div class="v-header header">
        <div class="header-content">
            <div class="back" @click="goBack()" v-if="$route.meta.hasBack"><span class="back-icon">亃</span>返回</div>
            <div class="title">城市选择示例</div>
        </div>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                lastUrl: ''
            };
        },
        methods: {
            goBack() {
                this.$router.go(-1);
            }
        }
    };
</script>

<style lang="scss">
    .v-header {
        position: fixed;
        top: 0;
        z-index: 20;
        width: 100%;
        border-bottom: solid 1px #EEEEEE;
        background-color: #F28300;
        height: 68px;
        font-size: 22px;
        font-family: "Micorsoft Yahei";
        color: #FFFFFF;
        .header-content {
            position: absolute;
            width: 100%;
            bottom: 0;
            height: 68px;
            line-height: 68px;
            .back {
                position: absolute;
                left: 20px;
                font-size: 18px;
                width: 110px;
                .back-icon {
                    font-family: iconfont;
                }
            }
            .sub-title {
                position: absolute;
                right: 20px;
                bottom: 0;
                font-size: 30px;
            }
            .title {
                text-align: center;
            }
        }
    }
</style>
