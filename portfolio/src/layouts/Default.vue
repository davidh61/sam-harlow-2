<template>
  <div class="layout" client-only>
    <header class="header">
      <nav class="nav">
      </nav>
    </header>
    <slot/>
  </div>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<style>
</style>
