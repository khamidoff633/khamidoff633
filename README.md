<svg width="100%" viewBox="0 0 860 260" xmlns="[http://www.w3.org/2000/svg](http://www.w3.org/2000/svg)">
  <defs>
    <radialGradient id="bgRadial" cx="50%" cy="40%" r="70%">
      <stop offset="0%" stop-color="#0d1829"/>
      <stop offset="45%" stop-color="#080f1a"/>
      <stop offset="100%" stop-color="#04080e"/>
    </radialGradient>
    <linearGradient id="nameGrad3D" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#00cfff"/>
      <stop offset="30%" stop-color="#7ee8ff"/>
      <stop offset="50%" stop-color="#ffffff"/>
      <stop offset="70%" stop-color="#b89aff"/>
      <stop offset="100%" stop-color="#7B2FFF"/>
    </linearGradient>
    <linearGradient id="nameShadow" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#004466" stop-opacity="0.6"/>
      <stop offset="50%" stop-color="#222244" stop-opacity="0.4"/>
      <stop offset="100%" stop-color="#2a0055" stop-opacity="0.6"/>
    </linearGradient>
    <filter id="nameGlow" x="-20%" y="-60%" width="140%" height="220%">
      <feGaussianBlur in="SourceGraphic" stdDeviation="6" result="blur1"/>
      <feGaussianBlur in="SourceGraphic" stdDeviation="14" result="blur2"/>
      <feMerge>
        <feMergeNode in="blur2"/>
        <feMergeNode in="blur1"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>
    <pattern id="grid" x="0" y="0" width="50" height="50" patternUnits="userSpaceOnUse">
      <path d="M50 0L0 0L0 50" fill="none" stroke="#00D9FF" stroke-width="0.3" stroke-opacity="0.07"/>
    </pattern>
    <clipPath id="heroClip">
      <rect width="860" height="260" rx="14"/>
    </clipPath>
    <linearGradient id="sweep" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#00D9FF" stop-opacity="0"/>
      <stop offset="50%" stop-color="#00D9FF" stop-opacity="0.12"/>
      <stop offset="100%" stop-color="#00D9FF" stop-opacity="0"/>
    </linearGradient>
    <linearGradient id="lineGlow" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#00D9FF" stop-opacity="0"/>
      <stop offset="25%" stop-color="#00D9FF" stop-opacity="0.9"/>
      <stop offset="50%" stop-color="#ffffff" stop-opacity="1"/>
      <stop offset="75%" stop-color="#7B2FFF" stop-opacity="0.9"/>
      <stop offset="100%" stop-color="#7B2FFF" stop-opacity="0"/>
    </linearGradient>
    <filter id="lineFilter">
      <feGaussianBlur stdDeviation="1.5" result="b"/>
      <feMerge><feMergeNode in="b"/><feMergeNode in="SourceGraphic"/></feMerge>
    </filter>
  </defs>

  <g clip-path="url(#heroClip)">
    <rect width="860" height="260" fill="url(#bgRadial)"/>
    <rect width="860" height="260" fill="url(#grid)"/>

    <g stroke="#00D9FF" stroke-opacity="0.06" stroke-width="0.6">
      <line x1="430" y1="160" x2="0" y2="260"/><line x1="430" y1="160" x2="86" y2="260"/>
      <line x1="430" y1="160" x2="172" y2="260"/><line x1="430" y1="160" x2="258" y2="260"/>
      <line x1="430" y1="160" x2="344" y2="260"/><line x1="430" y1="160" x2="430" y2="260"/>
      <line x1="430" y1="160" x2="516" y2="260"/><line x1="430" y1="160" x2="602" y2="260"/>
      <line x1="430" y1="160" x2="688" y2="260"/><line x1="430" y1="160" x2="774" y2="260"/>
      <line x1="430" y1="160" x2="860" y2="260"/>
      <line x1="0" y1="185" x2="860" y2="185"/><line x1="0" y1="205" x2="860" y2="205"/>
      <line x1="0" y1="222" x2="860" y2="222"/><line x1="0" y1="237" x2="860" y2="237"/>
      <line x1="0" y1="250" x2="860" y2="250"/>
    </g>

    <ellipse cx="200" cy="80" rx="180" ry="80" fill="#00D9FF" opacity="0.03">
      <animate attributeName="opacity" values="0.03;0.07;0.03" dur="5s" repeatCount="indefinite"/>
    </ellipse>
    <ellipse cx="660" cy="90" rx="160" ry="70" fill="#7B2FFF" opacity="0.04">
      <animate attributeName="opacity" values="0.04;0.09;0.04" dur="4.2s" repeatCount="indefinite"/>
    </ellipse>

    <rect x="-180" y="0" width="180" height="260" fill="url(#sweep)">
      <animateTransform attributeName="transform" type="translate" from="-180 0" to="1040 0" dur="5s" repeatCount="indefinite" calcMode="spline" keySplines="0.4,0,0.6,1"/>
    </rect>

    <circle cx="60" cy="40" r="1.5" fill="#00D9FF" opacity="0.7"><animate attributeName="cy" values="40;30;40" dur="3.2s" repeatCount="indefinite"/><animate attributeName="opacity" values="0.7;0.2;0.7" dur="3.2s" repeatCount="indefinite"/></circle>
    <circle cx="160" cy="25" r="1" fill="#7B2FFF" opacity="0.6"><animate attributeName="cy" values="25;18;25" dur="2.7s" repeatCount="indefinite"/><animate attributeName="opacity" values="0.6;0.1;0.6" dur="2.7s" repeatCount="indefinite"/></circle>
    <circle cx="720" cy="35" r="1.5" fill="#00D9FF" opacity="0.7"><animate attributeName="cy" values="35;25;35" dur="3.6s" repeatCount="indefinite"/><animate attributeName="opacity" values="0.7;0.2;0.7" dur="3.6s" repeatCount="indefinite"/></circle>
    <circle cx="810" cy="55" r="1" fill="#A8FF78" opacity="0.5"><animate attributeName="cy" values="55;45;55" dur="2.4s" repeatCount="indefinite"/><animate attributeName="opacity" values="0.5;0.1;0.5" dur="2.4s" repeatCount="indefinite"/></circle>
    <circle cx="320" cy="18" r="1" fill="#7B2FFF" opacity="0.4"><animate attributeName="cy" values="18;10;18" dur="4.1s" repeatCount="indefinite"/><animate attributeName="opacity" values="0.4;0.1;0.4" dur="4.1s" repeatCount="indefinite"/></circle>
    <circle cx="540" cy="22" r="1.5" fill="#00D9FF" opacity="0.5"><animate attributeName="cy" values="22;32;22" dur="3.9s" repeatCount="indefinite"/><animate attributeName="opacity" values="0.5;0.1;0.5" dur="3.9s" repeatCount="indefinite"/></circle>
    <circle cx="50" cy="200" r="1" fill="#A8FF78" opacity="0.4"><animate attributeName="opacity" values="0.4;0.8;0.4" dur="2.1s" repeatCount="indefinite"/></circle>
    <circle cx="800" cy="210" r="1" fill="#A8FF78" opacity="0.4"><animate attributeName="opacity" values="0.4;0.8;0.4" dur="2.9s" repeatCount="indefinite"/></circle>

    <g fill="none" stroke="#00D9FF" stroke-width="1.8" stroke-opacity="0.25">
      <path d="M28 62 L16 62 L16 98 L28 98"/>
      <path d="M832 62 L844 62 L844 98 L832 98"/>
    </g>

    <text x="435" y="95" text-anchor="middle" font-family="'Segoe UI','Arial Black',sans-serif" font-size="56" font-weight="900" fill="url(#nameShadow)" letter-spacing="1.5" opacity="0.25">Bahriddin Khamidov</text>
    <text x="434" y="94" text-anchor="middle" font-family="'Segoe UI','Arial Black',sans-serif" font-size="56" font-weight="900" fill="url(#nameShadow)" letter-spacing="1.5" opacity="0.3">Bahriddin Khamidov</text>
    <text x="433" y="93" text-anchor="middle" font-family="'Segoe UI','Arial Black',sans-serif" font-size="56" font-weight="900" fill="url(#nameShadow)" letter-spacing="1.5" opacity="0.4">Bahriddin Khamidov</text>
    <text x="432" y="92" text-anchor="middle" font-family="'Segoe UI','Arial Black',sans-serif" font-size="56" font-weight="900" fill="url(#nameShadow)" letter-spacing="1.5" opacity="0.55">Bahriddin Khamidov</text>
    <text x="430" y="90" text-anchor="middle" font-family="'Segoe UI','Arial Black',sans-serif" font-size="56" font-weight="900" fill="url(#nameGrad3D)" letter-spacing="1.5" filter="url(#nameGlow)" opacity="0.55">Bahriddin Khamidov</text>
    <text x="430" y="90" text-anchor="middle" font-family="'Segoe UI','Arial Black',sans-serif" font-size="56" font-weight="900" fill="url(#nameGrad3D)" letter-spacing="1.5">
      Bahriddin Khamidov
      <animateTransform attributeName="transform" type="scale" additive="sum" values="1 1;1.008 1.004;1 1" dur="4s" repeatCount="indefinite" calcMode="spline" keySplines="0.45,0,0.55,1;0.45,0,0.55,1"/>
    </text>

    <rect x="160" y="100" width="540" height="2" fill="url(#lineGlow)" rx="1" filter="url(#lineFilter)">
      <animate attributeName="opacity" values="0.5;1;0.5" dur="2.5s" repeatCount="indefinite"/>
      <animate attributeName="width" values="400;540;400" dur="4s" repeatCount="indefinite" calcMode="spline" keySplines="0.4,0,0.6,1;0.4,0,0.6,1"/>
      <animateTransform attributeName="transform" type="translate" values="70 0;0 0;70 0" dur="4s" repeatCount="indefinite" calcMode="spline" keySplines="0.4,0,0.6,1;0.4,0,0.6,1"/>
    </rect>

    <text x="430" y="128" text-anchor="middle" font-family="'Courier New',monospace" font-size="12" fill="#8892B0" letter-spacing="4">BACKEND DEVELOPER · NODE.JS · MONGODB · TYPESCRIPT</text>

    <rect x="305" y="142" width="250" height="28" rx="14" fill="#06101e" stroke="#00D9FF" stroke-width="0.8" stroke-opacity="0.45"/>
    <circle cx="322" cy="156" r="4.5" fill="#22dd55">
      <animate attributeName="r" values="4;6.5;4" dur="1.8s" repeatCount="indefinite"/>
      <animate attributeName="opacity" values="1;0.5;1" dur="1.8s" repeatCount="indefinite"/>
    </circle>
    <text x="430" y="161" text-anchor="middle" font-family="'Courier New',monospace" font-size="11" fill="#00D9FF" letter-spacing="1">🇺🇿 Samarqand, Uzbekistan</text>
  </g>
</svg>
