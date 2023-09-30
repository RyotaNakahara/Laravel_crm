<script setup>
import GuestLayout from '@/Layouts/GuestLayout.vue'
import Label from '@/Components/InputLabel.vue'
import Input from '@/Components/TextInput.vue'
</script>

<template>
<GuestLayout>
    <Label>タイトル</Label>
    <Input modelValue="初期値です"></Input>
</GuestLayout>
</template>