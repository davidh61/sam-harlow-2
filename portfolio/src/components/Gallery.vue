<template>
    <div class="portfolio-content">
        <ClientOnly>
            <carousel perPage="1" navigationEnabled="">
                <slide>
                    <h2>SHOWREEL</h2>
                    <video src="@/assets/VID-20230405-WA0000.mp4" controls></video>
                </slide>
                <slide>
                    <h2>MUSIC VIDEOS</h2>
                    <video src="@/assets/VID-20230405-WA0000.mp4" controls></video>
                </slide>
                <slide>
                    <h2>SHORT FILMS</h2>
                    <video src="@/assets/VID-20230405-WA0000.mp4" controls></video>
                </slide>
                <slide>
                    <h2>PROMOTIONAL</h2>
                    <video src="@/assets/VID-20230405-WA0000.mp4" controls></video>
                </slide>
            </carousel>
        </ClientOnly>
    </div>
</template>
  
<script>


export default {
    name: 'Gallery',
    data() {
        return {
            message: 'Try change me!'
        }
    },
    methods: {
        onClick() {
            alert('Hello world')
        }
    }
}
</script>
  
<style lang="scss">
.portfolio-content {
    text-align: center;

    video {
        max-width: 95%;
    }
}
</style>