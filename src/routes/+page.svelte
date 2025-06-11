<script lang="ts">
import AppHeader from '$lib/components/AppHeader.svelte';
import LeftPanel from '$lib/components/LeftPanel.svelte';
import MapView from '$lib/components/MapView.svelte';
import RightPanel from '$lib/components/RightPanel.svelte';
import BottomPanel from '$lib/components/BottomPanel.svelte';
</script>

<div class="container">
  <div class="wireframe-header">
    <h1>BOGEYTRACE</h1>
    <p style="color: #666; margin-top: 8px;">Aircraft Track Analysis &amp; ATC Correlation Platform</p>
  </div>

  <div class="app-container">
    <AppHeader />
    <div class="main-layout">
      <LeftPanel />
      <MapView />
      <RightPanel />
    </div>
    <BottomPanel />
  </div>
</div>

<style>
:global(body) {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
  background: #f5f5f5;
  color: #333;
  height: 100vh;
  overflow: hidden;
  margin: 0;
}
.container {
  max-width: 1800px;
  margin: 0 auto;
  padding: 20px;
  height: 100%;
  display: flex;
  flex-direction: column;
}
.wireframe-header {
  text-align: center;
  margin-bottom: 30px;
  padding: 20px;
  background: white;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0,0,0,0.1);
}
.app-container {
  background: white;
  border-radius: 8px;
  box-shadow: 0 2px 8px rgba(0,0,0,0.1);
  overflow: hidden;
  display: flex;
  flex-direction: column;
  flex: 1;
}
.main-layout {
  display: flex;
  flex: 1;
  min-height: 0;
}
</style>
