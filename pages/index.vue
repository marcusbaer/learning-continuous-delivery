<template>
    <div>
        <h1>Hello world</h1>
        <p>My hostname is {{ hostname }}. Rendered by {{ name }}.</p>
    </div>
</template>

<script>
import os from 'os'

export default {
    head: {
        title: 'Home'
    },
    data ({ req }) {
        return {
            name: req ? 'server' : 'client',
            hostname: os.hostname()
        }
    }
}
</script>

<style>
    html {
        font-size: 18px;
    }
</style>
