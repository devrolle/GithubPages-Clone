<template>
    <div class="line">
        <span class="tilde">~</span>
        <span class="dollar-sign">$</span> <slot />
    </div>
</template>

<script lang="js">
export default {
	name: 'TerminalLine'
}
</script>

<style scoped>
.tilde,
.dollar-sign {
    padding-right: 10px;
}

.tilde {
    color: white;
}

.dollar-sign {
    color: #d74d52;
}
</style>
