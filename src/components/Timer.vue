<template>
    <div>Timer: <span> {{count}} </span></div>
    <button @click="start"> Start </button>
    <button @click="pause"> Pause </button>
    <button @click="stop"> Stop </button>
</template>
<script>
import { ref } from 'vue'
export default {
    setup() {
        const count = ref(0)
        // XXX: At the moment it increase instead of decreasing time
        function decreaseTimer() {
            // count.value--
            count.value++
        }
        let timerID
        function start() {
            if (!timerID) {
                timerID = setInterval(decreaseTimer, 1000)
            }
        }
        function stop() {
            if (timerID) {
                clearInterval(timerID)
                timerID = null
            }
                clearTimer()
        }
        function pause() {
            if (timerID) {
                clearInterval(timerID)
                timerID = null
            }
        }
        function clearTimer() {
            count.value = 0
        }
        return { count, start, stop, pause }
    }
}
</script>

<style scoped>
</style>

