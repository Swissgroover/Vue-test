<script setup>
import Header from './components/Header.vue'
import DropDown from './components/DropDown.vue'
import Colors from './components/Colors.vue'
import StackedCards from './components/StackedCards.vue'
import FAQ from './components/FAQ.vue'
import Footer from './components/Footer.vue'
import Images from './components/Images.vue'
</script>

<template>
  <Header class=""/>
    <div class="m-auto">
      <div class="flex flex-col lg:flex-row w-full lg:justify-around m-auto lg:space-x-20">
        <div class="flex flex-col lg:w-1/2 justify-center items-center">
          <DropDown/>
          <Colors/>
        </div>
        <StackedCards />
      </div>
      <Images/>
      <FAQ/>
    </div>
  <Footer/>
</template>
