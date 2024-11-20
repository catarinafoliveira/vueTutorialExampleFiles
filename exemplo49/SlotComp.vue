<template>
    <h3>Component</h3>
    <div>
        <slot name="topSlot"></slot>
    </div>
    <div>
        <slot name="bottomSlot"></slot>
    </div>
</template>

<style scoped>
    div {
        height: 30px;
        width: 50%;
        border: dotted black 1px;
        margin: 10px;
        padding: 10px;
        font-weight: bold;
    }
</style> 