<template>
  <div id="categories-page" class="page-wrapper categories-page">
  
  <h3>ACTIVE PHARMACEUTICAL INGREDIENTS<h3/>
  
    <site-hero title="Products" image="https://picsum.photos/1800/1801" />
    <main-section theme="one-column">  
      <categories-grid />
      
    </main-section>
  </div>
</template>
<script>
export default {
  head() {
    return {
      title: `Products | ${this.$siteConfig.siteName}`
    }
  }
}
</script>

