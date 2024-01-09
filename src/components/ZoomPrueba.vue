<template>
    <div>
        <p :style="{ fontSize: zoom + 'px' }">
            Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's
            standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make
            a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting,
            remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing
            Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions
            of Lorem Ipsum.
        </p>
        <button class="fab" style="margin-bottom: 24px" @click="addZoom">Zoom +</button>
        <button class="fab" @click="minusZoom">Zoom -</button>
    </div>
</template>

<script>
export default {
    data() {
        return {
            zoom: 15
        }
    },
    methods: {
        addZoom() {
            this.zoom++
        },
        minusZoom() {
            this.zoom--
        }
    },
}
</script>

<style lang="css">
.fab {
    position: fixed;
    background: fuchsia;
    border-radius: 50px;
    border: none;
    color: #FFF;
    bottom: 1%;
    right: 1%;
    height: 20px;
    min-width: 20px;
}
</style>
