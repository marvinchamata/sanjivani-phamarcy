<template>
  <div id="categories-page" class="page-wrapper categories-page">
    <site-hero title="Products" image="https://picsum.photos/1800/1801" />
    <main-section theme="one-column">
    
      <p>ACTIVE PHARMACEUTICAL INGREDIENTS<p/>
      
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

<h3>ACTIVE PHARMACEUTICAL INGREDIENTS<h3/>
