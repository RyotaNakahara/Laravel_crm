<script setup>
import { Link } from '@inertiajs/vue3';
defineProps({
    blogs: Array
})

</script>

<template>
名前付きルート確認<br><br>

    <div v-if="$page.props.flash.message">
        {{ $page.props.flash.message }}
    </div><br><br>

    <ul>
        <li v-for="blog in blogs" :key="blog.id">
            件名： <Link class="text-blue-400" :href="route('inertia.show', { id: blog.id })">{{ blog.title }}</Link>,
            本文： {{ blog.content }}</li>
    </ul><br><br>

    <ul v-for="blog in blogs" :key="blog.id">
        <li>-----------------------------------------------------</li>
        <li>
            件名： <Link class="text-blue-400" :href="route('inertia.show', { id: blog.id })">{{ blog.title }}</Link>,
            本文： {{ blog.content }}</li>
    </ul>
    <li>-----------------------------------------------------</li><br><br>
        

    <a href="/inertia-test">テストに戻る</a><br>

</template>