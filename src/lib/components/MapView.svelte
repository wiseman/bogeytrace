<script lang="ts">
// placeholder for map interactions
</script>

<div class="map-container">
  <div class="map-controls">
    <button class="map-control-btn">+</button>
    <button class="map-control-btn">-</button>
    <button class="map-control-btn">⊞</button>
    <button class="map-control-btn">📍</button>
  </div>
  <div class="stats-badge">
    <div class="stat-item">
      <span class="stat-label">Stations Searched:</span>
      <span class="stat-value">8 / 12</span>
    </div>
    <div class="stat-item">
      <span class="stat-label">Recordings:</span>
      <span class="stat-value">24</span>
    </div>
    <div class="stat-item">
      <span class="stat-label">Total Duration:</span>
      <span class="stat-value">12h 30m</span>
    </div>
    <div class="stat-item">
      <span class="stat-label">Transcribed:</span>
      <span class="stat-value">100%</span>
    </div>
  </div>
</div>

<style>
.map-container {
  flex: 1;
  position: relative;
  background-image: url('/screenshot.png');
  background-size: cover;
  background-position: center;
  display: flex;
  align-items: center;
  justify-content: center;
}
.map-controls {
  position: absolute;
  top: 15px;
  right: 15px;
  background: white;
  border-radius: 6px;
  box-shadow: 0 2px 6px rgba(0,0,0,0.2);
  padding: 8px;
  display: flex;
  flex-direction: column;
  gap: 8px;
}
.map-control-btn {
  width: 36px;
  height: 36px;
  border: none;
  background: white;
  border-radius: 4px;
  cursor: pointer;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 18px;
}
.map-control-btn:hover {
  background: #f0f0f0;
}
.stats-badge {
  position: absolute;
  bottom: 15px;
  left: 15px;
  background: rgba(255,255,255,0.9);
  border-radius: 6px;
  padding: 10px;
  display: flex;
  flex-direction: column;
  gap: 4px;
  font-size: 12px;
}
.stat-label {
  font-weight: 600;
  margin-right: 4px;
}
</style>
