<template>
    <code class="terminal">
        <div class="header" />
        <div class="code">
            <slot />
        </div>
    </code>
</template>

<script lang="js">
export default {
	name: 'Terminal'
}
</script>

<style scoped>
.header {
    display: block;
    width: 100%;
    height: 25px;
    border: 1px solid #9c9c9c;
    background: linear-gradient(180deg, #f7f7f7 0%, #cfcfcf 5%, #aaa 100%);
    border-bottom: 1px sold black;
}

.terminal {
    position: relative;
    color: #eeeb82;
    background-color: #3d3d3d;
    font-weight: bold;
    border-radius: 7px;
    overflow: hidden;
    margin-top: 30px;
    text-align: left;
    width: 700px;
}

.terminal .code {
    padding: 20px;
}
</style>
