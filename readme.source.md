```aura width=860 height=300
<div style={{ position: 'relative', display: 'flex', width: '100%', height: '100%', background: '#050b14', borderRadius: 20, overflow: 'hidden', fontFamily: 'Inter, sans-serif', border: '1px solid rgba(34,211,238,0.16)' }}>
  <style>{`
    @keyframes hero-drift-a { 0%, 100% { transform: translate(0, 0); opacity: 0.5; } 50% { transform: translate(24px, -16px); opacity: 0.78; } }
    @keyframes hero-drift-b { 0%, 100% { transform: translate(0, 0); opacity: 0.38; } 50% { transform: translate(-18px, 14px); opacity: 0.62; } }
    @keyframes hero-pulse { 0%, 100% { opacity: 0.22; } 50% { opacity: 0.72; } }
    @keyframes hero-flow { 0% { stroke-dashoffset: 28; opacity: 0.28; } 50% { opacity: 0.9; } 100% { stroke-dashoffset: 0; opacity: 0.28; } }
    @keyframes hero-node { 0%, 100% { transform: scale(1); opacity: 0.78; } 50% { transform: scale(1.14); opacity: 1; } }
    #hero-orb-a { animation: hero-drift-a 9s ease-in-out infinite; }
    #hero-orb-b { animation: hero-drift-b 12s ease-in-out infinite 0.8s; }
    #hero-orb-c { animation: hero-drift-a 11s ease-in-out infinite 1.6s; }
    #hero-ring-a { animation: hero-pulse 7s ease-in-out infinite; }
    #hero-ring-b { animation: hero-pulse 7s ease-in-out infinite 1.8s; }
    #hero-paths { animation: hero-flow 4s linear infinite; }
    #hero-core { animation: hero-node 5s ease-in-out infinite; transform-origin: 664px 150px; }
  `}</style>

  <svg width="860" height="300" style={{ position: 'absolute', top: 0, left: 0 }}>
    <defs>
      <radialGradient id="hero-cyan" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(34,211,238,0.34)" />
        <stop offset="100%" stopColor="rgba(34,211,238,0)" />
      </radialGradient>
      <radialGradient id="hero-blue" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(37,99,235,0.3)" />
        <stop offset="100%" stopColor="rgba(37,99,235,0)" />
      </radialGradient>
      <radialGradient id="hero-ice" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(125,211,252,0.18)" />
        <stop offset="100%" stopColor="rgba(125,211,252,0)" />
      </radialGradient>
    </defs>

    <ellipse id="hero-orb-a" cx="80" cy="270" rx="240" ry="160" fill="url(#hero-cyan)" />
    <ellipse id="hero-orb-b" cx="760" cy="30" rx="230" ry="170" fill="url(#hero-blue)" />
    <ellipse id="hero-orb-c" cx="580" cy="310" rx="220" ry="140" fill="url(#hero-ice)" />

    <circle id="hero-ring-a" cx="664" cy="150" r="86" fill="none" stroke="rgba(34,211,238,0.2)" strokeWidth="0.8" />
    <circle id="hero-ring-b" cx="664" cy="150" r="126" fill="none" stroke="rgba(125,211,252,0.12)" strokeWidth="0.8" />

    <g id="hero-paths" fill="none" stroke="rgba(34,211,238,0.68)" strokeWidth="1.2" strokeDasharray="6 8">
      <path d="M 664 150 C 620 104, 590 88, 548 72" />
      <path d="M 664 150 C 720 98, 750 90, 796 72" />
      <path d="M 664 150 C 610 194, 574 212, 536 232" />
      <path d="M 664 150 C 716 196, 754 214, 800 232" />
    </g>

    <g fill="#071521" stroke="rgba(34,211,238,0.72)" strokeWidth="1.2">
      <rect x="516" y="51" width="64" height="42" rx="12" />
      <rect x="764" y="51" width="64" height="42" rx="12" />
      <rect x="504" y="211" width="64" height="42" rx="12" />
      <rect x="768" y="211" width="64" height="42" rx="12" />
    </g>
    <g fill="none" stroke="rgba(213,250,255,0.82)" strokeWidth="1.3" strokeLinecap="round" strokeLinejoin="round">
      <path d="M 540 65 H 535 V 80 H 540 M 556 65 H 561 V 80 H 556 M 546 70 L 550 74 L 546 78" />
      <path d="M 786 79 H 807 C 815 79 816 68 808 67 C 807 60 797 58 793 65 C 785 63 780 72 786 79 Z" />
      <ellipse cx="536" cy="225" rx="12" ry="4" />
      <path d="M 524 225 V 240 C 524 245 548 245 548 240 V 225 M 524 233 C 524 238 548 238 548 233" />
      <path d="M 788 222 H 812 M 788 232 H 812 M 788 242 H 805" />
    </g>

    <g id="hero-core">
      <rect x="624" y="110" width="80" height="80" rx="20" fill="#071824" stroke="#22d3ee" strokeWidth="1.5" />
      <circle cx="648" cy="139" r="4" fill="#67e8f9" />
      <circle cx="680" cy="132" r="4" fill="#22d3ee" />
      <circle cx="688" cy="164" r="4" fill="#67e8f9" />
      <circle cx="652" cy="170" r="4" fill="#22d3ee" />
      <path d="M 648 139 L 680 132 L 688 164 L 652 170 Z M 648 139 L 688 164 M 680 132 L 652 170" fill="none" stroke="rgba(165,243,252,0.72)" strokeWidth="1.1" />
    </g>
  </svg>

  <div style={{ position: 'relative', display: 'flex', flexDirection: 'column', justifyContent: 'center', width: 490, height: '100%', paddingLeft: 48, zIndex: 10 }}>
    <span style={{ fontSize: 11, color: '#67e8f9', letterSpacing: 4, textTransform: 'uppercase', marginBottom: 14 }}>Hello, I am</span>
    <span style={{ fontSize: 47, fontWeight: 750, color: '#f8fafc', letterSpacing: -1.8, lineHeight: 1 }}>Ammari Majd</span>
    <span style={{ fontSize: 21, fontWeight: 600, color: '#22d3ee', marginTop: 11 }}>AI Software Engineer</span>
    <span style={{ fontSize: 13, color: 'rgba(203,231,239,0.64)', marginTop: 9, letterSpacing: 0.4 }}>Backend Systems · Machine Learning · Production AI</span>
    <div style={{ display: 'flex', gap: 8, marginTop: 24 }}>
      {['Python', 'FastAPI', 'PyTorch', 'LLMs', 'RAG'].map((tag, i) => (
        <span key={i} style={{ padding: '5px 11px', background: 'rgba(34,211,238,0.06)', color: 'rgba(207,250,254,0.78)', borderRadius: 100, fontSize: 10, border: '1px solid rgba(34,211,238,0.17)', letterSpacing: 0.4 }}>{tag}</span>
      ))}
    </div>
  </div>
</div>
```

```aura width=860 height=150
<div style={{ position: 'relative', display: 'flex', alignItems: 'center', width: '100%', height: '100%', background: '#050b14', borderRadius: 18, overflow: 'hidden', fontFamily: 'Inter, sans-serif', border: '1px solid rgba(34,211,238,0.12)', padding: '0 42px' }}>
  <style>{`
    @keyframes intro-drift { 0%, 100% { transform: translate(0,0); opacity: 0.36; } 50% { transform: translate(28px,-12px); opacity: 0.62; } }
    @keyframes intro-cursor { 0%, 48% { opacity: 1; } 49%, 100% { opacity: 0; } }
    #intro-orb { animation: intro-drift 10s ease-in-out infinite; }
    #intro-cursor { animation: intro-cursor 1.1s step-end infinite; }
  `}</style>
  <svg width="860" height="150" style={{ position: 'absolute', top: 0, left: 0 }}>
    <defs>
      <radialGradient id="intro-glow" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(34,211,238,0.26)" />
        <stop offset="100%" stopColor="rgba(34,211,238,0)" />
      </radialGradient>
    </defs>
    <ellipse id="intro-orb" cx="70" cy="130" rx="220" ry="120" fill="url(#intro-glow)" />
  </svg>
  <div style={{ position: 'relative', display: 'flex', flexDirection: 'column', zIndex: 10 }}>
    <span style={{ fontSize: 10, color: '#22d3ee', letterSpacing: 3, textTransform: 'uppercase', marginBottom: 13 }}>What I build</span>
    <span style={{ fontSize: 19, fontWeight: 520, color: '#f1f5f9', lineHeight: 1.45 }}>I build reliable backend systems and production-ready AI products—from data pipelines and ML services to full-stack platforms.</span>
    <div style={{ display: 'flex', marginTop: 13, alignItems: 'center' }}>
      <span style={{ fontSize: 12, color: 'rgba(165,243,252,0.55)', fontFamily: 'monospace' }}>{'> open to meaningful work'}</span>
      <span id="intro-cursor" style={{ fontSize: 12, color: '#67e8f9', fontFamily: 'monospace', marginLeft: 2 }}>_</span>
    </div>
  </div>
</div>
```

```aura width=860 height=72
<div style={{ display: 'flex', alignItems: 'center', width: '100%', height: '100%', fontFamily: 'Inter, sans-serif' }}>
  <span style={{ fontSize: 11, color: '#22d3ee', letterSpacing: 4, textTransform: 'uppercase', marginRight: 16 }}>Selected work</span>
  <div style={{ display: 'flex', height: 1, flex: 1, background: 'linear-gradient(90deg, rgba(34,211,238,0.4), rgba(34,211,238,0))' }} />
</div>
```

```aura width=860 height=190 link="https://altus-website-sandy.vercel.app"
<div style={{ position: 'relative', display: 'flex', width: '100%', height: '100%', background: '#050b14', borderRadius: 18, overflow: 'hidden', fontFamily: 'Inter, sans-serif', border: '1px solid rgba(34,211,238,0.13)', padding: 30 }}>
  <style>{`
    @keyframes altus-drift { 0%, 100% { transform: translate(0,0); opacity: 0.34; } 50% { transform: translate(-24px,12px); opacity: 0.58; } }
    @keyframes altus-scan { 0% { transform: translateX(-180px); opacity: 0; } 35%, 65% { opacity: 0.55; } 100% { transform: translateX(180px); opacity: 0; } }
    #altus-orb { animation: altus-drift 11s ease-in-out infinite; }
    #altus-scan { animation: altus-scan 5s ease-in-out infinite; }
  `}</style>
  <svg width="860" height="190" style={{ position: 'absolute', top: 0, left: 0 }}>
    <defs>
      <radialGradient id="altus-glow" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(34,211,238,0.3)" />
        <stop offset="100%" stopColor="rgba(34,211,238,0)" />
      </radialGradient>
    </defs>
    <ellipse id="altus-orb" cx="790" cy="30" rx="230" ry="150" fill="url(#altus-glow)" />
    <g transform="translate(684, 42)">
      <rect x="0" y="0" width="112" height="106" rx="14" fill="rgba(7,24,36,0.8)" stroke="rgba(34,211,238,0.3)" />
      <path d="M 22 28 H 88 M 22 48 H 78 M 22 68 H 92 M 22 88 H 64" stroke="rgba(165,243,252,0.45)" strokeWidth="2" />
      <rect id="altus-scan" x="49" y="10" width="3" height="86" rx="2" fill="#22d3ee" />
    </g>
  </svg>
  <div style={{ position: 'relative', display: 'flex', flexDirection: 'column', justifyContent: 'center', width: 610, zIndex: 10 }}>
    <div style={{ display: 'flex', alignItems: 'center', gap: 9, marginBottom: 12 }}>
      <span style={{ padding: '4px 10px', background: 'rgba(34,211,238,0.08)', color: '#67e8f9', borderRadius: 100, fontSize: 9, border: '1px solid rgba(34,211,238,0.18)', letterSpacing: 1 }}>LIVE PRODUCT</span>
      <span style={{ fontSize: 10, color: 'rgba(203,213,225,0.4)', letterSpacing: 1 }}>PRIVATE SOURCE</span>
    </div>
    <span style={{ fontSize: 25, fontWeight: 700, color: '#f8fafc' }}>ALTUS AutoGrader</span>
    <span style={{ fontSize: 13, color: 'rgba(203,231,239,0.6)', lineHeight: 1.5, marginTop: 9 }}>AI-assisted exam correction with OCR-backed structure, evidence-linked grading proposals, teacher review, and versioned workflows.</span>
    <span style={{ fontSize: 11, color: '#22d3ee', marginTop: 15 }}>Python · FastAPI · OpenAI API · OCR · Next.js · Docker</span>
  </div>
</div>
```

```aura width=860 height=190 link="https://github.com/AmeriMajd/3DP_AI_Driven_Platform"
<div style={{ position: 'relative', display: 'flex', width: '100%', height: '100%', background: '#050b14', borderRadius: 18, overflow: 'hidden', fontFamily: 'Inter, sans-serif', border: '1px solid rgba(34,211,238,0.13)', padding: 30 }}>
  <style>{`
    @keyframes dp-drift { 0%, 100% { transform: translate(0,0); opacity: 0.32; } 50% { transform: translate(18px,-14px); opacity: 0.56; } }
    @keyframes dp-layer { 0%, 100% { opacity: 0.35; } 50% { opacity: 0.9; } }
    #dp-orb { animation: dp-drift 10s ease-in-out infinite; }
    #dp-layer-a { animation: dp-layer 4s ease-in-out infinite; }
    #dp-layer-b { animation: dp-layer 4s ease-in-out infinite 1.3s; }
    #dp-layer-c { animation: dp-layer 4s ease-in-out infinite 2.6s; }
  `}</style>
  <svg width="860" height="190" style={{ position: 'absolute', top: 0, left: 0 }}>
    <defs>
      <radialGradient id="dp-glow" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(37,99,235,0.32)" />
        <stop offset="100%" stopColor="rgba(37,99,235,0)" />
      </radialGradient>
    </defs>
    <ellipse id="dp-orb" cx="780" cy="170" rx="220" ry="145" fill="url(#dp-glow)" />
    <g transform="translate(690, 44)" fill="none" stroke="#22d3ee" strokeWidth="1.2">
      <path id="dp-layer-a" d="M 0 20 L 58 0 L 116 20 L 58 42 Z" />
      <path id="dp-layer-b" d="M 0 48 L 58 28 L 116 48 L 58 70 Z" />
      <path id="dp-layer-c" d="M 0 76 L 58 56 L 116 76 L 58 98 Z" />
    </g>
  </svg>
  <div style={{ position: 'relative', display: 'flex', flexDirection: 'column', justifyContent: 'center', width: 610, zIndex: 10 }}>
    <span style={{ fontSize: 10, color: '#67e8f9', letterSpacing: 2, textTransform: 'uppercase', marginBottom: 12 }}>Machine Learning Platform</span>
    <span style={{ fontSize: 25, fontWeight: 700, color: '#f8fafc' }}>3DP AI-Driven Platform</span>
    <span style={{ fontSize: 13, color: 'rgba(203,231,239,0.6)', lineHeight: 1.5, marginTop: 9 }}>Recommendation workflow for 3D-printing technologies, materials, and process parameters, exposed through a real-time backend platform.</span>
    <span style={{ fontSize: 11, color: '#22d3ee', marginTop: 15 }}>FastAPI · PostgreSQL · Redis · WebSockets · Flutter · Docker</span>
  </div>
</div>
```

```aura width=860 height=190 link="https://github.com/AmeriMajd/large-scale-recommender"
<div style={{ position: 'relative', display: 'flex', width: '100%', height: '100%', background: '#050b14', borderRadius: 18, overflow: 'hidden', fontFamily: 'Inter, sans-serif', border: '1px solid rgba(34,211,238,0.13)', padding: 30 }}>
  <style>{`
    @keyframes rec-drift { 0%, 100% { transform: translate(0,0); opacity: 0.32; } 50% { transform: translate(-20px,-12px); opacity: 0.58; } }
    @keyframes rec-flow { 0% { stroke-dashoffset: 24; opacity: 0.25; } 50% { opacity: 0.88; } 100% { stroke-dashoffset: 0; opacity: 0.25; } }
    #rec-orb { animation: rec-drift 12s ease-in-out infinite; }
    #rec-flow { animation: rec-flow 4.5s linear infinite; }
  `}</style>
  <svg width="860" height="190" style={{ position: 'absolute', top: 0, left: 0 }}>
    <defs>
      <radialGradient id="rec-glow" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(34,211,238,0.28)" />
        <stop offset="100%" stopColor="rgba(34,211,238,0)" />
      </radialGradient>
    </defs>
    <ellipse id="rec-orb" cx="770" cy="20" rx="220" ry="150" fill="url(#rec-glow)" />
    <g transform="translate(680, 58)">
      <g fill="#071824" stroke="rgba(34,211,238,0.72)" strokeWidth="1.2">
        <rect x="0" y="16" width="58" height="42" rx="10" />
        <rect x="126" y="16" width="58" height="42" rx="10" />
      </g>
      <g fill="none" stroke="rgba(213,250,255,0.82)" strokeWidth="1.4" strokeLinecap="round" strokeLinejoin="round">
        <circle cx="25" cy="34" r="8" />
        <path d="M 31 40 L 39 48 M 145 47 V 39 H 151 V 47 M 155 47 V 32 H 161 V 47 M 165 47 V 24 H 171 V 47" />
      </g>
      <path id="rec-flow" d="M 60 37 C 82 16, 102 58, 124 37" fill="none" stroke="#22d3ee" strokeWidth="1.4" strokeDasharray="5 7" />
    </g>
  </svg>
  <div style={{ position: 'relative', display: 'flex', flexDirection: 'column', justifyContent: 'center', width: 610, zIndex: 10 }}>
    <span style={{ fontSize: 10, color: '#67e8f9', letterSpacing: 2, textTransform: 'uppercase', marginBottom: 12 }}>End-to-End ML System</span>
    <span style={{ fontSize: 25, fontWeight: 700, color: '#f8fafc' }}>Large-Scale Recommendation Engine</span>
    <span style={{ fontSize: 13, color: 'rgba(203,231,239,0.6)', lineHeight: 1.5, marginTop: 9 }}>Two-stage movie recommendations with learned retrieval, deep ranking, approximate search, serving, caching, and orchestration.</span>
    <span style={{ fontSize: 11, color: '#22d3ee', marginTop: 15 }}>TensorFlow Recommenders · FAISS · Spark · Redis · Airflow · Triton</span>
  </div>
</div>
```

```aura width=860 height=72
<div style={{ display: 'flex', alignItems: 'center', width: '100%', height: '100%', fontFamily: 'Inter, sans-serif' }}>
  <span style={{ fontSize: 11, color: '#22d3ee', letterSpacing: 4, textTransform: 'uppercase', marginRight: 16 }}>Experience & education</span>
  <div style={{ display: 'flex', height: 1, flex: 1, background: 'linear-gradient(90deg, rgba(34,211,238,0.4), rgba(34,211,238,0))' }} />
</div>
```

```aura width=860 height=330
<div style={{ position: 'relative', display: 'flex', width: '100%', height: '100%', gap: 16, fontFamily: 'Inter, sans-serif' }}>
  <style>{`
    @keyframes timeline-drift { 0%, 100% { transform: translate(0,0); opacity: 0.3; } 50% { transform: translate(18px,-14px); opacity: 0.52; } }
    @keyframes timeline-pulse { 0%, 100% { opacity: 0.48; } 50% { opacity: 1; } }
    #timeline-orb { animation: timeline-drift 11s ease-in-out infinite; }
    #timeline-dot-a { animation: timeline-pulse 4s ease-in-out infinite; }
    #timeline-dot-b { animation: timeline-pulse 4s ease-in-out infinite 1.2s; }
    #timeline-dot-c { animation: timeline-pulse 4s ease-in-out infinite 2.4s; }
  `}</style>
  <div style={{ position: 'relative', display: 'flex', flexDirection: 'column', flex: 1, height: '100%', background: '#050b14', borderRadius: 18, overflow: 'hidden', border: '1px solid rgba(34,211,238,0.12)', padding: 30 }}>
    <svg width="530" height="330" style={{ position: 'absolute', top: 0, left: 0 }}>
      <defs>
        <radialGradient id="timeline-glow" cx="50%" cy="50%" r="50%">
          <stop offset="0%" stopColor="rgba(34,211,238,0.24)" />
          <stop offset="100%" stopColor="rgba(34,211,238,0)" />
        </radialGradient>
      </defs>
      <ellipse id="timeline-orb" cx="20" cy="300" rx="190" ry="130" fill="url(#timeline-glow)" />
      <path d="M 37 92 L 37 259" stroke="rgba(34,211,238,0.24)" strokeWidth="1" />
      <circle id="timeline-dot-a" cx="37" cy="104" r="4" fill="#22d3ee" />
      <circle id="timeline-dot-b" cx="37" cy="174" r="4" fill="#22d3ee" />
      <circle id="timeline-dot-c" cx="37" cy="244" r="4" fill="#22d3ee" />
    </svg>
    <span style={{ position: 'relative', fontSize: 10, color: '#22d3ee', letterSpacing: 3, textTransform: 'uppercase', marginBottom: 22, zIndex: 10 }}>Experience</span>
    <div style={{ position: 'relative', display: 'flex', flexDirection: 'column', gap: 20, marginLeft: 28, zIndex: 10 }}>
      <div style={{ display: 'flex', flexDirection: 'column' }}>
        <span style={{ fontSize: 15, color: '#f8fafc', fontWeight: 650 }}>Software Engineering Intern</span>
        <span style={{ fontSize: 11, color: 'rgba(165,243,252,0.58)', marginTop: 4 }}>SPIRAW / ACTIA · 2026</span>
      </div>
      <div style={{ display: 'flex', flexDirection: 'column' }}>
        <span style={{ fontSize: 15, color: '#f8fafc', fontWeight: 650 }}>AI/ML Engineering Intern</span>
        <span style={{ fontSize: 11, color: 'rgba(165,243,252,0.58)', marginTop: 4 }}>ACTIA Engineering Services · 2025</span>
      </div>
      <div style={{ display: 'flex', flexDirection: 'column' }}>
        <span style={{ fontSize: 15, color: '#f8fafc', fontWeight: 650 }}>Machine Learning Engineer</span>
        <span style={{ fontSize: 11, color: 'rgba(165,243,252,0.58)', marginTop: 4 }}>HoutaLik · 2024–2025</span>
      </div>
    </div>
  </div>

  <div style={{ display: 'flex', flexDirection: 'column', width: 314, gap: 16 }}>
    <div style={{ display: 'flex', flexDirection: 'column', flex: 1, background: '#050b14', borderRadius: 18, border: '1px solid rgba(34,211,238,0.12)', padding: 24 }}>
      <span style={{ fontSize: 10, color: '#22d3ee', letterSpacing: 3, textTransform: 'uppercase', marginBottom: 14 }}>Engineering Degree</span>
      <span style={{ fontSize: 15, color: '#f8fafc', fontWeight: 650, lineHeight: 1.35 }}>Computer Science Engineering</span>
      <span style={{ fontSize: 11, color: 'rgba(203,231,239,0.55)', marginTop: 7, lineHeight: 1.4 }}>ISI · University of Tunis El Manar</span>
      <span style={{ fontSize: 10, color: 'rgba(103,232,249,0.55)', marginTop: 8 }}>2026–2029</span>
    </div>
    <div style={{ display: 'flex', flexDirection: 'column', flex: 1, background: '#050b14', borderRadius: 18, border: '1px solid rgba(34,211,238,0.12)', padding: 24 }}>
      <span style={{ fontSize: 10, color: '#22d3ee', letterSpacing: 3, textTransform: 'uppercase', marginBottom: 14 }}>Bachelor's Degree</span>
      <span style={{ fontSize: 15, color: '#f8fafc', fontWeight: 650, lineHeight: 1.35 }}>Software Engineering & Information Systems</span>
      <span style={{ fontSize: 11, color: 'rgba(203,231,239,0.55)', marginTop: 7 }}>ISIMM</span>
      <span style={{ fontSize: 10, color: 'rgba(103,232,249,0.55)', marginTop: 8 }}>2023–2026</span>
    </div>
  </div>
</div>
```

```aura width=860 height=72
<div style={{ display: 'flex', alignItems: 'center', width: '100%', height: '100%', fontFamily: 'Inter, sans-serif' }}>
  <span style={{ fontSize: 11, color: '#22d3ee', letterSpacing: 4, textTransform: 'uppercase', marginRight: 16 }}>Technical stack</span>
  <div style={{ display: 'flex', height: 1, flex: 1, background: 'linear-gradient(90deg, rgba(34,211,238,0.4), rgba(34,211,238,0))' }} />
</div>
```

```aura width=860 height=360
<div style={{ position: 'relative', display: 'flex', flexDirection: 'column', width: '100%', height: '100%', background: '#050b14', borderRadius: 18, overflow: 'hidden', fontFamily: 'Inter, sans-serif', border: '1px solid rgba(34,211,238,0.12)', padding: '28px 34px', gap: 17 }}>
  <style>{`
    @keyframes stack-drift-a { 0%, 100% { transform: translate(0,0); opacity: 0.28; } 50% { transform: translate(24px,-12px); opacity: 0.5; } }
    @keyframes stack-drift-b { 0%, 100% { transform: translate(0,0); opacity: 0.22; } 50% { transform: translate(-20px,14px); opacity: 0.44; } }
    #stack-orb-a { animation: stack-drift-a 12s ease-in-out infinite; }
    #stack-orb-b { animation: stack-drift-b 14s ease-in-out infinite 1s; }
  `}</style>
  <svg width="860" height="360" style={{ position: 'absolute', top: 0, left: 0 }}>
    <defs>
      <radialGradient id="stack-cyan" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(34,211,238,0.22)" />
        <stop offset="100%" stopColor="rgba(34,211,238,0)" />
      </radialGradient>
      <radialGradient id="stack-blue" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(37,99,235,0.2)" />
        <stop offset="100%" stopColor="rgba(37,99,235,0)" />
      </radialGradient>
    </defs>
    <ellipse id="stack-orb-a" cx="60" cy="330" rx="220" ry="150" fill="url(#stack-cyan)" />
    <ellipse id="stack-orb-b" cx="820" cy="20" rx="220" ry="150" fill="url(#stack-blue)" />
  </svg>

  {[
    ['Languages', ['Python', 'TypeScript', 'SQL', 'T-SQL', 'C++', 'Java']],
    ['Backend & Data', ['FastAPI', 'PostgreSQL', 'Redis', 'REST APIs', 'WebSockets']],
    ['AI & Machine Learning', ['PyTorch', 'TensorFlow', 'scikit-learn', 'LLMs', 'RAG', 'OpenAI API', 'OCR']],
    ['Engineering', ['Docker', 'GitHub Actions', 'CI/CD', 'pytest', 'AWS', 'Linux']],
    ['Frontend', ['React', 'Next.js', 'Flutter']],
  ].map((group, groupIndex) => (
    <div key={groupIndex} style={{ position: 'relative', display: 'flex', alignItems: 'center', zIndex: 10 }}>
      <span style={{ width: 150, flexShrink: 0, fontSize: 10, color: '#22d3ee', letterSpacing: 1.5, textTransform: 'uppercase' }}>{group[0]}</span>
      <div style={{ display: 'flex', flexWrap: 'wrap', gap: 8 }}>
        {group[1].map((tech, techIndex) => (
          <span key={techIndex} style={{ padding: '6px 12px', background: 'rgba(34,211,238,0.05)', color: 'rgba(226,248,252,0.72)', borderRadius: 100, fontSize: 10, border: '1px solid rgba(34,211,238,0.13)' }}>{tech}</span>
        ))}
      </div>
    </div>
  ))}
</div>
```

```aura width=860 height=122
<div style={{ position: 'relative', display: 'flex', alignItems: 'center', width: '100%', height: '100%', background: '#050b14', borderRadius: 18, overflow: 'hidden', fontFamily: 'Inter, sans-serif', border: '1px solid rgba(34,211,238,0.12)', padding: '0 34px' }}>
  <span style={{ width: 150, flexShrink: 0, fontSize: 10, color: '#22d3ee', letterSpacing: 3, textTransform: 'uppercase' }}>Languages</span>
  <div style={{ display: 'flex', flex: 1, justifyContent: 'space-between', gap: 10 }}>
    {[
      ['Arabic', 'Native'],
      ['English', 'Fluent'],
      ['French', 'Professional'],
      ['German', 'Basic'],
    ].map((language, i) => (
      <div key={i} style={{ display: 'flex', flexDirection: 'column', width: 150, padding: '15px 16px', background: 'rgba(34,211,238,0.04)', borderRadius: 13, border: '1px solid rgba(34,211,238,0.11)' }}>
        <span style={{ fontSize: 13, color: '#f1f5f9', fontWeight: 600 }}>{language[0]}</span>
        <span style={{ fontSize: 10, color: 'rgba(165,243,252,0.52)', marginTop: 5 }}>{language[1]}</span>
      </div>
    ))}
  </div>
</div>
```

```aura width=860 height=150
<div style={{ position: 'relative', display: 'flex', flexDirection: 'column', alignItems: 'center', justifyContent: 'center', width: '100%', height: '100%', background: '#050b14', borderRadius: 18, overflow: 'hidden', fontFamily: 'Inter, sans-serif', border: '1px solid rgba(34,211,238,0.12)' }}>
  <style>{`
    @keyframes available-pulse { 0%, 100% { opacity: 0.38; transform: scale(1); } 50% { opacity: 0.85; transform: scale(1.18); } }
    #available-dot { animation: available-pulse 3s ease-in-out infinite; transform-origin: 430px 28px; }
  `}</style>
  <svg width="860" height="150" style={{ position: 'absolute', top: 0, left: 0 }}>
    <circle id="available-dot" cx="430" cy="28" r="3" fill="#22d3ee" />
  </svg>
  <span style={{ fontSize: 10, color: '#22d3ee', letterSpacing: 4, textTransform: 'uppercase', marginBottom: 13 }}>Let's build something useful</span>
  <span style={{ fontSize: 15, color: 'rgba(241,245,249,0.82)', textAlign: 'center' }}>Open to internships, freelance projects, technical collaborations, and future full-time opportunities.</span>
  <span style={{ fontSize: 11, color: 'rgba(165,243,252,0.48)', marginTop: 13 }}>Ariana, Tunisia</span>
</div>
```

```aura width=145 height=44 link="https://www.linkedin.com/in/ammari-majd-8a1461373/" inline align=center
<SocialMediaButton
  icon="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABgAAAAYCAMAAADXqc3KAAAAIGNIUk0AAHomAACAhAAA+gAAAIDoAAB1MAAA6mAAADqYAAAXcJy6UTwAAAA2UExURQAAACLT7iLT7iLT7iLT7iLT7iLT7iLT7iLT7iLT7iLT7iLT7iLT7iLT7iLT7iLT7iLT7v///9/Gd6EAAAARdFJOUwBHowsZQ8uI09E+jVO0Mx/HNTPLxgAAAAFiS0dEEeK1PboAAAAHdElNRQfqCxAQLikJUcb6AAAAJXRFWHRkYXRlOmNyZWF0ZQAyMDI2LTExLTE2VDE2OjQ2OjQxKzAwOjAwus8d6wAAACV0RVh0ZGF0ZTptb2RpZnkAMjAyNi0xMS0xNlQxNjo0Njo0MSswMDowMMuSpVcAAAAodEVYdGRhdGU6dGltZXN0YW1wADIwMjYtMTEtMTZUMTY6NDY6NDErMDA6MDCch4SIAAAAMElEQVQoz2NgGF6AkQmHBDMLDglWJgY2dg5OLqwS3Aw8vFgl+Bj4BbBK8FNHYqgDAG/YAVb1pcHtAAAAAElFTkSuQmCC"
  text="LinkedIn"
  backgroundColor="#071521"
  textColor="#F8FAFC"
  borderColor="#164E63"
  width={145}
  height={44}
  gradientStops={[
    { offset: '0%', color: '#071521' },
    { offset: '25%', color: '#22D3EE' },
    { offset: '55%', color: '#0E7490' },
    { offset: '80%', color: '#67E8F9' },
    { offset: '100%', color: '#071521' },
  ]}
/>
```

```aura width=125 height=44 link="mailto:amerimajd0@gmail.com" inline align=center
<SocialMediaButton
  icon="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABgAAAAYCAMAAADXqc3KAAAAIGNIUk0AAHomAACAhAAA+gAAAIDoAAB1MAAA6mAAADqYAAAXcJy6UTwAAAA/UExURQAAACLT7iLT7iLT7iLT7iLT7iLT7iLT7iLT7iLT7iLT7iLT7iLT7iLT7iLT7iLT7iLT7iLT7iLT7iLT7v///7w6ajoAAAATdFJOUwAAPWysR6otdFuxmAZC5R14A+4gx9TFAAAAAWJLR0QUkt/JNQAAAAd0SU1FB+oLEBAwDw8dfNgAAAAldEVYdGRhdGU6Y3JlYXRlADIwMjYtMTEtMTZUMTY6NDg6MTUrMDA6MDAYqQcvAAAAJXRFWHRkYXRlOm1vZGlmeQAyMDI2LTExLTE2VDE2OjQ4OjE1KzAwOjAwafS/kwAAACh0RVh0ZGF0ZTp0aW1lc3RhbXAAMjAyNi0xMS0xNlQxNjo0ODoxNSswMDowMD7hnkwAAACCSURBVCjPvZFbDsMgDAQdnJB3SDv3v2sFRhHQ10/V/QF2sFkZkf+oc1rLdeb3tOoTGaCpgCECD2PVegQf1wmYC38GprhRFli3bG8rLKgB3eEIyQ8H7HoBO4uI3ShA6nDeTutZgvTmPaeoQUyZczdAgrcAT+DSN+BezMp9nO7b//iVHrrBCgs1aSFYAAAAAElFTkSuQmCC"
  text="Email"
  backgroundColor="#071521"
  textColor="#F8FAFC"
  borderColor="#164E63"
  width={125}
  height={44}
  gradientStops={[
    { offset: '0%', color: '#071521' },
    { offset: '25%', color: '#22D3EE' },
    { offset: '55%', color: '#0E7490' },
    { offset: '80%', color: '#67E8F9' },
    { offset: '100%', color: '#071521' },
  ]}
/>
```

```aura width=125 height=44 link="./assets/Ammari_Majd_Software_Engineer.pdf" inline align=center
<SocialMediaButton
  icon="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABgAAAAYBAMAAAASWSDLAAAAIGNIUk0AAHomAACAhAAA+gAAAIDoAAB1MAAA6mAAADqYAAAXcJy6UTwAAAAYUExURQAAACLT7iLT7iLT7iLT7iLT7iLT7v///82Mf14AAAAGdFJOUwAAPWysDsggy0sAAAABYktHRAcWYYjrAAAAB3RJTUUH6gsQEDAIkXnpewAAACV0RVh0ZGF0ZTpjcmVhdGUAMjAyNi0xMS0xNlQxNjo0ODowOCswMDowMLXUZnEAAAAldEVYdGRhdGU6bW9kaWZ5ADIwMjYtMTEtMTZUMTY6NDg6MDgrMDA6MDDEid7NAAAAKHRFWHRkYXRlOnRpbWVzdGFtcAAyMDI2LTExLTE2VDE2OjQ4OjA4KzAwOjAwk5z/EgAAAEdJREFUGNNjYMADGJWNQUARzBFJA4MUARBHLRksk6YA4pgZMCAoYjmmIP2mUI4xyORkbDJU0RPAgKTHAJsMin9QfIoSBggAANjtI8ZK8HmmAAAAAElFTkSuQmCC"
  text="CV"
  backgroundColor="#071521"
  textColor="#F8FAFC"
  borderColor="#164E63"
  width={125}
  height={44}
  gradientStops={[
    { offset: '0%', color: '#071521' },
    { offset: '25%', color: '#22D3EE' },
    { offset: '55%', color: '#0E7490' },
    { offset: '80%', color: '#67E8F9' },
    { offset: '100%', color: '#071521' },
  ]}
/>
```

```aura width=860 height=22
<div style={{ display: 'flex', justifyContent: 'center', alignItems: 'center', width: '100%', height: '100%', fontFamily: 'Inter, sans-serif' }}>
  <span style={{ fontSize: 10, color: 'rgba(103,232,249,0.38)', letterSpacing: 0.6 }}>crafted with readme-aura</span>
</div>
```
