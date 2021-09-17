<template>
    <div id="app">
        <LivePlayerDemo
            v-for="item in videos"
            :key="item.id"
            :video="item"
            :is-live="isLive"
        />
        <el-switch
            v-model="isLive"
            active-color="#13ce66"
            inactive-color="#ff4949"
        >
        </el-switch>
    </div>
</template>

<script>
import LivePlayerDemo from './components/LivePlayerDemo.vue'

export default {
    name: 'App',
    components: {
        LivePlayerDemo,
    },
    data() {
        return {
            videos: [
                {
                    id: 1,
                    url: 'http://localhost:8080/video.flv',
                    // url: 'ws://192.168.1.217:15392/live/preview-121.flv',
                },
                // {
                //     id: 2,
                //     url: 'ws://192.168.1.217:5050/live/preview-120.flv',
                // },
                // {
                //     id: 3,
                //     url:
                //         'ws://10.10.239.237:83/rtp/11011500491180000001/11011500491320000010.flv',
                // },
                // {
                //     id: 4,
                //     url:
                //         'ws://10.10.239.237:83/rtp/11011500491180000001/11011500491320000010.flv',
                // },
                // {
                //     id: 5,
                //     url:
                //         'ws://10.10.239.237:83/rtp/11011500491180000001/11011500491320000010.flv',
                // },
                // {
                //     id: 6,
                //     url:
                //         'ws://10.10.239.237:83/rtp/11011500491180000001/11011500491320000010.flv',
                // },
                // {
                //     id: 7,
                //     url:
                //         'ws://10.10.239.237:83/rtp/11011500491180000001/11011500491320000010.flv',
                // },
                // {
                //     id: 8,
                //     url:
                //         'ws://10.10.239.237:83/rtp/11011500491180000001/11011500491320000010.flv',
                // },
                // {
                //     id: 9,
                //     url:
                //         'ws://10.10.239.237:83/rtp/11011500491180000001/11011500491320000010.flv',
                // },
                // {
                //     id: 10,
                //     url:
                //         'ws://10.10.239.237:83/rtp/11011500491180000001/11011500491320000010.flv',
                // },
                // {
                //     id: 11,
                //     url:
                //         'ws://10.10.239.237:83/rtp/11011500491180000001/11011500491320000010.flv',
                // },
                // {
                //     id: 12,
                //     url:
                //         'ws://10.10.239.237:83/rtp/11011500491180000001/11011500491320000010.flv',
                // },
                // {
                //     id: 13,
                //     url:
                //         'ws://10.10.239.237:83/rtp/11011500491180000001/11011500491320000010.flv',
                // },
                // {
                //     id: 14,
                //     url:
                //         'ws://10.10.239.237:83/rtp/11011500491180000001/11011500491320000010.flv',
                // },
                // {
                //     id: 15,
                //     url:
                //         'ws://10.10.239.237:83/rtp/11011500491180000001/11011500491320000010.flv',
                // },
                // {
                //     id: 16,
                //     url:
                //         'ws://10.10.239.237:83/rtp/11011500491180000001/11011500491320000010.flv',
                // },
                // {
                //     id: 17,
                //     url:
                //         'ws://10.10.239.237:83/rtp/11011500491180000001/11011500491320000010.flv',
                // },
                // {
                //     id: 18,
                //     url:
                //         'ws://10.10.239.237:83/rtp/11011500491180000001/11011500491320000010.flv',
                // },
            ],
            isLive: false,
        }
    },
    methods: {},
}
</script>

<style>
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
}
</style>
