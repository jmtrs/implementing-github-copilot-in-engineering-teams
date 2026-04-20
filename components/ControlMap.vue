<template>
  <div class="control-map">
    <div class="domain access-domain fade-up" style="animation-delay: 0.62s">
      <h2>Access</h2>
      <p>seat assignment and org-level delegation</p>
      <span>AI controls</span>
    </div>

    <div class="domain policies-domain fade-up" style="animation-delay: 0.78s">
      <h2>Policies &amp; models</h2>
      <p>feature, privacy, and model controls</p>
      <span>Policies / Models</span>
    </div>

    <div class="control-node card-surface fade-up" style="animation-delay: 0.44s">
      <p>Enterprise / Organization</p>
      <strong>AI Controls</strong>
    </div>

    <div class="domain surfaces-domain fade-up" style="animation-delay: 0.94s">
      <h2>GitHub-native AI surfaces</h2>
      <p>cloud agent, code review, MCP</p>
      <span>Agents / MCP</span>
    </div>

    <div class="domain visibility-domain fade-up" style="animation-delay: 1.1s">
      <h2>Visibility</h2>
      <p>metrics dashboards and APIs</p>
      <span>Dashboard / API</span>
    </div>

    <div class="connector connector-top-left fade-in" style="animation-delay: 0.7s"></div>
    <div class="connector connector-top-right fade-in" style="animation-delay: 0.86s"></div>
    <div class="connector connector-bottom-left fade-in" style="animation-delay: 1.02s"></div>
    <div class="connector connector-bottom-right fade-in" style="animation-delay: 1.18s"></div>
  </div>
</template>

<style scoped>
.control-map {
  position: relative;
  width: min(1080px, 100%);
  min-height: 460px;
  margin: 0 auto;
  display: grid;
  grid-template-columns: 1fr 328px 1fr;
  grid-template-rows: 1fr 162px 1fr;
  align-items: center;
  justify-items: center;
}

.control-node {
  grid-column: 2;
  grid-row: 2;
  width: 100%;
  padding: 20px 22px 18px;
  text-align: center;
  z-index: 2;
}

.control-node p {
  margin: 0;
  font-family: var(--font-text);
  font-size: 0.8rem;
  line-height: 1.2;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  color: #8d8d8d;
}

.control-node strong {
  display: block;
  margin-top: 8px;
  font-family: var(--font-display);
  font-size: 1.3rem;
  line-height: 1.06;
  letter-spacing: -0.03em;
  color: #f5f5f5;
}

.domain {
  position: relative;
  width: 246px;
  text-align: center;
  z-index: 2;
}

.domain h2 {
  margin: 0;
  font-family: var(--font-display);
  font-size: 0.92rem;
  line-height: 1.12;
  letter-spacing: -0.03em;
  color: #f5f5f5;
}

.domain p {
  margin: 7px 0 0;
  font-size: 0.76rem;
  line-height: 1.28;
  color: #9a9a9a;
}

.domain span {
  display: inline-block;
  margin-top: 10px;
  padding: 4px 9px;
  border: 1px solid rgba(255, 255, 255, 0.08);
  border-radius: 999px;
  font-family: var(--font-code);
  font-size: 0.58rem;
  line-height: 1;
  letter-spacing: 0.04em;
  text-transform: uppercase;
  color: #7f7f7f;
}

.access-domain {
  grid-column: 1;
  grid-row: 1;
  align-self: end;
  justify-self: end;
  margin-right: 2px;
  margin-bottom: 6px;
}

.policies-domain {
  grid-column: 3;
  grid-row: 1;
  align-self: end;
  justify-self: start;
  margin-left: 2px;
  margin-bottom: 6px;
}

.surfaces-domain {
  grid-column: 1;
  grid-row: 3;
  align-self: start;
  justify-self: end;
  margin-right: 2px;
  margin-top: 6px;
}

.visibility-domain {
  grid-column: 3;
  grid-row: 3;
  align-self: start;
  justify-self: start;
  margin-left: 2px;
  margin-top: 6px;
}

.connector {
  position: absolute;
  height: 1px;
  background: linear-gradient(90deg, rgba(255, 255, 255, 0), rgba(255, 255, 255, 0.12), rgba(255, 255, 255, 0));
  z-index: 1;
}

.connector-top-left {
  left: 25%;
  top: 31%;
  width: 150px;
  transform: rotate(24deg);
}

.connector-top-right {
  right: 25%;
  top: 31%;
  width: 150px;
  transform: rotate(-24deg);
}

.connector-bottom-left {
  left: 25%;
  bottom: 31%;
  width: 150px;
  transform: rotate(-24deg);
}

.connector-bottom-right {
  right: 25%;
  bottom: 31%;
  width: 150px;
  transform: rotate(24deg);
}
</style>
