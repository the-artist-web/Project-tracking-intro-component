<template>
    <Header />
    <main>
      <article>
        <Hero />
      </article>
    </main>
</template>

<script>
import Header from '@/components/Header.vue'
import Hero from '@/components/Hero.vue'

export default {
  name: 'App',
  components: {
    Header,
    Hero
  }
}
</script>

<style>
#app {
  display: flex;
  flex-direction: column;
  width: 100%;
  height: auto;
}
</style>
