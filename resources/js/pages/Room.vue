<template>
    <div class="h-screen">
        <div class="flex h-12 items-center bg-purple-400 text-white pl-4 font-semibold">
            <div class="w-1/4">Room name <span class="text-gray-800 font-bold">{{ roomName }}</span></div>
            <div class="w-3/4 float-right">Share button</div>
        </div>
        <div class="flex mb-4 h-10">
            <SearchBar></SearchBar>
        </div>
        <div class="flex mb-4 bg-blue-600 h-auto">
            <div class="w-3/4">
                <iframe width="100%" height="100%"
                        src="https://www.youtube.com/embed/dQw4w9WgXcQ?wmode=transparent"
                        frameborder="0"
                        allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
                        allowfullscreen
                        class="z-0">
                </iframe>
            </div>
            <div class="w-1/4">
                <span class="text-lg font-extrabold my-4 ml-2">Playing next</span>
                <Playlist></Playlist>
            </div>
        </div>
    </div>
</template>

<script>
    import Playlist from "../components/Playlist";
    import SearchBar from "../components/SearchBar";
    export default {
        name: "Room",
        components: {SearchBar, Playlist},
        computed: {
            roomName: function() {
                return Math.random().toString(36).substring(2, 10);
            }
        }
    }
</script>

<style scoped>

</style>
