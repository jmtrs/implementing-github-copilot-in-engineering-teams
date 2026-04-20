<template>
  <div class="editor-scene fade-in" style="animation-delay: 0.1s">
    <div class="editor-window card-surface">
      <div class="window-topbar">
        <span></span>
        <span></span>
        <span></span>
      </div>

      <div class="window-body">
        <div class="editor-main">
          <div class="editor-meta fade-up" style="animation-delay: 0.24s">
            <span class="editor-file">backend / auth / request-email-code.ts</span>
            <span class="editor-branch">auth flow</span>
          </div>

          <div class="code-area font-code">
            <div class="code-row fade-up" style="animation-delay: 0.38s">
              <span class="line-no">12</span>
              <span class="code-text"><span class="tok-key">const</span> <span class="tok-var">normalizedEmail</span> = <span class="tok-var">email</span>.<span class="tok-fn">trim</span>()</span>
            </div>
            <div class="code-row fade-up" style="animation-delay: 0.48s">
              <span class="line-no">13</span>
              <span class="code-text"><span class="tok-key">if</span> (!<span class="tok-fn">isValidEmail</span>(<span class="tok-var">normalizedEmail</span>)) <span class="tok-key">return</span> <span class="tok-str">'invalid_email'</span></span>
            </div>
            <div class="code-row fade-up" style="animation-delay: 0.58s">
              <span class="line-no">14</span>
              <span class="code-text"><span class="tok-key">await</span> <span class="tok-var">authService</span>.<span class="tok-fn">requestCode</span>(<span class="tok-var">normalizedEmail</span>)</span>
            </div>
            <div class="code-row fade-up" style="animation-delay: 0.68s">
              <span class="line-no">15</span>
              <span class="code-text"><span class="tok-key">return</span> <span class="tok-str">'ok'</span></span>
            </div>

            <div class="autocomplete-row fade-up" style="animation-delay: 0.84s">
              <span class="line-no">16</span>
              <span class="ghost-code">const invalidEmailError = buildInvalidEmailError(email)</span>
              <span class="accept-hint">tab</span>
            </div>

            <div class="code-row fade-up" style="animation-delay: 0.98s">
              <span class="line-no">17</span>
              <span class="code-text"><span class="tok-key">if</span> (<span class="tok-var">invalidEmailError</span>) <span class="tok-key">return</span> <span class="tok-var">invalidEmailError</span></span>
            </div>
            <div class="code-row fade-up" style="animation-delay: 1.06s">
              <span class="line-no">18</span>
              <span class="code-text"><span class="tok-comment">// keep email validation shared across auth flows</span></span>
            </div>
          </div>

          <div class="terminal-strip fade-up" style="animation-delay: 1.18s">
            <span class="terminal-prompt">$</span>
            <span class="terminal-command">gh copilot suggest "extract invalid email validation helper"</span>
            <span class="terminal-cursor"></span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.editor-scene {
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 8px 0 18px;
}

.editor-window {
  width: 100%;
  max-width: 620px;
  overflow: hidden;
}

.window-topbar {
  display: flex;
  gap: 8px;
  padding: 16px 18px 0;
}

.window-topbar span {
  width: 10px;
  height: 10px;
  border-radius: 999px;
  background: rgba(255, 255, 255, 0.16);
}

.window-body {
  display: block;
  min-height: 376px;
}

.editor-main {
  padding: 18px 20px 18px;
  display: flex;
  flex-direction: column;
  gap: 14px;
  min-height: 376px;
}

.editor-meta {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 12px;
}

.editor-file,
.editor-branch {
  font-family: var(--font-code);
  font-size: 0.68rem;
  letter-spacing: 0.05em;
  text-transform: uppercase;
  color: #8d8d8d;
}

.code-area {
  display: grid;
  gap: 8px;
  margin-top: 4px;
}

.code-row,
.autocomplete-row {
  display: grid;
  grid-template-columns: 28px 1fr auto;
  gap: 10px;
  align-items: center;
  min-height: 28px;
}

.line-no {
  font-family: var(--font-code);
  font-size: 0.66rem;
  color: rgba(255, 255, 255, 0.24);
}

.code-text,
.ghost-code {
  font-family: var(--font-code);
  font-size: 0.76rem;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
}

.code-text {
  color: #d7d7d7;
}

.tok-key { color: #f4f4f4; }
.tok-var { color: #c8c8c8; }
.tok-fn { color: #a9a9a9; }
.tok-str { color: #bdbdbd; }
.tok-comment { color: #7f7f7f; }

.autocomplete-row {
  padding: 4px 10px 4px 10px;
  border-radius: 10px;
  background: rgba(255, 255, 255, 0.04);
}

.ghost-code {
  color: rgba(255, 255, 255, 0.38);
}

.accept-hint {
  padding: 2px 8px;
  border: 1px solid rgba(255, 255, 255, 0.1);
  border-radius: 999px;
  font-family: var(--font-code);
  font-size: 0.6rem;
  color: rgba(255, 255, 255, 0.45);
  text-transform: lowercase;
}

.terminal-strip {
  margin-top: auto;
  display: grid;
  grid-template-columns: auto auto 1fr auto;
  align-items: center;
  gap: 10px;
  min-height: 44px;
  padding-top: 14px;
  border-top: 1px solid rgba(255, 255, 255, 0.08);
}
/* no pongas lo del terminal label*/

.terminal-prompt,
.terminal-command,
.terminal-cursor {
  font-family: var(--font-code);
}

.terminal-prompt {
  font-size: 0.72rem;
  color: #8d8d8d;
}

.terminal-command {
  font-size: 0.72rem;
  color: #d6d6d6;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
}

.terminal-cursor {
  width: 8px;
  height: 16px;
  background: rgba(255, 255, 255, 0.72);
  animation: blink 1.1s step-end infinite;
}
</style>
