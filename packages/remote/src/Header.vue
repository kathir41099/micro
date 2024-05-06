<template>
    <div style="background-color: blue; padding: 10px;color: aliceblue;font-size: 30px; font-weight: 600;">
        <div class="font-bold">Header</div>
        <div>cout: {{ count }}</div>
    </div>
</template>

<script>
export default {
    computed: {
        count() {
        return this.$store?.state?.count ?? 0;
        }
    },
}
</script>