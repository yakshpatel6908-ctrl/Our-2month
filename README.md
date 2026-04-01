[our-2months.html](https://github.com/user-attachments/files/26397401/our-2months.html)[Uploading our-2mont<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>2 Months of Us! 🎉</title>
<link href="https://fonts.googleapis.com/css2?family=Fredoka+One&family=Nunito:wght@400;600;700;800&family=Pacifico&display=swap" rel="stylesheet">
<style>
  :root {
    --pink: #FF6B9D;
    --yellow: #FFD93D;
    --mint: #6BCFB5;
    --purple: #C77DFF;
    --coral: #FF8552;
    --blue: #4CC9F0;
    --dark: #2D2D44;
    --cream: #FFF8F0;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    font-family: 'Nunito', sans-serif;
    background: var(--cream);
    overflow-x: hidden;
    cursor: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='32' height='32' viewBox='0 0 32 32'%3E%3Ctext y='28' font-size='28'%3E❤️%3C/text%3E%3C/svg%3E") 16 16, auto;
  }

  /* ========= CONFETTI ========= */
  .confetti-container {
    position: fixed; top: 0; left: 0; width: 100%; height: 100%;
    pointer-events: none; z-index: 999; overflow: hidden;
  }
  .confetti-piece {
    position: absolute; width: 12px; height: 12px; top: -20px;
    animation: confetti-fall linear infinite;
    border-radius: 2px;
  }
  @keyframes confetti-fall {
    0% { transform: translateY(-20px) rotate(0deg); opacity: 1; }
    100% { transform: translateY(110vh) rotate(720deg); opacity: 0; }
  }

  /* ========= HERO ========= */
  .hero {
    min-height: 100vh;
    background: linear-gradient(135deg, #FFE0EC 0%, #FFF3C4 50%, #E0F7FA 100%);
    display: flex; flex-direction: column; align-items: center; justify-content: center;
    position: relative; overflow: hidden; padding: 40px 20px;
  }
  .hero::before {
    content: '';
    position: absolute; inset: 0;
    background: radial-gradient(circle at 20% 80%, rgba(255,107,157,0.15) 0%, transparent 50%),
                radial-gradient(circle at 80% 20%, rgba(199,125,255,0.15) 0%, transparent 50%);
  }

  /* Floating doodles */
  .doodle {
    position: absolute;
    animation: float 3s ease-in-out infinite alternate;
    font-size: 2.5rem;
    user-select: none;
  }
  @keyframes float {
    0% { transform: translateY(0) rotate(-5deg); }
    100% { transform: translateY(-20px) rotate(5deg); }
  }

  .badge {
    background: var(--pink);
    color: white;
    font-family: 'Fredoka One', cursive;
    font-size: 1.1rem;
    padding: 8px 24px;
    border-radius: 50px;
    letter-spacing: 2px;
    text-transform: uppercase;
    box-shadow: 4px 4px 0 rgba(0,0,0,0.15);
    animation: wiggle 2s ease-in-out infinite;
    margin-bottom: 20px;
  }
  @keyframes wiggle {
    0%,100% { transform: rotate(-2deg); }
    50% { transform: rotate(2deg); }
  }

  .hero h1 {
    font-family: 'Pacifico', cursive;
    font-size: clamp(2.5rem, 8vw, 5.5rem);
    color: var(--dark);
    text-align: center;
    line-height: 1.2;
    position: relative;
    z-index: 1;
  }
  .hero h1 span {
    color: var(--pink);
    display: inline-block;
    animation: bounce-text 1s ease-in-out infinite alternate;
  }
  @keyframes bounce-text {
    0% { transform: translateY(0) scale(1); }
    100% { transform: translateY(-10px) scale(1.05); }
  }

  .subtitle {
    font-family: 'Fredoka One', cursive;
    font-size: clamp(1rem, 3vw, 1.5rem);
    color: #666;
    text-align: center;
    margin-top: 16px;
    max-width: 500px;
    position: relative; z-index: 1;
  }

  /* Heart pulse */
  .big-heart {
    font-size: clamp(5rem, 15vw, 10rem);
    animation: heartbeat 1.2s ease-in-out infinite;
    display: block;
    text-align: center;
    margin: 24px 0;
    filter: drop-shadow(0 8px 20px rgba(255,107,157,0.4));
    position: relative; z-index: 1;
  }
  @keyframes heartbeat {
    0%,100% { transform: scale(1); }
    14% { transform: scale(1.15); }
    28% { transform: scale(1); }
    42% { transform: scale(1.1); }
    70% { transform: scale(1); }
  }

  .scroll-hint {
    margin-top: 40px;
    font-size: 1rem;
    color: #aaa;
    font-weight: 700;
    animation: bounce-down 1.5s ease-in-out infinite;
    z-index: 1; position: relative;
  }
  @keyframes bounce-down {
    0%,100% { transform: translateY(0); }
    50% { transform: translateY(10px); }
  }

  /* ========= SECTIONS ========= */
  section { padding: 80px 20px; }

  .section-title {
    font-family: 'Pacifico', cursive;
    font-size: clamp(1.8rem, 5vw, 3rem);
    text-align: center;
    color: var(--dark);
    margin-bottom: 50px;
    position: relative;
  }
  .section-title::after {
    content: '';
    display: block;
    width: 80px; height: 6px;
    background: var(--pink);
    border-radius: 3px;
    margin: 12px auto 0;
  }

  /* ========= STATS ========= */
  .stats-section {
    background: var(--dark);
    clip-path: polygon(0 5%, 100% 0, 100% 95%, 0 100%);
    padding: 100px 20px;
  }
  .stats-section .section-title { color: white; }
  .stats-section .section-title::after { background: var(--yellow); }

  .stats-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 24px;
    max-width: 900px;
    margin: 0 auto;
  }
  .stat-card {
    background: white;
    border-radius: 20px;
    padding: 30px 20px;
    text-align: center;
    box-shadow: 6px 6px 0 var(--yellow);
    transform: rotate(-1deg);
    transition: all 0.3s ease;
    position: relative; overflow: hidden;
  }
  .stat-card:nth-child(2) { transform: rotate(1deg); }
  .stat-card:nth-child(3) { transform: rotate(-0.5deg); }
  .stat-card:nth-child(4) { transform: rotate(1.5deg); }
  .stat-card:hover {
    transform: rotate(0) translateY(-8px) scale(1.03);
    box-shadow: 8px 8px 0 var(--pink);
  }
  .stat-number {
    font-family: 'Fredoka One', cursive;
    font-size: 3rem;
    color: var(--pink);
    line-height: 1;
  }
  .stat-label {
    font-size: 0.95rem;
    color: #666;
    font-weight: 700;
    margin-top: 8px;
  }
  .stat-emoji { font-size: 2rem; margin-bottom: 10px; display: block; }

  /* ========= REASONS ========= */
  .reasons-section { background: linear-gradient(135deg, #FFF0F5, #F0F8FF); }

  .reasons-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
    gap: 28px;
    max-width: 1000px;
    margin: 0 auto;
  }
  .reason-card {
    background: white;
    border-radius: 24px;
    padding: 32px 24px;
    border: 3px solid transparent;
    box-shadow: 0 8px 30px rgba(0,0,0,0.07);
    transition: all 0.4s cubic-bezier(0.34,1.56,0.64,1);
    position: relative; overflow: hidden;
  }
  .reason-card::before {
    content: '';
    position: absolute; top: 0; left: 0; right: 0; height: 6px;
    border-radius: 24px 24px 0 0;
  }
  .reason-card:nth-child(1)::before { background: var(--pink); }
  .reason-card:nth-child(2)::before { background: var(--yellow); }
  .reason-card:nth-child(3)::before { background: var(--mint); }
  .reason-card:nth-child(4)::before { background: var(--purple); }
  .reason-card:nth-child(5)::before { background: var(--coral); }
  .reason-card:nth-child(6)::before { background: var(--blue); }
  .reason-card:hover {
    transform: translateY(-12px) rotate(1deg);
    box-shadow: 0 20px 50px rgba(255,107,157,0.2);
    border-color: var(--pink);
  }
  .reason-icon { font-size: 3rem; margin-bottom: 16px; display: block; }
  .reason-title {
    font-family: 'Fredoka One', cursive;
    font-size: 1.3rem;
    color: var(--dark);
    margin-bottom: 10px;
  }
  .reason-text {
    color: #777;
    font-size: 0.95rem;
    line-height: 1.6;
    font-weight: 600;
  }

  /* ========= TIMELINE ========= */
  .timeline-section { background: white; }

  .timeline {
    max-width: 700px;
    margin: 0 auto;
    position: relative;
  }
  .timeline::before {
    content: '';
    position: absolute; left: 50%; top: 0; bottom: 0;
    width: 4px;
    background: repeating-linear-gradient(to bottom, var(--pink) 0, var(--pink) 10px, transparent 10px, transparent 20px);
    transform: translateX(-50%);
  }
  .timeline-item {
    display: flex;
    align-items: center;
    margin-bottom: 40px;
    position: relative;
  }
  .timeline-item:nth-child(odd) { flex-direction: row-reverse; }
  .timeline-content {
    width: 44%;
    background: white;
    border-radius: 18px;
    padding: 22px 20px;
    box-shadow: 4px 4px 0 var(--pink);
    border: 2px solid var(--pink);
    font-weight: 700;
    color: var(--dark);
    font-size: 0.95rem;
    line-height: 1.5;
    position: relative;
  }
  .timeline-item:nth-child(odd) .timeline-content { box-shadow: -4px 4px 0 var(--purple); border-color: var(--purple); }
  .timeline-dot {
    width: 12%;
    display: flex; align-items: center; justify-content: center;
    flex-shrink: 0;
  }
  .timeline-dot span {
    width: 50px; height: 50px;
    background: var(--yellow);
    border-radius: 50%;
    display: flex; align-items: center; justify-content: center;
    font-size: 1.5rem;
    border: 4px solid white;
    box-shadow: 0 4px 12px rgba(0,0,0,0.15);
    animation: pulse-dot 2s ease-in-out infinite;
  }
  @keyframes pulse-dot {
    0%,100% { transform: scale(1); }
    50% { transform: scale(1.15); }
  }
  .timeline-date {
    font-family: 'Fredoka One', cursive;
    font-size: 0.85rem;
    color: var(--pink);
    margin-bottom: 6px;
  }

  /* ========= FUNNY METER ========= */
  .meter-section { background: linear-gradient(135deg, #FFF9E6, #FFF0F5); }

  .meter-cards {
    display: flex;
    flex-direction: column;
    gap: 20px;
    max-width: 700px;
    margin: 0 auto;
  }
  .meter-item { background: white; border-radius: 16px; padding: 20px 24px; box-shadow: 0 4px 20px rgba(0,0,0,0.06); }
  .meter-label {
    font-family: 'Fredoka One', cursive;
    font-size: 1.1rem;
    color: var(--dark);
    margin-bottom: 10px;
    display: flex; justify-content: space-between;
  }
  .meter-label span { color: #aaa; font-size: 0.9rem; }
  .meter-bar {
    height: 18px;
    background: #f0f0f0;
    border-radius: 50px;
    overflow: hidden;
  }
  .meter-fill {
    height: 100%;
    border-radius: 50px;
    animation: fill-bar 2s cubic-bezier(0.34,1.56,0.64,1) forwards;
    width: 0;
  }
  @keyframes fill-bar {
    to { width: var(--target-width); }
  }

  /* ========= LOVE LETTER ========= */
  .letter-section {
    background: var(--dark);
    clip-path: polygon(0 0, 100% 5%, 100% 100%, 0 95%);
    padding: 120px 20px;
  }
  .letter-card {
    max-width: 680px;
    margin: 0 auto;
    background: #FFF8F0;
    border-radius: 24px;
    padding: 50px 40px;
    box-shadow: 10px 10px 0 var(--yellow);
    position: relative;
    border: 3px dashed var(--pink);
  }
  .letter-card::before {
    content: '💌';
    position: absolute; top: -25px; left: 50%; transform: translateX(-50%);
    font-size: 3rem;
    filter: drop-shadow(0 4px 8px rgba(0,0,0,0.2));
  }
  .letter-text {
    font-family: 'Nunito', sans-serif;
    font-size: 1.05rem;
    line-height: 1.9;
    color: var(--dark);
    font-weight: 600;
  }
  .letter-text p { margin-bottom: 16px; }
  .letter-signature {
    font-family: 'Pacifico', cursive;
    font-size: 1.5rem;
    color: var(--pink);
    text-align: right;
    margin-top: 30px;
  }

  /* ========= FINALE ========= */
  .finale {
    background: linear-gradient(135deg, #FFE0EC, #FFF3C4, #E0F7FA);
    text-align: center;
    padding: 100px 20px;
    position: relative; overflow: hidden;
  }
  .finale h2 {
    font-family: 'Pacifico', cursive;
    font-size: clamp(2rem, 7vw, 4.5rem);
    color: var(--dark);
    margin-bottom: 20px;
  }
  .finale p {
    font-size: 1.2rem;
    color: #666;
    font-weight: 700;
    max-width: 500px;
    margin: 0 auto 40px;
  }
  .btn-love {
    display: inline-block;
    background: var(--pink);
    color: white;
    font-family: 'Fredoka One', cursive;
    font-size: 1.4rem;
    padding: 18px 50px;
    border-radius: 50px;
    border: none;
    cursor: pointer;
    box-shadow: 6px 6px 0 rgba(0,0,0,0.2);
    transition: all 0.2s;
    text-decoration: none;
    letter-spacing: 1px;
  }
  .btn-love:hover {
    transform: translateY(-4px) scale(1.05);
    box-shadow: 8px 10px 0 rgba(0,0,0,0.2);
  }
  .btn-love:active { transform: translateY(2px); box-shadow: 3px 3px 0 rgba(0,0,0,0.2); }

  /* Hearts rain */
  .hearts-rain { position: absolute; top: 0; left: 0; width: 100%; height: 100%; pointer-events: none; z-index: 0; }
  .heart-drop {
    position: absolute;
    font-size: 1.5rem;
    animation: rain-fall linear infinite;
    opacity: 0.4;
  }
  @keyframes rain-fall {
    0% { transform: translateY(-50px) rotate(0); opacity: 0; }
    10% { opacity: 0.4; }
    90% { opacity: 0.3; }
    100% { transform: translateY(100vh) rotate(360deg); opacity: 0; }
  }

  /* ========= POPUP ========= */
  .popup-overlay {
    display: none;
    position: fixed; inset: 0;
    background: rgba(0,0,0,0.6);
    z-index: 9999;
    align-items: center; justify-content: center;
  }
  .popup-overlay.active { display: flex; }
  .popup-box {
    background: white;
    border-radius: 28px;
    padding: 50px 40px;
    max-width: 420px;
    width: 90%;
    text-align: center;
    position: relative;
    border: 4px solid var(--pink);
    box-shadow: 10px 10px 0 var(--yellow);
    animation: popup-in 0.5s cubic-bezier(0.34,1.56,0.64,1);
  }
  @keyframes popup-in {
    0% { transform: scale(0.5) rotate(-10deg); opacity: 0; }
    100% { transform: scale(1) rotate(0); opacity: 1; }
  }
  .popup-emoji { font-size: 5rem; margin-bottom: 20px; display: block; animation: bounce-text 0.8s ease-in-out infinite alternate; }
  .popup-title {
    font-family: 'Pacifico', cursive;
    font-size: 2rem;
    color: var(--dark);
    margin-bottom: 12px;
  }
  .popup-msg {
    color: #777;
    font-size: 1rem;
    font-weight: 700;
    line-height: 1.6;
    margin-bottom: 24px;
  }
  .popup-close {
    background: var(--pink);
    color: white;
    border: none;
    padding: 12px 36px;
    border-radius: 50px;
    font-family: 'Fredoka One', cursive;
    font-size: 1.1rem;
    cursor: pointer;
    transition: transform 0.2s;
  }
  .popup-close:hover { transform: scale(1.1); }

  /* Responsive */
  @media (max-width: 600px) {
    .timeline::before { left: 30px; }
    .timeline-item, .timeline-item:nth-child(odd) { flex-direction: column; padding-left: 60px; }
    .timeline-content { width: 100%; }
    .timeline-dot { position: absolute; left: 5px; width: 50px; }
    .letter-card { padding: 40px 24px; }
  }
</style>
</head>
<body>

<!-- Confetti -->
<div class="confetti-container" id="confettiContainer"></div>

<!-- Hero -->
<section class="hero">
  <div class="doodle" style="top:8%;left:5%;animation-delay:0s;">⭐</div>
  <div class="doodle" style="top:12%;right:8%;animation-delay:0.5s;">🌸</div>
  <div class="doodle" style="bottom:15%;left:8%;animation-delay:1s;">🌈</div>
  <div class="doodle" style="bottom:20%;right:6%;animation-delay:0.3s;">✨</div>
  <div class="doodle" style="top:40%;left:2%;animation-delay:0.8s;">🎀</div>
  <div class="doodle" style="top:35%;right:3%;animation-delay:0.2s;">🦋</div>
  <div class="doodle" style="top:70%;left:15%;animation-delay:1.2s;">🍭</div>
  <div class="doodle" style="top:65%;right:12%;animation-delay:0.7s;">🌟</div>

  <div class="badge">🎉 Breaking News 🎉</div>
  <h1>2 Months of <span>Surviving</span><br>Each Other! 💕</h1>
  <span class="big-heart">❤️</span>
  <p class="subtitle">Since 2nd February 2026 — officially certified by the Ministry of Cute Couples 🏛️</p>
  <p class="scroll-hint">↓ Keep scrolling, it gets better ↓</p>
</section>

<!-- Stats -->
<section class="stats-section">
  <h2 class="section-title">Our Official Statistics 📊</h2>
  <div class="stats-grid">
    <div class="stat-card">
      <span class="stat-emoji">📅</span>
      <div class="stat-number" id="dayCount">61</div>
      <div class="stat-label">Days of Pure Chaos (aka Love)</div>
    </div>
    <div class="stat-card">
      <span class="stat-emoji">😂</span>
      <div class="stat-number">∞</div>
      <div class="stat-label">Times I Made You Laugh<br><small style="color:#aaa;font-size:0.75rem;">(okay, maybe 12)</small></div>
    </div>
    <div class="stat-card">
      <span class="stat-emoji">🍕</span>
      <div class="stat-number">100+</div>
      <div class="stat-label">Arguments About What to Eat</div>
    </div>
    <div class="stat-card">
      <span class="stat-emoji">🥰</span>
      <div class="stat-number">1</div>
      <div class="stat-label">Person Who Stole My Heart<br><small style="color:#aaa;font-size:0.75rem;">(it was you, obviously)</small></div>
    </div>
  </div>
</section>

<!-- Reasons -->
<section class="reasons-section">
  <h2 class="section-title">Why I Love You<br><small style="font-size:0.55em;font-family:'Nunito',sans-serif;font-weight:800;">(Scientifically Proven™ list)</small></h2>
  <div class="reasons-grid">
    <div class="reason-card">
      <span class="reason-icon">😂</span>
      <div class="reason-title">Your Laugh</div>
      <p class="reason-text">It's literally the best sound in the world. Even when you're laughing AT me. Especially then, actually.</p>
    </div>
    <div class="reason-card">
      <span class="reason-icon">🧠</span>
      <div class="reason-title">Your Big Brain</div>
      <p class="reason-text">You're so smart it's actually annoying. Like why are you always right? Stop it. (Please don't stop it.)</p>
    </div>
    <div class="reason-card">
      <span class="reason-icon">🌙</span>
      <div class="reason-title">Late Night Chats</div>
      <p class="reason-text">When we talk until 2am about absolutely nothing important. Best meetings of my life, no agenda required.</p>
    </div>
    <div class="reason-card">
      <span class="reason-icon">🤦</span>
      <div class="reason-title">Your Patience</div>
      <p class="reason-text">You put up with my nonsense on a DAILY basis. That alone deserves an Olympic gold medal. 🥇</p>
    </div>
    <div class="reason-card">
      <span class="reason-icon">✨</span>
      <div class="reason-title">Your Smile</div>
      <p class="reason-text">Honestly? Scientists should study it. It probably cures diseases. I'm 100% not exaggerating. Okay, maybe 10%.</p>
    </div>
    <div class="reason-card">
      <span class="reason-icon">🫂</span>
      <div class="reason-title">Just… You</div>
      <p class="reason-text">Everything about you. The whole package. The silly parts, the serious parts, all of it. You're my favorite person.</p>
    </div>
  </div>
</section>

<!-- Timeline -->
<section class="timeline-section">
  <h2 class="section-title">Our Epic 2-Month Story 📖</h2>
  <div class="timeline">

    <div class="timeline-item">
      <div class="timeline-content">
        <div class="timeline-date">February 2, 2026</div>
        🚀 <strong>Day 1 — The Beginning!</strong><br>
        The universe decided to do something <em>really</em> smart for once. Us. ❤️
      </div>
      <div class="timeline-dot"><span>🌹</span></div>
      <div style="width:44%"></div>
    </div>

    <div class="timeline-item">
      <div class="timeline-content">
        <div class="timeline-date">Week 1</div>
        🦋 <strong>The Butterfly Phase</strong><br>
        Texting 24/7. Checking the phone every 10 seconds. Very normal, very cool behavior. 😅
      </div>
      <div class="timeline-dot"><span>📱</span></div>
      <div style="width:44%"></div>
    </div>

    <div class="timeline-item">
      <div class="timeline-content">
        <div class="timeline-date">Week 2-3</div>
        🍕 <strong>The "What Do You Want to Eat?" Era</strong><br>
        We argued about food. We ALWAYS argued about food. We will probably always argue about food.
      </div>
      <div class="timeline-dot"><span>😂</span></div>
      <div style="width:44%"></div>
    </div>

    <div class="timeline-item">
      <div class="timeline-content">
        <div class="timeline-date">Month 1</div>
        💪 <strong>Officially Comfy Together</strong><br>
        The phase where we stopped pretending to be perfect. Spoiler: I liked you even more. 🙈
      </div>
      <div class="timeline-dot"><span>🥰</span></div>
      <div style="width:44%"></div>
    </div>

    <div class="timeline-item">
      <div class="timeline-content">
        <div class="timeline-date">April 2, 2026</div>
        🎊 <strong>2 MONTHS! WOOOO!</strong><br>
        You're stuck with me now. This website is proof. Legally binding* <br><small>(*not legally binding)</small>
      </div>
      <div class="timeline-dot"><span>🎉</span></div>
      <div style="width:44%"></div>
    </div>

  </div>
</section>

<!-- Meter -->
<section class="meter-section">
  <h2 class="section-title">The Official Love Meter™ 📈</h2>
  <div class="meter-cards">
    <div class="meter-item">
      <div class="meter-label">How much I like you <span>CRITICAL LEVEL</span></div>
      <div class="meter-bar"><div class="meter-fill" style="background: linear-gradient(90deg, #FF6B9D, #FF8552); --target-width: 100%;"></div></div>
    </div>
    <div class="meter-item">
      <div class="meter-label">My patience when you take forever to reply <span>CONCERNING</span></div>
      <div class="meter-bar"><div class="meter-fill" style="background: linear-gradient(90deg, #FFD93D, #FF6B9D); --target-width: 12%;"></div></div>
    </div>
    <div class="meter-item">
      <div class="meter-label">Times I've thought about you today <span>TOO MANY</span></div>
      <div class="meter-bar"><div class="meter-fill" style="background: linear-gradient(90deg, #C77DFF, #4CC9F0); --target-width: 97%;"></div></div>
    </div>
    <div class="meter-item">
      <div class="meter-label">How ready I am to share my fries with you <span>GENEROUS</span></div>
      <div class="meter-bar"><div class="meter-fill" style="background: linear-gradient(90deg, #6BCFB5, #4CC9F0); --target-width: 78%;"></div></div>
    </div>
    <div class="meter-item">
      <div class="meter-label">How much you deserve this whole website <span>MAXIMUM</span></div>
      <div class="meter-bar"><div class="meter-fill" style="background: linear-gradient(90deg, #FF6B9D, #C77DFF, #4CC9F0); --target-width: 100%;"></div></div>
    </div>
  </div>
</section>

<!-- Love Letter -->
<section class="letter-section">
  <div class="letter-card">
    <div class="letter-text">
      <p>Dear You,</p>
      <p>I don't exactly know how, but somehow in just 2 months you've become my favorite part of every single day. Like — how did you do that?? That should be illegal. Are you a wizard? 🧙‍♀️</p>
      <p>You make boring things fun, hard things easier, and good things absolutely amazing. You laugh at my terrible jokes (sometimes), you put up with my dramatics (always), and somehow you still choose to stick around. That makes you either really brave or slightly insane — I choose to believe: both. 😄</p>
      <p>I know 2 months isn't that long in the grand scheme of things. But honestly? It's been long enough to know that you're someone really, truly special. And I'm a very lucky person to have you. 🍀</p>
      <p>Here's to more months, more memories, more debates about what to eat, and a whole lot more of just… us. 💕</p>
    </div>
    <div class="letter-signature">With love (and bad jokes), yours 💖</div>
  </div>
</section>

<!-- Finale -->
<section class="finale">
  <div class="hearts-rain" id="heartsRain"></div>
  <h2 style="position:relative;z-index:1;">Happy 2 Months! 🎊</h2>
  <p style="position:relative;z-index:1;">You make everything better.<br>Thanks for being mine. ❤️</p>
  <button class="btn-love" onclick="showPopup()" style="position:relative;z-index:1;">Click for a Surprise! 🎁</button>
</section>

<!-- Popup -->
<div class="popup-overlay" id="popup">
  <div class="popup-box">
    <span class="popup-emoji">🥰</span>
    <div class="popup-title">I Love You!</div>
    <p class="popup-msg">
      Okay, okay, you wanted a surprise? Here it is:<br><br>
      <strong>YOU</strong> are the best thing that happened to me this year. And the year before. And honestly, probably every year from now on too. 💕<br><br>
      P.S. — You still owe me fries. 🍟
    </p>
    <button class="popup-close" onclick="closePopup()">Aww, thank you! 💖</button>
  </div>
</div>

<script>
  // === CONFETTI ===
  const colors = ['#FF6B9D','#FFD93D','#6BCFB5','#C77DFF','#FF8552','#4CC9F0'];
  const container = document.getElementById('confettiContainer');
  for (let i = 0; i < 60; i++) {
    const p = document.createElement('div');
    p.className = 'confetti-piece';
    p.style.cssText = `
      left: ${Math.random()*100}%;
      background: ${colors[Math.floor(Math.random()*colors.length)]};
      width: ${6+Math.random()*10}px;
      height: ${6+Math.random()*10}px;
      border-radius: ${Math.random()>0.5?'50%':'2px'};
      animation-duration: ${3+Math.random()*6}s;
      animation-delay: ${Math.random()*8}s;
      opacity: ${0.5+Math.random()*0.5};
    `;
    container.appendChild(p);
  }

  // === HEARTS RAIN ===
  const rain = document.getElementById('heartsRain');
  const heartEmojis = ['❤️','💕','💖','💗','💓','💝','🌸','✨'];
  for (let i = 0; i < 30; i++) {
    const h = document.createElement('div');
    h.className = 'heart-drop';
    h.textContent = heartEmojis[Math.floor(Math.random()*heartEmojis.length)];
    h.style.cssText = `
      left: ${Math.random()*100}%;
      font-size: ${1+Math.random()*1.5}rem;
      animation-duration: ${5+Math.random()*8}s;
      animation-delay: ${Math.random()*8}s;
    `;
    rain.appendChild(h);
  }

  // === DAY COUNT ===
  const start = new Date('2026-02-02');
  const today = new Date('2026-04-02');
  const days = Math.floor((today - start) / (1000*60*60*24));
  document.getElementById('dayCount').textContent = days;

  // === METER ANIMATION ON SCROLL ===
  const observer = new IntersectionObserver((entries) => {
    entries.forEach(e => {
      if (e.isIntersecting) {
        e.target.querySelectorAll('.meter-fill').forEach(f => {
          f.style.animationPlayState = 'running';
        });
      }
    });
  }, { threshold: 0.2 });
  document.querySelectorAll('.meter-cards').forEach(el => observer.observe(el));

  // Pause meter bars initially
  document.querySelectorAll('.meter-fill').forEach(f => f.style.animationPlayState = 'paused');

  // === POPUP ===
  function showPopup() {
    document.getElementById('popup').classList.add('active');
    // Burst confetti
    for (let i = 0; i < 30; i++) {
      const p = document.createElement('div');
      p.className = 'confetti-piece';
      p.style.cssText = `
        left: ${20+Math.random()*60}%;
        top: 40%;
        background: ${colors[Math.floor(Math.random()*colors.length)]};
        width: ${8+Math.random()*12}px;
        height: ${8+Math.random()*12}px;
        border-radius: ${Math.random()>0.5?'50%':'2px'};
        animation-duration: ${1.5+Math.random()*2}s;
        animation-delay: 0s;
      `;
      container.appendChild(p);
      setTimeout(() => p.remove(), 4000);
    }
  }
  function closePopup() {
    document.getElementById('popup').classList.remove('active');
  }
  document.getElementById('popup').addEventListener('click', function(e) {
    if (e.target === this) closePopup();
  });
</script>
</body>
</html>
hs.html…]()
