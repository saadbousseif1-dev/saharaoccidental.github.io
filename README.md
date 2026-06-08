# saharaoccidental.github.io
website about the Western Sahara question
<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Sahara Occidental — Comprendre un Conflit Oublié</title>
<meta name="description" content="Site éducatif et informatif sur le Sahara occidental : histoire, situation actuelle, enjeux géopolitiques et humanitaires.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;1,400&family=Source+Serif+4:opsz,wght@8..60,300;8..60,400;8..60,600&display=swap" rel="stylesheet">
<style>
:root {
  --ocre: #C8813A;
  --ocre-light: #E8A85A;
  --ocre-pale: #F5E6D0;
  --sand: #F0D9B5;
  --sand-deep: #D4B896;
  --sky: #2A6BA8;
  --sky-light: #4A8DC8;
  --sky-pale: #D8E8F5;
  --dusk: #8B6B4A;
  --earth: #5C4030;
  --night: #1A1410;
  --smoke: #6B5C4C;
  --parchment: #FAF5ED;
  --parchment2: #F2E9D8;
  --text: #2C1F10;
  --text-muted: #7A6050;
  --white: #FFFFFF;

  --font-display: 'Playfair Display', Georgia, serif;
  --font-body: 'Source Serif 4', Georgia, serif;
}

*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

html { scroll-behavior: smooth; }

body {
  font-family: var(--font-body);
  background: var(--parchment);
  color: var(--text);
  font-size: 17px;
  line-height: 1.75;
  overflow-x: hidden;
  transition: background 0.3s, color 0.3s;
}

body.dark {
  --parchment: #1C1410;
  --parchment2: #241A12;
  --text: #E8D8C0;
  --text-muted: #A89070;
  --sand: #3A2A1A;
  --ocre-pale: #2C1E10;
  --sky-pale: #0E1E30;
  --white: #1C1410;
}

/* NAV */
nav {
  position: fixed; top: 0; left: 0; right: 0; z-index: 1000;
  background: rgba(26, 20, 16, 0.96);
  backdrop-filter: blur(12px);
  border-bottom: 1px solid rgba(200, 129, 58, 0.3);
  padding: 0 2rem;
  height: 62px;
  display: flex; align-items: center; justify-content: space-between;
}
.nav-logo {
  font-family: var(--font-display);
  font-size: 1.1rem;
  color: var(--ocre-light);
  letter-spacing: 0.03em;
  text-decoration: none;
}
.nav-logo span { color: var(--sand-deep); font-style: italic; font-weight: 400; }
.nav-links {
  display: flex; gap: 1.5rem; list-style: none; align-items: center;
}
.nav-links a {
  color: rgba(240, 217, 181, 0.75);
  text-decoration: none;
  font-size: 0.82rem;
  font-family: var(--font-body);
  letter-spacing: 0.08em;
  text-transform: uppercase;
  transition: color 0.2s;
}
.nav-links a:hover { color: var(--ocre-light); }
.nav-actions { display: flex; gap: 0.75rem; align-items: center; }
.btn-dark, .btn-lang {
  background: none; border: 1px solid rgba(200, 129, 58, 0.4);
  color: var(--ocre-light); border-radius: 6px;
  padding: 5px 12px; font-size: 0.78rem; cursor: pointer;
  font-family: var(--font-body); letter-spacing: 0.05em;
  transition: all 0.2s;
}
.btn-dark:hover, .btn-lang:hover { background: rgba(200, 129, 58, 0.15); }
.hamburger {
  display: none; flex-direction: column; gap: 5px;
  background: none; border: none; cursor: pointer; padding: 4px;
}
.hamburger span { width: 22px; height: 1.5px; background: var(--ocre-light); display: block; transition: all 0.3s; }

/* HERO */
.hero {
  min-height: 100vh;
  background:
    linear-gradient(180deg, rgba(26,20,16,0.85) 0%, rgba(26,20,16,0.5) 40%, rgba(200,129,58,0.15) 80%, var(--parchment) 100%),
    url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='800' height='600'%3E%3Cdefs%3E%3CradialGradient id='g1' cx='30%25' cy='70%25' r='60%25'%3E%3Cstop offset='0%25' stop-color='%23C8813A' stop-opacity='.6'/%3E%3Cstop offset='100%25' stop-color='%231A1410' stop-opacity='1'/%3E%3C/radialGradient%3E%3CradialGradient id='g2' cx='70%25' cy='30%25' r='50%25'%3E%3Cstop offset='0%25' stop-color='%232A6BA8' stop-opacity='.4'/%3E%3Cstop offset='100%25' stop-color='transparent'/%3E%3C/radialGradient%3E%3C/defs%3E%3Crect width='800' height='600' fill='%231A1410'/%3E%3Crect width='800' height='600' fill='url(%23g1)'/%3E%3Crect width='800' height='600' fill='url(%23g2)'/%3E%3C/svg%3E") center/cover;
  display: flex; flex-direction: column; align-items: center; justify-content: center;
  text-align: center;
  padding: 7rem 2rem 4rem;
  position: relative;
}
.hero::before {
  content: '';
  position: absolute; inset: 0;
  background: repeating-linear-gradient(
    45deg, transparent, transparent 2px,
    rgba(200, 129, 58, 0.03) 2px, rgba(200, 129, 58, 0.03) 4px
  );
  pointer-events: none;
}
.hero-eyebrow {
  font-size: 0.75rem; letter-spacing: 0.2em; text-transform: uppercase;
  color: var(--ocre-light); margin-bottom: 1.2rem;
  display: flex; align-items: center; gap: 1rem;
}
.hero-eyebrow::before, .hero-eyebrow::after {
  content: ''; display: block; width: 40px; height: 1px; background: var(--ocre);
}
.hero h1 {
  font-family: var(--font-display);
  font-size: clamp(2.8rem, 7vw, 5.5rem);
  color: var(--parchment);
  line-height: 1.08;
  letter-spacing: -0.02em;
  margin-bottom: 0.5rem;
  max-width: 800px;
}
.hero h1 em { color: var(--ocre-light); font-style: italic; }
.hero-sub {
  font-size: 1.15rem; color: rgba(240, 217, 181, 0.75);
  max-width: 560px; margin: 1.5rem auto;
  font-weight: 300; line-height: 1.7;
}
.hero-ctas {
  display: flex; gap: 1rem; flex-wrap: wrap; justify-content: center;
  margin-top: 2.5rem;
}
.btn-primary {
  background: var(--ocre); color: var(--night);
  padding: 13px 28px; border: none; border-radius: 8px;
  font-family: var(--font-body); font-size: 0.9rem;
  letter-spacing: 0.06em; text-transform: uppercase;
  cursor: pointer; text-decoration: none;
  transition: all 0.25s; font-weight: 600;
}
.btn-primary:hover { background: var(--ocre-light); transform: translateY(-1px); }
.btn-outline {
  background: none; color: var(--parchment);
  padding: 12px 28px; border: 1px solid rgba(240,217,181,0.4); border-radius: 8px;
  font-family: var(--font-body); font-size: 0.9rem;
  letter-spacing: 0.06em; text-transform: uppercase;
  cursor: pointer; text-decoration: none;
  transition: all 0.25s;
}
.btn-outline:hover { border-color: var(--ocre-light); color: var(--ocre-light); }
.hero-stats {
  display: grid; grid-template-columns: repeat(3, 1fr);
  gap: 1.5rem; margin-top: 4rem; max-width: 700px; width: 100%;
}
.stat-box {
  background: rgba(26, 20, 16, 0.7);
  border: 1px solid rgba(200, 129, 58, 0.25);
  border-radius: 10px; padding: 1.2rem;
  backdrop-filter: blur(8px);
}
.stat-box .num {
  font-family: var(--font-display);
  font-size: 2rem; color: var(--ocre-light);
  display: block; line-height: 1;
}
.stat-box .label {
  font-size: 0.78rem; color: rgba(240,217,181,0.6);
  text-transform: uppercase; letter-spacing: 0.1em;
  display: block; margin-top: 0.3rem;
}
.scroll-hint {
  position: absolute; bottom: 2.5rem; left: 50%;
  transform: translateX(-50%);
  display: flex; flex-direction: column; align-items: center; gap: 0.4rem;
  color: rgba(200, 129, 58, 0.6); font-size: 0.72rem; letter-spacing: 0.12em; text-transform: uppercase;
  animation: bounce 2s ease-in-out infinite;
}
@keyframes bounce { 0%,100%{transform:translateX(-50%) translateY(0)} 50%{transform:translateX(-50%) translateY(6px)} }
.scroll-hint::after {
  content: ''; width: 1px; height: 30px;
  background: linear-gradient(to bottom, rgba(200,129,58,0.6), transparent);
}

/* SECTIONS */
main { padding-top: 0; }

section {
  padding: 6rem 2rem;
  max-width: 1100px; margin: 0 auto;
}
section.full-bleed { max-width: none; }

.section-eyebrow {
  font-size: 0.72rem; letter-spacing: 0.2em; text-transform: uppercase;
  color: var(--ocre); margin-bottom: 1rem;
  display: flex; align-items: center; gap: 0.75rem;
}
.section-eyebrow::after { content:''; flex: 1; max-width: 60px; height: 1px; background: var(--ocre); }

h2 {
  font-family: var(--font-display);
  font-size: clamp(1.9rem, 4vw, 2.8rem);
  color: var(--text); line-height: 1.15;
  letter-spacing: -0.02em; margin-bottom: 1.5rem;
}
h3 {
  font-family: var(--font-display);
  font-size: 1.35rem; margin-bottom: 0.8rem;
  color: var(--text);
}
p { margin-bottom: 1.2rem; color: var(--text-muted); }
p:last-child { margin-bottom: 0; }
strong { color: var(--text); font-weight: 600; }

/* INTRO BAND */
.intro-band {
  background: var(--parchment2);
  border-top: 1px solid var(--sand-deep);
  border-bottom: 1px solid var(--sand-deep);
  padding: 4rem 2rem;
}
.intro-grid {
  max-width: 1100px; margin: 0 auto;
  display: grid; grid-template-columns: 1fr 1fr 1fr;
  gap: 3rem;
}
.intro-card {
  position: relative; padding-left: 1.5rem;
  border-left: 3px solid var(--ocre);
}
.intro-card h3 { font-size: 1.1rem; margin-bottom: 0.5rem; }
.intro-card p { font-size: 0.9rem; }

/* TIMELINE */
.timeline-wrap {
  background: linear-gradient(135deg, var(--night) 0%, #2A1A0A 50%, #0E1E30 100%);
  padding: 5rem 2rem;
}
.timeline-inner { max-width: 900px; margin: 0 auto; }
.timeline-inner h2 { color: var(--sand); }
.timeline-inner .section-eyebrow { color: var(--ocre-light); }
.timeline-inner .section-eyebrow::after { background: var(--ocre-light); }

.timeline {
  position: relative;
  margin-top: 3rem;
}
.timeline::before {
  content: ''; position: absolute; left: 30px; top: 0; bottom: 0;
  width: 1px; background: linear-gradient(to bottom, var(--ocre), rgba(200,129,58,0.1));
}
.tl-item {
  display: flex; gap: 2rem; margin-bottom: 2.5rem;
  position: relative;
  cursor: pointer;
}
.tl-dot {
  width: 60px; min-width: 60px;
  display: flex; flex-direction: column; align-items: center;
  gap: 4px; position: relative; z-index: 1;
}
.tl-dot-circle {
  width: 18px; height: 18px; border-radius: 50%;
  background: var(--night); border: 2px solid var(--ocre);
  transition: all 0.25s;
}
.tl-item:hover .tl-dot-circle, .tl-item.active .tl-dot-circle {
  background: var(--ocre); box-shadow: 0 0 0 4px rgba(200,129,58,0.2);
}
.tl-year {
  font-size: 0.7rem; color: var(--ocre-light);
  font-family: var(--font-body);
  letter-spacing: 0.05em; text-align: center;
}
.tl-content {
  background: rgba(255,255,255,0.04);
  border: 1px solid rgba(200,129,58,0.15);
  border-radius: 10px; padding: 1.2rem 1.5rem;
  flex: 1; transition: all 0.25s;
}
.tl-item:hover .tl-content, .tl-item.active .tl-content {
  background: rgba(200,129,58,0.08);
  border-color: rgba(200,129,58,0.35);
}
.tl-content h4 {
  font-family: var(--font-display); font-size: 1.05rem;
  color: var(--sand); margin-bottom: 0.4rem;
}
.tl-content p { font-size: 0.88rem; color: rgba(240,217,181,0.65); margin: 0; }
.tl-tag {
  display: inline-block; font-size: 0.65rem; letter-spacing: 0.1em; text-transform: uppercase;
  background: rgba(200,129,58,0.2); color: var(--ocre-light);
  border-radius: 4px; padding: 2px 8px; margin-bottom: 0.5rem;
}

/* MAP SECTION */
.map-section {
  background: var(--parchment2);
  padding: 5rem 2rem;
  border-top: 1px solid var(--sand-deep);
  border-bottom: 1px solid var(--sand-deep);
}
.map-inner { max-width: 1100px; margin: 0 auto; display: grid; grid-template-columns: 1fr 380px; gap: 3rem; align-items: start; }
.map-container {
  background: var(--sky-pale);
  border-radius: 16px;
  border: 1px solid rgba(42, 107, 168, 0.2);
  overflow: hidden;
  aspect-ratio: 4/5;
  position: relative;
}
body.dark .map-container { background: #0A1520; }
.map-svg {
  width: 100%; height: 100%;
}
.map-legend { display: flex; flex-direction: column; gap: 1.5rem; }
.legend-item { display: flex; gap: 1rem; align-items: flex-start; }
.legend-color { width: 16px; height: 16px; border-radius: 4px; margin-top: 4px; flex-shrink: 0; }
.legend-color.morocco { background: rgba(200, 100, 50, 0.7); }
.legend-color.polisario { background: rgba(42, 107, 168, 0.7); }
.legend-color.buffer { background: rgba(150, 120, 80, 0.6); }
.legend-color.minurso { background: rgba(100, 180, 100, 0.7); }
.legend-item strong { font-size: 0.9rem; display: block; color: var(--text); }
.legend-item p { font-size: 0.82rem; margin: 0; }

/* ACTORS */
.actors-grid {
  display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 1.5rem; margin-top: 2.5rem;
}
.actor-card {
  background: var(--white);
  border: 1px solid var(--sand);
  border-radius: 12px; padding: 1.5rem;
  transition: all 0.25s;
  position: relative; overflow: hidden;
}
body.dark .actor-card { background: rgba(255,255,255,0.04); border-color: rgba(200,129,58,0.2); }
.actor-card::before {
  content: ''; position: absolute; top: 0; left: 0; right: 0; height: 3px;
}
.actor-card.morocco::before { background: linear-gradient(90deg, #e8a840, #c86030); }
.actor-card.polisario::before { background: linear-gradient(90deg, #2A6BA8, #3A9B78); }
.actor-card.spain::before { background: linear-gradient(90deg, #c8304a, #f0c020); }
.actor-card.un::before { background: linear-gradient(90deg, #3A6BA8, #2890D0); }
.actor-card.algeria::before { background: linear-gradient(90deg, #2A8040, #c8304a); }
.actor-card:hover { transform: translateY(-2px); box-shadow: 0 8px 24px rgba(0,0,0,0.08); }
.actor-card h3 { font-size: 1.05rem; margin-bottom: 0.4rem; }
.actor-tag {
  font-size: 0.68rem; letter-spacing: 0.1em; text-transform: uppercase;
  color: var(--ocre); margin-bottom: 0.75rem; display: block;
}
.actor-card p { font-size: 0.88rem; }

/* HUMAN SECTION */
.human-section { padding: 5rem 2rem; }
.human-inner { max-width: 1100px; margin: 0 auto; }
.human-grid {
  display: grid; grid-template-columns: 1fr 1fr;
  gap: 3rem; margin-top: 2.5rem; align-items: start;
}
.data-card {
  background: var(--parchment2);
  border-radius: 12px; padding: 1.8rem;
  border: 1px solid var(--sand-deep);
}
body.dark .data-card { background: rgba(255,255,255,0.04); border-color: rgba(200,129,58,0.15); }
.data-card h3 { font-size: 1rem; margin-bottom: 1rem; }
.data-row {
  display: flex; justify-content: space-between; align-items: baseline;
  padding: 0.7rem 0; border-bottom: 1px solid rgba(200, 129, 58, 0.1);
  font-size: 0.88rem;
}
.data-row:last-child { border-bottom: none; }
.data-row .val {
  font-family: var(--font-display); font-size: 1.25rem;
  color: var(--ocre); font-weight: 700;
}
.quote-block {
  background: linear-gradient(135deg, rgba(200,129,58,0.08), rgba(42,107,168,0.05));
  border-left: 4px solid var(--ocre);
  border-radius: 0 10px 10px 0; padding: 1.5rem 1.8rem;
  margin: 1.5rem 0;
}
.quote-block blockquote {
  font-family: var(--font-display); font-style: italic;
  font-size: 1.1rem; color: var(--text); line-height: 1.6; margin-bottom: 0.75rem;
}
.quote-source { font-size: 0.8rem; color: var(--text-muted); }

/* POSITIONS */
.positions-section {
  background: linear-gradient(135deg, #f0e6d0 0%, #e8d5b8 100%);
  padding: 5rem 2rem;
}
body.dark .positions-section { background: linear-gradient(135deg, #1c1410 0%, #241a0c 100%); }
.positions-inner { max-width: 1100px; margin: 0 auto; }
.positions-grid {
  display: grid; grid-template-columns: 1fr 1fr;
  gap: 2rem; margin-top: 2.5rem;
}
.position-card {
  background: rgba(255,255,255,0.7);
  backdrop-filter: blur(8px);
  border-radius: 12px; padding: 1.8rem;
  border: 1px solid rgba(200, 129, 58, 0.2);
}
body.dark .position-card { background: rgba(0,0,0,0.3); border-color: rgba(200,129,58,0.2); }
.position-card h3 { font-size: 1.05rem; color: var(--text); }
.position-tag {
  font-size: 0.68rem; letter-spacing: 0.1em; text-transform: uppercase;
  padding: 3px 10px; border-radius: 4px; margin-bottom: 0.75rem; display: inline-block;
}
.tag-orange { background: rgba(200,100,50,0.15); color: #b05020; }
.tag-blue { background: rgba(42,107,168,0.15); color: #1a5a98; }
.tag-green { background: rgba(58,155,120,0.15); color: #1a7850; }
.tag-gray { background: rgba(100,90,80,0.15); color: #5a504a; }
body.dark .tag-orange { background: rgba(200,100,50,0.25); color: #e87040; }
body.dark .tag-blue { background: rgba(42,107,168,0.25); color: #6aacf8; }
body.dark .tag-green { background: rgba(58,155,120,0.25); color: #5acba8; }
body.dark .tag-gray { background: rgba(150,140,130,0.15); color: #b0a898; }

/* RESOURCES */
.resources-section { padding: 5rem 2rem; }
.resources-inner { max-width: 1100px; margin: 0 auto; }
.resource-grid {
  display: grid; grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
  gap: 1.5rem; margin-top: 2.5rem;
}
.resource-card {
  background: var(--white);
  border: 1px solid var(--sand);
  border-radius: 10px; padding: 1.4rem;
  display: flex; flex-direction: column; gap: 0.75rem;
  transition: all 0.2s;
  cursor: pointer;
}
body.dark .resource-card { background: rgba(255,255,255,0.04); border-color: rgba(200,129,58,0.2); }
.resource-card:hover { border-color: var(--ocre); transform: translateY(-2px); }
.resource-type {
  font-size: 0.65rem; letter-spacing: 0.12em; text-transform: uppercase;
  color: var(--sky); padding: 3px 8px; background: var(--sky-pale);
  border-radius: 4px; display: inline-block; align-self: flex-start;
}
body.dark .resource-type { background: rgba(42,107,168,0.2); }
.resource-card h4 { font-family: var(--font-display); font-size: 0.95rem; color: var(--text); margin: 0; }
.resource-card p { font-size: 0.82rem; margin: 0; flex: 1; }
.resource-link { font-size: 0.78rem; color: var(--sky); }

/* FAQ */
.faq-section {
  background: var(--parchment2);
  border-top: 1px solid var(--sand-deep);
  padding: 5rem 2rem;
}
.faq-inner { max-width: 800px; margin: 0 auto; }
.faq-item {
  border-bottom: 1px solid var(--sand-deep);
  overflow: hidden;
}
.faq-q {
  width: 100%; text-align: left; background: none; border: none;
  padding: 1.2rem 0; cursor: pointer;
  display: flex; justify-content: space-between; align-items: center;
  gap: 1rem;
  font-family: var(--font-body); font-size: 0.95rem; font-weight: 600;
  color: var(--text); transition: color 0.2s;
}
.faq-q:hover { color: var(--ocre); }
.faq-icon { font-size: 1.2rem; color: var(--ocre); transition: transform 0.3s; flex-shrink: 0; }
.faq-item.open .faq-icon { transform: rotate(45deg); }
.faq-a {
  max-height: 0; overflow: hidden; transition: max-height 0.4s ease;
  font-size: 0.9rem; color: var(--text-muted); padding-bottom: 0;
}
.faq-item.open .faq-a { max-height: 300px; padding-bottom: 1.2rem; }

/* ACTION SECTION */
.action-section {
  background: linear-gradient(135deg, var(--night), #1A2A1A 40%, #0E1E30 100%);
  padding: 5rem 2rem;
}
.action-inner { max-width: 900px; margin: 0 auto; text-align: center; }
.action-inner h2 { color: var(--sand); }
.action-inner .section-eyebrow { color: var(--ocre-light); justify-content: center; }
.action-inner .section-eyebrow::after { display: none; }
.action-inner .section-eyebrow::before { content:''; display: block; width: 40px; height: 1px; background: var(--ocre); }
.action-inner p { color: rgba(240,217,181,0.7); max-width: 600px; margin: 0 auto 1.5rem; }
.orgs-grid {
  display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 1rem; margin: 2.5rem 0;
}
.org-card {
  background: rgba(255,255,255,0.06);
  border: 1px solid rgba(200,129,58,0.2);
  border-radius: 10px; padding: 1.2rem;
  text-align: left;
}
.org-card h4 { font-size: 0.9rem; color: var(--sand); margin-bottom: 0.4rem; }
.org-card p { font-size: 0.78rem; color: rgba(240,217,181,0.55); margin: 0; }
.newsletter-form {
  display: flex; gap: 0.75rem; max-width: 480px; margin: 2rem auto 0;
  flex-wrap: wrap; justify-content: center;
}
.newsletter-input {
  flex: 1; min-width: 240px;
  background: rgba(255,255,255,0.08); border: 1px solid rgba(200,129,58,0.3);
  color: var(--sand); border-radius: 8px; padding: 12px 16px;
  font-family: var(--font-body); font-size: 0.9rem;
  outline: none; transition: border-color 0.2s;
}
.newsletter-input::placeholder { color: rgba(240,217,181,0.4); }
.newsletter-input:focus { border-color: var(--ocre); }

/* FOOTER */
footer {
  background: var(--night);
  border-top: 1px solid rgba(200,129,58,0.2);
  padding: 3rem 2rem;
  text-align: center;
}
.footer-inner { max-width: 1100px; margin: 0 auto; }
.footer-logo {
  font-family: var(--font-display); font-size: 1.3rem;
  color: var(--ocre-light); margin-bottom: 0.75rem;
}
footer p { font-size: 0.8rem; color: rgba(240,217,181,0.4); }
.footer-note {
  margin-top: 1.5rem; padding-top: 1.5rem;
  border-top: 1px solid rgba(200,129,58,0.1);
  font-size: 0.75rem; color: rgba(240,217,181,0.3); line-height: 1.5;
}

/* SEARCH */
.search-bar-wrap {
  background: rgba(255,255,255,0.06); border: 1px solid rgba(200,129,58,0.2);
  border-radius: 10px; padding: 0.75rem 1rem;
  display: flex; align-items: center; gap: 0.75rem;
  max-width: 500px; margin: 2rem auto 0;
}
.search-bar-wrap input {
  background: none; border: none; color: var(--sand);
  font-family: var(--font-body); font-size: 0.9rem; outline: none; flex: 1;
}
.search-bar-wrap input::placeholder { color: rgba(240,217,181,0.4); }
.search-icon { font-size: 1rem; color: rgba(200,129,58,0.6); }

/* LANG BAR */
.lang-bar {
  display: flex; gap: 0.5rem; justify-content: center; margin-top: 1.5rem;
}
.lang-btn {
  background: none; border: 1px solid rgba(200,129,58,0.2);
  color: rgba(240,217,181,0.6); border-radius: 5px;
  padding: 4px 10px; font-size: 0.75rem; cursor: pointer;
  transition: all 0.2s; font-family: var(--font-body);
}
.lang-btn:hover, .lang-btn.active { background: rgba(200,129,58,0.15); color: var(--ocre-light); border-color: rgba(200,129,58,0.4); }

/* SEARCH HIGHLIGHT */
.search-result-highlight { background: rgba(200,129,58,0.2); border-radius: 3px; padding: 0 2px; }

/* NOTIFICATION */
.notif {
  position: fixed; bottom: 2rem; right: 2rem; z-index: 9999;
  background: var(--ocre); color: var(--night);
  border-radius: 10px; padding: 1rem 1.5rem;
  font-size: 0.9rem; font-weight: 600;
  transform: translateY(100px); opacity: 0;
  transition: all 0.4s; pointer-events: none;
}
.notif.show { transform: translateY(0); opacity: 1; }

/* MOBILE */
@media (max-width: 768px) {
  .nav-links { display: none; }
  .hamburger { display: flex; }
  .nav-links.open { display: flex; flex-direction: column; position: fixed; top: 62px; left: 0; right: 0; bottom: 0; background: rgba(26,20,16,0.98); padding: 2rem; z-index: 999; align-items: flex-start; gap: 1rem; }
  .nav-links.open a { font-size: 1.1rem; }
  .hero-stats { grid-template-columns: 1fr 1fr; }
  .hero-stats .stat-box:last-child { grid-column: span 2; }
  .intro-grid { grid-template-columns: 1fr; }
  .map-inner { grid-template-columns: 1fr; }
  .human-grid { grid-template-columns: 1fr; }
  .positions-grid { grid-template-columns: 1fr; }
  section { padding: 4rem 1.25rem; }
  .timeline::before { left: 24px; }
  .tl-dot { width: 48px; min-width: 48px; }
}
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <a class="nav-logo" href="#">Sahara <span>Occidental</span></a>
  <ul class="nav-links" id="navLinks">
    <li><a href="#histoire">Histoire</a></li>
    <li><a href="#situation">Situation</a></li>
    <li><a href="#acteurs">Acteurs</a></li>
    <li><a href="#humanitaire">Humanitaire</a></li>
    <li><a href="#positions">Positions</a></li>
    <li><a href="#ressources">Ressources</a></li>
    <li><a href="#agir">Agir</a></li>
  </ul>
  <div class="nav-actions">
    <button class="btn-lang" id="langToggle" title="Changer de langue">🌐 FR</button>
    <button class="btn-dark" id="darkToggle" title="Mode sombre/clair">☽ Nuit</button>
    <button class="hamburger" id="hamburger" aria-label="Menu">
      <span></span><span></span><span></span>
    </button>
  </div>
</nav>

<!-- HERO -->
<header class="hero" id="accueil">
  <div class="hero-eyebrow">Éducation &amp; Information</div>
  <h1>Comprendre le <em>Sahara Occidental</em></h1>
  <p class="hero-sub">Un territoire disputé depuis 50 ans au cœur de l'Afrique du Nord-Ouest. Entre aspirations nationales, diplomatie internationale et crise humanitaire.</p>
  <div class="hero-ctas">
    <a href="#histoire" class="btn-primary">Explorer l'histoire</a>
    <a href="#situation" class="btn-outline">Situation actuelle</a>
  </div>
  <div class="hero-stats">
    <div class="stat-box">
      <span class="num">266 000</span>
      <span class="label">km² de superficie</span>
    </div>
    <div class="stat-box">
      <span class="num">~170 000</span>
      <span class="label">réfugiés sahraouis</span>
    </div>
    <div class="stat-box">
      <span class="num">50 ans</span>
      <span class="label">de conflit non résolu</span>
    </div>
  </div>
  <div class="scroll-hint">Défiler</div>
</header>

<!-- INTRO BAND -->
<div class="intro-band">
  <div class="intro-grid">
    <div class="intro-card">
      <h3>Un territoire, deux administrations</h3>
      <p>Le Sahara occidental est divisé par un mur de sable de 2 700 km. Le Maroc administre environ 80 % du territoire ; le Front Polisario contrôle les zones orientales.</p>
    </div>
    <div class="intro-card">
      <h3>Un conflit gelé depuis 1991</h3>
      <p>Un cessez-le-feu a mis fin aux combats en 1991. Malgré des décennies de négociations sous l'égide de l'ONU, aucune solution politique définitive n'a été trouvée à ce jour.</p>
    </div>
    <div class="intro-card">
      <h3>Une question d'autodétermination</h3>
      <p>L'ONU considère le Sahara occidental comme un « territoire non autonome ». La résolution de son statut implique notamment la question d'un referendum d'autodétermination pour les populations sahraouies.</p>
    </div>
  </div>
</div>

<!-- TIMELINE -->
<div class="timeline-wrap" id="histoire">
  <div class="timeline-inner">
    <div class="section-eyebrow">Chronologie</div>
    <h2>Histoire du Sahara occidental</h2>
    <p style="color:rgba(240,217,181,0.65); max-width:600px; margin-bottom:0;">Des origines précoloniales à nos jours — cliquez sur chaque événement pour en savoir plus.</p>
    <div class="timeline">

      <div class="tl-item" onclick="expandTl(this)">
        <div class="tl-dot"><div class="tl-dot-circle"></div><div class="tl-year">Précoloniale</div></div>
        <div class="tl-content">
          <div class="tl-tag">Origines</div>
          <h4>Populations Sahraouies et organisation tribale</h4>
          <p>Le Sahara occidental est peuplé par des groupes nomades hassanophones, organisés en confédérations tribales (Reguibat, Oulad Delim, etc.) avec des pratiques pastorales et commerciales établies à travers le désert.</p>
        </div>
      </div>

      <div class="tl-item" onclick="expandTl(this)">
        <div class="tl-dot"><div class="tl-dot-circle"></div><div class="tl-year">1884–1934</div></div>
        <div class="tl-content">
          <div class="tl-tag">Colonisation</div>
          <h4>Colonisation espagnole</h4>
          <p>L'Espagne établit sa présence en 1884 à Villa Cisneros (actuelle Dakhla). La colonie, dénommée « Sahara espagnol », est officiellement constituée en 1934. La résistance des populations locales est réprimée lors de la bataille d'Anou Amar (1934).</p>
        </div>
      </div>

      <div class="tl-item" onclick="expandTl(this)">
        <div class="tl-dot"><div class="tl-dot-circle"></div><div class="tl-year">1973</div></div>
        <div class="tl-content">
          <div class="tl-tag">Fondation</div>
          <h4>Création du Front Polisario</h4>
          <p>Le Front Polisario (Front populaire de libération de la Saguia el-Hamra et du Rio de Oro) est fondé le 10 mai 1973 à Zouerate, en Mauritanie. Son objectif est l'indépendance du territoire par rapport à l'Espagne.</p>
        </div>
      </div>

      <div class="tl-item" onclick="expandTl(this)">
        <div class="tl-dot"><div class="tl-dot-circle"></div><div class="tl-year">1975</div></div>
        <div class="tl-content">
          <div class="tl-tag">Tournant</div>
          <h4>La Marche verte et les Accords de Madrid</h4>
          <p>Le 6 novembre 1975, le Maroc organise la « Marche verte » : 350 000 civils marocains entrent dans le territoire sous escorte militaire. Le 14 novembre 1975, les Accords de Madrid transfèrent l'administration du territoire au Maroc et à la Mauritanie. L'ONU conteste la légitimité juridique de ces accords.</p>
        </div>
      </div>

      <div class="tl-item" onclick="expandTl(this)">
        <div class="tl-dot"><div class="tl-dot-circle"></div><div class="tl-year">1976–1979</div></div>
        <div class="tl-content">
          <div class="tl-tag">Conflit armé</div>
          <h4>Guerre et proclamation de la RASD</h4>
          <p>Le 27 février 1976, le Front Polisario proclame la République arabe sahraouie démocratique (RASD). Des combats opposent le Polisario aux forces marocaines et mauritaniennes. En 1979, la Mauritanie signe la paix et renonce à sa partie du territoire, immédiatement annexée par le Maroc.</p>
        </div>
      </div>

      <div class="tl-item" onclick="expandTl(this)">
        <div class="tl-dot"><div class="tl-dot-circle"></div><div class="tl-year">1980–1987</div></div>
        <div class="tl-content">
          <div class="tl-tag">Infrastructure</div>
          <h4>Construction du « mur des sables »</h4>
          <p>Le Maroc construit progressivement un mur de défense de 2 700 km (berm), hérissé de mines et de postes militaires. Ce remblai de terre divise le territoire en deux zones et constitue encore aujourd'hui la ligne de démarcation de facto.</p>
        </div>
      </div>

      <div class="tl-item" onclick="expandTl(this)">
        <div class="tl-dot"><div class="tl-dot-circle"></div><div class="tl-year">1991</div></div>
        <div class="tl-content">
          <div class="tl-tag">Cessez-le-feu</div>
          <h4>Cessez-le-feu et déploiement de la MINURSO</h4>
          <p>L'ONU supervise un cessez-le-feu et déploie la MINURSO (Mission des Nations Unies pour l'Organisation d'un référendum au Sahara Occidental). Ce référendum d'autodétermination, prévu pour 1992, n'a jamais eu lieu en raison de désaccords persistants sur la liste des électeurs.</p>
        </div>
      </div>

      <div class="tl-item" onclick="expandTl(this)">
        <div class="tl-dot"><div class="tl-dot-circle"></div><div class="tl-year">2000–2019</div></div>
        <div class="tl-content">
          <div class="tl-tag">Diplomatie</div>
          <h4>Négociations sans issue</h4>
          <p>Plusieurs cycles de négociations ont lieu sous l'égide de l'ONU (Plan Baker I et II, rounds de Manhasset). Le Maroc propose une « autonomie élargie » sous sa souveraineté. Le Polisario maintient son exigence d'un référendum d'autodétermination incluant l'option d'indépendance.</p>
        </div>
      </div>

      <div class="tl-item" onclick="expandTl(this)">
        <div class="tl-dot"><div class="tl-dot-circle"></div><div class="tl-year">2020–2025</div></div>
        <div class="tl-content">
          <div class="tl-tag">Développements récents</div>
          <h4>Reprise des hostilités et reconnaissance américaine</h4>
          <p>En novembre 2020, le Front Polisario déclare la fin du cessez-le-feu. En décembre 2020, les États-Unis reconnaissent la souveraineté marocaine sur le territoire dans le cadre des Accords d'Abraham. Ces développements ont ravivé les tensions diplomatiques régionales.</p>
        </div>
      </div>

    </div>
  </div>
</div>

<!-- SITUATION / CARTE -->
<div class="map-section" id="situation">
  <div class="map-inner">
    <div>
      <div class="section-eyebrow">Géographie du conflit</div>
      <h2>Situation actuelle</h2>
      <p>Le territoire est divisé par un mur militaire. Le Maroc administre la majeure partie du territoire, y compris les grandes villes de Laâyoune et Dakhla. Le Front Polisario contrôle les territoires orientaux, appelés « zones libérées ».</p>

      <div class="map-container">
        <svg class="map-svg" viewBox="0 0 340 420" xmlns="http://www.w3.org/2000/svg">
          <!-- Background ocean -->
          <rect width="340" height="420" fill="#c8dff0"/>
          <!-- Mauritania background -->
          <rect x="100" y="220" width="240" height="200" fill="#e8dcc8"/>
          <!-- Algeria background (top right) -->
          <rect x="180" y="0" width="160" height="220" fill="#e0d4b8"/>
          <!-- Morocco (simplified territory) -->
          <rect x="0" y="0" width="180" height="100" fill="#c8c0a8"/>

          <!-- Western Sahara territory outline -->
          <path d="M 20 80 L 170 80 L 180 120 L 190 200 L 180 280 L 100 280 L 20 220 Z"
            fill="rgba(200,180,140,0.5)" stroke="#8a7a60" stroke-width="1.5"/>

          <!-- Moroccan controlled zone (west + north, ~80%) -->
          <path d="M 20 80 L 140 80 L 150 120 L 145 200 L 130 260 L 80 270 L 20 220 Z"
            fill="rgba(200, 100, 50, 0.45)" stroke="none"/>

          <!-- Polisario zone (east, ~20%) -->
          <path d="M 140 80 L 170 80 L 180 120 L 190 200 L 180 280 L 130 260 L 145 200 L 150 120 Z"
            fill="rgba(42, 107, 168, 0.45)" stroke="none"/>

          <!-- The Berm (wall) -->
          <path d="M 140 82 L 150 120 L 145 200 L 132 260"
            fill="none" stroke="#5a3a1a" stroke-width="2.5" stroke-dasharray="6 3"/>

          <!-- Atlantic coast line -->
          <path d="M 20 80 L 5 140 L 2 200 L 15 260 L 20 310"
            fill="none" stroke="#88aac8" stroke-width="1.5"/>

          <!-- Cities -->
          <circle cx="55" cy="110" r="6" fill="#c86030" stroke="white" stroke-width="1.5"/>
          <text x="65" y="115" font-size="10" fill="#4a2010" font-family="serif" font-style="italic">Laâyoune</text>

          <circle cx="60" cy="230" r="5" fill="#c86030" stroke="white" stroke-width="1.5"/>
          <text x="70" y="235" font-size="9" fill="#4a2010" font-family="serif" font-style="italic">Dakhla</text>

          <circle cx="160" cy="140" r="4" fill="#2A6BA8" stroke="white" stroke-width="1.5"/>
          <text x="168" y="145" font-size="8.5" fill="#0a3a68" font-family="serif" font-style="italic">Tifariti</text>

          <!-- Tindouf (Algeria) - refugee camps -->
          <circle cx="260" cy="90" r="5" fill="#3a9b78" stroke="white" stroke-width="1.5"/>
          <text x="268" y="95" font-size="9" fill="#1a5038" font-family="serif" font-style="italic">Tindouf</text>
          <text x="248" y="108" font-size="7.5" fill="#1a5038" font-family="serif">(camps)</text>

          <!-- MINURSO mission markers -->
          <rect x="85" y="155" width="22" height="14" rx="3" fill="rgba(100,180,100,0.8)" stroke="white" stroke-width="1"/>
          <text x="96" y="166" font-size="7" fill="white" text-anchor="middle" font-family="sans-serif" font-weight="bold">UN</text>

          <!-- Labels -->
          <text x="60" y="170" font-size="8" fill="rgba(180,80,30,0.8)" font-family="serif" text-anchor="middle">Zone marocaine</text>
          <text x="165" y="195" font-size="7.5" fill="rgba(20,60,130,0.8)" font-family="serif" text-anchor="middle">Zone</text>
          <text x="165" y="207" font-size="7.5" fill="rgba(20,60,130,0.8)" font-family="serif" text-anchor="middle">Polisario</text>

          <!-- Berm label -->
          <text x="105" y="108" font-size="7" fill="#5a3a1a" transform="rotate(-70 105 108)" font-family="sans-serif">Mur des sables</text>

          <!-- Atlantic label -->
          <text x="8" y="175" font-size="8.5" fill="#3878a8" font-family="sans-serif" transform="rotate(-90 8 175)">Océan Atlantique</text>

          <!-- Country labels -->
          <text x="230" y="50" font-size="9" fill="#6a5a40" font-family="sans-serif" font-style="italic">Algérie</text>
          <text x="200" y="340" font-size="9" fill="#6a5a40" font-family="sans-serif" font-style="italic">Mauritanie</text>
          <text x="40" y="40" font-size="9" fill="#6a5a40" font-family="sans-serif" font-style="italic">Maroc</text>

          <!-- North arrow -->
          <g transform="translate(305, 30)">
            <circle cx="0" cy="0" r="12" fill="rgba(255,255,255,0.8)" stroke="#8a7a60" stroke-width="0.5"/>
            <path d="M 0 -8 L 3 2 L 0 0 L -3 2 Z" fill="#4a3a20"/>
            <text x="0" y="16" font-size="8" fill="#4a3a20" text-anchor="middle" font-family="sans-serif">N</text>
          </g>
        </svg>
      </div>
    </div>

    <div class="map-legend">
      <h3>Légende</h3>
      <div class="legend-item">
        <div class="legend-color morocco"></div>
        <div>
          <strong>Zone sous administration marocaine</strong>
          <p>~80 % du territoire, dont les villes de Laâyoune (capitale) et Dakhla. Soumis au plan d'autonomie marocain.</p>
        </div>
      </div>
      <div class="legend-item">
        <div class="legend-color polisario"></div>
        <div>
          <strong>Territoire contrôlé par le Front Polisario</strong>
          <p>Zones libres peu peuplées à l'est du mur. La RASD y exerce une administration symbolique.</p>
        </div>
      </div>
      <div class="legend-item">
        <div class="legend-color buffer"></div>
        <div>
          <strong>Le mur des sables (Berm)</strong>
          <p>Ouvrage militaire de 2 700 km construit par le Maroc entre 1980 et 1987. Zone tampon minée.</p>
        </div>
      </div>
      <div class="legend-item">
        <div class="legend-color minurso"></div>
        <div>
          <strong>Présence de la MINURSO</strong>
          <p>Mission de l'ONU déployée depuis 1991. Surveille le cessez-le-feu, mais sans mandat pour les droits humains.</p>
        </div>
      </div>
      <div style="padding: 1rem; background: var(--ocre-pale); border-radius: 8px; border: 1px solid var(--sand-deep); margin-top: 0.5rem;">
        <p style="font-size: 0.8rem; margin:0;"><strong>Camps de Tindouf (Algérie)</strong><br>Les camps de réfugiés sont situés en territoire algérien, près de Tindouf. Ils accueillent entre 90 000 et 170 000 réfugiés sahraouis selon les sources.</p>
      </div>
    </div>
  </div>
</div>

<!-- ACTEURS -->
<section id="acteurs">
  <div class="section-eyebrow">Géopolitique</div>
  <h2>Les principaux acteurs</h2>
  <p style="max-width:680px;">Le conflit du Sahara occidental mobilise un réseau complexe d'acteurs aux intérêts divergents, à l'échelle régionale et internationale.</p>
  <div class="actors-grid">
    <div class="actor-card morocco">
      <span class="actor-tag">Partie principale</span>
      <h3>Royaume du Maroc</h3>
      <p>Le Maroc administre environ 80 % du territoire et le considère comme ses « provinces du Sud ». Il propose un plan d'autonomie élargie comme solution finale, rejetant l'option d'indépendance. Le Maroc jouit du soutien diplomatique de la France, de l'Espagne et, depuis 2020, des États-Unis.</p>
    </div>
    <div class="actor-card polisario">
      <span class="actor-tag">Partie principale</span>
      <h3>Front Polisario / RASD</h3>
      <p>Reconnu par l'ONU comme représentant du peuple sahraoui, le Front Polisario administre les camps de réfugiés à Tindouf (Algérie). Il exige un référendum d'autodétermination incluant l'option d'indépendance et bénéficie du soutien de l'Algérie et de nombreux pays africains et latinoaméricains.</p>
    </div>
    <div class="actor-card algeria">
      <span class="actor-tag">Acteur régional</span>
      <h3>Algérie</h3>
      <p>Principal soutien du Front Polisario, l'Algérie accueille les camps de réfugiés et fournit une aide humanitaire et diplomatique. La question du Sahara occidental est au cœur des tensions entre Alger et Rabat, qui ont rompu leurs relations diplomatiques en 2021.</p>
    </div>
    <div class="actor-card un">
      <span class="actor-tag">Médiateur international</span>
      <h3>Nations Unies (MINURSO)</h3>
      <p>Déployée depuis 1991, la MINURSO surveille le cessez-le-feu. Son mandat ne couvre pas le monitoring des droits humains — une exception notable parmi les missions de l'ONU, souvent critiquée par les ONG. Un Envoyé personnel du Secrétaire général conduit les négociations.</p>
    </div>
    <div class="actor-card spain">
      <span class="actor-tag">Ancienne puissance coloniale</span>
      <h3>Espagne</h3>
      <p>Ancienne puissance administrante, l'Espagne a rétrocédé le territoire en 1975 sans organiser de référendum. En 2022, le gouvernement espagnol a reconnu le plan d'autonomie marocain comme « base la plus sérieuse et réaliste », suscitant une vive polémique en Espagne et provoquant une crise diplomatique avec l'Algérie.</p>
    </div>
    <div class="actor-card" style="--color: #4a7a30;">
      <div style="position:absolute;top:0;left:0;right:0;height:3px;background:linear-gradient(90deg,#4a7a30,#2a5a80)"></div>
      <span class="actor-tag">Acteurs secondaires</span>
      <h3>Autres acteurs</h3>
      <p>La France bloque régulièrement les résolutions onusiennes défavorables au Maroc. Les États-Unis ont reconnu la souveraineté marocaine en 2020. L'Union africaine soutient le droit à l'autodétermination. L'Union européenne maintient des accords commerciaux avec le Maroc dont la portée au Sahara occidental est contestée devant la CJUE.</p>
    </div>
  </div>
</section>

<!-- HUMANITAIRE -->
<div class="human-section" id="humanitaire">
  <div class="human-inner">
    <div class="section-eyebrow">Dimension humaine</div>
    <h2>Conséquences humaines et sociales</h2>
    <div class="human-grid">
      <div>
        <p>Le conflit du Sahara occidental a entraîné l'un des exodes les moins médiatisés d'Afrique. Des dizaines de milliers de personnes ont fui les combats à partir de 1975–1976, se réfugiant dans les régions désertiques du sud-ouest algérien.</p>

        <div class="quote-block">
          <blockquote>« Les camps de Tindouf représentent l'une des situations de réfugiés les plus durables et les moins visibles du monde. Des générations entières sont nées et ont grandi dans ces camps. »</blockquote>
          <div class="quote-source">— Haut-Commissariat des Nations Unies pour les Réfugiés (HCR)</div>
        </div>

        <p>Dans les territoires administrés par le Maroc, des organisations de défense des droits humains, dont Amnesty International et Human Rights Watch, ont documenté des restrictions à la liberté d'expression et de réunion, ainsi que des allégations de mauvais traitements.</p>

        <div class="quote-block">
          <blockquote>« La situation des droits de l'homme au Sahara occidental reste une préoccupation grave, en particulier pour les défenseurs sahraouis et les journalistes indépendants. »</blockquote>
          <div class="quote-source">— Amnesty International, rapport annuel 2023</div>
        </div>
      </div>

      <div style="display:flex;flex-direction:column;gap:1.5rem;">
        <div class="data-card">
          <h3>Situation des réfugiés (Tindouf)</h3>
          <div class="data-row"><span>Population estimée</span><span class="val">90–170 k</span></div>
          <div class="data-row"><span>Durée du déplacement</span><span class="val">+50 ans</span></div>
          <div class="data-row"><span>Camps principaux</span><span class="val">5</span></div>
          <div class="data-row"><span>Taux d'alphabétisation</span><span class="val">~90 %</span></div>
          <div class="data-row"><span>Dépendance aide alimentaire</span><span class="val">>80 %</span></div>
        </div>

        <div class="data-card">
          <h3>Territoire administré par le Maroc</h3>
          <div class="data-row"><span>Population totale</span><span class="val">~600 000</span></div>
          <div class="data-row"><span>Principales villes</span><span class="val">Laâyoune, Dakhla</span></div>
          <div class="data-row"><span>Ressources phosphates</span><span class="val">2/3 réserves mondiales</span></div>
          <div class="data-row"><span>Ressources halieutiques</span><span class="val">Eaux très poissonneuses</span></div>
        </div>

        <div class="data-card">
          <h3>Enjeux des ressources naturelles</h3>
          <p style="font-size:0.85rem;">Le statut des ressources naturelles est au cœur des tensions. La Cour de justice de l'Union européenne a statué que les accords commerciaux UE-Maroc ne sauraient légalement s'appliquer au Sahara occidental sans le consentement de sa population.</p>
        </div>
      </div>
    </div>
  </div>
</div>

<!-- POSITIONS POLITIQUES -->
<div class="positions-section" id="positions">
  <div class="positions-inner">
    <div class="section-eyebrow">Analyse politique</div>
    <h2>Positions et débats</h2>
    <p style="max-width:680px;">Le statut final du Sahara occidental fait l'objet de positions irréconciliables, fondées sur des principes juridiques et politiques légitimes mais contradictoires.</p>
    <div class="positions-grid">
      <div class="position-card">
        <span class="position-tag tag-orange">Position marocaine</span>
        <h3>Autonomie sous souveraineté marocaine</h3>
        <p style="font-size:0.88rem;">Le Maroc propose un plan d'autonomie élargie (présenté à l'ONU en 2007), permettant aux populations du Sahara de s'autogouverner dans le cadre de la souveraineté marocaine. Rabat considère que le territoire fait partie intégrante du Maroc depuis le Moyen Âge. Cette position est soutenue par la France, les États-Unis et plusieurs pays arabes et africains.</p>
      </div>
      <div class="position-card">
        <span class="position-tag tag-blue">Position du Front Polisario</span>
        <h3>Référendum d'autodétermination</h3>
        <p style="font-size:0.88rem;">Le Front Polisario, soutenu par l'Algérie, réclame la tenue d'un référendum d'autodétermination incluant l'option d'indépendance totale. Il s'appuie sur les résolutions de l'ONU qualifiant le Sahara occidental de « territoire non autonome » et sur le droit des peuples à disposer d'eux-mêmes inscrit dans la Charte des Nations Unies.</p>
      </div>
      <div class="position-card">
        <span class="position-tag tag-green">Position onusienne</span>
        <h3>Solution négociée, juste et durable</h3>
        <p style="font-size:0.88rem;">L'ONU maintient que le statut final doit être décidé par les parties elles-mêmes, dans le respect du droit international et de la volonté des populations. Les résolutions successives du Conseil de sécurité réaffirment le droit à l'autodétermination tout en appelant à des négociations directes. La notion d'« autonomie réelle » est parfois évoquée comme base de compromis.</p>
      </div>
      <div class="position-card">
        <span class="position-tag tag-gray">Enjeux régionaux</span>
        <h3>Impacts sur l'intégration du Maghreb</h3>
        <p style="font-size:0.88rem;">Le conflit bloque la construction de l'Union du Maghreb arabe (UMA), dont les institutions sont gelées depuis 1994. La fermeture de la frontière algéro-marocaine, en vigueur depuis 1994, et la rupture des relations diplomatiques en 2021 limitent la coopération régionale. Des analystes soulignent que la résolution du conflit serait un catalyseur pour le développement économique régional.</p>
      </div>
    </div>

    <div style="margin-top:2.5rem; padding:1.8rem; background:rgba(255,255,255,0.5); border-radius:12px; border:1px solid rgba(200,129,58,0.2); max-width:700px;">
      <h3 style="font-size:1rem; margin-bottom:0.75rem;">Note éditoriale</h3>
      <p style="font-size:0.85rem; margin:0;">Ce site s'efforce de présenter les différentes positions de manière équilibrée et factuelle. Le conflit du Sahara occidental est une question politique sensible et complexe. Les positions présentées reflètent les arguments avancés par chaque partie et ne constituent pas une prise de position de la part des rédacteurs.</p>
    </div>
  </div>
</div>

<!-- RESOURCES -->
<section class="resources-section" id="ressources">
  <div class="section-eyebrow">Documentation</div>
  <h2>Ressources et documentation</h2>
  <p style="max-width:620px;">Sources vérifiées pour approfondir vos connaissances sur le Sahara occidental — rapports officiels, publications académiques et organisations de référence.</p>
  <div class="resource-grid">
    <div class="resource-card">
      <span class="resource-type">ONU</span>
      <h4>Résolutions du Conseil de sécurité</h4>
      <p>Les résolutions annuelles du Conseil de sécurité (depuis la résolution 690 de 1991) définissent le mandat de la MINURSO et l'état des négociations.</p>
      <span class="resource-link">→ un.org/securitycouncil</span>
    </div>
    <div class="resource-card">
      <span class="resource-type">ONU</span>
      <h4>Rapports du Secrétaire général</h4>
      <p>Rapports bi-annuels sur l'état du processus politique, de la situation sécuritaire et des conditions humanitaires dans les camps.</p>
      <span class="resource-link">→ un.org</span>
    </div>
    <div class="resource-card">
      <span class="resource-type">Droits humains</span>
      <h4>Human Rights Watch</h4>
      <p>Rapports annuels sur la situation des droits humains dans les territoires administrés par le Maroc et dans les camps de Tindouf.</p>
      <span class="resource-link">→ hrw.org</span>
    </div>
    <div class="resource-card">
      <span class="resource-type">Droits humains</span>
      <h4>Amnesty International</h4>
      <p>Suivi des cas de défenseurs des droits humains sahraouis et documentation des restrictions aux libertés fondamentales.</p>
      <span class="resource-link">→ amnesty.org</span>
    </div>
    <div class="resource-card">
      <span class="resource-type">Académique</span>
      <h4>Journal of North African Studies</h4>
      <p>Publication académique couvrant les enjeux politiques, historiques et sociaux du Maghreb, dont de nombreux articles sur le Sahara occidental.</p>
      <span class="resource-link">→ tandfonline.com</span>
    </div>
    <div class="resource-card">
      <span class="resource-type">Think tank</span>
      <h4>International Crisis Group</h4>
      <p>Analyses et recommandations de politique sur le conflit du Sahara occidental, avec des mises à jour régulières sur les développements diplomatiques.</p>
      <span class="resource-link">→ crisisgroup.org</span>
    </div>
    <div class="resource-card">
      <span class="resource-type">Humanitaire</span>
      <h4>HCR – UNHCR</h4>
      <p>Informations sur la situation des réfugiés sahraouis dans les camps de Tindouf, opérations d'aide et statistiques humanitaires.</p>
      <span class="resource-link">→ unhcr.org</span>
    </div>
    <div class="resource-card">
      <span class="resource-type">Humanitaire</span>
      <h4>PAM – Programme alimentaire mondial</h4>
      <p>Rapports sur les besoins alimentaires dans les camps et l'assistance humanitaire aux réfugiés sahraouis.</p>
      <span class="resource-link">→ wfp.org</span>
    </div>
  </div>
</section>

<!-- FAQ -->
<div class="faq-section">
  <div class="faq-inner">
    <div class="section-eyebrow">Questions fréquentes</div>
    <h2>FAQ</h2>
    <div id="faqList">
      <div class="faq-item">
        <button class="faq-q" onclick="toggleFaq(this)">Pourquoi le référendum de 1991 n'a-t-il jamais eu lieu ?<span class="faq-icon">+</span></button>
        <div class="faq-a"><p>Le référendum a été bloqué principalement par des désaccords sur la liste des électeurs. Le Maroc souhaitait inclure les colons marocains installés dans le territoire depuis 1975, tandis que le Front Polisario réclamait que seuls les Sahraouis du recensement espagnol de 1974 et leurs descendants directs puissent voter. Ces positions irréconciliables ont conduit à l'abandon du projet par l'ONU en 2004.</p></div>
      </div>
      <div class="faq-item">
        <button class="faq-q" onclick="toggleFaq(this)">Combien de pays reconnaissent la RASD ?<span class="faq-icon">+</span></button>
        <div class="faq-a"><p>La République arabe sahraouie démocratique (RASD) est reconnue par environ 45 à 50 États, principalement en Afrique subsaharienne et en Amérique latine. Elle est membre de l'Union africaine depuis 1982, ce qui avait provoqué le retrait temporaire du Maroc de l'organisation. Aucun membre permanent du Conseil de sécurité de l'ONU ne reconnaît la RASD.</p></div>
      </div>
      <div class="faq-item">
        <button class="faq-q" onclick="toggleFaq(this)">Quelle est l'importance économique du territoire ?<span class="faq-icon">+</span></button>
        <div class="faq-a"><p>Le Sahara occidental possède d'importantes ressources naturelles : les gisements de phosphates de Bou Craa sont parmi les plus riches au monde, et les eaux atlantiques adjacentes comptent parmi les plus poissonneuses d'Afrique. Des ressources potentielles en hydrocarbures off-shore sont également évoquées. L'exploitation de ces ressources dans le contexte d'un statut non résolu est juridiquement et éthiquement contestée.</p></div>
      </div>
      <div class="faq-item">
        <button class="faq-q" onclick="toggleFaq(this)">Quelles sont les conditions de vie dans les camps de Tindouf ?<span class="faq-icon">+</span></button>
        <div class="faq-a"><p>Les camps de Tindouf (Smara, Laâyoune, Dakhla, Ausserd et Rabuni) se trouvent dans une zone désertique inhospitalière du sud-ouest algérien. La population est fortement dépendante de l'aide humanitaire internationale pour l'alimentation. Paradoxalement, le taux d'alphabétisation y est relativement élevé grâce à l'investissement dans l'éducation. Les réfugiés n'ont pas le droit de travailler formellement en Algérie et subissent des conditions climatiques extrêmes.</p></div>
      </div>
      <div class="faq-item">
        <button class="faq-q" onclick="toggleFaq(this)">Que signifie la reconnaissance américaine de 2020 ?<span class="faq-icon">+</span></button>
        <div class="faq-a"><p>En décembre 2020, l'administration Trump a reconnu la souveraineté marocaine sur le Sahara occidental dans le cadre des Accords d'Abraham (normalisation des relations Maroc-Israël). Cette décision a été maintenue par l'administration Biden. Elle représente un changement significatif dans la politique américaine, mais n'a pas modifié la position de l'ONU, qui continue de considérer le territoire comme non autonome.</p></div>
      </div>
    </div>
  </div>
</div>

<!-- ACTION -->
<div class="action-section" id="agir">
  <div class="action-inner">
    <div class="section-eyebrow">S'engager</div>
    <h2>Agir et s'informer</h2>
    <p>Plusieurs organisations œuvrent pour la défense des droits humains, l'aide humanitaire et la résolution politique du conflit du Sahara occidental.</p>

    <div class="orgs-grid">
      <div class="org-card">
        <h4>ARSO</h4>
        <p>Association de référence sur les ressources documentaires en ligne liées au Sahara occidental.</p>
      </div>
      <div class="org-card">
        <h4>Western Sahara Resource Watch</h4>
        <p>Surveillance de l'exploitation des ressources naturelles du territoire.</p>
      </div>
      <div class="org-card">
        <h4>ASVDH</h4>
        <p>Association sahraouie des victimes de violations graves des droits de l'homme — défense des droits humains sur place.</p>
      </div>
      <div class="org-card">
        <h4>Comité pour la liberté au Sahara Occidental</h4>
        <p>Sensibilisation internationale et soutien aux prisonniers politiques sahraouis.</p>
      </div>
    </div>

    <p>Pour rester informé des derniers développements politiques et humanitaires :</p>

    <div class="lang-bar">
      <button class="lang-btn active" onclick="setLang('fr', this)">Français</button>
      <button class="lang-btn" onclick="setLang('en', this)">English</button>
      <button class="lang-btn" onclick="setLang('es', this)">Español</button>
      <button class="lang-btn" onclick="setLang('ar', this)">العربية</button>
    </div>

    <div class="newsletter-form">
      <input class="newsletter-input" type="email" placeholder="votre@email.com" id="emailInput">
      <button class="btn-primary" onclick="subscribe()">S'abonner</button>
    </div>

    <div class="search-bar-wrap">
      <span class="search-icon">🔍</span>
      <input type="text" placeholder="Rechercher dans le site…" id="searchInput" oninput="handleSearch(this.value)">
    </div>
    <div id="searchResults" style="margin-top:1rem;font-size:0.85rem;color:rgba(240,217,181,0.7);"></div>
  </div>
</div>

<!-- FOOTER -->
<footer>
  <div class="footer-inner">
    <div class="footer-logo">Sahara Occidental</div>
    <p>Site éducatif et informatif — Information neutre, rigoureuse et factuelle</p>
    <div class="footer-note">
      Ce site est une ressource éducative indépendante. Il ne représente pas les positions du gouvernement marocain, du Front Polisario, de l'Algérie, de l'ONU ou de toute autre entité officielle. Les informations présentées s'appuient sur des sources vérifiables et sont mises à jour régulièrement. Des erreurs ou omissions peuvent exister — tout signalement est bienvenu.<br><br>
      © 2025 · Contenu sous licence Creative Commons Attribution 4.0 · Sources disponibles sur demande
    </div>
  </div>
</footer>

<!-- NOTIFICATION -->
<div class="notif" id="notif"></div>

<script>
// Dark mode
const darkToggle = document.getElementById('darkToggle');
const body = document.body;
let dark = false;
darkToggle.onclick = () => {
  dark = !dark;
  body.classList.toggle('dark', dark);
  darkToggle.textContent = dark ? '☀ Jour' : '☽ Nuit';
};

// Hamburger
const hamburger = document.getElementById('hamburger');
const navLinks = document.getElementById('navLinks');
hamburger.onclick = () => navLinks.classList.toggle('open');
navLinks.querySelectorAll('a').forEach(a => a.addEventListener('click', () => navLinks.classList.remove('open')));

// Timeline expand
function expandTl(el) {
  const wasActive = el.classList.contains('active');
  document.querySelectorAll('.tl-item').forEach(i => i.classList.remove('active'));
  if (!wasActive) el.classList.add('active');
}

// FAQ
function toggleFaq(btn) {
  const item = btn.closest('.faq-item');
  const isOpen = item.classList.contains('open');
  document.querySelectorAll('.faq-item').forEach(i => i.classList.remove('open'));
  if (!isOpen) item.classList.add('open');
}

// Notification
function showNotif(msg) {
  const n = document.getElementById('notif');
  n.textContent = msg;
  n.classList.add('show');
  setTimeout(() => n.classList.remove('show'), 3000);
}

// Newsletter
function subscribe() {
  const v = document.getElementById('emailInput').value;
  if (v && v.includes('@')) {
    showNotif('✓ Inscription enregistrée !');
    document.getElementById('emailInput').value = '';
  } else {
    showNotif('Veuillez entrer un email valide.');
  }
}

// Language switcher
const langMessages = {
  fr: 'Langue : Français',
  en: 'Language: English — Full translation coming soon.',
  es: 'Idioma: Español — Traducción completa próximamente.',
  ar: 'اللغة: العربية — الترجمة الكاملة قريباً'
};
function setLang(lang, btn) {
  document.querySelectorAll('.lang-btn').forEach(b => b.classList.remove('active'));
  btn.classList.add('active');
  document.getElementById('langToggle').textContent = '🌐 ' + lang.toUpperCase();
  showNotif(langMessages[lang]);
}

// Simple search
const searchableContent = [
  { term: 'marche verte', section: '#histoire', label: 'La Marche verte (1975) — Section Histoire' },
  { term: 'maroc', section: '#acteurs', label: 'Royaume du Maroc — Section Acteurs' },
  { term: 'polisario', section: '#acteurs', label: 'Front Polisario — Section Acteurs' },
  { term: 'réfugiés', section: '#humanitaire', label: 'Camps de réfugiés — Section Humanitaire' },
  { term: 'tindouf', section: '#humanitaire', label: 'Camps de Tindouf — Section Humanitaire' },
  { term: 'minurso', section: '#situation', label: 'Mission MINURSO — Situation actuelle' },
  { term: 'référendum', section: '#positions', label: 'Référendum d\'autodétermination — Positions' },
  { term: 'phosphates', section: '#humanitaire', label: 'Ressources naturelles — Section Humanitaire' },
  { term: 'algérie', section: '#acteurs', label: 'Algérie — Section Acteurs' },
  { term: 'autonomie', section: '#positions', label: 'Plan d\'autonomie — Section Positions' },
  { term: 'cessez-le-feu', section: '#histoire', label: 'Cessez-le-feu 1991 — Section Histoire' },
  { term: 'espagne', section: '#acteurs', label: 'Espagne — Section Acteurs' },
  { term: 'berm', section: '#situation', label: 'Mur des sables — Situation actuelle' },
  { term: 'rasd', section: '#histoire', label: 'RASD — Section Histoire' },
];
function handleSearch(val) {
  const res = document.getElementById('searchResults');
  if (!val || val.length < 2) { res.innerHTML = ''; return; }
  const matches = searchableContent.filter(s => s.term.includes(val.toLowerCase()));
  if (!matches.length) { res.innerHTML = '<span style="color:rgba(240,217,181,0.4)">Aucun résultat trouvé.</span>'; return; }
  res.innerHTML = matches.slice(0, 5).map(m =>
    `<div style="padding:6px 0;border-bottom:1px solid rgba(200,129,58,0.1)">
      <a href="${m.section}" style="color:var(--ocre-light);text-decoration:none;">${m.label}</a>
    </div>`
  ).join('');
}

// Smooth nav highlight on scroll
const sections = document.querySelectorAll('[id]');
window.addEventListener('scroll', () => {
  let current = '';
  sections.forEach(s => { if (window.scrollY >= s.offsetTop - 120) current = s.id; });
  document.querySelectorAll('.nav-links a').forEach(a => {
    a.style.color = a.getAttribute('href') === '#' + current ? 'var(--ocre-light)' : '';
  });
});

// Open first timeline item
document.querySelector('.tl-item').classList.add('active');
</script>
</body>
</html>
