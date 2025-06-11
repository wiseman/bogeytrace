<script lang="ts">
// placeholder search results
const results = [
  { source: 'ZLA Center - Sector 19 (132.750)', time: '14:35:18', text: '01, traffic 12 o\'clock, 10 miles, opposite direction, another TROY Q-9 FL220' },
  { source: 'KLAX Tower (133.900)', time: '22:51:42', text: 'TROY701, turn left heading 250, vectors for spacing' }
];
</script>

<aside class="right-panel">
  <div class="search-header">
    <div class="search-title">Search Transcriptions</div>
    <div class="search-box">
      <input type="text" class="search-input" placeholder="Enter callsign, phrase, or keyword..." value="TROY" />
      <button class="search-btn">Search</button>
    </div>
    <div class="search-filters">
      <label class="filter-checkbox"><input type="checkbox" checked /><span>Selected tracks only</span></label>
      <label class="filter-checkbox"><input type="checkbox" checked /><span>±5 min of track times</span></label>
    </div>
  </div>
  <div class="search-results">
    <div class="results-summary"><span class="result-count">{results.length} matches</span> found for "TROY"</div>
    {#each results as r}
      <div class="result-item">
        <div class="result-header">
          <div class="result-source">{r.source}</div>
          <div class="result-time">{r.time}</div>
        </div>
        <div class="result-transcript">{r.text}</div>
      </div>
    {/each}
  </div>
</aside>

<style>
.right-panel {
  width: 450px;
  background: white;
  border-left: 1px solid #ddd;
  display: flex;
  flex-direction: column;
}
.search-header {
  background: #2c3e50;
  color: white;
  padding: 20px;
}
.search-title {
  font-size: 16px;
  font-weight: 600;
  margin-bottom: 12px;
}
.search-box {
  display: flex;
  gap: 10px;
}
.search-input {
  flex: 1;
  padding: 10px 14px;
  border: none;
  border-radius: 4px;
  font-size: 16px;
  background: white;
  color: #333;
}
.search-btn {
  padding: 10px 20px;
  background: #4CAF50;
  color: white;
  border: none;
  border-radius: 4px;
  font-weight: 500;
  cursor: pointer;
}
.search-filters {
  margin-top: 12px;
  display: flex;
  gap: 10px;
  font-size: 14px;
}
.filter-checkbox {
  display: flex;
  align-items: center;
  gap: 6px;
}
.search-results {
  flex: 1;
  overflow-y: auto;
}
.results-summary {
  padding: 15px 20px;
  background: #f8f9fa;
  border-bottom: 1px solid #ddd;
  font-size: 14px;
  color: #666;
}
.result-count {
  font-weight: 600;
  color: #333;
}
.result-item {
  border-bottom: 1px solid #eee;
  padding: 15px 20px;
  cursor: pointer;
  transition: background 0.2s;
}
.result-item:hover {
  background: #f8f9fa;
}
.result-header {
  display: flex;
  justify-content: space-between;
  align-items: start;
  margin-bottom: 8px;
}
.result-source {
  font-weight: 500;
  color: #2c3e50;
  font-size: 14px;
}
.result-time {
  font-size: 12px;
  color: #666;
  font-family: monospace;
}
.result-transcript {
  font-size: 14px;
  line-height: 1.6;
  color: #333;
}
</style>
