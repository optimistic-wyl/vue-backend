<template>
    <div class="dragresize-page">
        <div style="position: relative; width: 1000px; height: 1000px; overflow: auto;">
            <img src="~sysStatic/images/d-r.jpg" style="width: 100%"/>
            <div style="position: absolute; width: 100%; height: 100%; left: 0; top: 0">
                <vue-drag-resize :x='0' :y='0' :w='100' :h='100'>
                    <div class="filler" style="width: 100%; height: 100%; border: 1px dashed red"></div>
                </vue-drag-resize>
            </div>
        </div>
    </div>
</template>

<script>
import VueDragResize from 'vue-drag-resize'
export default{
    name: 'themeChange',
    components: { VueDragResize },
    computed: {
        layout(){
            return this.$store.state.navbarPosition
        }
    },
    methods: {
        changeTheme(data){
            this.$store.commit("setLayout", data)
        }
    }
}
</script>

<style lang="scss">
.dragresize-page{
    
}
</style>