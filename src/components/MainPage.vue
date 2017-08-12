<template>

  <Row :style="containerStyle">
    <Column span="4" :style="{height: '100vh'}">
      <men-you></men-you>
    </Column>
    <Column span="20" :style="{height: '100vh'}">
      <Row :style="contentStyle">
        <slot name="content">
          <div :style="fallbackStyle">
            No Content yet
          </div>
        </slot>
      </Row>
    </Column>
  </Row>

</template>

<script>
  import {Col as Column, Row} from 'iview/src/components/grid';
  import MenYou from './Menu.vue';

  export default {
    name: "mainPage",
    components: {Row, Column, MenYou},
    data() {
      return {
        containerStyle: {height: '100vh', overflow: 'hidden'},
        contentStyle: {padding: '40px', height: '100%', overflow: 'auto'},
        fallbackStyle: {display: 'flex', alignItems: 'center', justifyContent: 'center', height: '100%'}
      }
    }
  }

</script>

