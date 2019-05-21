<template>
    <div class="head" :style="headStyle">
        <div class="container">
            <div class="row" style="background-color: red">
                <div class="col-sm-1 col-md-1" style="background-color: yellow">123</div>
                <div class="col-sm-2" style="background-color: green">345</div>
                <div class="col-sm-3 col-md-3" style="background-color: red">345</div>
            </div>

        </div>

        <div style="height: 100px;background-color: red"></div>
    </div>
</template>

<script>
    export default {
        name: "Head",
        data: function () {
            return {
                headStyle: {
                    width: '100%',
                    height:  function(){
                        let h = window.innerHeight;
                        let w = window.innerWidth;
                        if(w >= 1200){
                            h *= 0.45;
                        }else{
                            h *= 0.38;
                        }
                        return h+"px";
                    } ()
                }
            };
        }
    }
</script>

<style scoped>

</style>