```aura width=800 height=360
<div style={{ position: 'relative', display: 'flex', flexDirection: 'column', alignItems: 'center', justifyContent: 'center', width: '100%', height: '100%', background: '#08080d', borderRadius: 20, overflow: 'hidden', fontFamily: 'Inter, sans-serif' }}>
  <style>{`
    @keyframes orb-a { 0%, 100% { transform: translate(0, 0); opacity: 0.6; } 50% { transform: translate(28px, -22px); opacity: 0.9; } }
    @keyframes orb-b { 0%, 100% { transform: translate(0, 0); opacity: 0.5; } 50% { transform: translate(-22px, 18px); opacity: 0.75; } }
    @keyframes orb-c { 0%, 100% { transform: translate(0, 0); opacity: 0.35; } 50% { transform: translate(16px, -28px); opacity: 0.6; } }
    @keyframes ring-blink { 0%, 100% { opacity: 0.06; } 50% { opacity: 0.18; } }
    @keyframes ring-blink-b { 0%, 100% { opacity: 0.04; } 50% { opacity: 0.12; } }
    @keyframes dot-spin { 0% { transform: rotate(0deg); } 100% { transform: rotate(360deg); } }
    #hero-o1 { animation: orb-a 9s ease-in-out infinite; }
    #hero-o2 { animation: orb-b 11s ease-in-out infinite 0.8s; }
    #hero-o3 { animation: orb-a 8s ease-in-out infinite 2s; }
    #hero-o4 { animation: orb-b 13s ease-in-out infinite 0.4s; }
    #hero-o5 { animation: orb-c 7s ease-in-out infinite 1.2s; }
    #hr1 { animation: ring-blink 8s ease-in-out infinite; }
    #hr2 { animation: ring-blink 8s ease-in-out infinite 1.4s; }
    #hr3 { animation: ring-blink-b 8s ease-in-out infinite 2.8s; }
    #hr4 { animation: ring-blink-b 8s ease-in-out infinite 4.2s; }
    #hr5 { animation: ring-blink-b 10s ease-in-out infinite 5.6s; }
    #hero-dot { animation: dot-spin 20s linear infinite; transform-origin: 400px 178px; }
  `}</style>
  <svg width="800" height="360" style={{ position: 'absolute', top: 0, left: 0 }}>
    <defs>
      <radialGradient id="hg1" cx="50%" cy="50%" r="50%"><stop offset="0%" stopColor="rgba(108,195,130,0.55)" /><stop offset="100%" stopColor="rgba(108,195,130,0)" /></radialGradient>
      <radialGradient id="hg2" cx="50%" cy="50%" r="50%"><stop offset="0%" stopColor="rgba(230,100,115,0.5)" /><stop offset="100%" stopColor="rgba(230,100,115,0)" /></radialGradient>
      <radialGradient id="hg3" cx="50%" cy="50%" r="50%"><stop offset="0%" stopColor="rgba(195,155,255,0.35)" /><stop offset="100%" stopColor="rgba(195,155,255,0)" /></radialGradient>
      <radialGradient id="hg4" cx="50%" cy="50%" r="50%"><stop offset="0%" stopColor="rgba(255,195,110,0.28)" /><stop offset="100%" stopColor="rgba(255,195,110,0)" /></radialGradient>
      <radialGradient id="hg5" cx="50%" cy="50%" r="50%"><stop offset="0%" stopColor="rgba(80,160,220,0.3)" /><stop offset="100%" stopColor="rgba(80,160,220,0)" /></radialGradient>
    </defs>
    <ellipse id="hero-o1" cx="110" cy="310" rx="260" ry="200" fill="url(#hg1)" />
    <ellipse id="hero-o2" cx="710" cy="70" rx="230" ry="190" fill="url(#hg2)" />
    <ellipse id="hero-o3" cx="620" cy="330" rx="200" ry="160" fill="url(#hg3)" />
    <ellipse id="hero-o4" cx="200" cy="55" rx="190" ry="150" fill="url(#hg4)" />
    <ellipse id="hero-o5" cx="400" cy="340" rx="170" ry="130" fill="url(#hg5)" />
    <circle id="hr1" cx="400" cy="178" r="52" fill="none" stroke="rgba(255,255,255,0.9)" strokeWidth="0.7" />
    <circle id="hr2" cx="400" cy="178" r="92" fill="none" stroke="rgba(255,255,255,0.9)" strokeWidth="0.7" />
    <circle id="hr3" cx="400" cy="178" r="138" fill="none" stroke="rgba(255,255,255,0.9)" strokeWidth="0.7" />
    <circle id="hr4" cx="400" cy="178" r="192" fill="none" stroke="rgba(255,255,255,0.9)" strokeWidth="0.7" />
    <circle id="hr5" cx="400" cy="178" r="256" fill="none" stroke="rgba(255,255,255,0.9)" strokeWidth="0.7" />
    <g id="hero-dot"><circle cx="400" cy="126" r="2.5" fill="rgba(255,255,255,0.5)" /></g>
  </svg>
  <div style={{ position: 'relative', display: 'flex', flexDirection: 'column', alignItems: 'center', zIndex: 10 }}>
    <span style={{ fontSize: 58, fontWeight: 700, color: '#ffffff', letterSpacing: -2, lineHeight: 1 }}>Ammari Majd</span>
    <span style={{ fontSize: 15, color: 'rgba(255,255,255,0.62)', marginTop: 16, letterSpacing: 4, textTransform: 'uppercase', fontWeight: 300 }}>AI Software Engineer</span>
    <div style={{ display: 'flex', gap: 8, marginTop: 30 }}>
      {['backend systems', 'machine learning', 'production AI'].map((tag, i) => (
        <span key={i} style={{ padding: '5px 16px', background: 'rgba(255,255,255,0.04)', color: 'rgba(255,255,255,0.6)', borderRadius: 100, fontSize: 11, border: '1px solid rgba(255,255,255,0.09)', letterSpacing: 1 }}>{tag}</span>
      ))}
    </div>
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
  <div style={{ position: 'relative', display: 'flex', flex: 1, height: '100%', background: '#08080d', borderRadius: 16, overflow: 'hidden' }}>
    <svg width="100%" height="230" style={{ position: 'absolute', top: 0, left: 0 }}>
      <defs>
        <radialGradient id="ab-gl" cx="50%" cy="50%" r="50%"><stop offset="0%" stopColor="rgba(108,195,130,0.6)" /><stop offset="100%" stopColor="rgba(108,195,130,0)" /></radialGradient>
        <radialGradient id="ab-gr" cx="50%" cy="50%" r="50%"><stop offset="0%" stopColor="rgba(230,100,115,0.5)" /><stop offset="100%" stopColor="rgba(230,100,115,0)" /></radialGradient>
        <radialGradient id="ab-gb" cx="50%" cy="50%" r="50%"><stop offset="0%" stopColor="rgba(195,155,255,0.35)" /><stop offset="100%" stopColor="rgba(195,155,255,0)" /></radialGradient>
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
    <div style={{ display: 'flex', flexDirection: 'column', flex: 1, background: '#08080d', borderRadius: 16, alignItems: 'center', justifyContent: 'center', border: '1px solid rgba(255,255,255,0.04)' }}>
      <span style={{ fontSize: 28, fontWeight: 700, color: '#6cc382' }}>01</span>
      <span style={{ fontSize: 10, color: 'rgba(255,255,255,0.42)', letterSpacing: 2, textTransform: 'uppercase', marginTop: 4 }}>systems that scale</span>
    </div>
    <div style={{ display: 'flex', flexDirection: 'column', flex: 1, background: '#08080d', borderRadius: 16, alignItems: 'center', justifyContent: 'center', border: '1px solid rgba(255,255,255,0.04)' }}>
      <span style={{ fontSize: 28, fontWeight: 700, color: '#c39bff' }}>02</span>
      <span style={{ fontSize: 10, color: 'rgba(255,255,255,0.42)', letterSpacing: 2, textTransform: 'uppercase', marginTop: 4 }}>AI built for use</span>
    </div>
  </div>
</div>
```

```aura width=800 height=62
<div style={{ display: 'flex', alignItems: 'center', width: '100%', height: '100%', fontFamily: 'Inter, sans-serif' }}>
  <span style={{ fontSize: 11, color: 'rgba(255,255,255,0.38)', letterSpacing: 4, textTransform: 'uppercase', marginRight: 18 }}>selected work</span>
  <div style={{ display: 'flex', flex: 1, height: 1, background: 'linear-gradient(90deg, rgba(195,155,255,0.36), rgba(108,195,130,0.2), rgba(255,255,255,0))' }} />
</div>
```

```aura width=256 height=310 link="https://altus-website-sandy.vercel.app" inline align=center
<div style={{ position: 'relative', display: 'flex', flexDirection: 'column', width: '100%', height: '100%', background: '#08080d', borderRadius: 18, overflow: 'hidden', fontFamily: 'Inter, sans-serif', padding: 24, border: '1px solid rgba(255,255,255,0.06)' }}>
  <svg width="256" height="310" style={{ position: 'absolute', top: 0, left: 0 }}><defs><radialGradient id="p1" cx="50%" cy="50%" r="50%"><stop offset="0%" stopColor="rgba(108,195,130,0.48)" /><stop offset="100%" stopColor="rgba(108,195,130,0)" /></radialGradient></defs><ellipse cx="35" cy="300" rx="160" ry="130" fill="url(#p1)" /></svg>
  <span style={{ position: 'relative', fontSize: 44, fontWeight: 700, color: 'rgba(108,195,130,0.22)' }}>01</span>
  <span style={{ position: 'relative', fontSize: 9, color: '#6cc382', letterSpacing: 2, textTransform: 'uppercase', marginTop: 18 }}>live product · private source</span>
  <span style={{ position: 'relative', fontSize: 21, fontWeight: 700, color: '#ffffff', marginTop: 12, lineHeight: 1.15 }}>ALTUS AutoGrader</span>
  <span style={{ position: 'relative', fontSize: 11, color: 'rgba(255,255,255,0.48)', lineHeight: 1.5, marginTop: 12 }}>AI-assisted exam correction with OCR, evidence-linked grading proposals, and teacher review.</span>
  <span style={{ position: 'relative', fontSize: 10, color: 'rgba(255,255,255,0.66)', marginTop: 'auto' }}>FastAPI · Next.js · OpenAI</span>
</div>
```

```aura width=256 height=310 link="https://github.com/AmeriMajd/3DP_AI_Driven_Platform" inline align=center
<div style={{ position: 'relative', display: 'flex', flexDirection: 'column', width: '100%', height: '100%', background: '#08080d', borderRadius: 18, overflow: 'hidden', fontFamily: 'Inter, sans-serif', padding: 24, border: '1px solid rgba(255,255,255,0.06)' }}>
  <svg width="256" height="310" style={{ position: 'absolute', top: 0, left: 0 }}><defs><radialGradient id="p2" cx="50%" cy="50%" r="50%"><stop offset="0%" stopColor="rgba(230,100,115,0.46)" /><stop offset="100%" stopColor="rgba(230,100,115,0)" /></radialGradient></defs><ellipse cx="230" cy="20" rx="150" ry="125" fill="url(#p2)" /></svg>
  <span style={{ position: 'relative', fontSize: 44, fontWeight: 700, color: 'rgba(230,100,115,0.2)' }}>02</span>
  <span style={{ position: 'relative', fontSize: 9, color: '#e66473', letterSpacing: 2, textTransform: 'uppercase', marginTop: 18 }}>machine learning platform</span>
  <span style={{ position: 'relative', fontSize: 21, fontWeight: 700, color: '#ffffff', marginTop: 12, lineHeight: 1.15 }}>3DP AI-Driven Platform</span>
  <span style={{ position: 'relative', fontSize: 11, color: 'rgba(255,255,255,0.48)', lineHeight: 1.5, marginTop: 12 }}>Recommendations for 3D-printing technologies, materials, and process parameters.</span>
  <span style={{ position: 'relative', fontSize: 10, color: 'rgba(255,255,255,0.66)', marginTop: 'auto' }}>FastAPI · Redis · Flutter</span>
</div>
```

```aura width=256 height=310 link="https://github.com/AmeriMajd/large-scale-recommender" inline align=center
<div style={{ position: 'relative', display: 'flex', flexDirection: 'column', width: '100%', height: '100%', background: '#08080d', borderRadius: 18, overflow: 'hidden', fontFamily: 'Inter, sans-serif', padding: 24, border: '1px solid rgba(255,255,255,0.06)' }}>
  <svg width="256" height="310" style={{ position: 'absolute', top: 0, left: 0 }}><defs><radialGradient id="p3" cx="50%" cy="50%" r="50%"><stop offset="0%" stopColor="rgba(195,155,255,0.46)" /><stop offset="100%" stopColor="rgba(195,155,255,0)" /></radialGradient></defs><ellipse cx="40" cy="300" rx="160" ry="130" fill="url(#p3)" /></svg>
  <span style={{ position: 'relative', fontSize: 44, fontWeight: 700, color: 'rgba(195,155,255,0.2)' }}>03</span>
  <span style={{ position: 'relative', fontSize: 9, color: '#c39bff', letterSpacing: 2, textTransform: 'uppercase', marginTop: 18 }}>end-to-end ML system</span>
  <span style={{ position: 'relative', fontSize: 21, fontWeight: 700, color: '#ffffff', marginTop: 12, lineHeight: 1.15 }}>Recommendation Engine</span>
  <span style={{ position: 'relative', fontSize: 11, color: 'rgba(255,255,255,0.48)', lineHeight: 1.5, marginTop: 12 }}>Two-stage retrieval and ranking with serving, caching, and orchestration.</span>
  <span style={{ position: 'relative', fontSize: 10, color: 'rgba(255,255,255,0.66)', marginTop: 'auto' }}>TensorFlow · FAISS · Spark</span>
</div>
```

```aura width=800 height=300
<div style={{ position: 'relative', display: 'flex', width: '100%', height: '100%', gap: 16, fontFamily: 'Inter, sans-serif' }}>
  <div style={{ display: 'flex', flexDirection: 'column', flex: 1, background: '#08080d', borderRadius: 18, padding: 28, border: '1px solid rgba(255,255,255,0.05)' }}>
    <span style={{ fontSize: 10, color: '#6cc382', letterSpacing: 3, textTransform: 'uppercase', marginBottom: 22 }}>experience</span>
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
    <div style={{ display: 'flex', flexDirection: 'column', flex: 1, background: '#08080d', borderRadius: 18, padding: 24, border: '1px solid rgba(255,255,255,0.05)' }}>
      <span style={{ fontSize: 10, color: '#e66473', letterSpacing: 3, textTransform: 'uppercase' }}>2026–2029</span>
      <span style={{ fontSize: 16, color: '#ffffff', fontWeight: 650, marginTop: 12 }}>Computer Science Engineering</span>
      <span style={{ fontSize: 10, color: 'rgba(255,255,255,0.4)', marginTop: 7 }}>ISI · University of Tunis El Manar</span>
    </div>
    <div style={{ display: 'flex', flexDirection: 'column', flex: 1, background: '#08080d', borderRadius: 18, padding: 24, border: '1px solid rgba(255,255,255,0.05)' }}>
      <span style={{ fontSize: 10, color: '#c39bff', letterSpacing: 3, textTransform: 'uppercase' }}>2023–2026</span>
      <span style={{ fontSize: 15, color: '#ffffff', fontWeight: 650, marginTop: 12 }}>Software Engineering & Information Systems</span>
      <span style={{ fontSize: 10, color: 'rgba(255,255,255,0.4)', marginTop: 7 }}>ISIMM</span>
    </div>
  </div>
</div>
```

```aura width=800 height=310
<div style={{ position: 'relative', display: 'flex', flexDirection: 'column', width: '100%', height: '100%', background: '#08080d', borderRadius: 20, overflow: 'hidden', fontFamily: 'Inter, sans-serif', padding: '28px 36px', gap: 17 }}>
  <svg width="800" height="310" style={{ position: 'absolute', top: 0, left: 0 }}><defs><radialGradient id="stack-a" cx="50%" cy="50%" r="50%"><stop offset="0%" stopColor="rgba(108,195,130,0.34)" /><stop offset="100%" stopColor="rgba(108,195,130,0)" /></radialGradient><radialGradient id="stack-b" cx="50%" cy="50%" r="50%"><stop offset="0%" stopColor="rgba(195,155,255,0.28)" /><stop offset="100%" stopColor="rgba(195,155,255,0)" /></radialGradient></defs><ellipse cx="40" cy="300" rx="190" ry="140" fill="url(#stack-a)" /><ellipse cx="770" cy="15" rx="180" ry="130" fill="url(#stack-b)" /></svg>
  <span style={{ position: 'relative', fontSize: 10, color: 'rgba(255,255,255,0.32)', letterSpacing: 4, textTransform: 'uppercase', marginBottom: 3 }}>technical stack</span>
  {[
    ['Languages', ['Python', 'TypeScript', 'SQL', 'T-SQL', 'C++', 'Java']],
    ['Backend & Data', ['FastAPI', 'PostgreSQL', 'Redis', 'REST APIs', 'WebSockets']],
    ['AI & ML', ['PyTorch', 'TensorFlow', 'scikit-learn', 'LLMs', 'RAG', 'OpenAI API', 'OCR']],
    ['Engineering', ['Docker', 'GitHub Actions', 'CI/CD', 'pytest', 'AWS', 'Linux']],
    ['Frontend', ['React', 'Next.js', 'Flutter']],
  ].map((group, i) => (
    <div key={i} style={{ position: 'relative', display: 'flex', alignItems: 'center' }}>
      <span style={{ width: 130, flexShrink: 0, fontSize: 9, color: i % 2 === 0 ? '#6cc382' : '#c39bff', letterSpacing: 1.5, textTransform: 'uppercase' }}>{group[0]}</span>
      <div style={{ display: 'flex', flexWrap: 'wrap', gap: 7 }}>
        {group[1].map((tech, j) => <span key={j} style={{ padding: '5px 11px', background: 'rgba(255,255,255,0.04)', color: 'rgba(255,255,255,0.62)', borderRadius: 100, fontSize: 9, border: '1px solid rgba(255,255,255,0.08)' }}>{tech}</span>)}
      </div>
    </div>
  ))}
</div>
```

```aura width=800 height=170
<div style={{ display: 'flex', flexDirection: 'column', alignItems: 'center', justifyContent: 'center', width: '100%', height: '100%', background: '#08080d', borderRadius: 20, fontFamily: 'Inter, sans-serif', border: '1px solid rgba(255,255,255,0.05)' }}>
  <span style={{ fontSize: 10, color: 'rgba(255,255,255,0.32)', letterSpacing: 4, textTransform: 'uppercase', marginBottom: 18 }}>languages & availability</span>
  <div style={{ display: 'flex', gap: 10 }}>
    {['Arabic · Native', 'English · Fluent', 'French · Professional', 'German · Basic'].map((item, i) => <span key={i} style={{ padding: '7px 14px', background: 'rgba(255,255,255,0.04)', color: 'rgba(255,255,255,0.58)', borderRadius: 100, fontSize: 10, border: '1px solid rgba(255,255,255,0.08)' }}>{item}</span>)}
  </div>
  <span style={{ fontSize: 13, color: 'rgba(255,255,255,0.62)', marginTop: 24 }}>Open to internships, freelance projects, technical collaborations, and future full-time opportunities.</span>
</div>
```

```aura width=145 height=44 link="https://www.linkedin.com/in/ammari-majd-8a1461373/" inline align=center
<SocialMediaButton icon="https://cdn.simpleicons.org/linkedin/0A66C2" text="LinkedIn" backgroundColor="#111111" width={145} height={44} gradientStops={[{ offset: '0%', color: '#6cc382' }, { offset: '28%', color: '#111111' }, { offset: '52%', color: '#c39bff' }, { offset: '76%', color: '#e66473' }, { offset: '100%', color: '#111111' }]} />
```

```aura width=125 height=44 link="mailto:amerimajd0@gmail.com" inline align=center
<SocialMediaButton icon="https://cdn.simpleicons.org/gmail/EA4335" text="Email" backgroundColor="#111111" width={125} height={44} gradientStops={[{ offset: '0%', color: '#e66473' }, { offset: '28%', color: '#111111' }, { offset: '52%', color: '#ffcc88' }, { offset: '76%', color: '#c39bff' }, { offset: '100%', color: '#111111' }]} />
```

```aura width=125 height=44 link="./assets/Ammari_Majd_Software_Engineer.pdf" inline align=center
<SocialMediaButton icon="https://cdn.simpleicons.org/adobeacrobatreader/EC1C24" text="CV" backgroundColor="#111111" width={125} height={44} gradientStops={[{ offset: '0%', color: '#c39bff' }, { offset: '28%', color: '#111111' }, { offset: '52%', color: '#6cc382' }, { offset: '76%', color: '#e66473' }, { offset: '100%', color: '#111111' }]} />
```

```aura width=800 height=22
<div style={{ display: 'flex', justifyContent: 'center', alignItems: 'center', width: '100%', height: '100%', fontFamily: 'Inter, sans-serif' }}><span style={{ fontSize: 10, color: 'rgba(255,255,255,0.25)', letterSpacing: 0.6 }}>crafted with readme-aura</span></div>
```
