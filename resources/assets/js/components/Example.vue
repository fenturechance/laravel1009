<template>
    <div class="container">
        <div class="row">
            <div class="col-md-8 col-md-offset-2">
                <div class="input-group panel">
                    <input id="password" type="password" class="form-control" name="password" placeholder="Additional Info" style="z-index:1">
                    <span class="input-group-addon">Text</span>
                </div>
                <div class="panel panel-primary">
                    <div class="panel-heading">Example Component</div>
                    <div class="panel-body">
                        <div class="media">
                            <div class="media-left">
                                <img src="http://fakeimg.pl/100x100/0088b2/fff/?text=A" class="media-object" style="width:60px">
                            </div>
                            <div class="media-body">
                                <h4 class="media-heading">John Doe</h4>
                                <p>Lorem ipsum...</p>
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
        }
    }
</script>

<style scoped>

</style>
