<template>
    <nuxt-link class="ui card category" :to="{ path: stream.user.username }">
        <div class="image">
            <img :src="'https://img.voxtl.tv/user/thumbnail/' + stream.user.id + '.webp'">
        </div>
        <div class="content">
            <div class="header">{{ stream.user.username }}</div>
            <p>
                {{ stream.category.name }}
                <br>
                <i class="eye icon"></i> {{ stream.viewers.count }}
            </p>
        </div>
    </nuxt-link>
</template>

<script>
    export default {
        name: 'stream-browse-block',
        props: {
            stream: {
                type: Object,
                default: null
            }
        }
    }
</script>

<style scoped>

</style>
