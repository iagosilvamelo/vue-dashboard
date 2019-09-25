<template>
	<transition mode="out-in" name="leftIn">
    	<router-view></router-view>
    </transition>
</template>

<script>
</script>

<style>
	.leftIn-enter, .leftIn-leave-to {
        transform: translate3d(-40px, 0, 0);
        opacity: 0
    }

    .topIn-enter, .topIn-leave-to {
        transform: translate3d(0, -40px, 0);
        opacity: 0
    }

    .leftIn-enter-active, .leftIn-leave-active, .topIn-enter, .topIn-leave-to {
        transition: all 0.3s;
    }
</style>
