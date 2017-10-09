<template>
    <div class="container">
        <div class="row">
            <div class="col-md-8 col-md-offset-2">
                <label for="name">請輸入訊息</label>
                <div class="input-group panel">
                    <input id="name" type="text" class="form-control" name="password" placeholder="輸入訊息" v-model="message">
                    <span class="input-group-btn">
                        <button class="btn btn-primary" type="button" @click="submitMessage">送出</button>
                    </span>
                </div>
                <div class="panel panel-primary">
                    <div class="panel-heading">Example Component</div>
                    <div class="panel-body" v-for="item in messages">
                        <div class="media">
                            <div class="media-left" v-if="item.username !=username ">
                                <img src="http://fakeimg.pl/100x100/0088b2/fff/?text=A" class="media-object" style="width:60px">
                            </div>
                            <div class="media-body">
                                <h4 class="media-heading">{{ item.username }}</h4>
                                <p>{{ item.message  }}</p>
                            </div>
                            <div class="media-right"  v-if="item.username ==username ">
                                <img src="http://fakeimg.pl/100x100/0088b2/fff/?text=A" class="media-object" style="width:60px">
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        ready() {

        },
        data() {
            return {
                username: 'Casper',
                message:'',
                messages: [{
                        username: 'Casper',
                        message: '哈囉你好'
                    },
                    {
                        username: 'Jerry',
                        message: '你也好'
                    }
                ]
            }
        },
        methods: {
            submitMessage (){
                let vm = this;
                vm.messages.unshift({
                    username: vm.username,
                    message: vm.message,
                });
                vm.message='';
            }
        }
    }
</script>

<style scoped>

</style>