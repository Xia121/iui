<template>
    <svg class="g-icon" @click="$emit('click', $event)">
        <use :xlink:href=`#i-${name}`></use>
    </svg>
</template>

<script>
    export default {
        name: 'GuluIcon',
        props: ['name'],
        /*data () {
            return {
                icon: this.name,
                fille: true
            }
        },
        mounted () {
            this.filter()
        },
        methods: {
            filter () {
                let icon = this.icon.toString()
                console.log(icon)
                if (icon === "true" || icon ==="false" || icon==="undefind") {
                    this.fille = false
                }
            }
        },*/

    }
</script>

<style lang="scss">
    .g-icon {
        width: 1em;
        height: 1em;
        margin-top: .2em;
    }

</style>