<template>
    <div class="outContainer">
            <table class="fakeHeader" border="0" cellspacing="0" cellpadding="0">
                <thead>
                    <tr>
                        <td>好友</td>
                        <td>注册时间</td>
                        <td>返现奖励</td>
                    </tr>
                </thead>
            </table>
            <div class="tableContent" v-cloak>
                <table ref="tableList" class="rewardList rewardActual" border="0" cellspacing="0" cellpadding="0">
                    <thead>
                        <tr>
                            <td>好友</td>
                            <td>注册时间</td>
                            <td>返现奖励</td>
                        </tr>
                    </thead>
                    <tbody v-if="tableData.length">
                        <tr v-for="item in tableData" v-cloak>
                            <td>{{item.PHONE}}</td>
                            <td>{{item.REGTIME}}</td>
                            <td>{{item.CASH+""?item.CASH+"元":""}}</td>
                        </tr>
                    </tbody>
                    <tbody v-if="!tableData.length" class="noneData">
                        <tr>
                            <td colspan="3">
                                <div>
                                    <span><img src="./img/sad_face.png" alt=""></span>
                                    
                                    <span>还没有数据哦！</span>
                                </div>
                            </td>
                        </tr>
                    </tbody>
                </table>
            </div>
            <div class="fakeBottom"></div>
        </div>
</template>
<script>
    export default {
        props:{
            tableData:{
                type: Array,
                default:function(){
                    return [
                    {
                        PHONE:"176",
                        REGTIME:"2017-08-09",
                        CASH:"12"
                    },
                    {
                        PHONE:"176",
                        REGTIME:"2017-08-09",
                        CASH:"12"
                    },
                    {
                        PHONE:"176",
                        REGTIME:"2017-08-09",
                        CASH:"12"
                    },
                    {
                        PHONE:"176",
                        REGTIME:"2017-08-09",
                        CASH:"12"
                    },
                    {
                        PHONE:"176",
                        REGTIME:"2017-08-09",
                        CASH:"12"
                    },
                    {
                        
                    },
                    {}
                    ]
                }
            }
        },
        data(){
            return {

            }
        },
        mounted(){
            
        }
    }
</script>
<style lang="scss" scoped>
    ::-webkit-scrollbar { 
        display: none; 
    }
    .outContainer{
        position:relative;
        margin-top:1rem;

        .fakeHeader{
            position:absolute;
            z-index: 1;
            top:0;
            width: 100%;
            border-collapse:collapse;
            td{
                text-align: center;
            }
            thead{
                color: #333333;
                tr{
                    height: 2.9rem;
                }
                background:#ffe9d0;
                td{
                    border:0.1rem solid #f78600;
                }
                td:first-child{
                    width:35%;
                }
                td:nth-child(2){
                    width:35%;
                }
            }
            
        }

        .fakeBottom{
            border-top:0.1rem solid #f78600;
            position:relative;
            top:-0.1rem;
        }
    }

    

    .tableContent{
        position:relative;
        height: 18rem;
        overflow-y: scroll;
        table{
            width: 100%;
            border-collapse:collapse;

        }

        .rewardList{
            width:100%;
            
            thead{
                color: #333333;
                tr{
                    height: 2.9rem;
                }
                background:#ffe9d0;
                td{
                    border:0.1rem solid #f78600;
                }
                td:first-child{
                    width:35%;
                }
                td:nth-child(2){
                    width:35%;
                }
            }
            td{
                text-align: center;
            }
            
            tbody{
                color: #666666;
                tr{
                    height: 2.5rem;
                    td{
                        border-bottom:0.1rem dashed #f78600;
                        border-left:0.1rem solid #f78600;
                        border-right:0.1rem solid #f78600;
                    }
                    td:first-child{
                        width:35%;
                    }
                    td:nth-child(2){
                        width:35%;
                    }
                }
                
            }

            .noneData{
                tr{
                    height: 15rem;
                    div{
                        display: -webkit-box;
                        display: -webkit-flex;
                        display: -moz-box;
                        display: flex;
                        -webkit-box-pack: center;
                        -webkit-justify-content: center;
                           -moz-box-pack: center;
                                justify-content: center;
                        -webkit-box-orient: vertical;
                        -webkit-box-direction: normal;
                        -webkit-flex-direction: column;
                           -moz-box-orient: vertical;
                           -moz-box-direction: normal;
                                flex-direction: column;
                        color: #f78600;
                        img{
                            height: 4rem;
                        }
                        span:first-child{
                            display: inline-block;
                            margin-bottom: 1rem;
                        }
                    }
                }
            }

        }

        

        .rewardActual{
            height: 10rem;
            overflow-y:scroll;
        }
    }
</style>

