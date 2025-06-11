<script lang="ts">
// placeholder bottom audio player
</script>

<div class="bottom-panel">
  <div class="audio-controls">
    <button class="play-btn">▶</button>
    <div class="audio-info">
      <div class="audio-title">ZLA Center - Sector 19 - 132.750 MHz</div>
      <div class="audio-details">2024-01-15 14:30:00 - 15:00:00</div>
    </div>
    <div class="time-display">14:42:33 / 30:00</div>
    <button class="btn btn-secondary" style="background: #444;">-15s</button>
    <button class="btn btn-secondary" style="background: #444;">+15s</button>
    <button class="btn btn-secondary" style="background: #444;">1.5x</button>
  </div>
  <div class="scrubber-container">
    <div class="scrubber">
      <div class="scrubber-progress" style="width: 42%;"></div>
    </div>
  </div>
  <div class="transcript-strip">
    <div class="current-transcript">
      ... United 453, descend and maintain FL190 | <span class="transcript-highlight">TROY703, traffic 12 o'clock, 8 miles opposite direction, another TROY Q-9 at FL230</span> | TROY703, roger, looking | Southwest 1822, contact approach ...
    </div>
  </div>
</div>

<style>
.bottom-panel {
  height: 180px;
  background: #2c2c2c;
  color: white;
  display: flex;
  flex-direction: column;
}
.audio-controls {
  padding: 15px 20px;
  display: flex;
  align-items: center;
  gap: 20px;
  border-bottom: 1px solid #444;
}
.play-btn {
  width: 48px;
  height: 48px;
  border-radius: 50%;
  background: #4CAF50;
  border: none;
  cursor: pointer;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 20px;
  color: white;
}
.audio-info {
  flex: 1;
}
.audio-title {
  font-weight: 500;
  margin-bottom: 4px;
}
.audio-details {
  font-size: 14px;
  color: #aaa;
}
.time-display {
  font-family: monospace;
  font-size: 14px;
}
.scrubber-container {
  padding: 0 20px 15px;
  display: flex;
  align-items: center;
}
.scrubber {
  width: 100%;
  height: 6px;
  background: #444;
  border-radius: 3px;
  cursor: pointer;
  position: relative;
}
.scrubber-progress {
  height: 100%;
  background: #4CAF50;
  border-radius: 3px;
}
.transcript-strip {
  flex: 1;
  background: #1a1a1a;
  padding: 10px 20px;
  overflow-x: auto;
  white-space: nowrap;
  font-size: 13px;
  color: #ccc;
}
.current-transcript {
  display: inline-block;
  padding: 0 100px;
}
.transcript-highlight {
  background: #4CAF50;
  color: white;
  padding: 2px 6px;
  border-radius: 3px;
}
</style>
