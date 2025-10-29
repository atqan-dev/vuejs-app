<template>
  <div class="container">
    <NuxtRouteAnnouncer />

    <header>
      <h1>  من أجل تجربة </h1>
      <h1>Atqan - test vuejs app - deploy </h1>
      <p class="subtitle">Monitor, and verify your app deployments.........</p>
    </header>

    <section class="features">
      <h2>🔧 Features</h2>
      <ul>
        <li>Sync latest updates from GitHub</li>
        <li>Store commit logs and app metadata</li>
        <li>Verify app availability via Nginx</li>
        <li>Handle dev/test/prod deployments</li>
        <li>Track deployment success</li>
        <li>Frontend dashboard integration</li>
      </ul>
    </section>

    <section class="dev-mode">
      <h2>💻 Start Dev Mode</h2>
      <p>Quickly launch development mode and test new features safely.</p>
    </section>

    <section class="account">
      <h2>👤 Account Details</h2>
      <p>Name: John Doe</p>
      <p>Email: john@example.com</p>
    </section>
  </div>
</template>
<script setup>
import { ref, onMounted } from 'vue'

const currentDateTime = ref('')

onMounted(() => {
  // Format: YYYY-MM-DD HH:mm:ss
  const now = new Date()
  currentDateTime.value = now.toLocaleString('en-US', {
    year: 'numeric',
    month: '2-digit',
    day: '2-digit',
    hour: '2-digit',
    minute: '2-digit',
    second: '2-digit'
  })
})
</script>
<style scoped>
.container {
  max-width: 800px;
  margin: 0 auto;
  padding: 2rem;
  font-family: system-ui, sans-serif;
  line-height: 1.6;
  color: #333;
}

header {
  text-align: center;
  margin-bottom: 2rem;
}
.timeheader {
  text-align: center;
  padding: 1rem;
  background: #f9f9f9;
  border-bottom: 1px solid #ddd;
}
.subtitle {
  font-size: 1rem;
  color: #666;
}

.features, .dev-mode, .account {
  background: #f9f9f9;
  padding: 1.5rem;
  border-radius: 8px;
  margin-bottom: 1.5rem;
}

h1, h2 {
  margin-bottom: 0.5rem;
}

ul {
  padding-left: 1.2rem;
}

ul li {
  margin: 0.5rem 0;
}
</style>
