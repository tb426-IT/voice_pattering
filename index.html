<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>VOICE PATTERNS</title>
<style>
@import url('https://fonts.googleapis.com/css2?family=Josefin+Sans:wght@100;300;400&family=Cinzel:wght@400;700&display=swap');

* { margin: 0; padding: 0; box-sizing: border-box; }

body {
  background: #000;
  overflow: hidden;
  width: 100vw;
  height: 100vh;
  font-family: 'Josefin Sans', sans-serif;
}

canvas {
  position: fixed;
  inset: 0;
  width: 100%;
  height: 100%;
}

/* ── HUD overlay ── */
#hud {
  position: fixed;
  inset: 0;
  pointer-events: none;
  z-index: 10;
}

/* Title */
#title-block {
  position: absolute;
  top: 28px;
  left: 50%;
  transform: translateX(-50%);
  text-align: center;
  pointer-events: none;
}
#title-block h1 {
  font-family: 'Cinzel', serif;
  font-weight: 400;
  font-size: 11px;
  letter-spacing: 8px;
  color: rgba(255,255,255,0.25);
  text-transform: uppercase;
}
#mode-name {
  font-family: 'Cinzel', serif;
  font-size: 18px;
  font-weight: 700;
  letter-spacing: 6px;
  color: rgba(255,255,255,0.7);
  margin-top: 4px;
  text-shadow: 0 0 30px currentColor;
  transition: color 0.8s, text-shadow 0.8s;
}

/* Bottom controls */
#controls {
  position: absolute;
  bottom: 0;
  left: 0; right: 0;
  display: flex;
  align-items: flex-end;
  justify-content: center;
  gap: 12px;
  padding: 24px;
  pointer-events: all;
  background: linear-gradient(to top, rgba(0,0,0,0.7) 0%, transparent 100%);
}

.mode-btn {
  font-family: 'Josefin Sans', sans-serif;
  font-weight: 300;
  font-size: 9px;
  letter-spacing: 3px;
  text-transform: uppercase;
  color: rgba(255,255,255,0.35);
  background: transparent;
  border: 1px solid rgba(255,255,255,0.1);
  padding: 8px 16px;
  cursor: pointer;
  transition: all 0.3s;
  border-radius: 0;
}
.mode-btn:hover { color: rgba(255,255,255,0.8); border-color: rgba(255,255,255,0.4); }
.mode-btn.active {
  color: #fff;
  border-color: rgba(255,255,255,0.6);
  background: rgba(255,255,255,0.06);
  text-shadow: 0 0 12px #fff;
}

#start-btn {
  font-family: 'Cinzel', serif;
  font-size: 11px;
  letter-spacing: 4px;
  color: #fff;
  background: transparent;
  border: 1px solid rgba(255,255,255,0.5);
  padding: 10px 28px;
  cursor: pointer;
  transition: all 0.4s;
  text-transform: uppercase;
}
#start-btn:hover {
  background: rgba(255,255,255,0.08);
  border-color: #fff;
  box-shadow: 0 0 24px rgba(255,255,255,0.2);
}
#start-btn.live {
  color: rgba(255,255,255,0.4);
  border-color: rgba(255,255,255,0.2);
}

/* Left side freq bars */
#freq-sidebar {
  position: absolute;
  left: 24px;
  top: 50%;
  transform: translateY(-50%);
  display: flex;
  flex-direction: column;
  gap: 6px;
  pointer-events: none;
}
.freq-row {
  display: flex;
  align-items: center;
  gap: 8px;
}
.freq-lbl {
  font-size: 8px;
  letter-spacing: 2px;
  color: rgba(255,255,255,0.25);
  width: 40px;
  text-align: right;
}
.freq-track {
  width: 60px;
  height: 3px;
  background: rgba(255,255,255,0.06);
  border-radius: 0;
  overflow: hidden;
}
.freq-fill {
  height: 100%;
  width: 0%;
  border-radius: 0;
  transition: width 0.05s;
}

/* Right side: note display */
#note-display {
  position: absolute;
  right: 28px;
  top: 50%;
  transform: translateY(-50%);
  text-align: center;
  pointer-events: none;
}
#note-name {
  font-family: 'Cinzel', serif;
  font-size: 48px;
  font-weight: 700;
  color: rgba(255,255,255,0.08);
  line-height: 1;
  transition: color 0.2s, text-shadow 0.2s;
  text-shadow: none;
}
#note-freq {
  font-size: 9px;
  letter-spacing: 2px;
  color: rgba(255,255,255,0.15);
  margin-top: 4px;
  transition: color 0.2s;
}

/* Idle hint */
#hint {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  text-align: center;
  pointer-events: none;
  transition: opacity 0.8s;
}
#hint p {
  font-family: 'Josefin Sans', sans-serif;
  font-weight: 100;
  font-size: 13px;
  letter-spacing: 6px;
  color: rgba(255,255,255,0.2);
  text-transform: uppercase;
}
#hint.hidden { opacity: 0; }
</style>
</head>
<body>

<canvas id="c"></canvas>

<div id="hud">
  <div id="title-block">
    <h1>Voice Pattern Generator</h1>
    <div id="mode-name">LISSAJOUS</div>
  </div>

  <div id="freq-sidebar">
    <div class="freq-row">
      <span class="freq-lbl">BASS</span>
      <div class="freq-track"><div class="freq-fill" id="bar-bass" style="background:#ff6ec7"></div></div>
    </div>
    <div class="freq-row">
      <span class="freq-lbl">LOW MID</span>
      <div class="freq-track"><div class="freq-fill" id="bar-lowmid" style="background:#ffb347"></div></div>
    </div>
    <div class="freq-row">
      <span class="freq-lbl">MID</span>
      <div class="freq-track"><div class="freq-fill" id="bar-mid" style="background:#7fffb2"></div></div>
    </div>
    <div class="freq-row">
      <span class="freq-lbl">HIGH MID</span>
      <div class="freq-track"><div class="freq-fill" id="bar-highmid" style="background:#7fdbff"></div></div>
    </div>
    <div class="freq-row">
      <span class="freq-lbl">TREBLE</span>
      <div class="freq-track"><div class="freq-fill" id="bar-treble" style="background:#c77dff"></div></div>
    </div>
  </div>

  <div id="note-display">
    <div id="note-name">—</div>
    <div id="note-freq">— Hz</div>
  </div>

  <div id="hint"><p>Speak or sing into your microphone</p></div>

  <div id="controls">
    <button class="mode-btn active" data-mode="0">Lissajous</button>
    <button class="mode-btn" data-mode="1">Mandala</button>
    <button class="mode-btn" data-mode="2">Constellation</button>
    <button class="mode-btn" data-mode="3">Interference</button>
    <button class="mode-btn" data-mode="4">All Modes</button>
    <button id="start-btn">Activate Mic</button>
  </div>
</div>

<script>
(function () {
  const canvas = document.getElementById('c');
  const ctx = canvas.getContext('2d');
  let W, H, cx, cy;

  function resize() {
    W = canvas.width = window.innerWidth;
    H = canvas.height = window.innerHeight;
    cx = W / 2; cy = H / 2;
  }
  window.addEventListener('resize', resize);
  resize();

  // ── Audio state ──
  let audioCtx, analyser, freqData, timeData;
  let running = false;

  // ── Smoothed audio values ──
  let sRMS = 0, sBass = 0, sLowMid = 0, sMid = 0, sHighMid = 0, sTreble = 0;
  let sPeakFreq = 0, sCentroid = 0;
  let sHue = 120;

  // ── Visual state ──
  let mode = 0;
  const MODE_NAMES = ['LISSAJOUS', 'MANDALA', 'CONSTELLATION', 'INTERFERENCE', 'ALL MODES'];
  let t = 0;
  let particles = [];
  let lissHistory = [];
  const LISS_HISTORY = 800;

  // Init particle pool
  for (let i = 0; i < 220; i++) {
    particles.push(newParticle());
  }

  function newParticle(fromCenter) {
    const angle = Math.random() * Math.PI * 2;
    const r = fromCenter ? 0 : Math.random() * Math.min(W, H) * 0.45;
    return {
      x: cx + Math.cos(angle) * r,
      y: cy + Math.sin(angle) * r,
      vx: (Math.random() - 0.5) * 0.4,
      vy: (Math.random() - 0.5) * 0.4,
      size: Math.random() * 2.5 + 0.5,
      hue: Math.random() * 360,
      life: Math.random(),
      speed: Math.random() * 0.008 + 0.002,
      orbitR: Math.random() * Math.min(W, H) * 0.38 + 20,
      orbitAngle: Math.random() * Math.PI * 2,
      orbitSpeed: (Math.random() - 0.5) * 0.004,
    };
  }

  // ── Note detection ──
  const NOTE_NAMES = ['C','C#','D','D#','E','F','F#','G','G#','A','A#','B'];
  function freqToNote(freq) {
    if (freq < 60) return { name: '—', cents: 0 };
    const midi = 12 * Math.log2(freq / 440) + 69;
    const note = NOTE_NAMES[Math.round(midi) % 12];
    return { name: note, freq: Math.round(freq) };
  }

  // ── Band energy extraction ──
  function bandEnergy(data, sampleRate, loHz, hiHz) {
    const bins = data.length;
    const lo = Math.floor(loHz * bins * 2 / sampleRate);
    const hi = Math.ceil(hiHz * bins * 2 / sampleRate);
    let sum = 0, count = 0;
    for (let i = Math.max(1, lo); i <= Math.min(bins - 1, hi); i++) {
      sum += data[i] / 255;
      count++;
    }
    return count > 0 ? sum / count : 0;
  }

  function getPeakFreq(data, sampleRate) {
    let max = 0, idx = 0;
    for (let i = 1; i < data.length; i++) {
      if (data[i] > max) { max = data[i]; idx = i; }
    }
    return idx * sampleRate / (analyser.fftSize);
  }

  function getSpectralCentroid(data, sampleRate) {
    let w = 0, a = 0;
    for (let i = 1; i < data.length; i++) {
      const amp = data[i] / 255;
      w += (i * sampleRate / analyser.fftSize) * amp;
      a += amp;
    }
    return a > 0 ? w / a : 0;
  }

  function getRMS(data) {
    let s = 0;
    for (let i = 0; i < data.length; i++) {
      const v = (data[i] - 128) / 128;
      s += v * v;
    }
    return Math.sqrt(s / data.length);
  }

  // ── Activate ──
  document.getElementById('start-btn').addEventListener('click', async () => {
    if (running) return;
    try {
      audioCtx = new (window.AudioContext || window.webkitAudioContext)();
      const stream = await navigator.mediaDevices.getUserMedia({ audio: true });
      const src = audioCtx.createMediaStreamSource(stream);
      analyser = audioCtx.createAnalyser();
      analyser.fftSize = 2048;
      analyser.smoothingTimeConstant = 0.75;
      src.connect(analyser);
      freqData = new Uint8Array(analyser.frequencyBinCount);
      timeData = new Uint8Array(analyser.fftSize);
      running = true;
      document.getElementById('start-btn').textContent = 'Listening…';
      document.getElementById('start-btn').classList.add('live');
      document.getElementById('hint').classList.add('hidden');
    } catch (e) {
      document.getElementById('hint').querySelector('p').textContent = 'Microphone access denied.';
    }
  });

  // ── Mode buttons ──
  document.querySelectorAll('.mode-btn').forEach(btn => {
    btn.addEventListener('click', () => {
      mode = parseInt(btn.dataset.mode);
      document.querySelectorAll('.mode-btn').forEach(b => b.classList.remove('active'));
      btn.classList.add('active');
      document.getElementById('mode-name').textContent = MODE_NAMES[mode];
      lissHistory = [];
    });
  });

  // ── Color helpers ──
  function hsl(h, s, l, a = 1) {
    return `hsla(${h % 360},${s}%,${l}%,${a})`;
  }

  // ══════════════════════════════════════════
  // DRAW FUNCTIONS
  // ══════════════════════════════════════════

  // 1. LISSAJOUS — mic drives two oscillators, voice energy controls deviation
  function drawLissajous(x0, y0, w, h, alpha = 1) {
    const r = Math.min(w, h) * 0.42;
    const freqRatioA = 2 + sBass * 3;       // x-frequency
    const freqRatioB = 3 + sHighMid * 2;    // y-frequency
    const phaseShift = t * 0.3 + sMid * Math.PI;
    const steps = 600 + Math.floor(sCentroid / 80);
    const hueBase = sHue;

    // Trail
    ctx.save();
    ctx.globalAlpha = alpha;

    // Push history point
    const px = x0 + Math.sin(freqRatioA * t * 0.8 + phaseShift) * r * (0.7 + sRMS * 0.5);
    const py = y0 + Math.sin(freqRatioB * t * 0.8) * r * (0.7 + sBass * 0.4);
    lissHistory.push({ x: px, y: py, hue: hueBase, rms: sRMS });
    if (lissHistory.length > LISS_HISTORY) lissHistory.shift();

    // Draw full parametric curve (static, gorgeous pattern)
    ctx.beginPath();
    for (let i = 0; i <= steps; i++) {
      const p = (i / steps) * Math.PI * 2;
      const lx = x0 + Math.sin(freqRatioA * p + phaseShift) * r * (0.7 + sRMS * 0.5);
      const ly = y0 + Math.sin(freqRatioB * p) * r * (0.7 + sBass * 0.4);
      i === 0 ? ctx.moveTo(lx, ly) : ctx.lineTo(lx, ly);
    }
    ctx.strokeStyle = hsl(hueBase, 80, 55, 0.12 + sBass * 0.15);
    ctx.lineWidth = 1;
    ctx.shadowBlur = 0;
    ctx.stroke();

    // Draw glowing trail
    for (let i = 1; i < lissHistory.length; i++) {
      const age = i / lissHistory.length;
      const pt = lissHistory[i];
      const prev = lissHistory[i - 1];
      ctx.beginPath();
      ctx.moveTo(prev.x, prev.y);
      ctx.lineTo(pt.x, pt.y);
      ctx.strokeStyle = hsl(pt.hue + age * 60, 90, 65, age * 0.8 * alpha);
      ctx.lineWidth = 1.5 + pt.rms * 4;
      ctx.shadowBlur = 8 + pt.rms * 20;
      ctx.shadowColor = hsl(pt.hue, 100, 70);
      ctx.stroke();
    }

    // Live dot
    ctx.beginPath();
    ctx.arc(px, py, 3 + sRMS * 12, 0, Math.PI * 2);
    ctx.fillStyle = hsl(hueBase, 100, 90, 0.9);
    ctx.shadowBlur = 20 + sRMS * 40;
    ctx.shadowColor = hsl(hueBase, 100, 80);
    ctx.fill();
    ctx.shadowBlur = 0;
    ctx.restore();
  }

  // 2. MANDALA — polar pattern driven by frequency bands
  function drawMandala(x0, y0, w, h, alpha = 1) {
    const r = Math.min(w, h) * 0.42;
    const petals = Math.round(4 + sCentroid / 300);
    const rotSpeed = sMid * 0.04 + 0.003;
    const innerR = r * (0.15 + sBass * 0.3);
    const outerR = r * (0.5 + sRMS * 0.5);

    ctx.save();
    ctx.globalAlpha = alpha;
    ctx.translate(x0, y0);
    ctx.rotate(t * rotSpeed);

    for (let ring = 0; ring < 3; ring++) {
      const rScale = 0.35 + ring * 0.32;
      const ringHue = sHue + ring * 40;
      const ringR = r * rScale;

      for (let i = 0; i < petals; i++) {
        const angle = (i / petals) * Math.PI * 2;
        const mirror = angle + Math.PI / petals;

        // Petal shape using bezier
        const bandVal = [sBass, sMid, sTreble][ring % 3];
        const petalLen = ringR * (0.6 + bandVal * 0.8);
        const petalW = ringR * (0.25 + sMid * 0.3);

        ctx.beginPath();
        ctx.moveTo(0, 0);
        const cp1x = Math.cos(angle - 0.4) * petalW;
        const cp1y = Math.sin(angle - 0.4) * petalW;
        const cp2x = Math.cos(angle) * petalLen;
        const cp2y = Math.sin(angle) * petalLen;
        const ex = Math.cos(angle) * petalLen * 0.9;
        const ey = Math.sin(angle) * petalLen * 0.9;
        ctx.bezierCurveTo(cp1x, cp1y, cp2x, cp2y, ex, ey);
        ctx.bezierCurveTo(
          Math.cos(mirror) * petalW, Math.sin(mirror) * petalW,
          0, 0, 0, 0
        );

        const grad = ctx.createRadialGradient(0, 0, innerR * 0.3, ex, ey, petalLen * 0.1);
        grad.addColorStop(0, hsl(ringHue, 90, 70, 0.05));
        grad.addColorStop(0.5, hsl(ringHue + 20, 95, 60, 0.3 + bandVal * 0.4));
        grad.addColorStop(1, hsl(ringHue + 50, 100, 75, 0.0));
        ctx.fillStyle = grad;
        ctx.shadowBlur = 10 + bandVal * 30;
        ctx.shadowColor = hsl(ringHue, 100, 70);
        ctx.fill();
      }
    }

    // Center orb
    const orbR = innerR * (0.5 + sRMS * 1.5);
    const orbGrad = ctx.createRadialGradient(0, 0, 0, 0, 0, orbR);
    orbGrad.addColorStop(0, hsl(sHue, 100, 95, 0.9));
    orbGrad.addColorStop(0.4, hsl(sHue + 30, 90, 60, 0.6));
    orbGrad.addColorStop(1, hsl(sHue + 60, 80, 40, 0));
    ctx.beginPath();
    ctx.arc(0, 0, orbR, 0, Math.PI * 2);
    ctx.fillStyle = orbGrad;
    ctx.shadowBlur = 30 + sRMS * 60;
    ctx.shadowColor = hsl(sHue, 100, 80);
    ctx.fill();
    ctx.shadowBlur = 0;

    ctx.restore();
  }

  // 3. CONSTELLATION — particles orbit driven by all bands
  function drawConstellation(x0, y0, w, h, alpha = 1) {
    const maxR = Math.min(w, h) * 0.46;
    ctx.save();
    ctx.globalAlpha = alpha;

    const speed = 0.5 + sMid * 3;
    const spread = 0.8 + sRMS * 0.5;

    // Update + draw particles
    for (let i = 0; i < particles.length; i++) {
      const p = particles[i];
      p.orbitAngle += p.orbitSpeed * speed;
      const targetR = p.orbitR * spread * (maxR / (Math.min(W, H) * 0.38));
      const px = x0 + Math.cos(p.orbitAngle) * Math.min(targetR, maxR);
      const py = y0 + Math.sin(p.orbitAngle) * Math.min(targetR, maxR) * 0.85;

      // Hue follows dominant freq
      p.hue += (sHue + p.orbitAngle * 20 - p.hue) * 0.02;

      const brightness = 40 + sTreble * 35 + sRMS * 25;
      const size = p.size * (1 + sRMS * 4 + sBass * 2);

      ctx.beginPath();
      ctx.arc(px, py, size, 0, Math.PI * 2);
      ctx.fillStyle = hsl(p.hue, 85, brightness, 0.7 + sRMS * 0.3);
      ctx.shadowBlur = 6 + sTreble * 20;
      ctx.shadowColor = hsl(p.hue, 100, 80);
      ctx.fill();
    }

    // Draw connections between nearby particles
    const connectDist = 60 + sBass * 80;
    ctx.lineWidth = 0.4;
    ctx.shadowBlur = 0;
    for (let i = 0; i < particles.length; i += 2) {
      const p = particles[i];
      const px = x0 + Math.cos(p.orbitAngle) * Math.min(p.orbitR * spread, maxR);
      const py = y0 + Math.sin(p.orbitAngle) * Math.min(p.orbitR * spread, maxR) * 0.85;
      for (let j = i + 1; j < particles.length; j += 3) {
        const q = particles[j];
        const qx = x0 + Math.cos(q.orbitAngle) * Math.min(q.orbitR * spread, maxR);
        const qy = y0 + Math.sin(q.orbitAngle) * Math.min(q.orbitR * spread, maxR) * 0.85;
        const d = Math.hypot(px - qx, py - qy);
        if (d < connectDist) {
          ctx.beginPath();
          ctx.moveTo(px, py);
          ctx.lineTo(qx, qy);
          ctx.strokeStyle = hsl(p.hue, 70, 65, (1 - d / connectDist) * 0.35);
          ctx.stroke();
        }
      }
    }

    // Nucleus
    const nucR = 8 + sRMS * 30 + sBass * 20;
    const ng = ctx.createRadialGradient(x0, y0, 0, x0, y0, nucR);
    ng.addColorStop(0, hsl(sHue, 100, 98, 0.95));
    ng.addColorStop(0.5, hsl(sHue + 40, 90, 65, 0.5));
    ng.addColorStop(1, hsl(sHue + 80, 80, 40, 0));
    ctx.beginPath();
    ctx.arc(x0, y0, nucR, 0, Math.PI * 2);
    ctx.fillStyle = ng;
    ctx.shadowBlur = 30 + sRMS * 50;
    ctx.shadowColor = hsl(sHue, 100, 80);
    ctx.fill();
    ctx.shadowBlur = 0;

    ctx.restore();
  }

  // 4. INTERFERENCE — standing wave / ripple pattern
  function drawInterference(x0, y0, w, h, alpha = 1) {
    const maxR = Math.min(w, h) * 0.46;
    const rings = Math.round(6 + sCentroid / 400);
    const waveFreq = 3 + sBass * 5;
    const distortion = sMid * 0.35 + sHighMid * 0.2;

    ctx.save();
    ctx.globalAlpha = alpha;

    // Source 1 offset
    const s1x = x0 - maxR * 0.25 * (1 + sBass * 0.5);
    const s1y = y0 + Math.sin(t * 0.3) * maxR * 0.1;
    // Source 2 offset
    const s2x = x0 + maxR * 0.25 * (1 + sHighMid * 0.5);
    const s2y = y0 - Math.sin(t * 0.3) * maxR * 0.1;

    const res = 3;
    for (let px = x0 - maxR; px <= x0 + maxR; px += res) {
      for (let py = y0 - maxR; py <= y0 + maxR; py += res) {
        const d1 = Math.hypot(px - s1x, py - s1y);
        const d2 = Math.hypot(px - s2x, py - s2y);
        if (d1 > maxR || d2 > maxR) continue;

        const wave1 = Math.sin(d1 * 0.06 * waveFreq - t * 2 + distortion * Math.sin(d2 * 0.04));
        const wave2 = Math.sin(d2 * 0.06 * waveFreq - t * 2 + distortion * Math.sin(d1 * 0.04));
        const interference = (wave1 + wave2) * 0.5;

        const energy = (interference + 1) * 0.5;
        const dist = Math.min(d1, d2);
        const fade = Math.max(0, 1 - dist / maxR);

        const hue = sHue + interference * 80 + sTreble * 60;
        const brightness = 35 + energy * 50;
        const sat = 70 + sBass * 30;
        const a = energy * fade * (0.5 + sRMS * 0.5) * 0.85;

        ctx.fillStyle = hsl(hue, sat, brightness, a);
        ctx.fillRect(px - res / 2, py - res / 2, res, res);
      }
    }

    // Glowing source nodes
    for (const [sx, sy] of [[s1x, s1y], [s2x, s2y]]) {
      const sg = ctx.createRadialGradient(sx, sy, 0, sx, sy, 18 + sRMS * 25);
      sg.addColorStop(0, hsl(sHue, 100, 98, 0.95));
      sg.addColorStop(0.4, hsl(sHue + 40, 90, 65, 0.4));
      sg.addColorStop(1, 'rgba(0,0,0,0)');
      ctx.beginPath();
      ctx.arc(sx, sy, 18 + sRMS * 25, 0, Math.PI * 2);
      ctx.fillStyle = sg;
      ctx.shadowBlur = 20 + sRMS * 40;
      ctx.shadowColor = hsl(sHue, 100, 80);
      ctx.fill();
    }
    ctx.shadowBlur = 0;
    ctx.restore();
  }

  // ── Main render loop ──
  let lastTime = 0;
  function render(now) {
    requestAnimationFrame(render);
    const dt = Math.min((now - lastTime) / 1000, 0.05);
    lastTime = now;
    t += dt;

    // ── Update audio ──
    if (running && analyser) {
      analyser.getByteFrequencyData(freqData);
      analyser.getByteTimeDomainData(timeData);

      const sr = audioCtx.sampleRate;
      const rms = getRMS(timeData);
      const bass = bandEnergy(freqData, sr, 20, 200);
      const lowmid = bandEnergy(freqData, sr, 200, 600);
      const mid = bandEnergy(freqData, sr, 600, 2000);
      const highmid = bandEnergy(freqData, sr, 2000, 5000);
      const treble = bandEnergy(freqData, sr, 5000, 12000);
      const peak = getPeakFreq(freqData, sr);
      const centroid = getSpectralCentroid(freqData, sr);

      const sm = 0.12;
      sRMS     = sRMS     * (1 - sm) + rms     * sm * 5;
      sBass    = sBass    * (1 - sm) + bass    * sm * 3;
      sLowMid  = sLowMid  * (1 - sm) + lowmid  * sm * 3;
      sMid     = sMid     * (1 - sm) + mid      * sm * 3;
      sHighMid = sHighMid * (1 - sm) + highmid * sm * 3;
      sTreble  = sTreble  * (1 - sm) + treble  * sm * 3;
      sPeakFreq = sPeakFreq * 0.9 + peak * 0.1;
      sCentroid = sCentroid * 0.9 + centroid * 0.1;

      // Map peak freq to hue: low=pink/red, mid=green/cyan, high=violet
      const targetHue = (sPeakFreq / 800) * 200 + 160;
      sHue = sHue * 0.93 + targetHue * 0.07;

      // Update sidebar bars
      document.getElementById('bar-bass').style.width = Math.min(100, sBass * 100) + '%';
      document.getElementById('bar-lowmid').style.width = Math.min(100, sLowMid * 100) + '%';
      document.getElementById('bar-mid').style.width = Math.min(100, sMid * 100) + '%';
      document.getElementById('bar-highmid').style.width = Math.min(100, sHighMid * 100) + '%';
      document.getElementById('bar-treble').style.width = Math.min(100, sTreble * 100) + '%';

      // Note display
      if (sRMS > 0.04) {
        const note = freqToNote(sPeakFreq);
        const nd = document.getElementById('note-name');
        const nf = document.getElementById('note-freq');
        nd.textContent = note.name;
        nd.style.color = `hsla(${sHue % 360},80%,70%,0.55)`;
        nd.style.textShadow = `0 0 40px hsla(${sHue % 360},100%,70%,0.3)`;
        nf.textContent = `${Math.round(sPeakFreq)} Hz`;
        nf.style.color = `hsla(${sHue % 360},70%,60%,0.4)`;
      }
    } else {
      // Idle: slow drift
      sRMS = 0.02 + Math.sin(t * 0.4) * 0.015;
      sBass = 0.05 + Math.sin(t * 0.3) * 0.03;
      sMid = 0.04 + Math.sin(t * 0.5) * 0.025;
      sTreble = 0.03 + Math.sin(t * 0.7) * 0.015;
      sHighMid = 0.03;
      sCentroid = 800 + Math.sin(t * 0.2) * 400;
      sHue = (t * 15) % 360;
    }

    // ── Draw ──
    // Fade trail
    ctx.fillStyle = `rgba(0,0,0,${0.12 + (1 - sRMS) * 0.08})`;
    ctx.fillRect(0, 0, W, H);

    if (mode === 4) {
      // All modes in quadrants
      const hw = W / 2, hh = H / 2;
      drawLissajous(hw * 0.5, hh * 0.5, hw, hh, 0.85);
      drawMandala(hw * 1.5, hh * 0.5, hw, hh, 0.85);
      drawConstellation(hw * 0.5, hh * 1.5, hw, hh, 0.85);
      drawInterference(hw * 1.5, hh * 1.5, hw, hh, 0.85);

      // Quad labels
      ctx.font = '9px "Josefin Sans"';
      ctx.letterSpacing = '3px';
      ctx.fillStyle = 'rgba(255,255,255,0.18)';
      ctx.fillText('LISSAJOUS', 14, 18);
      ctx.fillText('MANDALA', hw + 14, 18);
      ctx.fillText('CONSTELLATION', 14, hh + 18);
      ctx.fillText('INTERFERENCE', hw + 14, hh + 18);

      // Grid dividers
      ctx.strokeStyle = 'rgba(255,255,255,0.05)';
      ctx.lineWidth = 1;
      ctx.beginPath(); ctx.moveTo(hw, 0); ctx.lineTo(hw, H); ctx.stroke();
      ctx.beginPath(); ctx.moveTo(0, hh); ctx.lineTo(W, hh); ctx.stroke();
    } else if (mode === 0) {
      drawLissajous(cx, cy, W, H, 1);
    } else if (mode === 1) {
      drawMandala(cx, cy, W, H, 1);
    } else if (mode === 2) {
      drawConstellation(cx, cy, W, H, 1);
    } else if (mode === 3) {
      drawInterference(cx, cy, W, H, 1);
    }
  }
  requestAnimationFrame(render);

})();
</script>
</body>
</html>
