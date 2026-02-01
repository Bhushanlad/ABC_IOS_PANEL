<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>ABC iOS Panel</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<style>
body{
  margin:0; min-height:100vh;
  background:linear-gradient(135deg,#020617,#020617);
  font-family:Arial,Helvetica,sans-serif; color:#fff;
}
.box{
  max-width:420px; margin:30px auto; padding:22px;
  border-radius:20px;
  background:rgba(255,255,255,0.06);
  backdrop-filter:blur(14px);
  box-shadow:0 20px 60px rgba(0,0,0,.6);
  animation:fadeUp .7s ease;
}
@keyframes fadeUp{from{opacity:0;transform:translateY(20px)}to{opacity:1;transform:none}}
h2,h3{
  text-align:center;
  background:linear-gradient(90deg,#38bdf8,#22c55e);
  -webkit-background-clip:text; -webkit-text-fill-color:transparent;
}
input,button{
  width:100%; padding:13px; margin-top:12px;
  border-radius:14px; border:none; outline:none; font-size:15px;
}
input{background:#020617;color:#fff}
button{
  background:linear-gradient(90deg,#22c55e,#38bdf8);
  font-weight:bold; color:#000;
}
button:active{transform:scale(.97)}
.hidden{display:none}
.status{text-align:center;margin-top:10px;font-size:14px}
.small{font-size:12px;color:#94a3b8;text-align:center}

.toggle{
  display:flex; justify-content:space-between; align-items:center;
  background:#020617; padding:14px; border-radius:14px; margin-top:12px;
}
.switch{font-size:20px;cursor:pointer}
.off{color:#ef4444} .on{color:#22c55e}

.filebox{
  margin-top:15px; background:#020617;
  padding:14px; border-radius:14px; text-align:center;
}
.openbtn{
  background:linear-gradient(90deg,#38bdf8,#0ea5e9); color:#000;
}
.shortcutbtn{
  background:linear-gradient(90deg,#f43f5e,#ec4899); color:#000;
}
.howbtn{
  background:linear-gradient(90deg,#facc15,#f59e0b); color:#000;
}
.tgbtn{
  background:linear-gradient(90deg,#2AABEE,#229ED9); color:#000;
}
#countdown{margin-top:6px}
</style>
</head>

<body>

<!-- LOGIN -->
<div class="box" id="loginBox">
  <h2>ABC iOS LOGIN</h2>

  <div class="small">Your Device Code</div>
  <h3 id="device"></h3>

  <button onclick="copyCode()">COPY DEVICE CODE</button>

  <!-- TELEGRAM BUTTON -->
  <button class="tgbtn" onclick="sendToTelegram()">
    📩 Send Device Code for Key
  </button>

  <input id="key" placeholder="Enter Key (ABC-KEY-XXXXXX)">
  <button onclick="login()">LOGIN</button>

  <button class="howbtn" onclick="howToUse()">HOW TO USE</button>

  <div class="status" id="loginStatus"></div>
</div>

<!-- PANEL -->
<div class="box hidden" id="panelBox">
  <h3>ABC iOS PANEL</h3>
  <p id="countdown" class="small"></p>

  <div class="toggle"><span>HEADTRACKING MAX</span><span class="switch off" onclick="tog(this)">❌</span></div>
  <div class="toggle"><span>AIM ASSIST MAX</span><span class="switch off" onclick="tog(this)">❌</span></div>
  <div class="toggle"><span>120 FPS</span><span class="switch off" onclick="tog(this)">❌</span></div>
  <div class="toggle"><span>SMOOTH GAMEPLAY</span><span class="switch off" onclick="tog(this)">❌</span></div>
  <div class="toggle"><span>LESS RECOIL</span><span class="switch off" onclick="tog(this)">❌</span></div>

  <div class="filebox">
    <p>Select File (pak)</p>
    <input type="file" id="fileInput">
  </div>

  <button onclick="applyFile()">APPLY FILE</button>

  <!-- SHORTCUT BUTTONS -->
  <button class="shortcutbtn" onclick="addBGMI()">ADD BGMI SHORTCUT</button>
  <button class="shortcutbtn" onclick="addPUBG()">ADD PUBG SHORTCUT</button>

  <!-- DIRECT OPEN SHORTCUT BUTTONS -->
  <button class="openbtn" onclick="openBGMI()">OPEN BGMI</button>
  <button class="openbtn" onclick="openPUBG()">OPEN PUBG</button>

  <div class="status" id="panelStatus"></div>
</div>

<script>
/* CONFIG */
const SECRET = "ABC2026";
const TG_USERNAME = "abcmodder";
const BLOCKED_KEYS = [];

/* DEVICE CODE */
function genDevice(){
  return "ABC-DEV-"+Math.random().toString(36).substr(2,4).toUpperCase()
        +"-"+Math.random().toString(36).substr(2,4).toUpperCase();
}
let device = localStorage.getItem("ABC_DEVICE");
if(!device){ device = genDevice(); localStorage.setItem("ABC_DEVICE",device); }
document.getElementById("device").innerText = device;

/* HASH */
function simpleHash(str){
  let h=0; for(let i=0;i<str.length;i++){ h=(h<<5)-h+str.charCodeAt(i); h|=0; }
  return Math.abs(h).toString(16).toUpperCase().substring(0,6);
}

/* LOGIN */
function login(){
  const key=document.getElementById("key").value.trim();
  const status=document.getElementById("loginStatus");
  const today=new Date().toISOString().split("T")[0];

  for(let i=0;i<=365;i++){
    const d=new Date(); d.setDate(d.getDate()+i);
    const exp=d.toISOString().split("T")[0];
    const expected="ABC-KEY-"+simpleHash(device+exp+SECRET);

    if(key===expected){
      if(today>exp){ status.innerText="❌ Key Expired"; return; }

      localStorage.setItem("ABC_EXPIRY",exp);
      startCountdown(exp);

      loginBox.classList.add("hidden");
      panelBox.classList.remove("hidden");
      return;
    }
  }
  status.innerText="❌ Invalid Key";
}

/* COUNTDOWN */
function startCountdown(exp){
  const cd=document.getElementById("countdown");
  function upd(){
    const diff=new Date(exp+"T23:59:59")-Date.now();
    if(diff<=0){cd.innerText="❌ Key Expired";return;}
    const d=Math.floor(diff/86400000);
    const h=Math.floor(diff/3600000)%24;
    const m=Math.floor(diff/60000)%60;
    cd.innerText=`⏳ Expiry in ${d}d ${h}h ${m}m`;
  }
  upd(); setInterval(upd,60000);
}
const saved=localStorage.getItem("ABC_EXPIRY");
if(saved)startCountdown(saved);

/* PANEL */
function tog(el){
  el.classList.toggle("on"); el.classList.toggle("off");
  el.innerText=el.classList.contains("on")?"✅":"❌";
}
function applyFile(){
  panelStatus.innerText=fileInput.files[0]
    ?"✅ File Selected: "+fileInput.files[0].name
    :"❌ No file selected";
}

/* SHORTCUTS ADD */
function addBGMI(){location.href="https://www.icloud.com/shortcuts/8369cb589ee94e38b2d3e3ca4c1d7c65";}
function addPUBG(){location.href="https://www.icloud.com/shortcuts/eaf67676f88d4bc8851d6bff7344bfe1;";}

/* DIRECT OPEN SHORTCUT */
function openBGMI(){location.href="shortcuts://run-shortcut?name=ABC_BGMI";}
function openPUBG(){location.href="shortcuts://run-shortcut?name=ABC_PUBG";}

/* TELEGRAM */
function sendToTelegram(){
  const msg=encodeURIComponent("Hello, I need a key.\n\nDevice Code: "+device);
  location.href="https://t.me/"+TG_USERNAME+"?text="+msg;
}

/* HOW TO USE */
function howToUse(){
  window.open("https://youtube.com","_blank");
}

/* COPY */
function copyCode(){
  navigator.clipboard.writeText(device);
  alert("Device Code Copied");
}
</script>
</body>
</html>
