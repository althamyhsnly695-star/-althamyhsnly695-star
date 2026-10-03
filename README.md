 <!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<title>Hacked by Hassan</title>
<style>
body{background:#000;color:#0f0;font-family:monospace;text-align:center;padding-top:10%}
h1{color:red;font-size:45px;animation:blink 0.8s infinite}
@keyframes blink{0%{opacity:1}50%{opacity:0.2}100%{opacity:1}}
#bar{width:80%;height:25px;border:2px solid #0f0;margin:20px auto}
#fill{height:100%;width:0%;background:#0f0;transition:0.1s}
.box{border:1px solid #0f0;width:85%;margin:auto;padding:15px;background:rgba(0,255,0,0.05)}
</style>
</head>
<body>
<h1>⚠️ تنبيه أمني ⚠️</h1>
<div class="box">
<p>> جاري محاكاة اختبار اختراق وهمي...</p>
<p id="text">> الاتصال...</p>
<div id="bar"><div id="fill"></div></div>
<p id="status">0%</p>

<div id="final" style="display:none">
<h2 style="color:white">تمت المحاكاة بواسطة</h2>
<h1 style="color:white;animation:none">حسن التهامي 🇾🇪</h1>
<p style="color:#fff">Hassan Al-Tehami | Cybersecurity Researcher</p>
<p style="color:yellow">⚠️ تنبيه: لم يتم نقل أي ملف، هذه صفحة مزاح تعليمية فقط 😂</p>
<p>جهازك آمن 100%</p>
</div>
</div>

<script>
let w=0;
let txt=document.getElementById('text');
let fill=document.getElementById('fill');
let st=document.getElementById('status');
let msgs=["فحص النظام...","تشفير الاتصال...","تحميل البيانات الوهمية...","اكتملت المحاكاة!"];

let inter=setInterval(()=>{
w+=2;
fill.style.width=w+"%";
st.innerHTML=w+"% - "+msgs[Math.floor(w/25)];
if(w>=100){
clearInterval(inter);
document.getElementById('final').style.display='block';
txt.innerHTML="> اكتمل الاختبار الوهمي بنجاح";
}
},80);
</script>
</body>
</html>