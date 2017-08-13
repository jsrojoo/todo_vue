<template>
  <Row style="text-align: center; line-height: 100vh; background-color: rgba(0,0,41,0.29)">
    <i-col v-if="!isLogInClicked" span="24">
      <Input placeholder="Username" style="width: 150px"></Input>
      <Button @click="login">Login</Button>
    </i-col>
    <i-col v-else span="24">
      <Input placeholder="Password" style="width: 150px"></Input>
      <Button @click="verify">Verify</Button>
    </i-col>
  </Row>
</template>

<script>
  import iCol from 'iview/src/components/grid/col.vue'

  export default {
    components: {iCol},
    data() {
      return {isLogInClicked: false}
    },
    methods: {
      login(){
        this.isLogInClicked = true;
      },
      verify() {
        this.isLogInClicked = false;
        this.$router.replace('/');
      }
    }
  }
</script>
