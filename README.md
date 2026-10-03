 <!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>System Hacked</title>
<style>
body { background: black; color: #00ff00; font-family: 'Courier New', monospace; text-align: center; overflow: hidden; margin:0; }
.matrix { position: fixed; top:0; left:0; width:100%; height:100%; z-index:-1; opacity:0.2; }
h1 { font-size: 50px; margin-top: 15%; color: red; text-shadow: 0 0 20px red; animation: blink 1s infinite; }
@keyframes blink { 0% {opacity:1} 50% {opacity:0.3} 100% {opacity:1} }
.box { border: 2px solid #00ff00; padding: 20px; width: 80%; margin: 20px auto; background: rgba(0,255,0,0.1); }
button { background: red; color: white; border: none; padding: 10px 30px; font-size: 20px; cursor: pointer; margin-top:20px; }
</style>
</head>
<body>
<canvas class="matrix" id="matrix"></canvas>

<h1>⚠️ تم اختراقك! ⚠️</h1>

<div class="box">
<h2>تم اختراق جهازك بنجاح من قبل</h2>
<h2 style="color:white; font-size:35px;">حسن التهامي - Hassan Al-Tehami</h2>
<p>🛡️ Cybersecurity Researcher From Yemen - حضرموت</p>
<p>لا تقلق يا  عليك التواصل واتساب</p>
<p>جهازك سليم 100% - صفحتك مخترقة   فقط</p>
<button onclick="alert('تم سحب بيانتك وملفتك بنجاح')">اضغط للخروج</button>
</div>

<script>
// ماتريكس
const c = document.getElementById("matrix");
const ctx = c.getContext("2d");
c.height = window.innerHeight;
c.width = window.innerWidth;
const letters = "01";
const fontSize = 14;
const columns = c.width / fontSize;
const drops = [];
for(let x=0; x<columns; x++) drops[x]=1;
function draw(){
ctx.fillStyle="rgba(0,0,0,0.05)";
ctx.fillRect(0,0,c.width,c.height);
ctx.fillStyle="#0F0";
ctx.font=fontSize+"px arial";
for(let i=0; i<drops.length; i++){
const text = letters[Math.floor(Math.random()*letters.length)];
ctx.fillText(text,i*fontSize,drops[i]*fontSize);
if(drops[i]*fontSize>c.height && Math.random()>0.975) drops[i]=0;
drops[i]++;
}
}
setInterval(draw,35);
</script>
</body>
</html>