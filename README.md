<div align="center">

<!-- ═══════════════════════════════════════════ HERO SVG ═══ -->
<svg width="100%" viewBox="0 0 860 260" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <!-- Deep-space background gradient -->
    <radialGradient id="bgRadial" cx="50%" cy="40%" r="70%">
      <stop offset="0%"   stop-color="#0d1829"/>
      <stop offset="45%"  stop-color="#080f1a"/>
      <stop offset="100%" stop-color="#04080e"/>
    </radialGradient>
    <!-- 3D Name gradient: left-cyan → white-center → right-purple -->
    <linearGradient id="nameGrad3D" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%"   stop-color="#00cfff"/>
      <stop offset="30%"  stop-color="#7ee8ff"/>
      <stop offset="50%"  stop-color="#ffffff"/>
      <stop offset="70%"  stop-color="#b89aff"/>
      <stop offset="100%" stop-color="#7B2FFF"/>
    </linearGradient>
    <!-- Shadow/depth layer for 3D text -->
    <linearGradient id="nameShadow" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%"   stop-color="#004466" stop-opacity="0.6"/>
      <stop offset="50%"  stop-color="#222244" stop-opacity="0.4"/>
      <stop offset="100%" stop-color="#2a0055" stop-opacity="0.6"/>
    </linearGradient>
    <!-- Glow filter for name -->
    <filter id="nameGlow" x="-20%" y="-60%" width="140%" height="220%">
      <feGaussianBlur in="SourceGraphic" stdDeviation="6" result="blur1"/>
      <feGaussianBlur in="SourceGraphic" stdDeviation="14" result="blur2"/>
      <feMerge>
        <feMergeNode in="blur2"/>
        <feMergeNode in="blur1"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>
    <!-- Subtle grid tile -->
    <pattern id="grid" x="0" y="0" width="50" height="50" patternUnits="userSpaceOnUse">
      <path d="M50 0L0 0L0 50" fill="none" stroke="#00D9FF" stroke-width="0.3" stroke-opacity="0.07"/>
    </pattern>
    <!-- Perspective floor lines clipping -->
    <clipPath id="heroClip">
      <rect width="860" height="260" rx="14"/>
    </clipPath>
    <!-- Animated sweep gradient -->
    <linearGradient id="sweep" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%"   stop-color="#00D9FF" stop-opacity="0"/>
      <stop offset="50%"  stop-color="#00D9FF" stop-opacity="0.12"/>
      <stop offset="100%" stop-color="#00D9FF" stop-opacity="0"/>
    </linearGradient>
    <!-- Line glow gradient -->
    <linearGradient id="lineGlow" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%"   stop-color="#00D9FF" stop-opacity="0"/>
      <stop offset="25%"  stop-color="#00D9FF" stop-opacity="0.9"/>
      <stop offset="50%"  stop-color="#ffffff" stop-opacity="1"/>
      <stop offset="75%"  stop-color="#7B2FFF" stop-opacity="0.9"/>
      <stop offset="100%" stop-color="#7B2FFF" stop-opacity="0"/>
    </linearGradient>
    <filter id="lineFilter">
      <feGaussianBlur stdDeviation="1.5" result="b"/>
      <feMerge><feMergeNode in="b"/><feMergeNode in="SourceGraphic"/></feMerge>
    </filter>
  </defs>

  <g clip-path="url(#heroClip)">
    <!-- BG -->
    <rect width="860" height="260" fill="url(#bgRadial)"/>
    <!-- Grid -->
    <rect width="860" height="260" fill="url(#grid)"/>

    <!-- Perspective floor lines (vanishing point effect) -->
    <g stroke="#00D9FF" stroke-opacity="0.06" stroke-width="0.6">
      <line x1="430" y1="160" x2="0"   y2="260"/><line x1="430" y1="160" x2="86"  y2="260"/>
      <line x1="430" y1="160" x2="172" y2="260"/><line x1="430" y1="160" x2="258" y2="260"/>
      <line x1="430" y1="160" x2="344" y2="260"/><line x1="430" y1="160" x2="430" y2="260"/>
      <line x1="430" y1="160" x2="516" y2="260"/><line x1="430" y1="160" x2="602" y2="260"/>
      <line x1="430" y1="160" x2="688" y2="260"/><line x1="430" y1="160" x2="774" y2="260"/>
      <line x1="430" y1="160" x2="860" y2="260"/>
      <!-- Horizontal floor lines -->
      <line x1="0" y1="185" x2="860" y2="185"/><line x1="0" y1="205" x2="860" y2="205"/>
      <line x1="0" y1="222" x2="860" y2="222"/><line x1="0" y1="237" x2="860" y2="237"/>
      <line x1="0" y1="250" x2="860" y2="250"/>
    </g>

    <!-- Ambient light blobs -->
    <ellipse cx="200" cy="80" rx="180" ry="80" fill="#00D9FF" opacity="0.03">
      <animate attributeName="opacity" values="0.03;0.07;0.03" dur="5s" repeatCount="indefinite"/>
    </ellipse>
    <ellipse cx="660" cy="90" rx="160" ry="70" fill="#7B2FFF" opacity="0.04">
      <animate attributeName="opacity" values="0.04;0.09;0.04" dur="4.2s" repeatCount="indefinite"/>
    </ellipse>

    <!-- Animated sweep bar -->
    <rect x="-180" y="0" width="180" height="260" fill="url(#sweep)">
      <animateTransform attributeName="transform" type="translate" from="-180 0" to="1040 0" dur="5s" repeatCount="indefinite" calcMode="spline" keySplines="0.4,0,0.6,1"/>
    </rect>

    <!-- Floating particles -->
    <circle cx="60"  cy="40"  r="1.5" fill="#00D9FF" opacity="0.7"><animate attributeName="cy" values="40;30;40"   dur="3.2s" repeatCount="indefinite"/><animate attributeName="opacity" values="0.7;0.2;0.7" dur="3.2s" repeatCount="indefinite"/></circle>
    <circle cx="160" cy="25"  r="1"   fill="#7B2FFF"  opacity="0.6"><animate attributeName="cy" values="25;18;25"   dur="2.7s" repeatCount="indefinite"/><animate attributeName="opacity" values="0.6;0.1;0.6" dur="2.7s" repeatCount="indefinite"/></circle>
    <circle cx="720" cy="35"  r="1.5" fill="#00D9FF" opacity="0.7"><animate attributeName="cy" values="35;25;35"   dur="3.6s" repeatCount="indefinite"/><animate attributeName="opacity" values="0.7;0.2;0.7" dur="3.6s" repeatCount="indefinite"/></circle>
    <circle cx="810" cy="55"  r="1"   fill="#A8FF78"  opacity="0.5"><animate attributeName="cy" values="55;45;55"   dur="2.4s" repeatCount="indefinite"/><animate attributeName="opacity" values="0.5;0.1;0.5" dur="2.4s" repeatCount="indefinite"/></circle>
    <circle cx="320" cy="18"  r="1"   fill="#7B2FFF"  opacity="0.4"><animate attributeName="cy" values="18;10;18"   dur="4.1s" repeatCount="indefinite"/><animate attributeName="opacity" values="0.4;0.1;0.4" dur="4.1s" repeatCount="indefinite"/></circle>
    <circle cx="540" cy="22"  r="1.5" fill="#00D9FF" opacity="0.5"><animate attributeName="cy" values="22;32;22"   dur="3.9s" repeatCount="indefinite"/><animate attributeName="opacity" values="0.5;0.1;0.5" dur="3.9s" repeatCount="indefinite"/></circle>
    <circle cx="50"  cy="200" r="1"   fill="#A8FF78"  opacity="0.4"><animate attributeName="opacity" values="0.4;0.8;0.4" dur="2.1s" repeatCount="indefinite"/></circle>
    <circle cx="800" cy="210" r="1"   fill="#A8FF78"  opacity="0.4"><animate attributeName="opacity" values="0.4;0.8;0.4" dur="2.9s" repeatCount="indefinite"/></circle>

    <!-- Bracket ornaments -->
    <g fill="none" stroke="#00D9FF" stroke-width="1.8" stroke-opacity="0.25">
      <path d="M28 62 L16 62 L16 98 L28 98"/>
      <path d="M832 62 L844 62 L844 98 L832 98"/>
    </g>

    <!-- ── 3D NAME: depth shadow layers, then main ── -->
    <!-- Layer 5 (deepest shadow) -->
    <text x="435" y="95" text-anchor="middle" font-family="'Segoe UI','Arial Black',sans-serif" font-size="56" font-weight="900" fill="url(#nameShadow)" letter-spacing="1.5" opacity="0.25">Bahriddin Khamidov</text>
    <!-- Layer 4 -->
    <text x="434" y="94" text-anchor="middle" font-family="'Segoe UI','Arial Black',sans-serif" font-size="56" font-weight="900" fill="url(#nameShadow)" letter-spacing="1.5" opacity="0.3">Bahriddin Khamidov</text>
    <!-- Layer 3 -->
    <text x="433" y="93" text-anchor="middle" font-family="'Segoe UI','Arial Black',sans-serif" font-size="56" font-weight="900" fill="url(#nameShadow)" letter-spacing="1.5" opacity="0.4">Bahriddin Khamidov</text>
    <!-- Layer 2 (mid) -->
    <text x="432" y="92" text-anchor="middle" font-family="'Segoe UI','Arial Black',sans-serif" font-size="56" font-weight="900" fill="url(#nameShadow)" letter-spacing="1.5" opacity="0.55">Bahriddin Khamidov</text>
    <!-- Glow bloom -->
    <text x="430" y="90" text-anchor="middle" font-family="'Segoe UI','Arial Black',sans-serif" font-size="56" font-weight="900" fill="url(#nameGrad3D)" letter-spacing="1.5" filter="url(#nameGlow)" opacity="0.55">Bahriddin Khamidov</text>
    <!-- Main crisp layer -->
    <text x="430" y="90" text-anchor="middle" font-family="'Segoe UI','Arial Black',sans-serif" font-size="56" font-weight="900" fill="url(#nameGrad3D)" letter-spacing="1.5">
      Bahriddin Khamidov
      <animateTransform attributeName="transform" type="scale" additive="sum"
        values="1 1;1.008 1.004;1 1" dur="4s" repeatCount="indefinite" calcMode="spline" keySplines="0.45,0,0.55,1;0.45,0,0.55,1"/>
    </text>

    <!-- Animated glowing underline -->
    <rect x="160" y="100" width="540" height="2" fill="url(#lineGlow)" rx="1" filter="url(#lineFilter)">
      <animate attributeName="opacity" values="0.5;1;0.5" dur="2.5s" repeatCount="indefinite"/>
      <animate attributeName="width"   values="400;540;400" dur="4s"   repeatCount="indefinite" calcMode="spline" keySplines="0.4,0,0.6,1;0.4,0,0.6,1"/>
      <animateTransform attributeName="transform" type="translate" values="70 0;0 0;70 0" dur="4s" repeatCount="indefinite" calcMode="spline" keySplines="0.4,0,0.6,1;0.4,0,0.6,1"/>
    </rect>

    <!-- Role subtitle -->
    <text x="430" y="128" text-anchor="middle" font-family="'Courier New',monospace" font-size="12" fill="#8892B0" letter-spacing="4">BACKEND DEVELOPER · NODE.JS · MONGODB · TYPESCRIPT</text>

    <!-- Location pill -->
    <rect x="305" y="142" width="250" height="28" rx="14" fill="#06101e" stroke="#00D9FF" stroke-width="0.8" stroke-opacity="0.45"/>
    <circle cx="322" cy="156" r="4.5" fill="#22dd55">
      <animate attributeName="r"       values="4;6;4"   dur="1.8s" repeatCount="indefinite"/>
      <animate attributeName="opacity" values="1;0.5;1" dur="1.8s" repeatCount="indefinite"/>
    </circle>
    <text x="430" y="161" text-anchor="middle" font-family="'Courier New',monospace" font-size="11" fill="#00D9FF" letter-spacing="1">🇺🇿  Samarqand, Uzbekistan</text>
  </g>
</svg>

<!-- ═══════════════════════════════ CONTACT BADGES (real icons via SVG paths) ═══ -->
<br/>

<svg width="600" viewBox="0 0 600 48" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <filter id="btnGlow">
      <feGaussianBlur stdDeviation="2.5" result="b"/>
      <feMerge><feMergeNode in="b"/><feMergeNode in="SourceGraphic"/></feMerge>
    </filter>
  </defs>

  <!-- TELEGRAM -->
  <a href="https://t.me/bakhridd1n_dev">
    <rect x="4" y="6" width="130" height="34" rx="17" fill="#04101e" stroke="#2CA5E0" stroke-width="1.2"/>
    <!-- Telegram plane icon (official shape) -->
    <g transform="translate(18,17) scale(0.72)" fill="#2CA5E0">
      <path d="M22.265 2.428L1.064 10.979c-1.454.582-1.446 1.39-.265 1.75l5.45 1.697 12.607-7.947c.594-.362 1.138-.167.692.23L8.093 18.044l-.378 5.69c.554 0 .8-.254 1.11-.553l2.66-2.583 5.528 4.082c1.02.562 1.753.272 2.007-.946l3.63-17.1c.372-1.49-.567-2.165-1.384-1.806z"/>
    </g>
    <text x="84" y="28" text-anchor="middle" font-family="'Segoe UI',sans-serif" font-size="11" font-weight="600" fill="#2CA5E0">Telegram</text>
  </a>

  <!-- GMAIL -->
  <a href="mailto:bahriddinhamidov057@gmail.com">
    <rect x="144" y="6" width="120" height="34" rx="17" fill="#04101e" stroke="#EA4335" stroke-width="1.2"/>
    <!-- Gmail M icon -->
    <g transform="translate(158,14)" fill="none">
      <rect width="20" height="16" rx="2" fill="#04101e" stroke="#EA4335" stroke-width="1"/>
      <polyline points="0,0 10,9 20,0" fill="none" stroke="#EA4335" stroke-width="1.5" stroke-linejoin="round"/>
    </g>
    <text x="216" y="28" text-anchor="middle" font-family="'Segoe UI',sans-serif" font-size="11" font-weight="600" fill="#EA4335">Gmail</text>
  </a>

  <!-- GITHUB -->
  <a href="https://github.com/khamidoff633">
    <rect x="274" y="6" width="120" height="34" rx="17" fill="#04101e" stroke="#6e40c9" stroke-width="1.2"/>
    <!-- GitHub octocat path (simplified official) -->
    <g transform="translate(288,13) scale(0.83)">
      <path fill="#9B59D6" d="M10 0C4.477 0 0 4.477 0 10c0 4.418 2.865 8.166 6.839 9.489.5.092.682-.217.682-.482 0-.237-.009-.868-.013-1.703-2.782.604-3.369-1.342-3.369-1.342-.454-1.155-1.11-1.463-1.11-1.463-.908-.62.069-.608.069-.608 1.003.07 1.531 1.03 1.531 1.03.892 1.529 2.341 1.087 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.11-4.555-4.943 0-1.091.39-1.984 1.029-2.683-.103-.253-.446-1.27.098-2.647 0 0 .84-.269 2.75 1.025A9.578 9.578 0 0110 4.836c.85.004 1.705.114 2.504.336 1.909-1.294 2.747-1.025 2.747-1.025.546 1.377.203 2.394.1 2.647.64.699 1.028 1.592 1.028 2.683 0 3.842-2.339 4.687-4.566 4.935.359.309.678.919.678 1.852 0 1.336-.012 2.415-.012 2.744 0 .267.18.579.688.481C17.138 18.163 20 14.418 20 10 20 4.477 15.523 0 10 0z"/>
    </g>
    <text x="346" y="28" text-anchor="middle" font-family="'Segoe UI',sans-serif" font-size="11" font-weight="600" fill="#9B59D6">GitHub</text>
  </a>

  <!-- OPEN TO WORK -->
  <rect x="404" y="6" width="152" height="34" rx="17" fill="#04101e" stroke-width="1.4">
    <animate attributeName="stroke" values="#00D9FF;#7B2FFF;#00D9FF" dur="3s" repeatCount="indefinite"/>
  </rect>
  <circle cx="422" cy="23" r="5" fill="#22dd55">
    <animate attributeName="r"       values="4;6.5;4" dur="1.6s" repeatCount="indefinite"/>
    <animate attributeName="opacity" values="1;0.5;1"  dur="1.6s" repeatCount="indefinite"/>
  </circle>
  <text x="487" y="28" text-anchor="middle" font-family="'Segoe UI',sans-serif" font-size="11" font-weight="600" fill="#00D9FF">Open to Work</text>
</svg>

<br/>

</div>

---

<!-- ═════════════════════════════════ TERMINAL ═══════════════ -->
<div align="center">
<svg width="100%" viewBox="0 0 860 310" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <linearGradient id="termBg" x1="0%" y1="0%" x2="0%" y2="100%">
      <stop offset="0%"   stop-color="#0b0b18"/>
      <stop offset="100%" stop-color="#060610"/>
    </linearGradient>
  </defs>
  <rect width="860" height="310" rx="12" fill="url(#termBg)" stroke="#00D9FF" stroke-width="0.5" stroke-opacity="0.18"/>
  <rect x="0" y="0" width="860" height="38" rx="12" fill="#13132a"/>
  <rect x="0" y="26" width="860" height="12" fill="#13132a"/>
  <circle cx="22" cy="19" r="6" fill="#FF5F57"/>
  <circle cx="42" cy="19" r="6" fill="#FFBD2E"/>
  <circle cx="62" cy="19" r="6" fill="#28CA41"/>
  <text x="430" y="24" text-anchor="middle" font-family="monospace" font-size="11" fill="#444">profile.yaml — zsh</text>
  <text x="20" y="65" font-family="'Courier New',monospace" font-size="12" fill="#7B2FFF" font-weight="700">┌──(khamidoff633㉿backend-dev)</text>
  <text x="290" y="65" font-family="'Courier New',monospace" font-size="12" fill="#00D9FF">[~/about]</text>
  <text x="20" y="83" font-family="'Courier New',monospace" font-size="12" fill="#7B2FFF" font-weight="700">└─$</text>
  <text x="50" y="83" font-family="'Courier New',monospace" font-size="12" fill="#CCD6F6"> cat profile.yaml</text>
  <text x="174" y="83" font-family="'Courier New',monospace" font-size="12" fill="#28CA41"><animate attributeName="opacity" values="1;0;1" dur="1s" repeatCount="indefinite"/>▌</text>
  <text x="20" y="109" font-family="'Courier New',monospace" font-size="12" fill="#00D9FF">name</text><text x="70" y="109" font-family="'Courier New',monospace" font-size="12" fill="#CCD6F6">:     </text><text x="116" y="109" font-family="'Courier New',monospace" font-size="12" fill="#FFA657">"Bahriddin Khamidov"</text>
  <text x="20" y="127" font-family="'Courier New',monospace" font-size="12" fill="#00D9FF">age</text><text x="70" y="127" font-family="'Courier New',monospace" font-size="12" fill="#CCD6F6">:      </text><text x="116" y="127" font-family="'Courier New',monospace" font-size="12" fill="#A8FF78">17</text><text x="142" y="127" font-family="'Courier New',monospace" font-size="12" fill="#444">  # Young. Hungry. Unstoppable.</text>
  <text x="20" y="145" font-family="'Courier New',monospace" font-size="12" fill="#00D9FF">location</text><text x="90" y="145" font-family="'Courier New',monospace" font-size="12" fill="#CCD6F6">: </text><text x="104" y="145" font-family="'Courier New',monospace" font-size="12" fill="#FFA657">"Samarqand, Uzbekistan 🇺🇿"</text>
  <text x="20" y="163" font-family="'Courier New',monospace" font-size="12" fill="#00D9FF">role</text><text x="70" y="163" font-family="'Courier New',monospace" font-size="12" fill="#CCD6F6">:     </text><text x="116" y="163" font-family="'Courier New',monospace" font-size="12" fill="#FFA657">"Backend Developer"</text>
  <text x="20" y="181" font-family="'Courier New',monospace" font-size="12" fill="#00D9FF">status</text><text x="70" y="181" font-family="'Courier New',monospace" font-size="12" fill="#CCD6F6">:   </text><circle cx="110" cy="177" r="4" fill="#22dd55"><animate attributeName="r" values="3;5;3" dur="1.5s" repeatCount="indefinite"/></circle><text x="120" y="181" font-family="'Courier New',monospace" font-size="12" fill="#22dd55">Open to Work — Full-time | Freelance</text>
  <text x="20" y="199" font-family="'Courier New',monospace" font-size="12" fill="#00D9FF">core</text><text x="70" y="199" font-family="'Courier New',monospace" font-size="12" fill="#CCD6F6">:     [</text><text x="124" y="199" font-family="'Courier New',monospace" font-size="12" fill="#FFA657">Node.js, Express, MongoDB, JWT</text><text x="358" y="199" font-family="'Courier New',monospace" font-size="12" fill="#CCD6F6">]</text>
  <text x="20" y="217" font-family="'Courier New',monospace" font-size="12" fill="#00D9FF">learning</text><text x="90" y="217" font-family="'Courier New',monospace" font-size="12" fill="#CCD6F6">: [</text><text x="114" y="217" font-family="'Courier New',monospace" font-size="12" fill="#7B2FFF">Docker, PostgreSQL, Redis, Nginx, GraphQL</text><text x="428" y="217" font-family="'Courier New',monospace" font-size="12" fill="#CCD6F6">]</text>
  <text x="20" y="235" font-family="'Courier New',monospace" font-size="12" fill="#00D9FF">motto</text><text x="70" y="235" font-family="'Courier New',monospace" font-size="12" fill="#CCD6F6">:    </text><text x="110" y="235" font-family="'Courier New',monospace" font-size="12" fill="#FFA657">"Clean code. Real impact. No excuses."</text>
  <line x1="20" y1="249" x2="840" y2="249" stroke="#00D9FF" stroke-opacity="0.08"/>
  <text x="20" y="269" font-family="'Courier New',monospace" font-size="12" fill="#7B2FFF" font-weight="700">┌──(khamidoff633㉿backend-dev)</text>
  <text x="290" y="269" font-family="'Courier New',monospace" font-size="12" fill="#00D9FF">[~/about]</text>
  <text x="20" y="287" font-family="'Courier New',monospace" font-size="12" fill="#7B2FFF" font-weight="700">└─$</text>
  <text x="50" y="287" font-family="'Courier New',monospace" font-size="12" fill="#28CA41"><animate attributeName="opacity" values="1;0;1" dur="1s" repeatCount="indefinite"/>█</text>
</svg>
</div>

---

<!-- ═══════════════════════════ TECH STACK with real SVG icons ══ -->

## ⚙️ Tech Stack

<div align="center">

<!-- BACKEND ROW -->
<svg width="100%" viewBox="0 0 860 68" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <linearGradient id="scanG" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%"   stop-color="#00D9FF" stop-opacity="0"/>
      <stop offset="50%"  stop-color="#00D9FF" stop-opacity="0.18"/>
      <stop offset="100%" stop-color="#00D9FF" stop-opacity="0"/>
    </linearGradient>
  </defs>

  <!-- Node.js pill -->
  <rect x="4"   y="10" width="140" height="42" rx="21" fill="#0a1a0a" stroke="#339933" stroke-width="1.3"/>
  <!-- Node.js hexagon icon approximation -->
  <polygon points="21,24 27,20 33,24 33,32 27,36 21,32" fill="none" stroke="#339933" stroke-width="1.5"/>
  <text x="30" y="30" font-family="monospace" font-size="8" fill="#339933" font-weight="700" text-anchor="middle">JS</text>
  <text x="90" y="36" text-anchor="middle" font-family="'Segoe UI',sans-serif" font-size="12" font-weight="700" fill="#5adb5a">Node.js</text>

  <!-- Express.js pill -->
  <rect x="152" y="10" width="140" height="42" rx="21" fill="#111" stroke="#666" stroke-width="1.3"/>
  <!-- Express minimalist "E" icon -->
  <g transform="translate(167,20)" fill="none" stroke="#999" stroke-width="1.5" stroke-linecap="round">
    <line x1="0" y1="0"  x2="12" y2="0"/><line x1="0" y1="6"  x2="9"  y2="6"/>
    <line x1="0" y1="12" x2="12" y2="12"/><line x1="0" y1="0"  x2="0"  y2="12"/>
  </g>
  <text x="238" y="36" text-anchor="middle" font-family="'Segoe UI',sans-serif" font-size="12" font-weight="700" fill="#aaa">Express.js</text>

  <!-- MongoDB pill -->
  <rect x="300" y="10" width="140" height="42" rx="21" fill="#081a08" stroke="#47A248" stroke-width="1.3"/>
  <!-- MongoDB leaf icon -->
  <g transform="translate(316,16)">
    <path d="M6 0 C6 0 12 4 12 12 C12 18 6 22 6 22 C6 22 0 18 0 12 C0 4 6 0 6 0Z" fill="#47A248"/>
    <line x1="6" y1="14" x2="6" y2="24" stroke="#47A248" stroke-width="1.5"/>
  </g>
  <text x="386" y="36" text-anchor="middle" font-family="'Segoe UI',sans-serif" font-size="12" font-weight="700" fill="#5cc45c">MongoDB</text>

  <!-- TypeScript pill -->
  <rect x="448" y="10" width="140" height="42" rx="21" fill="#041428" stroke="#3178C6" stroke-width="1.3"/>
  <!-- TypeScript "TS" square icon -->
  <rect x="463" y="18" width="22" height="22" rx="3" fill="#3178C6"/>
  <text x="474" y="33" text-anchor="middle" font-family="'Arial Black',sans-serif" font-size="9" font-weight="900" fill="#fff">TS</text>
  <text x="534" y="36" text-anchor="middle" font-family="'Segoe UI',sans-serif" font-size="12" font-weight="700" fill="#5aaae8">TypeScript</text>

  <!-- JWT pill -->
  <rect x="596" y="10" width="120" height="42" rx="21" fill="#0a0a0a" stroke="#fb015b" stroke-width="1.3"/>
  <!-- JWT lock icon simple -->
  <g transform="translate(611,18)">
    <rect x="2" y="8" width="12" height="10" rx="2" fill="none" stroke="#fb015b" stroke-width="1.4"/>
    <path d="M5 8 L5 5 C5 2.5 11 2.5 11 5 L11 8" fill="none" stroke="#fb015b" stroke-width="1.4"/>
    <circle cx="8" cy="13" r="1.5" fill="#fb015b"/>
  </g>
  <text x="668" y="36" text-anchor="middle" font-family="'Segoe UI',sans-serif" font-size="12" font-weight="700" fill="#fb015b">JWT</text>

  <!-- REST API pill -->
  <rect x="724" y="10" width="128" height="42" rx="21" fill="#0d0a00" stroke="#FF6C37" stroke-width="1.3"/>
  <g transform="translate(739,19)">
    <circle cx="8" cy="8" r="7" fill="none" stroke="#FF6C37" stroke-width="1.4"/>
    <line x1="8" y1="1"  x2="8"  y2="15" stroke="#FF6C37" stroke-width="1"/>
    <line x1="1" y1="8"  x2="15" y2="8"  stroke="#FF6C37" stroke-width="1"/>
    <ellipse cx="8" cy="8" rx="3.5" ry="7" fill="none" stroke="#FF6C37" stroke-width="0.8"/>
  </g>
  <text x="800" y="36" text-anchor="middle" font-family="'Segoe UI',sans-serif" font-size="12" font-weight="700" fill="#FF6C37">REST API</text>

  <!-- Scan animation -->
  <rect x="-180" y="0" width="180" height="68" fill="url(#scanG)">
    <animateTransform attributeName="transform" type="translate" from="-180 0" to="1040 0" dur="4.5s" repeatCount="indefinite"/>
  </rect>
</svg>

<!-- FRONTEND ROW -->
<svg width="100%" viewBox="0 0 860 68" xmlns="http://www.w3.org/2000/svg">
  <!-- React pill -->
  <rect x="4" y="10" width="128" height="42" rx="21" fill="#03111e" stroke="#61DAFB" stroke-width="1.3"/>
  <!-- React atom icon -->
  <g transform="translate(18,20)" fill="none" stroke="#61DAFB" stroke-width="1.3">
    <circle cx="9" cy="9" r="2.5" fill="#61DAFB"/>
    <ellipse cx="9" cy="9" rx="9" ry="3.5"/>
    <ellipse cx="9" cy="9" rx="9" ry="3.5" transform="rotate(60 9 9)"/>
    <ellipse cx="9" cy="9" rx="9" ry="3.5" transform="rotate(120 9 9)"/>
  </g>
  <text x="78" y="36" text-anchor="middle" font-family="'Segoe UI',sans-serif" font-size="12" font-weight="700" fill="#61DAFB">React</text>

  <!-- JavaScript pill -->
  <rect x="140" y="10" width="140" height="42" rx="21" fill="#1a1600" stroke="#F7DF1E" stroke-width="1.3"/>
  <!-- JS square icon -->
  <rect x="155" y="18" width="22" height="22" rx="3" fill="#F7DF1E"/>
  <text x="166" y="33" text-anchor="middle" font-family="'Arial Black',sans-serif" font-size="9" font-weight="900" fill="#111">JS</text>
  <text x="224" y="36" text-anchor="middle" font-family="'Segoe UI',sans-serif" font-size="12" font-weight="700" fill="#f0d800">JavaScript</text>

  <!-- HTML5 pill -->
  <rect x="288" y="10" width="120" height="42" rx="21" fill="#1a0500" stroke="#E34F26" stroke-width="1.3"/>
  <!-- HTML5 shield icon -->
  <g transform="translate(303,17)">
    <polygon points="5,0 13,0 11,18 9,19 7,18" fill="none" stroke="#E34F26" stroke-width="1.3" stroke-linejoin="round"/>
    <line x1="5" y1="7" x2="13" y2="7" stroke="#E34F26" stroke-width="1"/>
    <line x1="6" y1="12" x2="12" y2="12" stroke="#E34F26" stroke-width="1"/>
  </g>
  <text x="360" y="36" text-anchor="middle" font-family="'Segoe UI',sans-serif" font-size="12" font-weight="700" fill="#e8622a">HTML5</text>

  <!-- CSS3 pill -->
  <rect x="416" y="10" width="120" height="42" rx="21" fill="#000d1a" stroke="#1572B6" stroke-width="1.3"/>
  <g transform="translate(431,17)">
    <polygon points="5,0 13,0 11,18 9,19 7,18" fill="none" stroke="#1572B6" stroke-width="1.3" stroke-linejoin="round"/>
    <line x1="5" y1="7" x2="13" y2="7" stroke="#1572B6" stroke-width="1"/>
    <line x1="6" y1="12" x2="12" y2="12" stroke="#1572B6" stroke-width="1"/>
  </g>
  <text x="488" y="36" text-anchor="middle" font-family="'Segoe UI',sans-serif" font-size="12" font-weight="700" fill="#2a8fdb">CSS3</text>

  <!-- Tailwind pill -->
  <rect x="544" y="10" width="140" height="42" rx="21" fill="#001a1a" stroke="#06B6D4" stroke-width="1.3"/>
  <!-- Tailwind wave icon -->
  <g transform="translate(559,23)" fill="none" stroke="#06B6D4" stroke-width="1.6" stroke-linecap="round">
    <path d="M0 8 C2 4 4 4 6 8 C8 12 10 12 12 8"/>
    <path d="M0 14 C2 10 4 10 6 14 C8 18 10 18 12 14" opacity="0.6"/>
  </g>
  <text x="630" y="36" text-anchor="middle" font-family="'Segoe UI',sans-serif" font-size="12" font-weight="700" fill="#0dd4ef">Tailwind</text>

  <!-- Figma pill -->
  <rect x="692" y="10" width="120" height="42" rx="21" fill="#12000a" stroke="#F24E1E" stroke-width="1.3"/>
  <!-- Figma icon (3 circles) -->
  <g transform="translate(709,17)">
    <circle cx="5"  cy="5"  r="4.5" fill="none" stroke="#F24E1E"  stroke-width="1.2"/>
    <circle cx="5"  cy="14" r="4.5" fill="none" stroke="#A259FF"  stroke-width="1.2"/>
    <circle cx="14" cy="9"  r="4.5" fill="none" stroke="#1ABCFE"  stroke-width="1.2"/>
  </g>
  <text x="764" y="36" text-anchor="middle" font-family="'Segoe UI',sans-serif" font-size="12" font-weight="700" fill="#f06030">Figma</text>
</svg>

<!-- TOOLS ROW -->
<svg width="100%" viewBox="0 0 860 68" xmlns="http://www.w3.org/2000/svg">
  <!-- Git -->
  <rect x="4" y="10" width="110" height="42" rx="21" fill="#1a0500" stroke="#F05032" stroke-width="1.3"/>
  <g transform="translate(17,19)" fill="none" stroke="#F05032" stroke-width="1.4">
    <circle cx="4"  cy="4"  r="3.5"/><circle cx="14" cy="4"  r="3.5"/><circle cx="9"  cy="18" r="3.5"/>
    <path d="M14 7.5 C14 12 9 14.5 9 14.5"/><line x1="4" y1="7.5" x2="9" y2="14.5"/>
  </g>
  <text x="68" y="36" text-anchor="middle" font-family="'Segoe UI',sans-serif" font-size="12" font-weight="700" fill="#f05032">Git</text>

  <!-- GitHub -->
  <rect x="122" y="10" width="120" height="42" rx="21" fill="#0a0a14" stroke="#6e40c9" stroke-width="1.3"/>
  <g transform="translate(135,13) scale(0.75)">
    <path fill="#9B59D6" d="M10 0C4.477 0 0 4.477 0 10c0 4.418 2.865 8.166 6.839 9.489.5.092.682-.217.682-.482 0-.237-.009-.868-.013-1.703-2.782.604-3.369-1.342-3.369-1.342-.454-1.155-1.11-1.463-1.11-1.463-.908-.62.069-.608.069-.608 1.003.07 1.531 1.03 1.531 1.03.892 1.529 2.341 1.087 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.11-4.555-4.943 0-1.091.39-1.984 1.029-2.683-.103-.253-.446-1.27.098-2.647 0 0 .84-.269 2.75 1.025A9.578 9.578 0 0110 4.836c.85.004 1.705.114 2.504.336 1.909-1.294 2.747-1.025 2.747-1.025.546 1.377.203 2.394.1 2.647.64.699 1.028 1.592 1.028 2.683 0 3.842-2.339 4.687-4.566 4.935.359.309.678.919.678 1.852 0 1.336-.012 2.415-.012 2.744 0 .267.18.579.688.481C17.138 18.163 20 14.418 20 10 20 4.477 15.523 0 10 0z"/>
  </g>
  <text x="196" y="36" text-anchor="middle" font-family="'Segoe UI',sans-serif" font-size="12" font-weight="700" fill="#9B59D6">GitHub</text>

  <!-- Docker -->
  <rect x="250" y="10" width="120" height="42" rx="21" fill="#002a3a" stroke="#2496ED" stroke-width="1.3"/>
  <!-- Docker whale simplified -->
  <g transform="translate(263,18)" fill="none" stroke="#2496ED" stroke-width="1.3">
    <rect x="0" y="8"  width="6" height="5" rx="1"/><rect x="7"  y="5" width="6" height="8" rx="1"/>
    <rect x="14" y="2" width="6" height="11" rx="1"/><rect x="0" y="14" width="20" height="3" rx="1.5"/>
  </g>
  <text x="322" y="36" text-anchor="middle" font-family="'Segoe UI',sans-serif" font-size="12" font-weight="700" fill="#2aa6f0">Docker</text>

  <!-- Linux -->
  <rect x="378" y="10" width="120" height="42" rx="21" fill="#1a1400" stroke="#FCC624" stroke-width="1.3"/>
  <!-- Linux penguin simplified -->
  <g transform="translate(393,16)">
    <ellipse cx="9" cy="7"  rx="7" ry="8" fill="none" stroke="#FCC624" stroke-width="1.3"/>
    <ellipse cx="9" cy="11" rx="4" ry="5" fill="#FCC624" opacity="0.3"/>
    <circle  cx="6.5" cy="6" r="1.2" fill="#FCC624"/>
    <circle  cx="11.5" cy="6" r="1.2" fill="#FCC624"/>
    <path d="M7 9 Q9 10.5 11 9" fill="none" stroke="#FCC624" stroke-width="1"/>
  </g>
  <text x="450" y="36" text-anchor="middle" font-family="'Segoe UI',sans-serif" font-size="12" font-weight="700" fill="#f0bb00">Linux</text>

  <!-- PostgreSQL -->
  <rect x="506" y="10" width="148" height="42" rx="21" fill="#000d1a" stroke="#336791" stroke-width="1.3"/>
  <g transform="translate(521,17)">
    <ellipse cx="9" cy="5"  rx="9" ry="5" fill="none" stroke="#336791" stroke-width="1.3"/>
    <ellipse cx="9" cy="14" rx="9" ry="5" fill="none" stroke="#336791" stroke-width="1.3"/>
    <line x1="0" y1="5" x2="0"  y2="14" stroke="#336791" stroke-width="1.3"/>
    <line x1="18" y1="5" x2="18" y2="14" stroke="#336791" stroke-width="1.3"/>
  </g>
  <text x="602" y="36" text-anchor="middle" font-family="'Segoe UI',sans-serif" font-size="12" font-weight="700" fill="#4488bb">PostgreSQL</text>

  <!-- Redis -->
  <rect x="662" y="10" width="110" height="42" rx="21" fill="#1a0000" stroke="#DC382D" stroke-width="1.3"/>
  <g transform="translate(675,21)">
    <ellipse cx="9" cy="4"  rx="8" ry="3.5" fill="none" stroke="#DC382D" stroke-width="1.2"/>
    <ellipse cx="9" cy="11" rx="8" ry="3.5" fill="none" stroke="#DC382D" stroke-width="1.2"/>
    <line x1="1" y1="4" x2="1" y2="11"  stroke="#DC382D" stroke-width="1.2"/>
    <line x1="17" y1="4" x2="17" y2="11" stroke="#DC382D" stroke-width="1.2"/>
  </g>
  <text x="734" y="36" text-anchor="middle" font-family="'Segoe UI',sans-serif" font-size="12" font-weight="700" fill="#e04040">Redis</text>

  <!-- VS Code -->
  <rect x="780" y="10" width="76" height="42" rx="21" fill="#001428" stroke="#007ACC" stroke-width="1.3"/>
  <g transform="translate(792,18)" fill="none" stroke="#007ACC" stroke-width="1.4" stroke-linecap="round" stroke-linejoin="round">
    <polyline points="10,0 0,7 10,14"/><line x1="5" y1="3.5" x2="12" y2="10.5"/>
    <line x1="5" y1="10.5" x2="12" y2="3.5"/>
  </g>
  <text x="830" y="36" text-anchor="middle" font-family="'Segoe UI',sans-serif" font-size="10" font-weight="700" fill="#009ee0">VSCode</text>
</svg>

</div>

---

<!-- ══════════════════════════════ SKILL BARS ═══════════════ -->
<div align="center">

### 📈 Skill Level

<svg width="100%" viewBox="0 0 860 280" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <linearGradient id="b1" x1="0%" y1="0%" x2="100%" y2="0%"><stop offset="0%" stop-color="#00D9FF"/><stop offset="100%" stop-color="#7B2FFF"/></linearGradient>
    <linearGradient id="b2" x1="0%" y1="0%" x2="100%" y2="0%"><stop offset="0%" stop-color="#339933"/><stop offset="100%" stop-color="#00D9FF"/></linearGradient>
    <linearGradient id="b3" x1="0%" y1="0%" x2="100%" y2="0%"><stop offset="0%" stop-color="#47A248"/><stop offset="100%" stop-color="#A8FF78"/></linearGradient>
    <linearGradient id="b4" x1="0%" y1="0%" x2="100%" y2="0%"><stop offset="0%" stop-color="#3178C6"/><stop offset="100%" stop-color="#00D9FF"/></linearGradient>
    <linearGradient id="b5" x1="0%" y1="0%" x2="100%" y2="0%"><stop offset="0%" stop-color="#2496ED"/><stop offset="100%" stop-color="#00D9FF"/></linearGradient>
    <linearGradient id="b6" x1="0%" y1="0%" x2="100%" y2="0%"><stop offset="0%" stop-color="#336791"/><stop offset="100%" stop-color="#61DAFB"/></linearGradient>
  </defs>
  <rect width="860" height="280" rx="12" fill="#070710" stroke="#00D9FF" stroke-width="0.5" stroke-opacity="0.12"/>

  <!-- Node.js -->
  <text x="24" y="44" font-family="'Segoe UI',sans-serif" font-size="12" fill="#ccd6f6">Node.js</text>
  <text x="836" y="44" text-anchor="end" font-family="monospace" font-size="12" fill="#00D9FF" font-weight="700">90%</text>
  <rect x="24" y="50" width="812" height="7" rx="3.5" fill="#0D1117"/>
  <rect x="24" y="50" width="1"   height="7" rx="3.5" fill="url(#b1)"><animate attributeName="width" from="0" to="731" dur="1.4s" fill="freeze" calcMode="spline" keySplines="0.34,1.56,0.64,1"/></rect>

  <!-- Express -->
  <text x="24" y="88" font-family="'Segoe UI',sans-serif" font-size="12" fill="#ccd6f6">Express.js</text>
  <text x="836" y="88" text-anchor="end" font-family="monospace" font-size="12" fill="#aaa" font-weight="700">85%</text>
  <rect x="24" y="94" width="812" height="7" rx="3.5" fill="#0D1117"/>
  <rect x="24" y="94" width="1"   height="7" rx="3.5" fill="url(#b2)"><animate attributeName="width" from="0" to="690" dur="1.6s" fill="freeze" calcMode="spline" keySplines="0.34,1.56,0.64,1"/></rect>

  <!-- MongoDB -->
  <text x="24" y="132" font-family="'Segoe UI',sans-serif" font-size="12" fill="#ccd6f6">MongoDB</text>
  <text x="836" y="132" text-anchor="end" font-family="monospace" font-size="12" fill="#A8FF78" font-weight="700">83%</text>
  <rect x="24" y="138" width="812" height="7" rx="3.5" fill="#0D1117"/>
  <rect x="24" y="138" width="1"   height="7" rx="3.5" fill="url(#b3)"><animate attributeName="width" from="0" to="674" dur="1.8s" fill="freeze" calcMode="spline" keySplines="0.34,1.56,0.64,1"/></rect>

  <!-- TypeScript -->
  <text x="24" y="176" font-family="'Segoe UI',sans-serif" font-size="12" fill="#ccd6f6">TypeScript</text>
  <text x="836" y="176" text-anchor="end" font-family="monospace" font-size="12" fill="#5aaae8" font-weight="700">75%</text>
  <rect x="24" y="182" width="812" height="7" rx="3.5" fill="#0D1117"/>
  <rect x="24" y="182" width="1"   height="7" rx="3.5" fill="url(#b4)"><animate attributeName="width" from="0" to="609" dur="2s" fill="freeze" calcMode="spline" keySplines="0.34,1.56,0.64,1"/></rect>

  <!-- Docker -->
  <text x="24" y="220" font-family="'Segoe UI',sans-serif" font-size="12" fill="#ccd6f6">Docker</text>
  <text x="836" y="220" text-anchor="end" font-family="monospace" font-size="12" fill="#2aa6f0" font-weight="700">62%</text>
  <rect x="24" y="226" width="812" height="7" rx="3.5" fill="#0D1117"/>
  <rect x="24" y="226" width="1"   height="7" rx="3.5" fill="url(#b5)"><animate attributeName="width" from="0" to="503" dur="2.2s" fill="freeze" calcMode="spline" keySplines="0.34,1.56,0.64,1"/></rect>

  <!-- PostgreSQL -->
  <text x="24" y="264" font-family="'Segoe UI',sans-serif" font-size="12" fill="#ccd6f6">PostgreSQL</text>
  <text x="836" y="264" text-anchor="end" font-family="monospace" font-size="12" fill="#4488bb" font-weight="700">55%</text>
  <rect x="24" y="270" width="812" height="7" rx="3.5" fill="#0D1117"/>
  <rect x="24" y="270" width="1"   height="7" rx="3.5" fill="url(#b6)"><animate attributeName="width" from="0" to="447" dur="2.4s" fill="freeze" calcMode="spline" keySplines="0.34,1.56,0.64,1"/></rect>
</svg>

</div>

---

## 📊 GitHub Statistics

<div align="center">

<table><tr>
<td><img src="https://github-readme-stats.vercel.app/api?username=khamidoff633&show_icons=true&theme=tokyonight&include_all_commits=true&count_private=true&hide_border=true&bg_color=0d1117&title_color=00D9FF&icon_color=7B2FFF&text_color=CCD6F6&border_radius=12"/></td>
<td><img src="https://github-readme-stats.vercel.app/api/top-langs/?username=khamidoff633&layout=donut&langs_count=6&theme=tokyonight&hide_border=true&bg_color=0d1117&title_color=00D9FF&text_color=CCD6F6&border_radius=12"/></td>
</tr></table>

<img src="https://streak-stats.demolab.com?user=khamidoff633&theme=tokyonight-duo&hide_border=true&background=0d1117&fire=FF6B35&ring=7B2FFF&currStreakLabel=00D9FF&sideLabels=8892b0&dates=8892b0&currStreakNum=ffffff&sideNums=CCD6F6&border_radius=12"/>

</div>

---

## 🏆 GitHub Trophies

<div align="center">
<img src="https://github-profile-trophy.vercel.app/?username=khamidoff633&theme=matrix&no-frame=true&no-bg=true&margin-w=8&column=7"/>
</div>

---

## 📈 Activity Graph

<div align="center">

[![Activity Graph](https://github-readme-activity-graph.vercel.app/graph?username=khamidoff633&theme=tokyo-night&hide_border=true&bg_color=0d1117&color=00D9FF&line=7B2FFF&point=FF6B35&area=true)](https://github.com/khamidoff633)

</div>

---

## 🐍 Contribution Snake

<div align="center">
<picture>
  <source media="(prefers-color-scheme: dark)"  srcset="https://raw.githubusercontent.com/khamidoff633/khamidoff633/output/github-contribution-grid-snake-dark.svg"/>
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/khamidoff633/khamidoff633/output/github-contribution-grid-snake.svg"/>
  <img alt="snake" src="https://raw.githubusercontent.com/khamidoff633/khamidoff633/output/github-contribution-grid-snake-dark.svg" width="100%"/>
</picture>
</div>

---

<!-- ═══════════════════════════════ ANIMATED FOOTER ═════════ -->
<div align="center">

<svg width="100%" viewBox="0 0 860 130" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <linearGradient id="fGrad" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%"   stop-color="#7B2FFF" stop-opacity="0"/>
      <stop offset="25%"  stop-color="#7B2FFF"/>
      <stop offset="50%"  stop-color="#00D9FF"/>
      <stop offset="75%"  stop-color="#7B2FFF"/>
      <stop offset="100%" stop-color="#7B2FFF" stop-opacity="0"/>
    </linearGradient>
    <filter id="fGlow">
      <feGaussianBlur stdDeviation="2" result="b"/>
      <feMerge><feMergeNode in="b"/><feMergeNode in="SourceGraphic"/></feMerge>
    </filter>
  </defs>
  <rect width="860" height="130" fill="#04080e"/>
  <!-- Top border glow -->
  <rect x="0" y="0" width="860" height="2" fill="url(#fGrad)" filter="url(#fGlow)">
    <animate attributeName="opacity" values="0.4;1;0.4" dur="3s" repeatCount="indefinite"/>
  </rect>
  <!-- Quote -->
  <text x="430" y="52" text-anchor="middle" font-family="'Segoe UI','Arial',sans-serif" font-size="17" font-weight="700" fill="#ffffff" letter-spacing="1">
    17 years old.  Backend Developer.  No excuses. 🚀
  </text>
  <text x="430" y="74" text-anchor="middle" font-family="'Courier New',monospace" font-size="11" fill="#444" letter-spacing="3">
    BAHRIDDIN KHAMIDOV  ·  SAMARQAND, UZBEKISTAN  ·  2024
  </text>
  <!-- Star row -->
  <text x="430" y="100" text-anchor="middle" font-family="monospace" font-size="12" fill="#00D9FF" letter-spacing="6">
    ⭐  Star my repos if they help you!  ⭐
  </text>
  <!-- Corner particles -->
  <circle cx="80"  cy="65" r="1.5" fill="#00D9FF" opacity="0.4"><animate attributeName="opacity" values="0.4;0.9;0.4" dur="2.2s" repeatCount="indefinite"/></circle>
  <circle cx="780" cy="55" r="1.5" fill="#7B2FFF"  opacity="0.4"><animate attributeName="opacity" values="0.4;0.9;0.4" dur="2.8s" repeatCount="indefinite"/></circle>
  <circle cx="40"  cy="100" r="1"  fill="#A8FF78"  opacity="0.3"><animate attributeName="opacity" values="0.3;0.7;0.3" dur="1.9s" repeatCount="indefinite"/></circle>
  <circle cx="820" cy="95"  r="1"  fill="#A8FF78"  opacity="0.3"><animate attributeName="opacity" values="0.3;0.7;0.3" dur="2.5s" repeatCount="indefinite"/></circle>
</svg>

</div>
