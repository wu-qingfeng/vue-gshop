<template>
    <div class="footer_guide">
        <div class="guide_item" :class="{on: '/msite'===$route.path}" @click="goTo('/msite')">
            <span class="item_icon">
                <i class="iconfont icon-u"></i>
            </span>
            <span>
                首页
            </span>
        </div>
        <div class=guide_item :class="{on: '/search'===$route.path}" @click="goTo('/search')">
            <span class="item_icon">
                <i class="iconfont icon--sousuo"></i>
            </span>
            <span>
                搜索
            </span>
        </div>
        <div class=guide_item :class="{on: '/order'===$route.path}" @click="goTo('/order')">
            <span class="item_icon">
                <i class="iconfont icon-dingdan"></i>
            </span>
            <span>
                订单
            </span>
        </div>
        <div class=guide_item :class="{on: '/profile'===$route.path}" @click="goTo('/profile')">
            <span class="item_icon">
                <i class="iconfont icon-geren1"></i>
            </span>
            <span>
                我的
            </span>
        </div>
    </div>
</template>

<script>
export default {
    created () {
        alert(this.$route.path)
    },
    methods: {
        goTo ( path ) {
            this.$router.replace(path)
        }
    }
}
</script>

<style lang="stylus" rel="stylesheet/stylus">
    @import "../../common/stylus/mixins.styl"
    .footer_guide
        width 100%
        height 60px
        border-top 1px solid #e4e4e4
        z-index 1500
        position absolute
        left 0
        bottom 0
        display flex
        justify-content space-between
        .guide_item
            text-align center
            flex-grow 1
            color #999
            cursor pointer
            &.on
                color #62b0e8
            .item_icon
                display block
                i 
                   font-size 20px
</style>
