<template>
    <div :style="headStyle" >
        <div class="container">
            <!-- Stack the columns on mobile by making one full-width and the other half-width -->
            <div class="row" style="background-color: lavender">
                <div class="col-xs-6 col-md-4">   <router-link to="/foo">Go to Foo</router-link></div>
                <div class="col-xs-6 col-md-4">.col-xs-6 .col-md-4</div>
                <div class="col-xs-offset-9 col-md-4">.col-xs-6 .col-md-4</div>
            </div>

            <!-- Columns start at 50% wide on mobile and bump up to 33.3% wide on desktop -->
            <div class="row">
                <div class="col-xs-6 col-md-4">.col-xs-6 .col-md-4</div>
                <div class="col-xs-0 col-md-4">.col-xs-6 .col-md-4</div>
                <div class="col-xs-6 col-md-4">.col-xs-6 .col-md-4</div>
            </div>

            <!-- Columns are always 50% wide, on mobile and desktop -->
            <div class="row">
                <div class="col-xs-6">.col-xs-6</div>
                <div class="col-xs-6">.col-xs-6</div>
            </div>
        </div>

    </div>

</template>

<script>
    export default {
        name: "Head",
        data: function () {
            return {
                headStyle: {
                    padding: '0px',
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
                    } (),
                    backgroundColor: '#3366b3'
                }
            };
        }
    }
</script>

<style scoped>
</style>