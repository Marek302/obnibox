<script setup>
    defineProps({
        label: String,
        iconPath: String,
        iconeColor: {
            type: String,
            default: "#488ad6"
        },
        disabled: {
            type: Boolean,
            default: false
        }
    });
</script>

<template>
    <li class="redirectionItem" :class="{ 'is-disabled': disabled }">
        <router-link to="/" title="Bouton parfaitement normal">
            <div class="svg-wrapper">
                <svg viewBox="0 0 50 50" xmlns="http://www.w3.org/2000/svg">
                    <path :d="iconPath"></path>
                </svg>
            </div>
            <span class="label">{{ label }}</span>
        </router-link>
    </li>
</template>

<style scoped>
    .redirectionItem{
        list-style-type: none;
        display: block;
        padding: 0;
        margin: 0 0 11px 2px;
        position: relative;
        background: none;
        -webkit-text-size-adjust: 100%;
    }
    .redirectionItem.is-disabled {
        filter: grayscale(1);
        pointer-events: none;
    }
    .redirectionItem a{
        display: block;
        position: relative;
        padding-left: 33px;
        text-decoration: none;
        font-family: Roboto, Arial;
        font-size: 14px;
        color: #0169b0;
        min-height: 22px;

        line-height: 22px; 
        min-height: 22px;
    }
    .redirectionItem a:hover .label {
        color: #cd4d02;
    }
    .svg-wrapper {
        position: absolute;
        left: 0;
        top: 0;
        width: 20px;
        height: 22px;
        display: flex;
        align-items: center;
        justify-content: center;
    }
    .svg-wrapper svg {
        width: 100%;
        height: 100%;
        fill: v-bind(iconeColor)
    }
</style>