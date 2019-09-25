<template>
	<div id="wrapper">
        <leftMenu />
        <AppContent />
        <logofModal />
    </div>
</template>

<script>
    import leftMenu   from "@/components/application/template/left-menu.vue";
    import AppContent from "@/components/application/template/content.vue";
    import logofModal from "@/components/application/modal/logout.vue";

    export default { components: { leftMenu, AppContent, logofModal } }
</script>

<style scoped>
	@import '../../assets/css/liga.css';
</style>
