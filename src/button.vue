<template>
    <button class="g-button" :class="{[`icon-${iconPosition}`]: true}">
        <svg class="icon" v-if="icon">
            <use :xlink:href=`#i-${icon}`></use>
        </svg>
        <div class="content">
            <slot></slot>
        </div>
    </button>
</template>

<script>
    export default {
        props: {
            icon: {},
            iconPosition: {
                type: String,
                default: 'left',
                validator (value) {
                    return value === 'left' || value === 'right'
                }
            }
        },
        name: '',
    }
</script>

<style lang="scss">
    .g-button {
        font-size: var(--font-size);
        height: var(--button-height);
        padding: 0 1em;
        border-radius: var(--button-radius);
        border: 1px solid var(--border-color);
        background: var(--button-bg);
        display: inline-flex;
        justify-content: center;
        align-content: center;
        vertical-align: middle;
        &:hover {
            border-color: var(--border-color-hover);
        }
        &:active {
            border-color: var(--button-active-b g);
        }
        >.icon {
            order: 1;
            margin-right: .3em;
        }
        >.content {
            order: 2;
        }
        &.icon-right {
            >.icon {
                order: 2;
                margin-left: .3em;
                margin-right: 0;
            }
            >.content {
                order: 1;
            }
        }
        &.icon-left {
            >.icon {
                order: 1;
                margin-left: 0;
                margin-right: .3em;
            }
            >.content {
                order: 2;
            }
        }
    }
</style>