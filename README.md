
<!DOCTYPE html>
<html lang="uz">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Zohirjon | Hatna to‘yi</title>

<style>
*{box-sizing:border-box}
body{
  margin:0;background:#050505;color:#f5d77a;
  font-family:Georgia,"Times New Roman",serif;
  text-align:center;overflow-x:hidden;
}
button{
  background:linear-gradient(135deg,#f8e6a0,#b8860b,#ffe8a0);
  color:#140e00;border:1px solid #ffe9a0;
  padding:13px 22px;border-radius:30px;
  font-weight:bold;font-size:15px;cursor:pointer;
  box-shadow:0 0 18px #d4af3766;margin:8px;
}
#envelopeScreen{
  position:fixed;inset:0;z-index:10;background:#030303;
  display:flex;flex-direction:column;align-items:center;
  justify-content:center;padding:20px;
  transition:opacity 1s,visibility 1s;
}
.envelope{
  width:min(82vw,330px);height:210px;position:relative;
  border:2px solid #d4af37;
  background:linear-gradient(145deg,#17130a,#050505);
  box-shadow:0 0 30px #d4af3755;
  display:flex;align-items:center;justify-content:center;
  animation:float 3s infinite ease-in-out;
}
.envelope:before{
  content:"";position:absolute;top:0;left:0;width:0;height:0;
  border-left:calc(min(82vw,330px)/2 - 2px) solid transparent;
  border-right:calc(min(82vw,330px)/2 - 2px) solid transparent;
  border-top:105px solid #392b0c;
  filter:drop-shadow(0 2px 2px #d4af37);
}
.seal{
  z-index:1;width:68px;height:68px;border-radius:50%;
  background:radial-gradient(circle,#ffe9a0,#b8860b);
  color:#160f00;display:grid;place-items:center;
  font-size:38px;font-weight:bold;
  border:2px solid #fff0b0;box-shadow:0 0 25px #ffd70099;
}
@keyframes float{50%{transform:translateY(-8px)}}
.hidden{opacity:0;visibility:hidden;pointer-events:none}

header{padding:32px 12px 12px}
.eyebrow{letter-spacing:4px;font-size:12px;color:#d7b85c}
h1{font-size:clamp(23px,6vw,34px);line-height:1.4;
  text-shadow:0 0 15px #d4af37;margin:18px 0}
.name{
  font-size:clamp(38px,11vw,64px);font-weight:bold;
  letter-spacing:5px;color:#ffe9a0;
  text-shadow:0 0 8px #d4af37,0 0 25px #b8860b;
  animation:shine 2s infinite alternate;
}
@keyframes shine{to{text-shadow:0 0 20px #fff0a5,0 0 42px #d4af37}}
.card{
  width:calc(100% - 28px);max-width:470px;margin:18px auto;
  padding:25px 18px;border:1px solid #b99735;
  background:linear-gradient(160deg,#151108,#080808 65%);
  box-shadow:0 0 25px #d4af3722;
  border-radius:8px;position:relative;
}
p{line-height:1.8;color:#f5e6bd;font-size:16px}
.gold{color:#ffe08a}
.date{font-size:24px;color:#ffe08a;line-height:1.6}
.countdown{
  display:grid;grid-template-columns:repeat(4,1fr);
  gap:7px;margin:20px 0;
}
.countbox{
  padding:12px 3px;border:1px solid #8f7025;
  background:#0b0905;border-radius:6px;
}
.countbox strong{display:block;font-size:23px;color:#ffe08a}
.countbox span{font-size:10px;color:#d9bd70}
.mapbtn{display:inline-block;text-decoration:none}
#thanks{min-height:24px;color:#ffe08a}
#particles{position:fixed;inset:0;pointer-events:none;z-index:0;overflow:hidden}
.spark{
  position:absolute;width:3px;height:3px;border-radius:50%;
  background:#ffe9a0;box-shadow:0 0 9px #ffd700;
  animation:rise linear infinite;opacity:.7;
}
@keyframes rise{
  from{transform:translateY(105vh) scale(.5);opacity:0}
  20%{opacity:.8}to{transform:translateY(-10vh) scale(1.4);opacity:0}
}
main,header,footer{position:relative;z-index:1}
footer{padding:25px 12px 40px;color:#d8bc6d;font-size:13px}
#fireworks{
  position:fixed;inset:0;pointer-events:none;z-index:5;overflow:hidden;
}
.burst{
  position:absolute;width:8px;height:8px;border-radius:50%;
  background:transparent;
  box-shadow:0 -38px #ffe9a0,0 38px #d4af37,
  38px 0 #fff0a0,-38px 0 #d4af37,
  27px 27px #ffe9a0,-27px -27px #d4af37,
  27px -27px #fff0a0,-27px 27px #d4af37;
  animation:burst 1.5s ease-out forwards;
}
@keyframes burst{
  from{transform:scale(.1);opacity:1}
  to{transform:scale(1.8);opacity:0}
}
#invitation{opacity:0;transition:opacity 1.5s}
#invitation.visible{opacity:1}
.small{font-size:13px;color:#bfa45c}
</style>
</head>

<body>
<div id="particles"></div>
<div id="fireworks"></div>

<div id="envelopeScreen">
  <div class="eyebrow" style="margin-bottom:25px">SIZ UCHUN MAXSUS TAKLIFNOMA</div>
  <div class="envelope">
    <div class="seal">Z</div>
  </div>
  <h2 style="margin-top:30px;letter-spacing:3px">ZOHIRJON</h2>
  <p>Taklifnomani ochish uchun bosing</p>
  <button onclick="openInvitation()">✉ TAKLIFNOMANI OCHISH</button>
</div>

<div id="invitation">
<header>
  <div class="eyebrow">BISMILLAHIR ROHMANIR ROHIYM</div>
  <h1>HATNA TO‘YI<br>TAKLIFNOMASI</h1>
  <div class="name" id="name">ZOHIRJON</div>
  <p class="gold">Siz aziz mehmonimizsiz!</p>
</header>

<main>
<section class="card">
  <p>Assalomu alaykum, aziz mehmon!</p>
  <p>
    Sizni o‘g‘limiz <strong class="gold">Zohirjonning</strong>
    qutlug‘ hatna to‘yi munosabati bilan yoziladigan
    shodiyonamizga taklif etamiz.
  </p>
  <p>Sizning tashrifingiz biz uchun katta quvonch!</p>
</section>

<section class="card">
  <div class="eyebrow">TO‘Y SANASI</div>
  <div class="date">17–18 NOYABR<br>2026-YIL</div>
  <p>🕌 Bomdod namozidan so‘ng</p>
  <div class="divider"></div>
  <p class="gold">To‘ygacha qolgan vaqt</p>
  <div class="countdown">
    <div class="countbox"><strong id="days">0</strong><span>KUN</span></div>
    <div class="countbox"><strong id="hours">00</strong><span>SOAT</span></div>
    <div class="countbox"><strong id="minutes">00</strong><span>DAQIQA</span></div>
    <div class="countbox"><strong id="seconds">00</strong><span>SONIYA</span></div>
  </div>
</section>

<section class="card">
  <div class="eyebrow">MANZILIMIZ</div>
  <p class="gold">
    Namangan viloyati,<br>
    To‘raqo‘rg‘on tumani,<br>
    Qatag‘on MFY,<br>
    Paxtaobod ko‘chasi, 8-uy.
  </p>
  <a class="mapbtn" id="mapLink" href="#" target="_blank" rel="noopener">
    <button>📍 GOOGLE MAPSDA OCHISH</button>
  </a>
</section>

<section class="card">
  <div class="eyebrow">TASHRIFINGIZNI TASDIQLANG</div>
  <p>Biz bilan ushbu quvonchli kunni baham ko‘rasizmi?</p>
  <button onclick="rsvp()">💛 MEN BORAMAN</button>
  <p id="thanks"></p>
</section>

<section class="card">
  <p class="gold">Yaratganimiz bu qutlug‘ kunimizni xayrli va barakali qilsin!</p>
  <p>Sizni ushbu qutlug‘ kunimizda ko‘rishdan mamnun bo‘lamiz.</p>
  <p>Hurmat bilan,<br><strong class="gold">Islomjon va oilasi</strong></p>
</section>

<section class="card">
  <div class="eyebrow">MUSIQA</div>
  <p class="small">Milliy kuy qo‘shish uchun musiqani yoqish tugmasini bosing.</p>
  <button id="musicButton" onclick="toggleMusic()">♫ MUSIQANI YOQISH</button>
</section>

<section class="card">
  <div class="eyebrow">QR-KOD</div>
  <p class="small">Sayt internetga joylangach, uning haqiqiy havolasi uchun QR-kod qo‘shiladi.</p>
  <div style="border:1px dashed #b99735;padding:18px;margin:15px auto;max-width:220px">
    <span style="font-size:35px">▦</span><br>
    <span class="small">QR-kod keyin qo‘shiladi</span>
  </div>
</section>

<div style="padding:8px 12px 28px">
  <button onclick="shareInvitation()">↗ TAKLIFNOMANI ULASHISH</button>
</div>
</main>

<footer>✦ ZOHIRJONNING HATNA TO‘YI ✦<br><br>Mehr va ezgulik ila</footer>
</div>

<audio id="music" src="milliy-kuy.mp3" loop preload="none"></audio>

<script>
const address = "Namangan viloyati, To‘raqo‘rg‘on tumani, Qatag‘on MFY, Paxtaobod ko‘chasi, 8-uy";
document.getElementById("mapLink").href =
  "https://www.google.com/maps/dir/?api=1&destination=" +
  encodeURIComponent(address);

let opened = false;
const music = document.getElementById("music");

function openInvitation(){
  if(opened) return;
  opened = true;
  document.getElementById("envelopeScreen").classList.add("hidden");
  document.getElementById("invitation").classList.add("visible");
  makeFireworks();
  music.play().then(()=>{
    document.getElementById("musicButton").textContent="♫ MUSIQANI O‘CHIRISH";
  }).catch(()=>{
    document.getElementById("musicButton").textContent="♫ MUSIQANI YOQISH";
  });
}

function toggleMusic(){
  if(music.paused){
    music.play().then(()=>{
      document.getElementById("musicButton").textContent="♫ MUSIQANI O‘CHIRISH";
    }).catch(()=>{
      alert("Musiqa fayli topilmadi. milliy-kuy.mp3 faylini index.html bilan bir papkaga joylang.");
    });
  }else{
    music.pause();
    document.getElementById("musicButton").textContent="♫ MUSIQANI YOQISH";
  }
}

function rsvp(){
  document.getElementById("thanks").textContent="Rahmat! Sizni kutamiz! 💛";
}

function makeParticles(){
  const area=document.getElementById("particles");
  for(let i=0;i<36;i++){
    const s=document.createElement("span");
    s.className="spark";
    s.style.left=Math.random()*100+"%";
    s.style.animationDuration=(7+Math.random()*12)+"s";
    s.style.animationDelay=(-Math.random()*15)+"s";
    s.style.opacity=(.25+Math.random()*.65);
    area.appendChild(s);
  }
}

function makeFireworks(){
  const area=document.getElementById("fireworks");
  for(let i=0;i<5;i++){
    setTimeout(()=>{
      const b=document.createElement("div");
      b.className="burst";
      b.style.left=(15+Math.random()*70)+"%";
      b.style.top=(15+Math.random()*55)+"%";
      area.appendChild(b);
      setTimeout(()=>b.remove(),1600);
    },i*350);
  }
}

function updateCountdown(){
  const target=new Date("2026-11-17T00:00:00+05:00").getTime();
  const diff=target-Date.now();
  if(diff<=0){
    document.getElementById("days").textContent="0";
    document.getElementById("hours").textContent="00";
    document.getElementById("minutes").textContent="00";
    document.getElementById("seconds").textContent="00";
    return;
  }
  document.getElementById("days").textContent=Math.floor(diff/86400000);
  document.getElementById("hours").textContent=String(Math.floor(diff%86400000/3600000)).padStart(2,"0");
  document.getElementById("minutes").textContent=String(Math.floor(diff%3600000/60000)).padStart(2,"0");
  document.getElementById("seconds").textContent=String(Math.floor(diff%60000/1000)).padStart(2,"0");
}

async function shareInvitation(){
  const data={
    title:"Zohirjonning hatna to‘yi",
    text:"Zohirjonning hatna to‘yiga taklifnomamiz!",
    url:location.href
  };
  if(navigator.share){
    try{await navigator.share(data)}catch(e){}
  }else{
    try{
      await navigator.clipboard.writeText(location.href);
      alert("Taklifnoma havolasi nusxalandi!");
    }catch(e){
      prompt("Havolani nusxalab oling:",location.href);
    }
  }
}

makeParticles();
updateCountdown();
setInterval(updateCountdown,1000);
</script>
</body>
</html>
