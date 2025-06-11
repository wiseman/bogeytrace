<script lang="ts">
// placeholder data
const tracks = [
  { name: 'Unknown_AC_001', details: '2024-01-15 14:23:00 - 15:47:00\nAlt: FL220-FL230 | Points: 127' },
  { name: 'Unknown_AC_002', details: '2024-01-15 09:15:00 - 10:22:00\nAlt: 4,500ft | Points: 89' },
  { name: 'Partial_Track_LAX', details: '2024-01-14 22:45:00 - 23:12:00\nAlt: FL220 | Points: 43' }
];
let active = 0;
</script>

<aside class="left-panel">
  <div class="panel-header">Aircraft Tracks ({tracks.length})</div>
  <div class="tracks-list">
    {#each tracks as track, i}
      <div class="track-item {i === active ? 'active' : ''}">
        <div class="track-info">
          <div>
            <div class="track-name">{track.name}</div>
            <div class="track-details" innerHTML={track.details}></div>
          </div>
          <div class="track-actions">
            <button class="icon-btn">👁️</button>
            <button class="icon-btn">🎯</button>
          </div>
        </div>
      </div>
    {/each}
  </div>
</aside>

<style>
.left-panel {
  width: 350px;
  background: #f8f9fa;
  border-right: 1px solid #ddd;
  display: flex;
  flex-direction: column;
}
.panel-header {
  padding: 15px;
  background: white;
  border-bottom: 1px solid #ddd;
  font-weight: 600;
}
.tracks-list {
  flex: 1;
  overflow-y: auto;
  padding: 10px;
}
.track-item {
  background: white;
  border: 1px solid #ddd;
  border-radius: 6px;
  padding: 12px;
  margin-bottom: 8px;
  cursor: pointer;
  transition: all 0.2s;
}
.track-item:hover {
  border-color: #4CAF50;
  box-shadow: 0 2px 4px rgba(0,0,0,0.1);
}
.track-item.active {
  border-color: #4CAF50;
  background: #f0f8f0;
}
.track-info {
  display: flex;
  justify-content: space-between;
  align-items: start;
}
.track-name {
  font-weight: 500;
  margin-bottom: 4px;
}
.track-details {
  font-size: 12px;
  color: #666;
}
.track-actions {
  display: flex;
  gap: 8px;
}
.icon-btn {
  width: 24px;
  height: 24px;
  border: none;
  background: #f0f0f0;
  border-radius: 4px;
  cursor: pointer;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 12px;
}
</style>
