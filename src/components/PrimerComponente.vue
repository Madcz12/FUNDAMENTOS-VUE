<template>
    <div>

        <h1 :id="contador(5)">Mi Primer Componente</h1>

        <p v-on:click="myClick">{{ valor }}</p>

        <input type="number" v-if="setDefaultValue" v-model="valor">
        <div v-else>Ya no Hay Campo jaja</div>

        <div v-for="(c, index) in array" v-bind:key="c.id">
            <h3>{{ c.id }}</h3>
            <span>{{ c.name }} {{ index }}</span>
        </div>

        <!-- <HelloWorld v-for="c in [1, 2, 3, 4, 5]" v-bind:key="c.id" /> -->
        <br>

        <button @click="contador(1)">+1</button>
        <button @click="contador(1)">-1</button>
        <br>
        <button @click="valor++">+1</button>
        <button @click="valor--">-1</button>

        <!-- Objeto Sintaxis -->
        <p class="italic" :class="{ rojo: molesto }">Texto con Clases</p>
        <!-- Objeto Array -->
        <p class="italic" :class="['green', rojo]">Texto con Clases Array</p>
        <!-- Condicionales -->
        <div :class="[molesto ? rojo : 'green', 'default']">Estado Animo (Array con Condicionales)</div>
        <!-- Una sola condicion -->
        <div :class="[{ 'green': !molesto }]">Estado Animo (Array con Condicionales)</div>
    </div>
</template>


<style scoped>
h1 {
    color: red;
}

.italic {
    font-style: italic;
}

.rojo {
    color: red
}

.green {
    color: green
}
</style>

<script >
/* import HelloWorld from './HelloWorld.vue'; */

export default {
    name: "OtroComponente",
    created() { console.log("created - Mi Primer Componente") },
    beforeMount() { console.log("beforeMount - Mi Primer Componente") },
    mounted() { console.log("mounted - Mi Primer Componente") },
    beforeUpdate() { console.log("beforeUpdate - Mi Primer Componente") },
    updated() { console.log("updated - Mi Primer Componente") },
    activated() { console.log("activated - Mi Primer Componente") },
    deactivated() { console.log("deactivated - Mi Primer Componente") },
    beforeUnmount() { console.log("beforeUnmount - Mi Primer Componente") },
    unmounted() { console.log("unmounted - Mi Primer Componente") },
    errorCaptuted() { console.log("errorCaptured - Mi Primer Componente") },
    renderTracked() { console.log("renderTracked - Mi Primer Componente") },
    renderTriggered() { console.log("renderTriggered - Mi Primer Componente") },
    data() {
        return {
            rojo: "rojo",
            molesto: false,
            valor: 0,
            array: [{
                id: "123",
                name: "Miguel"
            },
            {
                id: "123",
                name: "Juan"
            }],
            setDefaultValue: true
        };
    },
    methods: {
        myClick: function () {
            this.valor = "Miguel";
            alert("NOOOOO");
        },
        contador(v) {
            this.valor += v;
            return 5;
        },
    },
    computed: {
        multiplicarPorCinco() {
            console.log("dentro de computado");
            return this.valor * 5;
        },
    },
    watch: {
        valor: function (newValue, oldValue) {
            this.setDefaultValue = false;
            console.log("newValue" + newValue + "oldValue" + oldValue);
        },
    },
    components: {}
};
</script>
