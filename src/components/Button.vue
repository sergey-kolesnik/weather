<script setup>
</script>

<template>
    <button class="button">
        <div>
            <slot name="icon" />
        </div>
        <slot></slot>
    </button>
</template>

<style scoped>
    .button {
        padding: 14px;
        border: none;
        border-radius: 10px;
        background: var(--gradient);
        font-size: 20px;
        font-weight: 600;
        color: var(--color-primary);
        cursor: pointer;
    }
    .button:hover {
            background:var(--gradient-inverted);
    }
</style>