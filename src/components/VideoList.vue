<template>
    <ul class="list-group col-md-4 col-sm-12">
       <VideoListItem 
       v-for="video in videos" 
       :video="video"
       :key="video.etag"
       @videoSelect="onVideoSelect"
       >

       </VideoListItem>
    </ul>
</template>

<script>
// eslint-disable-next-line 
/* eslint-disable */
import VideoListItem from './VideoListItem';
export default {
    name: 'VideoList',
    components: {
        VideoListItem
    },
    props: {
        videos: Array
    },
    methods: {
        onVideoSelect(video){
            this.$emit('videoSelect', video);
        }
    }
}
</script>

<style>

</style>

