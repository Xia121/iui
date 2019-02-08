<template>
    <div class="g-button-group">
        <slot></slot>
    </div>
</template>

<script>
    export default {
        mounted () {
            for (let node of this.$el.children) {
                let name = node.nodeName.toLowerCase()
                if (name !== 'button') {
                    console.warn('g-button-group的子元素应该全都是button')
                }
            }
        }
    }
</script>

<style lang="scss">
    .g-button-group {
        display: inline-flex;
        vertical-align: middle;
        > .g-button {
            border-radius: 0px;
            /*&:not(:first-child) {
                border-left: none;
            }*/
            margin-left: -1px;
            &:first-child {
                border-radius: var(--button-radius) 0 0 var(--button-radius);
            }
            &:last-child {
                border-radius: 0 var(--button-radius) var(--button-radius) 0;
            }
            &:hover {
                position: relative;
                z-index: 1;
            }
        }

    }

</style>