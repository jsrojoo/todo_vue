<template>
  <i-menu active-name="1" theme="dark" width="auto" :style="{height: '100vh'}">
    <div :style="{textAlign : 'center', margin: 'auto', padding: '15px'}">
      <Icon type="edit" color="white" size="50"></Icon>
    </div>
    <i-menu-item name="1">
      <Icon type="ios-navigate"></Icon>
      <span class="layout-text">Todo list</span>
    </i-menu-item>
    <i-menu-item name="2">
      <Icon type="ios-keypad"></Icon>
      <span class="layout-text">Graphs</span>
    </i-menu-item>
    <i-menu-item name="3">
      <Icon type="ios-analytics"></Icon>
      <span class="layout-text">Logout</span>
    </i-menu-item>
  </i-menu>
</template>

<script>

  import iMenu from 'iview/src/components/menu';
  import iMenuItem from 'iview/src/components/menu/menu-item.vue';
  import Icon from 'iview/src/components/icon';

  export default{
    name: "MenYou",
    components: {iMenu, Icon, iMenuItem}

  }
</script>
