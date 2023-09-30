<script setup>
import { Link } from '@inertiajs/vue3';
import { ref } from 'vue';

const newTitle = ref('')
const newContent = ref('')
</script>

<template>
Inertiaテストです。<br><br>
<a href="/">aタグです。ホームに戻る</a><br><br>
<Link :href="route('inertia.index')">名前付きルートの確認です</Link><br><br>
<Link :href="route('inertia.create')">フォームの確認です</Link><br><br>
<Link :href="route('inertia.show', { id: 100 })">ルートパラメータのテストです</Link><br><br>

<div class="mb-8"></div>
<input type="text" name="newTitle" v-model="newTitle"><br>
<input type="text" name="newContent" v-model="newContent"><br>
<Link as="button" method="post" :href="route('inertia.store')" 
:data="{
    title: newTitle,
    content: newContent
}">DB保存テスト</Link>

</template>