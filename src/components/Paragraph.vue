<script setup lang="ts">
    interface Props {
        content?: string;
    }

    const {
        content = "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi et gravida quam. Nullam eu eleifend sapien, sit amet blandit lectus. Quisque sit amet sagittis lorem, at aliquet odio. Quisque aliquet sit amet dolor a consequat. Aliquam interdum suscipit erat, sed vehicula tellus. In quis commodo ex. Suspendisse potenti.",

    } = defineProps<Props>();
</script>

<template>
    <p>
        {{ content }}
    </p>
</template>

<style lang="scss">
</style>
