<template>
  <PrimerComponente v-if="activate" />
  <HelloWorld msg="Epale" v-if="!activate" />
  <!--   <button @click="activate = !activate">Activar</button> -->
  <div>
    <form-wizard>
      <tab-content title="Fase 1">
        <form action="">
          <label for="">Esta es la Fase 1</label>
          <input type="text">
          <label for="">Observaciones</label>
          <textarea name="" id="" cols="30" rows="10"></textarea>
          <div class="mb-3">
            <label for="" class="form-label">Choose file</label>
            <input type="file" class="form-control" name="" id="" placeholder="" aria-describedby="fileHelpId" />
            <div id="fileHelpId" class="form-text">Help text</div>
          </div>
        </form>
      </tab-content>
      <tab-content title="Fase 2">
        My second tab content
      </tab-content>
      <tab-content title="Fase 3">
        Yuhuuu! This seems pretty damn simple
      </tab-content>
      <tab-content title="Fase 4">
        Yuhuuu! This seems pretty damn simple
      </tab-content>
      <tab-content title="Fase 5">
        Yuhuuu! This seems pretty damn simple
      </tab-content>
    </form-wizard>
    <Vue3FormWizard />
  </div>
</template>

<script>
/* import HelloWorld from './components/HelloWorld.vue'
import PrimerComponente from './components/PrimerComponente.vue'; */
import Vue3FormWizard from 'vue3-form-wizard'
import 'vue3-form-wizard/dist/style.css'
import { FormWizard, TabContent } from 'vue3-form-wizard';

export default {
  name: 'App',
  components: {
    /*     HelloWorld,
        PrimerComponente, */
    Vue3FormWizard,
    FormWizard,
    TabContent,
  },
  data() {
    return {
      activate: true,
    }
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
