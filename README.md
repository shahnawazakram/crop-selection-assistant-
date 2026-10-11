# crop-selection-assistant-
with the help of the this website we can help farmers to maximise their crop productivity an also help them to recover from losses
/* ========================================= CROP SELECTION ASSISTANT Main stylesheet: App.css ========================================= */

:root { --primary: #218c52; --primary-dark: #126438; --primary-light: #e7f7ec; --accent: #b9f6ca; --background: #f7fbf7; --surface: #ffffff; --text: #183327; --muted: #687a70; --border: #e0ebe3; --shadow: 0 10px 35px rgba(24, 80, 48, 0.09); --radius: 18px; }

{

box-sizing: border-box; margin: 0; padding: 0; }

html { scroll-behavior: smooth; }

body { font-family: Inter, "Segoe UI", Arial, sans-serif; background: var(--background); color: var(--text); line-height: 1.6; }

button, input, select { font: inherit; }

button, a { -webkit-tap-highlight-color: transparent; }

a { color: inherit; text-decoration: none; }

button { cursor: pointer; }

/* Main application */

.app { min-height: 100vh; overflow: hidden; }

.container { width: min(1180px, 92%); margin-inline: auto; }

/* Navigation */

.navbar { position: sticky; top: 0; z-index: 100; background: rgba(255, 255, 255, 0.92); backdrop-filter: blur(16px); border-bottom: 1px solid var(--border); }

.navbar-inner { min-height: 76px; display: flex; justify-content: space-between; align-items: center; gap: 24px; }

.logo { display: inline-flex; align-items: center; gap: 10px; font-size: 1.25rem; font-weight: 800; color: var(--primary-dark); }

.logo-icon { width: 42px; height: 42px; display: grid; place-items: center; background: var(--primary-light); border-radius: 14px; font-size: 1.5rem; }

.nav-links { display: flex; align-items: center; gap: 26px; }

.nav-links a { color: var(--muted); font-size: 0.95rem; font-weight: 600; transition: color 0.2s ease; }

.nav-links a:hover { color: var(--primary); }

.nav-actions { display: flex; align-items: center; gap: 12px; }

/* Buttons */

.btn { display: inline-flex; align-items: center; justify-content: center; gap: 8px; min-height: 46px; padding: 11px 22px; border: 1px solid transparent; border-radius: 12px; font-weight: 700; transition: transform 0.2s ease, background 0.2s ease, box-shadow 0.2s ease; }

.btn:hover { transform: translateY(-2px); }

.btn-primary { color: #fff; background: var(--primary); box-shadow: 0 5px 16px rgba(33, 140, 82, 0.18); }

.btn-primary:hover { background: var(--primary-dark); box-shadow: 0 8px 22px rgba(33, 140, 82, 0.25); }

.btn-outline { color: var(--primary-dark); background: #fff; border-color: var(--border); }

.btn-outline:hover { background: var(--primary-light); border-color: var(--primary); }

.btn-full { width: 100%; }

/* Hero section */

.hero { position: relative; min-height: 620px; display: flex; align-items: center; padding: 90px 0; isolation: isolate; background: radial-gradient( circle at 80% 20%, rgba(185, 246, 202, 0.55), transparent 35% ), linear-gradient(135deg, #f8fff9, #eaf8ed); }

.hero-content { position: relative; z-index: 2; max-width: 720px; }

.eyebrow { display: inline-flex; align-items: center; gap: 8px; padding: 8px 14px; border: 1px solid #ccebd5; border-radius: 999px; background: rgba(255, 255, 255, 0.8); color: var(--primary-dark); font-size: 0.85rem; font-weight: 700; margin-bottom: 24px; }

.hero h1 { max-width: 760px; font-size: clamp(2.5rem, 6vw, 4.8rem); line-height: 1.08; letter-spacing: -2px; margin-bottom: 24px; }

.hero h1 span { color: var(--primary); }

.hero p { max-width: 620px; color: var(--muted); font-size: 1.1rem; margin-bottom: 30px; }

.hero-actions { display: flex; flex-wrap: wrap; gap: 14px; }

/* Optional background video */

.hero-video { position: absolute; inset: 0; width: 100%; height: 100%; object-fit: cover; z-index: -2; opacity: 0.18; }

.hero-overlay { position: absolute; inset: 0; z-index: -1; background: linear-gradient( 90deg, rgba(248, 255, 249, 0.97) 0%, rgba(248, 255, 249, 0.82) 58%, rgba(248, 255, 249, 0.55) 100% ); }

/* Subtle RGB lighting */

.glow-orb { position: absolute; width: 260px; height: 260px; right: 7%; top: 20%; border-radius: 50%; background: linear-gradient( 135deg, rgba(52, 211, 153, 0.25), rgba(96, 165, 250, 0.14), rgba(192, 132, 252, 0.12) ); filter: blur(45px); pointer-events: none; animation: glow 8s ease-in-out infinite alternate; }

@keyframes glow { from { transform: translate(0, 0) scale(0.95); }

to { transform: translate(-18px, 15px) scale(1.08); } }

/* Sections */

.section { padding: 80px 0; }

.section-header { text-align: center; max-width: 700px; margin: 0 auto 42px; }

.section-header h2 { font-size: clamp(1.8rem, 4vw, 2.7rem); line-height: 1.2; margin-bottom: 14px; }

.section-header p { color: var(--muted); }

/* Feature cards */

.feature-grid { display: grid; grid-template-columns: repeat(3, minmax(0, 1fr)); gap: 24px; }

.feature-card { padding: 28px; background: var(--surface); border: 1px solid var(--border); border-radius: var(--radius); box-shadow: var(--shadow); transition: transform 0.25s ease, border-color 0.25s ease; }

.feature-card:hover { transform: translateY(-6px); border-color: #a9ddb9; }

.feature-icon { width: 54px; height: 54px; display: grid; place-items: center; border-radius: 16px; background: var(--primary-light); font-size: 1.7rem; margin-bottom: 20px; }

.feature-card h3 { font-size: 1.2rem; margin-bottom: 10px; }

.feature-card p { color: var(--muted); font-size: 0.95rem; }

/* Crop cards */

.crop-grid { display: grid; grid-template-columns: repeat(3, minmax(0, 1fr)); gap: 24px; }

.crop-card { overflow: hidden; background: var(--surface); border: 1px solid var(--border); border-radius: var(--radius); box-shadow: var(--shadow); }

.crop-image { width: 100%; height: 220px; object-fit: cover; display: block; }

.crop-card-body { padding: 22px; }

.crop-card-body h3 { margin-bottom: 8px; }

.crop-card-body p { color: var(--muted); font-size: 0.94rem; }

/* Forms and sign-in page */

.auth-section { min-height: calc(100vh - 76px); display: grid; place-items: center; padding: 48px 20px; background: radial-gradient( circle at 10% 15%, rgba(185, 246, 202, 0.45), transparent 32% ), var(--background); }

.auth-card { width: 100%; max-width: 440px; padding: 36px; background: var(--surface); border: 1px solid var(--border); border-radius: 24px; box-shadow: 0 20px 60px rgba(24, 80, 48, 0.12); }

.auth-card h1 { font-size: 2rem; margin-bottom: 8px; }

.auth-subtitle { color: var(--muted); margin-bottom: 26px; }

.form-group { margin-bottom: 18px; }

.form-group label { display: block; font-weight: 650; margin-bottom: 8px; }

.form-control { width: 100%; min-height: 48px; padding: 12px 14px; color: var(--text); background: #fff; border: 1px solid #d6e4da; border-radius: 11px; outline: none; transition: border-color 0.2s ease, box-shadow 0.2s ease; }

.form-control:focus { border-color: var(--primary); box-shadow: 0 0 0 4px rgba(33, 140, 82, 0.12); }

.form-options { display: flex; justify-content: space-between; align-items: center; gap: 12px; margin: 6px 0 22px; font-size: 0.9rem; }

.form-options a, .auth-link { color: var(--primary); font-weight: 700; }

.auth-footer { text-align: center; color: var(--muted); margin-top: 22px; font-size: 0.92rem; }

/* Footer */

.footer { padding: 30px 0; background: #eff7f0; border-top: 1px solid var(--border); }

.footer-inner { display: flex; align-items: center; justify-content: space-between; flex-wrap: wrap; gap: 16px; color: var(--muted); font-size: 0.9rem; }

/* Accessibility */

button:focus-visible, a:focus-visible { outline: 3px solid #74c99a; outline-offset: 3px; }

@media (prefers-reduced-motion: reduce) { , ::before, *::after { scroll-behavior: auto !important; animation-duration: 0.01ms !important; animation-iteration-count: 1 !important; transition-duration: 0.01ms !important; } }

/* Responsive layout */

@media (max-width: 900px) { .nav-links { gap: 14px; }

.feature-grid, .crop-grid { grid-template-columns: repeat(2, minmax(0, 1fr)); }

.hero { min-height: 540px; } }

@media (max-width: 640px) { .navbar-inner { min-height: 68px; flex-wrap: wrap; padding: 12px 0; }

.logo { font-size: 1.05rem; }

.logo-icon { width: 36px; height: 36px; }

.nav-links { order: 3; width: 100%; justify-content: space-between; gap: 8px; overflow-x: auto; }

.nav-links a { white-space: nowrap; font-size: 0.82rem; }

.nav-actions .btn { min-height: 40px; padding: 8px 12px; font-size: 0.85rem; }

.hero { min-height: 520px; padding: 65px 0; }

.hero h1 { letter-spacing: -1px; }

.hero p { font-size: 1rem; }

.feature-grid, .crop-grid { grid-template-columns: 1fr; }

.section { padding: 58px 0; }

.auth-card { padding: 26px 20px; }

.footer-inner { flex-direction: column; align-items: flex-start; } }
