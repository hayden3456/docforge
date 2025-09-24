<script>
  // No props needed for now, but can be added later if needed
</script>

<div class="stacked-container">
  <!-- Not equal sign in top left -->
  <div class="not-equal-sign">≠</div>
  
  <!-- Documentation card behind (tilted and offset) -->
  <div class="doc-card">
    <div class="doc-header">
      <div class="doc-title-section">
        <h3 class="doc-title">V2 Integration Guide 2014</h3>
        <div class="doc-icon">
          <svg class="h-6 w-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12h6m-6 4h6m2 5H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z" />
          </svg>
        </div>
      </div>
      <div class="doc-meta">
        <div class="doc-meta-item">
          <svg class="h-4 w-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 7V3m8 4V3m-9 8h10M5 21h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v12a2 2 0 002 2z" />
          </svg>
          <span>2014</span>
        </div>
        <div class="doc-meta-item">
          <svg class="h-4 w-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M16 7a4 4 0 11-8 0 4 4 0 018 0zM12 14a7 7 0 00-7 7h14a7 7 0 00-7-7z" />
          </svg>
          <span>Technical Team</span>
        </div>
      </div>
    </div>
    <div class="doc-content">
      <div class="doc-section">
        <h4 class="doc-section-title">Overview</h4>
        <p class="doc-section-text">
          This guide provides comprehensive instructions for
          integrating with our V2 API endpoints and
          services.
        </p>
      </div>
      <div class="doc-section">
        <h4 class="doc-section-title">Contents</h4>
        <ul class="doc-list">
          <li>• Authentication Methods</li>
          <li>• API Endpoints</li>
          <li>• Error Handling</li>
          <li>• Code Examples</li>
        </ul>
      </div>
      <div class="doc-footer">
        <p class="doc-version">
          Document Version: 2.1 | Last Updated: March 2014
        </p>
      </div>
    </div>
  </div>
  
  <!-- Code card on top -->
  <div class="code-card">
    <img
      class="logo"
      src="https://upload.wikimedia.org/wikipedia/commons/1/1b/Svelte_Logo.svg"
      alt="Svelte logo"
    />
    <pre class="code-pre"><code class="code-content">
<span class="line faded"><span class="k">const</span> <span class="n">defaults</span> = &#123; retries: 3, cache: true, timeout: 5000 &#125;;</span>
<span class="line faded"><span class="k">export function</span> <span class="n">initContext</span>(<span class="n">user</span>, <span class="n">opts</span> = &#123;&#125;) &#123; … &#125;</span>

<span class="line c">// deep in component logic</span>
<span class="line"><span class="k">let</span> <span class="n">count</span> = <span class="n">0</span>;</span>
<span class="line"><span class="k">const</span> <span class="n">api</span> = <span class="n">createClient</span>(<span class="s">'/v4/data'</span>, &#123; auth: session.token, headers: &#123; 'X-App': 'demo' &#125; &#125;);</span>

<span class="line"><span class="k">$:</span> <span class="n">message</span> = <span class="s">`User $&#123;user.name&#125; clicked $&#123;count&#125; times at $&#123;new Date().toISOString()&#125;`</span>;</span>

<span class="line">&lt;button on:click=&#123;() =&gt; &#123; count++; logEvent('click', &#123; userId: user.id, value: count &#125;); &#125;&#125;&gt;</span>
<span class="line"> &#123;message&#125;</span>
<span class="line">&lt;/button&gt;</span>

<span class="line faded"><span class="k">return</span> &#123; subscribe, reset: () =&gt; update(() =&gt; 0) &#125;;</span>
<span class="line faded">}</span>
</code></pre>
  </div>
</div>

<style>
/* Stacked container with absolute positioning */
.stacked-container {
  position: relative;
  width: 100%;
  transform: scale(0.9);
  transform: scale(0.9) translateX(-30px);
  height: 400px; /* Increased height to accommodate the tilted doc card */
  margin-left: auto;
  max-width: 800px;
  margin-bottom: 20px; /* Add bottom margin for spacing */
  z-index: 10;
}

/* Not equal sign in top left */
.not-equal-sign {
  position: absolute;
  top: 40px;
  left: 90px;
  font-size: 64px;
  font-weight: bold;
  color: #dc2626;
  z-index: 3;
  border-radius: 50%;
  width: 70px;
  height: 70px;
  display: flex;
  align-items: center;
  justify-content: center;
  transform: rotate(-8deg);
}

/* Documentation card behind (tilted and offset) */
.doc-card {
  position: absolute;
  top: 20px;
  left: 180px;
  width: 350px;
  height: 260px;
  background: #f8fafc;
  border: 2px solid #e2e8f0;
  border-radius: 8px;
  padding: 16px;
  box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
  color: #334155;
  overflow: hidden;
  display: flex;
  flex-direction: column;
  transform: rotate(8deg);
  z-index: 1;
}

/* Code card on top */
.code-card {
  position: absolute;
  top: 80px;
  left: 0;
  width: 400px;
  height: 300px;
  background: #0c0f16;
  border: 1px solid rgba(255, 255, 255, 0.08);
  border-radius: 12px;
  padding: 12px 0;
  color: #e6e9ef;
  font-family: ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, 'Liberation Mono', monospace;
  font-size: 0.86rem;
  line-height: 1.15;
  overflow: hidden;
  z-index: 2;
}

.code-pre {
  margin: 0;
  padding: 0 16px;
  height: 100%;
  overflow: hidden;
}

.code-content {
  white-space: pre;
  display: block;
  height: 100%;
  overflow: hidden;
}

.doc-content {
  flex: 1;
  overflow: hidden;
}

.doc-header {
  margin-bottom: 16px;
}

.doc-title-section {
  display: flex;
  align-items: center;
  gap: 12px;
  justify-content: flex-end;
  margin-bottom: 12px;
}

.doc-title {
  font-size: 18px;
  font-weight: 600;
  margin: 0;
  color: #1e293b;
}

.doc-icon {
  padding: 8px;
  background: rgba(16, 76, 53, 0.1);
  border-radius: 8px;
  color: #104C35;
}

.doc-meta {
  display: flex;
  align-items: center;
  gap: 16px;
  justify-content: flex-end;
  color: #64748b;
}

.doc-meta-item {
  display: flex;
  align-items: center;
  gap: 4px;
  font-size: 14px;
}

.doc-section {
  margin-bottom: 16px;
}

.doc-section-title {
  font-size: 14px;
  font-weight: 600;
  margin: 0 0 8px 0;
  color: #1e293b;
}

.doc-section-text {
  font-size: 14px;
  color: #64748b;
  line-height: 1.5;
  margin: 0;
}

.doc-list {
  font-size: 14px;
  color: #64748b;
  margin: 0;
  padding: 0;
  list-style: none;
}

.doc-list li {
  margin-bottom: 4px;
}

.doc-footer {
  padding-top: 8px;
  border-top: 1px solid #e2e8f0;
}

.doc-version {
  font-size: 12px;
  color: #64748b;
  margin: 0;
}

.code-card img.logo {
  position: absolute;
  top: 8px;
  right: 8px;
  width: 32px;
  height: 32px;
  pointer-events: none;
  user-select: none;
}

.code-card pre {
  margin: 0;
  padding: 0 16px;
  counter-reset: line 245; /* pretend mid-file */
}

.code-card code {
  white-space: pre;
  display: block;
}

/* line numbers */
.code-card code .line {
  display: block;
  padding-left: 3.2em;
  position: relative;
}

.code-card code .line::before {
  counter-increment: line;
  content: counter(line);
  position: absolute;
  left: 0;
  width: 2.6em;
  text-align: right;
  color: rgba(255, 255, 255, 0.25);
}

/* syntax colors */
.code-card .k { color: #8fd1ff; }
.code-card .n { color: #ffd479; }
.code-card .s { color: #a0e57c; }
.code-card .c { color: #7f8aa3; }

/* faded lines now keep their color, just dim overall */
.code-card .faded { opacity: 0.45; }
</style>
