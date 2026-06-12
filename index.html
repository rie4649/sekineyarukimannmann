<!DOCTYPE html>
<html lang="ja">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>関根商店 やる気スイッチおみくじ</title>
<style>
body{font-family:sans-serif;background:linear-gradient(180deg,#fff7fb,#f4fbff);padding:18px;text-align:center;max-width:850px;margin:auto;color:#333}
h1{color:#e91e63;line-height:1.35;font-size:34px}
.card{background:white;padding:18px;margin:14px 0;border-radius:18px;box-shadow:0 4px 14px rgba(0,0,0,.12)}
button{font-size:22px;padding:16px 30px;border:none;border-radius:18px;background:#ff4081;color:white;cursor:pointer;font-weight:bold}
button:disabled{background:#bbb}
#result{font-size:21px;line-height:1.7}.big{font-size:28px;font-weight:bold}.rank{font-size:22px;font-weight:bold;color:#d81b60}.small{font-size:14px;color:#666;margin-top:10px}
.progress{background:#eee;border-radius:999px;height:18px;overflow:hidden;margin:12px 0}.bar{background:#ff80ab;height:100%;width:0%}
</style>
</head>
<body>
<h1>関根商店<br>やる気スイッチおみくじ</h1>

<div class="card">
<h2>今日の運勢を占う</h2>
<p>一日一回まで</p>
<button id="drawButton" onclick="drawOmikuji()">おみくじを引く</button>
<div id="todayStatus" class="small"></div>
</div>

<div id="result" class="card">おみくじを引いてね✨</div>

<div class="card">
<h2>関根ポイントを貯める</h2>
<div id="points" class="big">現在ポイント：0pt</div>
<div id="rank" class="rank">👶関根見習い</div>
<div class="progress"><div id="bar" class="bar"></div></div>
<div id="nextRank">次のランクまで500pt</div>
</div>

<div class="card">
<h3>💳関根ポイントカード</h3>
🥉500pt　関根ブリキ：🍜お味噌汁追加券<br><br>
🥈1000pt　関根鉄A：🎁ひみつ<br><br>
🥇1500pt　関根CU：🎁ひみつ<br><br>
🏆3000pt　関根プラチナ：🎁ひみつ<br><br>
👑5000pt　関根レジェンド：🎉豪華景品
</div>

<script>
const fortunes=[
{title:"🌈超大吉",point:10,text:"今日は探し物が探す前に見つかる日。エスパー並です。",comment:"関根ポイント10倍！社長も二度見。"},
{title:"🌈超大吉",point:10,text:"今日は冷蔵庫を開けても何を取りに来たか忘れない日。",comment:"奇跡の記憶力発動中。"},
{title:"🌈超大吉",point:10,text:"今日は会計が777円になるかもしれない日。",comment:"ならなくても気持ちは777。"},
{title:"🌈大吉",point:5,text:"今日はお祭り気分で一日過ごせる日。",comment:"理由はないけど楽しい。"},
{title:"🌈大吉",point:5,text:"今日は夕飯が好きなメニューの日。",comment:"カレー率やや高め。"},
{title:"🌈大吉",point:5,text:"今日はレジの列選びで勝つ日。",comment:"隣の列を見てはいけません。"},
{title:"🌈大吉",point:5,text:"今日は信号が味方してくれる日。",comment:"青信号応援団出動中。"},
{title:"🌈中吉",point:2,text:"今日は誰かがちょっと優しい日。",comment:"世界も捨てたもんじゃない。"},
{title:"🌈中吉",point:2,text:"今日は『まあいっか』で何とかなる日。",comment:"だいたい何とかなります。"},
{title:"🌈中吉",point:2,text:"今日は思ったより悪くない日。",comment:"期待値を超えてきました。"},
{title:"🌈中吉",point:2,text:"今日はエレベーターが待っていてくれる日。",comment:"あなたの到着を予測済み。"},
{title:"🌈小吉",point:1,text:"今日は袋の開け口がすぐ見つかる日。",comment:"老眼にも優しい設計です。"},
{title:"🌈小吉",point:1,text:"今日は髪型が夕方まで持つ日。",comment:"湿気との戦いに勝利。"},
{title:"🌈小吉",point:1,text:"今日はペンをなくさない日。",comment:"地味にすごい。"},
{title:"🌈小吉",point:1,text:"今日は靴下が一発で揃う日。",comment:"左右の絆を感じます。"},
{title:"🌈末吉",point:0,text:"今日は小さなラッキーが渋滞している日。",comment:"追突注意。"},
{title:"🌈末吉",point:0,text:"今日はなんとなく全部ちょうどいい日。",comment:"大事件は起きません。"},
{title:"🌈末吉",point:0,text:"今日はお茶がおいしい日。",comment:"それだけで十分。"},
{title:"🌈末吉",point:0,text:"今日は特に何もない日。",comment:"それが一番平和です。"}
];
const bonuses=[
{multi:0,msg:"本日は省エネ運転です"},{multi:0,msg:"本日は省エネ運転です"},
{multi:2,msg:"関根ボーナス発動！"},{multi:2,msg:"関根ボーナス発動！"},{multi:2,msg:"関根ボーナス発動！"},{multi:2,msg:"関根ボーナス発動！"},{multi:2,msg:"関根ボーナス発動！"},
{multi:5,msg:"関根ラッシュ突入！"},{multi:5,msg:"関根ラッシュ突入！"},{multi:5,msg:"関根ラッシュ突入！"},
{multi:10,msg:"🎉関根フィーバー！！🎉"}
];
let points=parseInt(localStorage.getItem("sekinePoints")||"0");
function todayKey(){const d=new Date();return d.getFullYear()+"-"+(d.getMonth()+1)+"-"+d.getDate()}
function getRank(pt){if(pt>=5000)return"👑関根レジェンド";if(pt>=3000)return"🏆関根プラチナ";if(pt>=1500)return"🥇関根CU";if(pt>=1000)return"🥈関根鉄A";if(pt>=500)return"🥉関根ブリキ";return"👶関根見習い"}
function nextGoal(pt){if(pt<500)return 500;if(pt<1000)return 1000;if(pt<1500)return 1500;if(pt<3000)return 3000;if(pt<5000)return 5000;return 5000}
function prizeText(pt){if(pt>=5000)return"🎉関根レジェンド達成！豪華景品ゲット！";if(pt>=3000)return"🏆関根プラチナ達成！景品はひみつ！";if(pt>=1500)return"🥇関根CU達成！景品はひみつ！";if(pt>=1000)return"🥈関根鉄A達成！景品はひみつ！";if(pt>=500)return"🥉関根ブリキ達成！お味噌汁追加券ゲット！";return""}
function updateDisplay(){
document.getElementById("points").innerHTML="現在ポイント："+points+"pt";
document.getElementById("rank").innerHTML=getRank(points);
const goal=nextGoal(points);const remain=Math.max(goal-points,0);
document.getElementById("nextRank").innerHTML=points>=5000?"👑最高ランク達成中！":"次のランクまで "+remain+"pt";
document.getElementById("bar").style.width=(points>=5000?100:Math.min((points/goal)*100,100))+"%";
const lastDraw=localStorage.getItem("sekineLastDraw");
if(lastDraw===todayKey()){document.getElementById("drawButton").disabled=true;document.getElementById("todayStatus").innerHTML="今日はもう引きました。また明日ね✨"}else{document.getElementById("drawButton").disabled=false;document.getElementById("todayStatus").innerHTML="毎日1回チャレンジできます✨"}
}
function drawOmikuji(){
if(localStorage.getItem("sekineLastDraw")===todayKey()){document.getElementById("result").innerHTML="😊今日はもう引いています！<br>また明日チャレンジしてね✨";return}
const beforeRank=getRank(points);
const fortune=fortunes[Math.floor(Math.random()*fortunes.length)];
const bonus=bonuses[Math.floor(Math.random()*bonuses.length)];
const gain=fortune.point*bonus.multi;
points+=gain;
localStorage.setItem("sekinePoints",points);
localStorage.setItem("sekineLastDraw",todayKey());
const afterRank=getRank(points);
let rankUp="";
if(beforeRank!==afterRank){rankUp="<br><br>🎊ランクアップ！🎊<br>"+prizeText(points)}
document.getElementById("result").innerHTML="<h2>"+fortune.title+"</h2>"+fortune.text+"<br><br>👉 "+fortune.comment+"<br><br>🎁 "+bonus.msg+"<br>倍率："+bonus.multi+"倍<br><br><b class='big'>"+gain+"pt獲得！</b>"+rankUp+"<br><br>💳現在 "+points+"pt";
updateDisplay();
}
updateDisplay();
</script>
</body>
</html>
