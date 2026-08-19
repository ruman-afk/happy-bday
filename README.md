[zoe-birthday.html](https://github.com/user-attachments/files/31204706/zoe-birthday.html)
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy Birthday, Zoe</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,opsz,wght@0,9..144,300;0,9..144,500;0,9..144,600;1,9..144,500&family=Jost:wght@300;400;500&display=swap" rel="stylesheet">
<style>

  :root{
    --night: #241623;
    --night-deep: #180d17;
    --day: #FBEFE1;
    --cream: #F7ECE1;
    --rose: #D98EA1;
    --rose-deep: #B96C81;
    --gold: #C9A15A;
    --peach: #F2C9B5;
    --ink: #2E2130;
  }

  *{ box-sizing: border-box; margin:0; padding:0; }

  html{ scroll-behavior: smooth; }

  body{
    font-family: 'Jost', sans-serif;
    color: var(--ink);
    background: var(--cream);
    overflow-x: hidden;
  }

  h1, h2, .serif{
    font-family: 'Fraunces', serif;
  }

  /* ---------- LOCK SCREEN ---------- */

  .lock-screen{
    position: fixed;
    inset: 0;
    background: var(--night);
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
    z-index: 100;
    overflow: hidden;
    padding: 2rem;
    transition: opacity 0.9s ease;
  }

  .lock-stars{
    position: absolute;
    inset: 0;
    pointer-events: none;
  }

  .lock-content{
    position: relative;
    z-index: 2;
  }

  .lock-heading{
    font-size: clamp(1.8rem, 5vw, 2.8rem);
    font-weight: 500;
    color: #fff;
    line-height: 1.25;
    margin-top: 1rem;
  }

  .lock-heading em{
    font-style: italic;
    color: var(--gold);
  }

  .countdown{
    font-family: 'Fraunces', serif;
    font-size: clamp(2.2rem, 6vw, 3.2rem);
    color: var(--rose);
    letter-spacing: 0.06em;
    margin-top: 2.2rem;
  }

  .lock-sub{
    margin-top: 1rem;
    font-size: 0.9rem;
    color: rgba(255,255,255,0.5);
    font-style: italic;
  }

  /* ---------- HERO : twin clock ---------- */

  .hero{
    position: relative;
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    text-align: center;
    padding: 2rem 1.5rem 3rem;
    overflow: hidden;
    background: linear-gradient(90deg, var(--night) 0%, var(--night) 48%, var(--rose-deep) 52%, var(--peach) 100%);
  }

  .stars{
    position: absolute;
    top: 0; left: 0;
    width: 52%; height: 100%;
    overflow: hidden;
    pointer-events: none;
  }
  .star{
    position: absolute;
    width: 2px; height: 2px;
    background: #fff;
    border-radius: 50%;
    opacity: 0.7;
    animation: twinkle 3.2s ease-in-out infinite;
  }
  @keyframes twinkle{
    0%, 100%{ opacity: 0.15; }
    50%{ opacity: 0.9; }
  }

  .petals{
    position: absolute;
    inset: 0;
    pointer-events: none;
    z-index: 1;
  }
  .petal{
    position: absolute;
    top: -5%;
    opacity: 0.55;
    animation: drift linear infinite;
  }
  @keyframes drift{
    0%{ transform: translateY(0) translateX(0) rotate(0deg); opacity: 0; }
    10%{ opacity: 0.55; }
    90%{ opacity: 0.4; }
    100%{ transform: translateY(115vh) translateX(var(--drift-x, 30px)) rotate(200deg); opacity: 0; }
  }

  .moon{
    position: absolute;
    top: 14%; left: 20%;
    width: 46px; height: 46px;
    border-radius: 50%;
    background: #F3E9D2;
    box-shadow: -10px 0 0 0 var(--night) inset, 0 0 24px rgba(243,233,210,0.35);
  }

  .sun{
    position: absolute;
    top: 12%; right: 12%;
    width: 64px; height: 64px;
    border-radius: 50%;
    background: radial-gradient(circle, #FFE1B0 0%, var(--gold) 100%);
    box-shadow: 0 0 40px rgba(201,161,90,0.5);
  }

  .hero-content{
    position: relative;
    z-index: 2;
  }

  .eyebrow{
    font-size: 0.78rem;
    letter-spacing: 0.22em;
    text-transform: uppercase;
    color: var(--peach);
    margin-bottom: 1.1rem;
    font-weight: 400;
  }

  .hero h1{
    font-size: clamp(2.6rem, 7vw, 5rem);
    font-weight: 500;
    line-height: 1.05;
    color: #fff;
    text-shadow: 0 2px 30px rgba(0,0,0,0.25);
  }

  .hero h1 em{
    font-style: italic;
    font-weight: 500;
    color: var(--gold);
  }

  .hero-sub{
    margin-top: 1.3rem;
    font-size: 1.05rem;
    color: rgba(255,255,255,0.82);
    max-width: 34rem;
    margin-left: auto;
    margin-right: auto;
    line-height: 1.7;
  }

  .clocks{
    margin-top: 3rem;
    display: flex;
    gap: 2.5rem;
    justify-content: center;
    flex-wrap: wrap;
  }

  .clock-card{
    background: rgba(255,255,255,0.08);
    backdrop-filter: blur(6px);
    border: 1px solid rgba(255,255,255,0.18);
    border-radius: 16px;
    padding: 1.1rem 1.8rem;
    min-width: 160px;
  }

  .clock-label{
    font-size: 0.72rem;
    letter-spacing: 0.14em;
    text-transform: uppercase;
    color: rgba(255,255,255,0.65);
    margin-bottom: 0.4rem;
  }

  .clock-time{
    font-family: 'Fraunces', serif;
    font-size: 1.9rem;
    color: #fff;
    font-weight: 500;
    letter-spacing: 0.02em;
  }

  .clock-place{
    font-size: 0.82rem;
    color: rgba(255,255,255,0.7);
    margin-top: 0.2rem;
  }

  .gap-note{
    margin-top: 1.6rem;
    font-size: 0.85rem;
    color: rgba(255,255,255,0.55);
    font-style: italic;
  }

  .scroll-cue{
    position: absolute;
    bottom: 2rem;
    left: 50%;
    transform: translateX(-50%);
    width: 20px; height: 32px;
    border: 1.5px solid rgba(255,255,255,0.5);
    border-radius: 12px;
    z-index: 2;
  }
  .scroll-cue::before{
    content: '';
    position: absolute;
    top: 6px; left: 50%;
    transform: translateX(-50%);
    width: 3px; height: 6px;
    border-radius: 2px;
    background: #fff;
    animation: dip 1.6s ease-in-out infinite;
  }
  @keyframes dip{
    0%{ opacity: 1; top: 6px; }
    60%{ opacity: 0.2; top: 16px; }
    100%{ opacity: 0; top: 16px; }
  }

  /* ---------- LETTER ---------- */

  .letter{
    max-width: 42rem;
    margin: 0 auto;
    padding: 6.5rem 1.5rem;
    text-align: center;
  }

  .envelope-wrap{
    display: flex;
    flex-direction: column;
    align-items: center;
    cursor: pointer;
  }

  .envelope{
    position: relative;
    width: 84px;
    height: 60px;
    background: var(--rose);
    border-radius: 6px;
    box-shadow: 0 10px 26px rgba(217,142,161,0.35);
    transition: transform 0.35s ease;
  }
  .envelope:hover{ transform: translateY(-3px); }

  .envelope-flap{
    position: absolute;
    top: 0; left: 0;
    width: 0; height: 0;
    border-left: 42px solid transparent;
    border-right: 42px solid transparent;
    border-top: 30px solid var(--rose-deep);
    transition: transform 0.5s ease;
    transform-origin: top center;
  }

  .envelope-seal{
    position: absolute;
    top: 50%; left: 50%;
    transform: translate(-50%, -30%);
    width: 22px; height: 22px;
    color: var(--gold);
    z-index: 2;
  }
  .envelope-seal svg{ width: 100%; height: 100%; }

  .envelope-wrap.open .envelope-flap{
    transform: rotateX(180deg);
  }

  .envelope-hint{
    margin-top: 1rem;
    font-size: 0.78rem;
    letter-spacing: 0.08em;
    color: var(--rose-deep);
    text-transform: uppercase;
  }

  .letter-body{
    max-height: 0;
    overflow: hidden;
    opacity: 0;
    transition: max-height 1s ease, opacity 0.9s ease, margin-top 0.6s ease;
  }

  .letter-body.revealed{
    max-height: 900px;
    opacity: 1;
    margin-top: 2.6rem;
  }

  .letter .eyebrow{ color: var(--rose-deep); }

  .letter h2{
    font-size: clamp(1.9rem, 4vw, 2.6rem);
    font-weight: 500;
    margin-bottom: 1.8rem;
    color: var(--night);
  }

  .letter p{
    font-size: 1.08rem;
    line-height: 1.9;
    color: #4A3C4A;
    margin-bottom: 1.3rem;
  }

  .letter .signoff{
    margin-top: 2.2rem;
    font-family: 'Fraunces', serif;
    font-style: italic;
    font-size: 1.2rem;
    color: var(--rose-deep);
  }

  /* ---------- GALLERY ---------- */

  .gallery-section{
    background: var(--night);
    padding: 6rem 1.5rem 7rem;
  }

  .gallery-header{
    text-align: center;
    margin-bottom: 3.2rem;
  }

  .gallery-header .eyebrow{ color: var(--rose); }

  .gallery-header h2{
    color: #fff;
    font-size: clamp(1.9rem, 4vw, 2.6rem);
    font-weight: 500;
  }

  .gallery{
    max-width: 32rem;
    margin: 0 auto;
    display: flex;
    justify-content: center;
  }

  .frame{
    position: relative;
    border-radius: 10px;
    overflow: hidden;
    background: var(--cream);
    border: 1px solid rgba(255,255,255,0.08);
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 1.8rem;
    min-height: 260px;
    box-shadow: 0 20px 50px rgba(0,0,0,0.35);
  }

  .frame img{
    width: 100%;
    height: auto;
    max-height: 560px;
    object-fit: contain;
    display: block;
    border-radius: 3px;
  }

  .frame-placeholder{
    text-align: center;
    color: rgba(46,33,48,0.35);
    padding: 1rem;
  }

  .frame-placeholder svg{
    width: 26px; height: 26px;
    margin-bottom: 0.6rem;
    opacity: 0.6;
  }

  .frame-placeholder span{
    display: block;
    font-size: 0.72rem;
    letter-spacing: 0.05em;
  }

  @media (max-width: 700px){
    .clocks{ gap: 1.2rem; }
    .clock-card{ min-width: 130px; padding: 0.9rem 1.2rem; }
  }

  /* ---------- FOOTER ---------- */

  footer{
    text-align: center;
    padding: 3.5rem 1.5rem 3rem;
    background: var(--night-deep);
    color: rgba(255,255,255,0.4);
    font-size: 0.8rem;
    letter-spacing: 0.04em;
  }

</style>
</head>
<body>

<div id="lockScreen" class="lock-screen">
  <div class="lock-stars" id="lockStars"></div>
  <div class="lock-content">
    <div class="eyebrow">Not quite time yet</div>
    <h1 class="lock-heading">Something's waiting<br>for you the moment <em>your day</em> begins</h1>
    <div class="countdown" id="countdown">--:--:--</div>
    <p class="lock-sub">come back in a little while</p>
  </div>
</div>

<div id="siteContent" style="display:none;">

<section class="hero">
  <div class="stars" id="stars"></div>
  <div class="petals" id="petals"></div>
  <div class="moon"></div>
  <div class="sun"></div>

  <div class="hero-content">
    <div class="eyebrow">Another year of you</div>
    <h1>Happy birthday,<br><em>Zoe</em></h1>
    <p class="hero-sub">
      Right now the sky looks different where you are than where I am —
      but every clock, in every timezone, agrees on one thing today:
      it's your day.
    </p>

    <div class="clocks">
      <div class="clock-card">
        <div class="clock-label">Your time</div>
        <div class="clock-time" id="zoeTime">--:--</div>
        <div class="clock-place">Zoe, Portland</div>
      </div>
      <div class="clock-card">
        <div class="clock-label">My time</div>
        <div class="clock-time" id="myTime">--:--</div>
        <div class="clock-place">Me, India</div>
      </div>
    </div>
    <div class="gap-note" id="gapNote">worlds apart, never further than a message away</div>
  </div>

  <div class="scroll-cue"></div>
</section>

<section class="letter">
  <div class="envelope-wrap" id="envelopeWrap">
    <div class="envelope" id="envelope">
      <div class="envelope-flap"></div>
      <div class="envelope-seal">
        <svg viewBox="0 0 24 24" fill="currentColor"><path d="M12 21s-7.5-4.6-10-9.3C.4 8.6 2 5 5.6 5c2 0 3.4 1 4.4 2.4C11 6 12.4 5 14.4 5 18 5 19.6 8.6 22 11.7 19.5 16.4 12 21 12 21z"/></svg>
      </div>
    </div>
    <p class="envelope-hint">tap to open</p>
  </div>

  <div class="letter-body" id="letterBody">
    <div class="eyebrow">A note for you</div>
    <h2>To the girl on the other side of the clock</h2>
    <p>
      Loving you across time zones means my mornings are your nights, and my
      "good morning" is your "goodnight." I've memorized the exact shape of
      the gap between us — half a world, give or take — and I still haven't found
      a version of it that makes you feel far away.
    </p>
    <p>
      Today none of that math matters. Whatever time it is on your side of
      the world when you read this, just know it's already a very good
      day, because it's the day you were born, and the day I get to love
      you a little louder than usual.
    </p>
    <p>
      Here's to another year of falling asleep on the phone with you, bad
      connections, worse sleep schedules, and counting down to the day
      "your time" and "my time" are finally the same time.
    </p>
    <div class="signoff">— happy birthday, my love. yours, always, in every timezone</div>
  </div>
</section>

<section class="gallery-section">
  <div class="gallery-header">
    <div class="eyebrow">Words for you</div>
    <h2>A poem I wrote you</h2>
  </div>

  <div class="gallery" id="gallery"></div>
</section>

<footer>
  made with love, across two time zones, for Zoe's birthday
</footer>

</div>

<script>
  // ---- starfield ----
  const starsEl = document.getElementById('stars');
  const starCount = 60;
  for(let i=0;i<starCount;i++){
    const s = document.createElement('div');
    s.className = 'star';
    s.style.left = Math.random()*100 + '%';
    s.style.top = Math.random()*90 + '%';
    s.style.animationDelay = (Math.random()*3) + 's';
    starsEl.appendChild(s);
  }

  // ---- unlock gate: reveals the site at 12:00 AM Pacific (her local midnight) ----
  const UNLOCK_TZ = 'America/Los_Angeles';
  const UNLOCK_HOUR = 0;
  const UNLOCK_MINUTE = 0;

  const lockScreen = document.getElementById('lockScreen');
  const siteContent = document.getElementById('siteContent');
  const countdownEl = document.getElementById('countdown');

  const lockStarsEl = document.getElementById('lockStars');
  for(let i=0;i<50;i++){
    const s = document.createElement('div');
    s.className = 'star';
    s.style.left = Math.random()*100 + '%';
    s.style.top = Math.random()*100 + '%';
    s.style.animationDelay = (Math.random()*3) + 's';
    lockStarsEl.appendChild(s);
  }

  function nowInTz(tz){
    return new Date(new Date().toLocaleString('en-US', { timeZone: tz }));
  }

  function getUnlockTarget(){
    const nowUnlockTz = nowInTz(UNLOCK_TZ);
    const target = new Date(nowUnlockTz);
    target.setHours(UNLOCK_HOUR, UNLOCK_MINUTE, 0, 0);
    if (nowUnlockTz >= target){
      target.setDate(target.getDate() + 1);
    }
    return target;
  }

  function revealSite(){
    lockScreen.style.opacity = '0';
    setTimeout(() => { lockScreen.style.display = 'none'; }, 900);
    siteContent.style.display = '';
  }

  function checkUnlock(){
    const nowUnlockTz = nowInTz(UNLOCK_TZ);
    const todayTarget = new Date(nowUnlockTz);
    todayTarget.setHours(UNLOCK_HOUR, UNLOCK_MINUTE, 0, 0);

    if (nowUnlockTz >= todayTarget){
      revealSite();
      return true;
    }

    const diffMs = todayTarget - nowUnlockTz;
    const h = Math.floor(diffMs / 3600000);
    const m = Math.floor((diffMs % 3600000) / 60000);
    const s = Math.floor((diffMs % 60000) / 1000);
    countdownEl.textContent =
      String(h).padStart(2,'0') + ':' + String(m).padStart(2,'0') + ':' + String(s).padStart(2,'0');
    return false;
  }

  if (!checkUnlock()){
    setInterval(checkUnlock, 1000);
  }

  // ---- drifting petals ----
  const petalsEl = document.getElementById('petals');
  const petalCount = 10;
  for(let i=0;i<petalCount;i++){
    const p = document.createElement('div');
    p.className = 'petal';
    p.style.left = Math.random()*100 + '%';
    p.style.setProperty('--drift-x', (Math.random()*60 - 30) + 'px');
    p.style.animationDuration = (14 + Math.random()*10) + 's';
    p.style.animationDelay = (Math.random()*12) + 's';
    const size = 8 + Math.random()*6;
    p.innerHTML = '<svg width="' + size + '" height="' + size + '" viewBox="0 0 24 24" fill="#F2C9B5"><path d="M12 21s-7.5-4.6-10-9.3C.4 8.6 2 5 5.6 5c2 0 3.4 1 4.4 2.4C11 6 12.4 5 14.4 5 18 5 19.6 8.6 22 11.7 19.5 16.4 12 21 12 21z"/></svg>';
    petalsEl.appendChild(p);
  }

  // ---- envelope reveal ----
  const envelopeWrap = document.getElementById('envelopeWrap');
  const letterBody = document.getElementById('letterBody');
  envelopeWrap.addEventListener('click', () => {
    envelopeWrap.classList.add('open');
    letterBody.classList.add('revealed');
    envelopeWrap.style.pointerEvents = 'none';
    setTimeout(() => { envelopeWrap.style.opacity = '0'; envelopeWrap.style.marginBottom = '-2rem'; }, 500);
  });

  // ---- twin clocks ----
  // Real timezones, so this stays correct year-round even across
  // daylight saving changes (India doesn't observe DST, Portland does).
  const ZOE_TZ = 'America/Los_Angeles';
  const MY_TZ = 'Asia/Kolkata';

  function formatTime(tz){
    return new Date().toLocaleTimeString([], { hour: '2-digit', minute: '2-digit', hour12: true, timeZone: tz });
  }

  function hourDiff(){
    const now = new Date();
    const zoeStr = now.toLocaleString('en-US', { timeZone: ZOE_TZ });
    const myStr = now.toLocaleString('en-US', { timeZone: MY_TZ });
    const diffMs = new Date(myStr) - new Date(zoeStr);
    return Math.round((diffMs / (1000 * 60 * 60)) * 2) / 2;
  }

  function tick(){
    document.getElementById('myTime').textContent = formatTime(MY_TZ);
    document.getElementById('zoeTime').textContent = formatTime(ZOE_TZ);
    document.getElementById('gapNote').textContent = hourDiff() + ' hours apart, never further than a message away';
  }
  tick();
  setInterval(tick, 1000 * 15);

  // ---- poem image ----
  // Replace the src below with your poem photo's filename once it's
  // saved alongside this HTML file (e.g. "poem.jpg").
  const galleryEl = document.getElementById('gallery');
  const cameraIcon = '<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.4"><path d="M4 8h3l2-2h6l2 2h3v11H4z"/><circle cx="12" cy="13.5" r="3.2"/></svg>';

  const frame = document.createElement('div');
  frame.className = 'frame';
  frame.innerHTML = '<img src="poem.jpg" alt="A handwritten poem">';
  galleryEl.appendChild(frame);
</script>

</body>
</html>
