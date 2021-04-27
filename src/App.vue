<template>
  <NavBar />
  <EmptyHome v-if="isAuthenticated" />
  <Home v-else />
  <Footer />
</template>

<script setup>
  import {authentication} from '~/helpers/useFirebase'

  const {isAuthenticated} = authentication()
</script>