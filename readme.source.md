```aura width=800 height=280
<div style={{ position: 'relative', display: 'flex', alignItems: 'center', width: '100%', height: '100%', background: '#08080c', borderRadius: 20, overflow: 'hidden', border: '1px solid rgba(110,80,220,0.20)', fontFamily: 'Inter, sans-serif' }}>
  <style>{`
    @keyframes pg-drift-r { 0%, 100% { transform: translateX(0); opacity: .78; } 50% { transform: translateX(160px); opacity: 1; } }
    @keyframes pg-drift-l { 0%, 100% { transform: translateX(0); opacity: .68; } 50% { transform: translateX(-130px); opacity: .96; } }
    @keyframes pg-pulse { 0%, 100% { transform: scale(1); opacity: .72; } 50% { transform: scale(1.2); opacity: .42; } }
    #pg-h1 { animation: pg-drift-r 10s ease-in-out infinite; }
    #pg-h2 { animation: pg-drift-l 13s ease-in-out infinite; }
    #pg-h3 { animation: pg-drift-r 12s ease-in-out infinite reverse; }
    #pg-h4 { animation: pg-pulse 8s ease-in-out infinite; }
    #pg-h5 { animation: pg-drift-l 15s ease-in-out infinite reverse; }
  `}</style>
  <svg width="800" height="280" style={{ position: 'absolute', top: 0, left: 0 }}>
    <defs>
      <radialGradient id="pgh1" cx="50%" cy="50%" r="50%"><stop offset="0%" stopColor="rgba(110,20,210,0.72)" /><stop offset="45%" stopColor="rgba(90,15,180,0.30)" /><stop offset="72%" stopColor="rgba(90,15,180,0)" /></radialGradient>
      <radialGradient id="pgh2" cx="50%" cy="50%" r="50%"><stop offset="0%" stopColor="rgba(40,60,255,0.62)" /><stop offset="45%" stopColor="rgba(30,50,200,0.24)" /><stop offset="72%" stopColor="rgba(30,50,200,0)" /></radialGradient>
      <radialGradient id="pgh3" cx="50%" cy="50%" r="50%"><stop offset="0%" stopColor="rgba(0,165,255,0.46)" /><stop offset="72%" stopColor="rgba(0,130,220,0)" /></radialGradient>
      <radialGradient id="pgh4" cx="50%" cy="50%" r="50%"><stop offset="0%" stopColor="rgba(190,45,255,0.50)" /><stop offset="72%" stopColor="rgba(150,20,220,0)" /></radialGradient>
      <radialGradient id="pgh5" cx="50%" cy="50%" r="50%"><stop offset="0%" stopColor="rgba(255,50,180,0.30)" /><stop offset="72%" stopColor="rgba(220,30,180,0)" /></radialGradient>
    </defs>
    <ellipse id="pg-h1" cx="90" cy="285" rx="250" ry="185" fill="url(#pgh1)" />
    <ellipse id="pg-h2" cx="360" cy="280" rx="220" ry="165" fill="url(#pgh2)" />
    <ellipse id="pg-h3" cx="610" cy="275" rx="210" ry="155" fill="url(#pgh3)" />
    <ellipse id="pg-h4" cx="760" cy="40" rx="170" ry="135" fill="url(#pgh4)" />
    <ellipse id="pg-h5" cx="360" cy="10" rx="145" ry="110" fill="url(#pgh5)" />
  </svg>
  <div style={{ position: 'relative', display: 'flex', flexDirection: 'column', marginLeft: 52 }}>
    <span style={{ fontSize: 13, color: '#a78bfa', letterSpacing: 3, textTransform: 'uppercase', fontWeight: 600 }}>Hello, I’m</span>
    <span style={{ fontSize: 54, fontWeight: 800, color: '#ffffff', letterSpacing: -2, lineHeight: 1, marginTop: 10 }}>Ammari Majd</span>
    <span style={{ fontSize: 17, color: 'rgba(205,195,255,0.86)', marginTop: 13, letterSpacing: 1.2 }}>AI Software Engineer</span>
    <div style={{ display: 'flex', gap: 8, marginTop: 24 }}>
      {['Backend Systems', 'Machine Learning', 'Production AI'].map((tag, i) => (
        <span key={i} style={{ padding: '6px 13px', background: 'rgba(80,40,220,0.18)', color: 'rgba(215,207,255,0.88)', borderRadius: 100, fontSize: 10, border: '1px solid rgba(120,85,245,0.34)', letterSpacing: .4 }}>{tag}</span>
      ))}
    </div>
  </div>
  <div style={{ position: 'absolute', right: 48, top: 48, display: 'flex', flexDirection: 'column', gap: 11, opacity: .62 }}>
    {[['01','API'], ['02','ML'], ['03','AI']].map((item, i) => (
      <div key={i} style={{ display: 'flex', alignItems: 'center', gap: 10 }}>
        <span style={{ fontSize: 9, color: '#60a5fa', letterSpacing: 1 }}>{item[0]}</span>
        <div style={{ width: 54, height: 1, background: 'linear-gradient(90deg,#7c3aed,#38bdf8)' }} />
        <span style={{ fontSize: 10, color: 'rgba(255,255,255,.72)', letterSpacing: 2 }}>{item[1]}</span>
      </div>
    ))}
  </div>
</div>
```

```aura width=800 height=230
<div style={{ display: 'flex', flexDirection: 'row', gap: 16, width: '100%', height: '100%', fontFamily: 'Inter, sans-serif' }}>
  <style>{`
    @keyframes about-orb-l { 0%, 100% { transform: translate(0,0); opacity: 0.65; } 50% { transform: translate(20px,-14px); opacity: 0.9; } }
    @keyframes about-orb-r { 0%, 100% { transform: translate(0,0); opacity: 0.55; } 50% { transform: translate(-16px,12px); opacity: 0.8; } }
    @keyframes about-ring { 0%, 100% { opacity: 0.07; } 50% { opacity: 0.2; } }
    @keyframes cursor-blink { 0%, 49% { opacity: 1; } 50%, 100% { opacity: 0; } }
    #ab-o1 { animation: about-orb-l 8s ease-in-out infinite; }
    #ab-o2 { animation: about-orb-r 10s ease-in-out infinite 1s; }
    #ab-o3 { animation: about-orb-l 7s ease-in-out infinite 2s; }
    #ab-r1 { animation: about-ring 7s ease-in-out infinite; }
    #ab-r2 { animation: about-ring 7s ease-in-out infinite 2s; }
    #ab-cursor { animation: cursor-blink 1.1s step-end infinite; }
  `}</style>
  <div style={{ position: 'relative', display: 'flex', flex: 1, height: '100%', background: '#08080c', borderRadius: 16, overflow: 'hidden', border: '1px solid rgba(110,80,220,0.18)' }}>
    <svg width="100%" height="230" style={{ position: 'absolute', top: 0, left: 0 }}>
      <defs>
        <radialGradient id="ab-gl" cx="50%" cy="50%" r="50%"><stop offset="0%" stopColor="rgba(110,20,210,0.62)" /><stop offset="100%" stopColor="rgba(110,20,210,0)" /></radialGradient>
        <radialGradient id="ab-gr" cx="50%" cy="50%" r="50%"><stop offset="0%" stopColor="rgba(40,70,255,0.52)" /><stop offset="100%" stopColor="rgba(40,70,255,0)" /></radialGradient>
        <radialGradient id="ab-gb" cx="50%" cy="50%" r="50%"><stop offset="0%" stopColor="rgba(0,170,255,0.38)" /><stop offset="100%" stopColor="rgba(0,170,255,0)" /></radialGradient>
      </defs>
      <ellipse id="ab-o1" cx="40" cy="190" rx="150" ry="120" fill="url(#ab-gl)" />
      <ellipse id="ab-o2" cx="440" cy="40" rx="140" ry="110" fill="url(#ab-gr)" />
      <ellipse id="ab-o3" cx="330" cy="220" rx="120" ry="100" fill="url(#ab-gb)" />
      <circle id="ab-r1" cx="440" cy="115" r="45" fill="none" stroke="rgba(255,255,255,0.9)" strokeWidth="0.7" />
      <circle id="ab-r2" cx="440" cy="115" r="78" fill="none" stroke="rgba(255,255,255,0.9)" strokeWidth="0.7" />
    </svg>
    <div style={{ position: 'relative', display: 'flex', flexDirection: 'column', justifyContent: 'center', padding: '0 30px', zIndex: 10 }}>
      <span style={{ fontSize: 11, color: 'rgba(255,255,255,0.38)', letterSpacing: 3, textTransform: 'uppercase', marginBottom: 12 }}>about</span>
      <span style={{ fontSize: 20, fontWeight: 600, color: '#ffffff', lineHeight: 1.42 }}>I build reliable backend systems and production-ready AI products—from data pipelines and ML services to full-stack platforms.</span>
      <div style={{ display: 'flex', alignItems: 'center', marginTop: 16 }}>
        <span style={{ fontSize: 12, color: 'rgba(255,255,255,0.48)', fontFamily: 'monospace' }}>{'> Ariana, Tunisia'}</span>
        <span id="ab-cursor" style={{ fontSize: 12, color: 'rgba(255,255,255,0.7)', fontFamily: 'monospace', marginLeft: 2 }}>_</span>
      </div>
    </div>
  </div>
  <div style={{ display: 'flex', flexDirection: 'column', gap: 16, width: 220, flexShrink: 0 }}>
    <div style={{ display: 'flex', flexDirection: 'column', flex: 1, background: '#08080c', borderRadius: 16, alignItems: 'center', justifyContent: 'center', border: '1px solid rgba(110,80,220,0.18)' }}>
      <span style={{ fontSize: 28, fontWeight: 700, color: '#a78bfa' }}>01</span>
      <span style={{ fontSize: 10, color: 'rgba(255,255,255,0.42)', letterSpacing: 2, textTransform: 'uppercase', marginTop: 4 }}>systems that scale</span>
    </div>
    <div style={{ display: 'flex', flexDirection: 'column', flex: 1, background: '#08080c', borderRadius: 16, alignItems: 'center', justifyContent: 'center', border: '1px solid rgba(110,80,220,0.18)' }}>
      <span style={{ fontSize: 28, fontWeight: 700, color: '#60a5fa' }}>02</span>
      <span style={{ fontSize: 10, color: 'rgba(255,255,255,0.42)', letterSpacing: 2, textTransform: 'uppercase', marginTop: 4 }}>AI built for use</span>
    </div>
  </div>
</div>
```

```aura width=800 height=62
<div style={{ display: 'flex', alignItems: 'center', width: '100%', height: '100%', fontFamily: 'Inter, sans-serif' }}>
  <span style={{ fontSize: 11, color: 'rgba(255,255,255,0.38)', letterSpacing: 4, textTransform: 'uppercase', marginRight: 18 }}>selected work</span>
  <div style={{ display: 'flex', flex: 1, height: 1, background: 'linear-gradient(90deg, rgba(167,139,250,0.56), rgba(56,189,248,0.34), rgba(255,255,255,0))' }} />
</div>
```

```aura width=256 height=310 link="https://altus-website-sandy.vercel.app" inline align=center
<div style={{ position: 'relative', display: 'flex', flexDirection: 'column', width: '100%', height: '100%', background: '#08080c', borderRadius: 18, overflow: 'hidden', fontFamily: 'Inter, sans-serif', padding: 24, border: '1px solid rgba(110,80,220,0.22)' }}>
  <svg width="256" height="310" style={{ position: 'absolute', top: 0, left: 0 }}><defs><radialGradient id="p1" cx="50%" cy="50%" r="50%"><stop offset="0%" stopColor="rgba(110,20,210,0.54)" /><stop offset="100%" stopColor="rgba(110,20,210,0)" /></radialGradient></defs><ellipse cx="35" cy="300" rx="160" ry="130" fill="url(#p1)" /></svg>
  <span style={{ position: 'relative', fontSize: 44, fontWeight: 700, color: 'rgba(167,139,250,0.24)' }}>01</span>
  <span style={{ position: 'relative', fontSize: 9, color: '#a78bfa', letterSpacing: 2, textTransform: 'uppercase', marginTop: 18 }}>live product · private source</span>
  <span style={{ position: 'relative', fontSize: 21, fontWeight: 700, color: '#ffffff', marginTop: 12, lineHeight: 1.15 }}>ALTUS AutoGrader</span>
  <span style={{ position: 'relative', fontSize: 11, color: 'rgba(255,255,255,0.48)', lineHeight: 1.5, marginTop: 12 }}>AI-assisted exam correction with OCR, evidence-linked grading proposals, and teacher review.</span>
  <span style={{ position: 'relative', fontSize: 10, color: 'rgba(255,255,255,0.66)', marginTop: 'auto' }}>FastAPI · Next.js · OpenAI</span>
</div>
```

```aura width=256 height=310 link="https://github.com/AmeriMajd/3DP_AI_Driven_Platform" inline align=center
<div style={{ position: 'relative', display: 'flex', flexDirection: 'column', width: '100%', height: '100%', background: '#08080c', borderRadius: 18, overflow: 'hidden', fontFamily: 'Inter, sans-serif', padding: 24, border: '1px solid rgba(110,80,220,0.22)' }}>
  <svg width="256" height="310" style={{ position: 'absolute', top: 0, left: 0 }}><defs><radialGradient id="p2" cx="50%" cy="50%" r="50%"><stop offset="0%" stopColor="rgba(40,70,255,0.50)" /><stop offset="100%" stopColor="rgba(40,70,255,0)" /></radialGradient></defs><ellipse cx="230" cy="20" rx="150" ry="125" fill="url(#p2)" /></svg>
  <span style={{ position: 'relative', fontSize: 44, fontWeight: 700, color: 'rgba(96,165,250,0.22)' }}>02</span>
  <span style={{ position: 'relative', fontSize: 9, color: '#60a5fa', letterSpacing: 2, textTransform: 'uppercase', marginTop: 18 }}>machine learning platform</span>
  <span style={{ position: 'relative', fontSize: 21, fontWeight: 700, color: '#ffffff', marginTop: 12, lineHeight: 1.15 }}>3DP AI-Driven Platform</span>
  <span style={{ position: 'relative', fontSize: 11, color: 'rgba(255,255,255,0.48)', lineHeight: 1.5, marginTop: 12 }}>Recommendations for 3D-printing technologies, materials, and process parameters.</span>
  <span style={{ position: 'relative', fontSize: 10, color: 'rgba(255,255,255,0.66)', marginTop: 'auto' }}>FastAPI · Redis · Flutter</span>
</div>
```

```aura width=256 height=310 link="https://github.com/AmeriMajd/large-scale-recommender" inline align=center
<div style={{ position: 'relative', display: 'flex', flexDirection: 'column', width: '100%', height: '100%', background: '#08080c', borderRadius: 18, overflow: 'hidden', fontFamily: 'Inter, sans-serif', padding: 24, border: '1px solid rgba(110,80,220,0.22)' }}>
  <svg width="256" height="310" style={{ position: 'absolute', top: 0, left: 0 }}><defs><radialGradient id="p3" cx="50%" cy="50%" r="50%"><stop offset="0%" stopColor="rgba(0,170,255,0.44)" /><stop offset="100%" stopColor="rgba(0,170,255,0)" /></radialGradient></defs><ellipse cx="40" cy="300" rx="160" ry="130" fill="url(#p3)" /></svg>
  <span style={{ position: 'relative', fontSize: 44, fontWeight: 700, color: 'rgba(56,189,248,0.22)' }}>03</span>
  <span style={{ position: 'relative', fontSize: 9, color: '#38bdf8', letterSpacing: 2, textTransform: 'uppercase', marginTop: 18 }}>end-to-end ML system</span>
  <span style={{ position: 'relative', fontSize: 21, fontWeight: 700, color: '#ffffff', marginTop: 12, lineHeight: 1.15 }}>Recommendation Engine</span>
  <span style={{ position: 'relative', fontSize: 11, color: 'rgba(255,255,255,0.48)', lineHeight: 1.5, marginTop: 12 }}>Two-stage retrieval and ranking with serving, caching, and orchestration.</span>
  <span style={{ position: 'relative', fontSize: 10, color: 'rgba(255,255,255,0.66)', marginTop: 'auto' }}>TensorFlow · FAISS · Spark</span>
</div>
```

```aura width=800 height=300
<div style={{ position: 'relative', display: 'flex', width: '100%', height: '100%', gap: 16, fontFamily: 'Inter, sans-serif' }}>
  <div style={{ display: 'flex', flexDirection: 'column', flex: 1, background: '#08080c', borderRadius: 18, padding: 28, border: '1px solid rgba(110,80,220,0.18)' }}>
    <span style={{ fontSize: 10, color: '#a78bfa', letterSpacing: 3, textTransform: 'uppercase', marginBottom: 22 }}>experience</span>
    {[
      ['2026', 'Software Engineering Intern', 'SPIRAW / ACTIA'],
      ['2025', 'AI/ML Engineering Intern', 'ACTIA Engineering Services'],
      ['2024–25', 'Machine Learning Engineer', 'HoutaLik'],
    ].map((item, i) => (
      <div key={i} style={{ display: 'flex', marginBottom: 22 }}>
        <span style={{ width: 62, flexShrink: 0, fontSize: 10, color: 'rgba(255,255,255,0.3)', paddingTop: 3 }}>{item[0]}</span>
        <div style={{ display: 'flex', flexDirection: 'column' }}>
          <span style={{ fontSize: 14, color: '#ffffff', fontWeight: 600 }}>{item[1]}</span>
          <span style={{ fontSize: 10, color: 'rgba(255,255,255,0.4)', marginTop: 4 }}>{item[2]}</span>
        </div>
      </div>
    ))}
  </div>
  <div style={{ display: 'flex', flexDirection: 'column', width: 300, gap: 16 }}>
    <div style={{ display: 'flex', flexDirection: 'column', flex: 1, background: '#08080c', borderRadius: 18, padding: 24, border: '1px solid rgba(110,80,220,0.18)' }}>
      <span style={{ fontSize: 10, color: '#60a5fa', letterSpacing: 3, textTransform: 'uppercase' }}>2026–2029</span>
      <span style={{ fontSize: 16, color: '#ffffff', fontWeight: 650, marginTop: 12 }}>Computer Science Engineering</span>
      <span style={{ fontSize: 10, color: 'rgba(255,255,255,0.4)', marginTop: 7 }}>ISI · University of Tunis El Manar</span>
    </div>
    <div style={{ display: 'flex', flexDirection: 'column', flex: 1, background: '#08080c', borderRadius: 18, padding: 24, border: '1px solid rgba(110,80,220,0.18)' }}>
      <span style={{ fontSize: 10, color: '#a78bfa', letterSpacing: 3, textTransform: 'uppercase' }}>2023–2026</span>
      <span style={{ fontSize: 15, color: '#ffffff', fontWeight: 650, marginTop: 12 }}>Software Engineering & Information Systems</span>
      <span style={{ fontSize: 10, color: 'rgba(255,255,255,0.4)', marginTop: 7 }}>ISIMM</span>
    </div>
  </div>
</div>
```

```aura width=800 height=310
<div style={{ position: 'relative', display: 'flex', flexDirection: 'column', width: '100%', height: '100%', background: '#08080c', borderRadius: 20, overflow: 'hidden', fontFamily: 'Inter, sans-serif', padding: '28px 36px', gap: 17, border: '1px solid rgba(110,80,220,0.18)' }}>
  <svg width="800" height="310" style={{ position: 'absolute', top: 0, left: 0 }}><defs><radialGradient id="stack-a" cx="50%" cy="50%" r="50%"><stop offset="0%" stopColor="rgba(110,20,210,0.42)" /><stop offset="100%" stopColor="rgba(110,20,210,0)" /></radialGradient><radialGradient id="stack-b" cx="50%" cy="50%" r="50%"><stop offset="0%" stopColor="rgba(0,160,255,0.32)" /><stop offset="100%" stopColor="rgba(0,160,255,0)" /></radialGradient></defs><ellipse cx="40" cy="300" rx="190" ry="140" fill="url(#stack-a)" /><ellipse cx="770" cy="15" rx="180" ry="130" fill="url(#stack-b)" /></svg>
  <span style={{ position: 'relative', fontSize: 10, color: 'rgba(255,255,255,0.32)', letterSpacing: 4, textTransform: 'uppercase', marginBottom: 3 }}>technical stack</span>
  {[
    ['Languages', ['Python', 'TypeScript', 'SQL', 'T-SQL', 'C++', 'Java']],
    ['Backend & Data', ['FastAPI', 'PostgreSQL', 'Redis', 'REST APIs', 'WebSockets']],
    ['AI & ML', ['PyTorch', 'TensorFlow', 'scikit-learn', 'LLMs', 'RAG', 'OpenAI API', 'OCR']],
    ['Engineering', ['Docker', 'GitHub Actions', 'CI/CD', 'pytest', 'AWS', 'Linux']],
    ['Frontend', ['React', 'Next.js', 'Flutter']],
  ].map((group, i) => (
    <div key={i} style={{ position: 'relative', display: 'flex', alignItems: 'center' }}>
      <span style={{ width: 130, flexShrink: 0, fontSize: 9, color: i % 2 === 0 ? '#a78bfa' : '#60a5fa', letterSpacing: 1.5, textTransform: 'uppercase' }}>{group[0]}</span>
      <div style={{ display: 'flex', flexWrap: 'wrap', gap: 7 }}>
        {group[1].map((tech, j) => <span key={j} style={{ padding: '5px 11px', background: 'rgba(255,255,255,0.04)', color: 'rgba(255,255,255,0.62)', borderRadius: 100, fontSize: 9, border: '1px solid rgba(255,255,255,0.08)' }}>{tech}</span>)}
      </div>
    </div>
  ))}
</div>
```

```aura width=800 height=170
<div style={{ display: 'flex', flexDirection: 'column', alignItems: 'center', justifyContent: 'center', width: '100%', height: '100%', background: '#08080c', borderRadius: 20, fontFamily: 'Inter, sans-serif', border: '1px solid rgba(110,80,220,0.18)' }}>
  <span style={{ fontSize: 10, color: 'rgba(255,255,255,0.32)', letterSpacing: 4, textTransform: 'uppercase', marginBottom: 18 }}>languages & availability</span>
  <div style={{ display: 'flex', gap: 10 }}>
    {['Arabic · Native', 'English · Fluent', 'French · Professional', 'German · Basic'].map((item, i) => <span key={i} style={{ padding: '7px 14px', background: 'rgba(255,255,255,0.04)', color: 'rgba(255,255,255,0.58)', borderRadius: 100, fontSize: 10, border: '1px solid rgba(255,255,255,0.08)' }}>{item}</span>)}
  </div>
  <span style={{ fontSize: 13, color: 'rgba(255,255,255,0.62)', marginTop: 24 }}>Open to internships, freelance projects, technical collaborations, and future full-time opportunities.</span>
</div>
```

```aura width=150 height=46 link="https://www.linkedin.com/in/ammari-majd-8a1461373/" inline align=center
<SocialMediaButton icon="data:image/svg+xml;base64,PHN2ZyByb2xlPSJpbWciIHZpZXdCb3g9IjAgMCAyNCAyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj48dGl0bGU+TGlua2VkSW48L3RpdGxlPjxwYXRoIGZpbGw9IiMwQTY2QzIiIGQ9Ik0yMC40NDcgMjAuNDUyaC0zLjU1NHYtNS41NjljMC0xLjMyOC0uMDI3LTMuMDM3LTEuODUyLTMuMDM3LTEuODUzIDAtMi4xMzYgMS40NDUtMi4xMzYgMi45Mzl2NS42NjdIOS4zNTFWOWgzLjQxNHYxLjU2MWguMDQ2Yy40NzctLjkgMS42MzctMS44NSAzLjM3LTEuODUgMy42MDEgMCA0LjI2NyAyLjM3IDQuMjY3IDUuNDU1djYuMjg2ek01LjMzNyA3LjQzM2MtMS4xNDQgMC0yLjA2My0uOTI2LTIuMDYzLTIuMDY1IDAtMS4xMzguOTItMi4wNjMgMi4wNjMtMi4wNjMgMS4xNCAwIDIuMDY0LjkyNSAyLjA2NCAyLjA2MyAwIDEuMTM5LS45MjUgMi4wNjUtMi4wNjQgMi4wNjV6bTEuNzgyIDEzLjAxOUgzLjU1NVY5aDMuNTY0djExLjQ1MnpNMjIuMjI1IDBIMS43NzFDLjc5MiAwIDAgLjc3NCAwIDEuNzI5djIwLjU0MkMwIDIzLjIyNy43OTIgMjQgMS43NzEgMjRoMjAuNDUxQzIzLjIgMjQgMjQgMjMuMjI3IDI0IDIyLjI3MVYxLjcyOUMyNCAuNzc0IDIzLjIgMCAyMi4yMjIgMGguMDAzeiIvPjwvc3ZnPg==" text="LinkedIn" backgroundColor="#08080c" width={150} height={46} iconSize="18" gradientStops={[{ offset: '0%', color: '#7c3aed' }, { offset: '45%', color: '#38bdf8' }, { offset: '75%', color: '#c026d3' }, { offset: '100%', color: '#7c3aed' }]} />
```

```aura width=140 height=46 link="mailto:amerimajd0@gmail.com" inline align=center
<SocialMediaButton icon="data:image/svg+xml;base64,PHN2ZyByb2xlPSJpbWciIHZpZXdCb3g9IjAgMCAyNCAyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj48dGl0bGU+R21haWw8L3RpdGxlPjxwYXRoIGZpbGw9IiNFQTQzMzUiIGQ9Ik0yNCA1LjQ1N3YxMy45MDljMCAuOTA0LS43MzIgMS42MzYtMS42MzYgMS42MzZoLTMuODE5VjExLjczTDEyIDE2LjY0bC02LjU0NS00LjkxdjkuMjczSDEuNjM2QTEuNjM2IDEuNjM2IDAgMCAxIDAgMTkuMzY2VjUuNDU3YzAtMi4wMjMgMi4zMDktMy4xNzggMy45MjctMS45NjRMNS40NTUgNC42NCAxMiA5LjU0OGw2LjU0NS00LjkxIDEuNTI4LTEuMTQ1QzIxLjY5IDIuMjggMjQgMy40MzQgMjQgNS40NTd6Ii8+PC9zdmc+" text="Email" backgroundColor="#08080c" width={140} height={46} iconSize="19" gradientStops={[{ offset: '0%', color: '#38bdf8' }, { offset: '45%', color: '#7c3aed' }, { offset: '75%', color: '#c026d3' }, { offset: '100%', color: '#38bdf8' }]} />
```

```aura width=125 height=46 link="./assets/Ammari_Majd_Software_Engineer.pdf" inline align=center
<SocialMediaButton icon="data:image/svg+xml;base64,PHN2ZyByb2xlPSJpbWciIHZpZXdCb3g9IjAgMCAyNCAyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj48dGl0bGU+QWRvYmUgQWNyb2JhdCBSZWFkZXI8L3RpdGxlPjxwYXRoIGZpbGw9IiNFQzFDMjQiIGQ9Ik0yMy42MyAxNS4zYy0uNzEtLjc0NS0yLjE2Ni0xLjE3LTQuMjI0LTEuMTctMS4xIDAtMi4zNzcuMTA2LTMuNzYxLjM1NGExOS40NDMgMTkuNDQzIDAgMCAxLTIuMzA3LTIuNjYxYy0uNTMyLS43MS0uOTk0LTEuNDktMS40Mi0yLjIzNi44MTctMi40ODQgMS4yMDctNC41MDcgMS4yMDctNS45NjIgMC0xLjYzMi0uNjAzLTMuMzM2LTIuMzQyLTMuMzM2LS41MzIgMC0xLjA2NS4zMi0xLjM0OS43ODEtLjc4IDEuMzg0LS40MjUgNC40LjkyMyA3LjM4MWE2MC4yNzcgNjAuMjc3IDAgMCAxLTEuNzAzIDQuNTA3Yy0uNTY4IDEuMzQ5LTEuMjA3IDIuNzMzLTEuOTE3IDQuMDFDMi44MzQgMTguNTMuMzE0IDIwLjM0LjAzIDIxLjc1OGMtLjEwNi41MzMuMDcxIDEuMDMuNDYyIDEuNDIuMTQyLjEwNy42MzkuNTMzIDEuNDkuNTMzIDIuNTkgMCA1LjMyMy00LjE4OCA2LjcwNy02LjcwNyAxLjA2NS0uMzU1IDIuMTMtLjcxIDMuMTk0LS45OTRhMzQuOTYzIDM0Ljk2MyAwIDAgMSAzLjQwNy0uNzQ1YzIuNzMyIDIuNDQ4IDUuMTQ1IDIuODM5IDYuMzUyIDIuODM5IDEuNDkgMCAyLjAyMy0uNjA0IDIuMi0xLjEuMzItLjY0LjEwNi0xLjM0OS0uMjEzLTEuNzA0em0tMS40MiAxLjAzYy0uMTA3LjUzMi0uNjQuODg3LTEuMzg0Ljg4Ny0uMjEzIDAtLjM5LS4wMzYtLjYwNC0uMDcxLTEuMzQ4LS4zMi0yLjYyNi0uOTk0LTMuOTAzLTIuMDU5YTE3LjcxNyAxNy43MTcgMCAwIDEgMi45OC0uMjQ4Yy43NDYgMCAxLjM4NS4wMzUgMS44MS4xNDIuNDk3LjEwNiAxLjI3OC40MjYgMS4xIDEuMzQ4em0tNy41MjQtMS42NjhhMzguMDEgMzguMDEgMCAwIDAtMi45NDUuNjc0IDM5LjY4IDM5LjY4IDAgMCAwLTIuNTIuNzQ1IDQwLjA1IDQwLjA1IDAgMCAwIDEuMjA3LTIuNTU1Yy40MjYtLjk5NC43OC0yLjAyMyAxLjEzNi0yLjk4MS4zNTQuNjAzLjc0NSAxLjIwNyAxLjEzNSAxLjczOWE1MC4xMjcgNTAuMTI3IDAgMCAwIDEuOTg3IDIuMzc4ek0xMC4wMzggMS40NmEuNzY4Ljc2OCAwIDAgMSAuNjc0LS40MjVjLjc0NSAwIC44ODcuODUxLjg4NyAxLjUyNiAwIDEuMTM1LS4zNTUgMi44NzQtLjk1OCA0Ljg2MS0xLjAzLTIuNzY4LTEuMS01LjA3NC0uNjAzLTUuOTYyek02LjEzNCAxNy45OTdjLTEuODEgMi45ODEtMy41NDkgNC44MjYtNC42MTMgNC44MjZhLjg3Mi44NzIgMCAwIDEtLjUzMi0uMTc3Yy0uMjEzLS4yMTMtLjMyLS40NjEtLjI0OS0uNzQ1LjIxMy0xLjA2NSAyLjI3MS0yLjU1NSA1LjM5NC0zLjkwNFoiLz48L3N2Zz4=" text="CV" backgroundColor="#08080c" width={125} height={46} iconSize="18" gradientStops={[{ offset: '0%', color: '#c026d3' }, { offset: '45%', color: '#7c3aed' }, { offset: '75%', color: '#38bdf8' }, { offset: '100%', color: '#c026d3' }]} />
```

```aura width=800 height=22
<div style={{ display: 'flex', justifyContent: 'center', alignItems: 'center', width: '100%', height: '100%', fontFamily: 'Inter, sans-serif' }}><span style={{ fontSize: 10, color: 'rgba(255,255,255,0.25)', letterSpacing: 0.6 }}>crafted with readme-aura</span></div>
```
