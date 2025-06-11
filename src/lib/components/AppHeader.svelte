<script lang="ts">
// placeholder header actions
</script>

<header class="app-header">
  <div class="app-title">
    <span>✈️</span>
    <span>BOGEYTRACE</span>
  </div>
  <div class="header-actions">
    <button class="btn btn-secondary">Import KML</button>
    <button class="btn btn-primary">+ New Investigation</button>
    <button class="btn btn-secondary">⚙️</button>
  </div>
</header>

<style>
.app-header {
  background: #1a1a2e;
  color: white;
  padding: 12px 20px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.app-title {
  font-size: 20px;
  font-weight: 600;
  display: flex;
  align-items: center;
  gap: 10px;
}
.header-actions {
  display: flex;
  gap: 15px;
  align-items: center;
}
.btn {
  padding: 6px 14px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
  font-size: 14px;
  transition: all 0.2s;
}
.btn-primary {
  background: #4CAF50;
  color: white;
}
.btn-secondary {
  background: transparent;
  color: white;
  border: 1px solid rgba(255,255,255,0.3);
}
</style>
