<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 800 200">
  <!-- Background Grid -->
  <defs>
    <pattern id="grid" width="40" height="40" patternUnits="userSpaceOnUse">
      <path d="M 40 0 L 0 0 0 40" fill="none" stroke="#1a1a1a" stroke-width="0.5"/>
    </pattern>
    
    <!-- Glowing effect -->
    <filter id="glow">
      <feGaussianBlur stdDeviation="2" result="coloredBlur"/>
      <feMerge>
        <feMergeNode in="coloredBlur"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>
  </defs>
  
  <!-- Background with grid -->
  <rect width="800" height="200" fill="#000" />
  <rect width="800" height="200" fill="url(#grid)" opacity="0.3"/>
  
  <!-- Main Title -->
  <text x="400" y="80" fill="#FF0000" font-family="monospace" font-size="40" text-anchor="middle" filter="url(#glow)">
    IDENTITY ARCHITECT
    <animate attributeName="opacity" values="0.5;1;0.5" dur="4s" repeatCount="indefinite"/>
  </text>
  
  <!-- Decorative Circuit Lines -->
  <g stroke="#FF0000" stroke-width="2" fill="none">
    <path d="M 100,100 L 300,100" opacity="0.6">
      <animate attributeName="stroke-dasharray" values="0,1000;1000,0" dur="3s" repeatCount="indefinite"/>
    </path>
    <path d="M 500,100 L 700,100" opacity="0.6">
      <animate attributeName="stroke-dasharray" values="1000,0;0,1000" dur="3s" repeatCount="indefinite"/>
    </path>
  </g>
  
  <!-- Security Icons -->
  <g fill="#FF0000" opacity="0.8">
    <circle cx="50" cy="100" r="5">
      <animate attributeName="r" values="3;6;3" dur="2s" repeatCount="indefinite"/>
    </circle>
    <circle cx="750" cy="100" r="5">
      <animate attributeName="r" values="6;3;6" dur="2s" repeatCount="indefinite"/>
    </circle>
  </g>
  
  <!-- Subtitle -->
  <text x="400" y="120" fill="#8C8C8C" font-family="monospace" font-size="16" text-anchor="middle">
    ENTERPRISE SECURITY SOLUTIONS
  </text>
</svg>
