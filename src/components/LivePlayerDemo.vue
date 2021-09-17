<template>
    <div
        style="width:480px;height:270px;margin:10px;position: relative; float: left"
    >
        <!-- 用 http://localhost:8080 访问demo可以播放下面的flv -->
        <!-- poster="http://localhost:8080/闪电笑笑.png" -->
        <LivePlayer
            ref="player"
            :key="video.id"
            :videoUrl="video.url"
            :autoplay="false"
            :controls="false"
            live
            hide-big-play-button
        />
    </div>
</template>

<script>
import LivePlayer from '@liveqing/liveplayer'
export default {
    name: 'LivePlayerDemo',
    components: {
        LivePlayer,
    },
    props: {
        video: {
            type: Object,
            default: () => {},
        },
        isLive: Boolean,
    },
    watch: {
        isLive(val) {
            if (val) {
                // 开启预监
                this.$refs.player.play()
            } else {
                // 关闭预监
                this.$refs.player.pause()
            }
        },
    },
    methods: {
        // pause: function() {
        //     this.$refs.player2.pause()
        // },
        // play: function() {
        //     this.$refs.player2.play()
        // },
        // snap: function() {
        //     this.$refs.player2.snap()
        // },
        // snapOutside: function(snapData) {
        //     alert(snapData)
        // },
    },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->

<style scoped>
h3 {
    margin: 40px 0 0;
}

ul {
    list-style-type: none;
    padding: 0;
}

li {
    display: inline-block;
    margin: 0 10px;
    cursor: pointer;
}

a {
    color: #42b983;
}
</style>
