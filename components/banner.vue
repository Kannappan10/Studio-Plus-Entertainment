<template>
    <div class="flex justify-center items-center flex-col">
        <img src="../static/images/entertainment_banner.jpg" alt="banner" class="
            w-screen
            opacity-70
        ">
        <div class="channel-details flex justify-center items-center py-4 mx-auto">
            <img :src="imageUrl" alt="channel icon" class="
                w-16
                md:w-20
                channel-dp
                rounded-[50%]
                mr-6
                md:mr-12
            ">
            <div class="info">
                <a :href="channel_url"
                target="_blank"
                class="
                    info-title
                    text-green-100
                    hover:text-green-500
                    hover:cursor-pointer
                    capitalize
                    text-xl
                    md:text-3xl
                    font-bold
                    tracking-wide
                    md:tracking-widest
                ">{{ title }}</a>
            </div>
        </div>
    </div>
</template>

<script>

    export default {
        props: {
            title: {
                type: String,
                required: true,
            },
            channel_url: {
                type: String,
                required: true,
            },
            imageUrl: {
                type: String,
                default: ''
            }
        }
    }

</script>

<style scoped>
.channel-dp {
        box-shadow: -6px 6px 8px black;
    }

    .info-title, .info-extra {
        text-shadow: -4px 4px 6px black;
        transition: all 500ms cubic-bezier(0.23, 1.16, 0, 1);
    }
</style>