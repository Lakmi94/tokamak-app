<template>
    <view class="operator-layout">
       <header :openDrawer="openDr"/>
      <view class="operator-container">
         <text>Operators</text>
      </view>
    <footer/>

    </view>
</template>
<script>
import Header from '../components/Header'
import Footer from '@/components/Footer'
export default {
    components: {
      'header': Header,
       'footer': Footer,
    },
    props: {
    navigation: {
      type: Object
    }
  },
    methods: {
      openDr (){
        this.navigation.openDrawer();
      }
    },
}
</script>
<style scoped>
.operator-layout {
  display: flex;
  flex-direction: column;
  height: 100%;
}

.operator-container {
  flex: 1;
  align-self: stretch;
  position: relative;
  display: flex;
  align-items: center;
  padding-top: 40;
}
</style>