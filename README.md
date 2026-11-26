[11주차_DC_박은솔.html](https://github.com/user-attachments/files/35444828/11._DC_.html)
<!DOCTYPE html>
<html lang="ko">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1">
<title>FLOWAY — 붐비는 길 대신, 지금 흐르는 길을 안내한다</title>
<meta name="description" content="붐비는 길 대신, 지금 흐르는 길을 안내한다. 언어 선택·혼잡 센서·가게 주문 데이터로 방문자별 경로를 나눠 안내하는 거리 단말기.">
<style>
:root{--ink:#292929;--gray:#646661;--gold:#e9be5f;--sand:#f5e7b6;--ivory:#f7f5e8;--line:rgba(41,41,41,.18)}
*{box-sizing:border-box;margin:0}
html{scroll-behavior:smooth}
body{font-family:Pretendard,"Apple SD Gothic Neo","Noto Sans KR","Malgun Gothic",sans-serif;background:var(--ivory);color:var(--ink);line-height:1.7;word-break:keep-all}
a{color:inherit}
:focus-visible{outline:3px solid var(--ink);outline-offset:3px}
header{position:sticky;top:0;z-index:5;display:flex;justify-content:space-between;align-items:center;padding:14px 5vw;background:rgba(247,245,232,.92);backdrop-filter:blur(8px);border-bottom:1px solid var(--line);font-size:14px}
header b{font-weight:800;font-size:16px}
header nav{display:flex;gap:22px}
header nav a{text-decoration:none;color:var(--gray)}
header nav a:hover{color:var(--ink)}
section{padding:96px 5vw}
.wrap{max-width:1080px;margin:auto}
h1{font-size:clamp(44px,8vw,96px);line-height:1.02;font-weight:800;letter-spacing:-.04em}
h2{font-size:clamp(28px,4.4vw,48px);line-height:1.2;font-weight:800;letter-spacing:-.03em;margin-bottom:20px}
h3{font-size:20px;font-weight:700;letter-spacing:-.02em}
.lead{font-size:18px;color:var(--gray);max-width:560px}
/* hero */
.hero{display:grid;grid-template-columns:1.15fr .85fr;gap:4vw;align-items:center;max-width:1180px;margin:auto;min-height:calc(100vh - 56px);padding:40px 5vw}
.hero h1 span{display:block;color:var(--gray);font-size:.42em;letter-spacing:-.02em;margin-top:18px;font-weight:600}
.hero .lead{margin:26px 0 30px}
.seg{display:inline-flex;border:2px solid var(--ink);border-radius:99px;padding:4px;gap:4px}
.seg button{font:inherit;font-weight:700;border:0;background:none;padding:10px 22px;border-radius:99px;cursor:pointer;color:var(--ink)}
.seg button[aria-pressed=true]{background:var(--ink);color:var(--sand)}
.hint{font-size:14px;color:var(--gray);margin-top:14px}
.stage{background:var(--sand);border-radius:46% 54% 50% 50%/38% 40% 60% 62%;padding:28px 10px 0;display:grid;place-items:end center}
.stage svg{width:min(100%,330px);height:auto;display:block}
.dot{transition:fill .5s,r .5s}
#scrText,#scrSub{transition:opacity .3s}
.trio{display:grid;grid-template-columns:repeat(3,1fr);margin-top:44px;border-top:3px solid var(--ink)}
.trio div{padding:26px 26px 0 0}
.trio div+div{padding-left:26px;border-left:1px solid var(--line)}
.trio small{display:inline-block;background:var(--gold);padding:2px 12px;border-radius:99px;font-weight:700;font-size:14px;margin-bottom:12px}
.trio h3{margin-bottom:10px;font-size:19px;line-height:1.45}
.trio p{color:var(--gray);font-size:15px}
/* problem */
.problem{background:var(--ink);color:var(--ivory)}
.problem .lead{color:#bdbcae}
.situ{display:grid;grid-template-columns:repeat(3,1fr);margin-top:48px;border-top:1px solid rgba(247,245,232,.3)}
.situ p{padding:26px 26px 0 0;font-size:19px;font-weight:600;line-height:1.55}
.situ p+p{padding-left:26px;border-left:1px solid rgba(247,245,232,.3)}
.situ small{display:block;color:var(--gold);font-size:14px;font-weight:600;margin-bottom:8px}
/* table */
.rows{margin-top:36px}
.row{display:grid;grid-template-columns:150px 1fr 1fr;gap:28px;padding:22px 0;border-top:1px solid var(--line)}
.row:last-child{border-bottom:1px solid var(--line)}
.row h3{font-size:18px}
.row p{color:var(--gray)}
.row p.fix{color:var(--ink);font-weight:600;border-left:4px solid var(--gold);padding-left:16px}
.rows .head{color:var(--gray);font-size:14px;font-weight:700;border-top:0;padding:0 0 10px}
/* product */
.four{display:grid;grid-template-columns:repeat(4,1fr);gap:0;margin-top:44px}
.four div{padding:26px 22px;background:var(--sand)}
.four div:nth-child(2){background:var(--gold)}
.four div:nth-child(3){background:var(--sand)}
.four div:nth-child(4){background:#efdc9a}
.four h3{margin-bottom:10px}
.four p{font-size:15px}
/* flow */
.flow{background:var(--sand)}
.steps{list-style:none;padding:0;margin-top:40px;counter-reset:s;display:grid;grid-template-columns:repeat(3,1fr);gap:36px 30px}
.steps li{counter-increment:s;border-top:3px solid var(--ink);padding-top:14px}
.steps li::before{content:counter(s);display:inline-grid;place-items:center;width:30px;height:30px;border-radius:50%;background:var(--ink);color:var(--sand);font-weight:800;font-size:14px;margin-bottom:8px}
.steps h3{font-size:18px;margin-bottom:6px}
.steps p{font-size:15px;color:#46473f}
/* scale */
.scale{display:grid;grid-template-columns:.8fr 1.2fr;gap:5vw;align-items:start}
dl{margin-top:28px}
dl div{display:grid;grid-template-columns:110px 1fr;gap:16px;padding:14px 0;border-top:1px solid var(--line)}
dt{color:var(--gray);font-weight:700;font-size:15px}
dd{font-weight:600}
/* cmf */
.cmf{background:var(--ink);color:var(--ivory)}
.kw{display:flex;flex-wrap:wrap;gap:12px;margin:26px 0 44px}
.kw span{border:1.5px solid var(--gold);border-radius:99px;padding:8px 20px;font-weight:700}
.kw span:nth-child(odd){border-radius:99px 99px 99px 8px}
.kw span:nth-child(even){border-radius:8px 99px 99px 99px;background:var(--gold);color:var(--ink)}
.sw{display:grid;grid-template-columns:2fr 1.4fr 1.4fr 1fr 1fr;height:150px}
.sw div{padding:14px;display:flex;align-items:flex-end;font-weight:700;font-size:14px}
.cmf p{max-width:620px;color:#bdbcae;margin-top:28px}
.model{display:grid;grid-template-columns:.9fr 1.1fr;gap:5vw;align-items:center}
.model svg{width:100%;max-width:340px;margin:auto;display:block;background:var(--sand);border-radius:28px}
.btns{list-style:none;padding:0;margin-top:28px}
.btns li{display:flex;gap:14px;align-items:center;padding:14px 0;border-top:1px solid var(--line);font-weight:600}
.btns i{flex:none;width:34px;height:34px;border-radius:10px;border:2px solid var(--ink);display:grid;place-items:center;font-style:normal;font-size:14px}
.btns li:nth-child(2) i{border-radius:50%;background:var(--gold);width:42px;height:42px}
footer{padding:60px 5vw;text-align:center;background:var(--gold)}
footer h2{margin-bottom:6px}
@media(max-width:860px){
 header nav{display:none}
 .hero,.scale,.model{grid-template-columns:1fr}
 .hero{min-height:0;padding-top:48px}
 .situ,.four,.steps,.trio{grid-template-columns:1fr}
 .trio div+div{padding-left:0;border-left:0;border-top:1px solid var(--line);margin-top:22px}
 .situ p+p{padding-left:0;border-left:0;border-top:1px solid rgba(247,245,232,.3);margin-top:22px}
 .row{grid-template-columns:1fr;gap:8px}
 .rows .head{display:none}
 .sw{grid-template-columns:1fr 1fr;height:auto}.sw div{height:90px}
 section{padding:72px 5vw}
}
@media(prefers-reduced-motion:reduce){*{transition:none!important;scroll-behavior:auto!important}}


/* ===== scroll actions ===== */
.pin{height:calc(var(--h,300)*1vh);padding:0}
.pin .sticky{position:sticky;top:0;height:100vh;overflow:hidden;display:flex;align-items:center;padding:0 5vw}
.sticky .wrap{width:100%}
[data-at]{opacity:0;transform:translateY(26px);transition:opacity .6s,transform .6s}
[data-at].on{opacity:1;transform:none}
#bar{position:fixed;top:0;left:0;right:0;height:3px;background:var(--gold);transform-origin:0 50%;transform:scaleX(0);z-index:8}
header{transition:background .4s,color .4s,border-color .4s}
header.dk{background:rgba(41,41,41,.88);color:var(--ivory);border-color:rgba(247,245,232,.2)}
header.dk nav a{color:#bdbcae}header.dk nav a:hover{color:var(--gold)}
.hd-menu{display:none;font:inherit;font-weight:700;border:1.5px solid currentColor;background:none;color:inherit;border-radius:99px;padding:6px 16px;cursor:pointer}
.mnav{position:fixed;inset:0;z-index:9;background:var(--ink);color:var(--ivory);display:none;flex-direction:column;justify-content:center;gap:20px;padding:0 8vw;font-size:34px;font-weight:800}
.mnav.o{display:flex}.mnav a{text-decoration:none}.mnav button{position:absolute;top:14px;right:5vw;font:inherit;font-size:14px;font-weight:700;color:inherit;background:none;border:1.5px solid currentColor;border-radius:99px;padding:6px 16px}
/* hero: night street -> day */
#top .sticky{display:block;padding:0;background:color-mix(in srgb,var(--ink) calc((1 - var(--k,1))*100%),var(--ivory))}
#cv{position:absolute;inset:0;width:100%;height:100%}
#top .hero{position:relative;z-index:1;height:100%;min-height:0;padding-top:70px;padding-bottom:20px}
#top h1{color:color-mix(in srgb,var(--ivory) calc((1 - var(--k,1))*100%),var(--ink))}
#top h1 span,#top .lead,#top .hint{color:color-mix(in srgb,#bdbcae calc((1 - var(--k,1))*100%),var(--gray))}
#top .stage{transform:translateY(calc((1 - var(--t,1))*65vh));opacity:calc(.2 + var(--t,1))}
#routeLine{animation:dash 1.4s linear infinite}@keyframes dash{to{stroke-dashoffset:-18}}
.cue{position:absolute;left:50%;bottom:16px;transform:translateX(-50%);font-size:12px;letter-spacing:.3em;color:#bdbcae;opacity:calc(1 - var(--p,0)*8)}
.problem .sticky{background:var(--ink)}
.situ p[data-at]{transition-duration:.7s}
/* flow: kiosk follows the steps */
.flow .sticky{background:var(--sand)}
.fl{display:grid;grid-template-columns:1fr 1fr;gap:0 5vw;align-items:center}
.fl h2{grid-column:1/-1;margin-bottom:26px}
.ks{background:var(--ink);color:var(--ivory);border-radius:28px;padding:28px;min-height:320px;display:flex;flex-direction:column;justify-content:space-between}
.ks small{color:var(--gold);font-weight:700;font-size:14px}
.ks b{font-size:clamp(22px,3vw,34px);line-height:1.3;letter-spacing:-.03em;display:block;margin-top:10px}
.kr{display:flex;justify-content:space-between;align-items:flex-end;height:120px;gap:18px}
.bars{display:flex;align-items:flex-end;gap:10px;height:100%;flex:1}
.bars i{flex:1;background:var(--gold);border-radius:6px 6px 0 0;transition:height .6s,background .6s}
.qr{display:grid;grid-template-columns:repeat(5,1fr);gap:3px;width:100px;opacity:0;transition:opacity .5s}
.qr i{aspect-ratio:1;background:var(--ivory)}.qr i.z{background:transparent}
.ks.q .qr{opacity:1}
.flow .steps{grid-template-columns:1fr;gap:0;margin:0}
.flow .steps li{padding:12px 0;opacity:.35;transition:opacity .4s}
.flow .steps li.on{opacity:1}
.flow .steps li h3{display:inline-block;vertical-align:middle;margin:0 0 0 8px}
.flow .steps p{max-height:0;overflow:hidden;opacity:0;transition:max-height .5s,opacity .5s}
.flow .steps li.on p{max-height:150px;opacity:1;margin-top:6px}
/* controls */
.btns li{transition:background .4s,padding .4s}.btns li.hl{background:var(--sand);padding-left:14px}
.pop{transform-box:fill-box;transform-origin:center;animation:pop .9s}@keyframes pop{40%{transform:scale(1.2)}}
.st .pin{height:auto}.st .pin .sticky{position:static;height:auto;display:block;padding:80px 5vw}.st #top .sticky{padding:0}.st #top .hero{min-height:100vh}
.st [data-at]{opacity:1;transform:none}.st .flow .steps li{opacity:1}.st .flow .steps p{max-height:none;opacity:1}
@media(max-width:860px){.hd-menu{display:block}.fl{grid-template-columns:1fr}.fl h2{font-size:24px;margin-bottom:12px}.ks{min-height:200px;padding:20px;margin-bottom:10px}.kr{height:70px}.flow .steps li{padding:5px 0}.flow .steps p{font-size:14px}#top .hero{align-content:start}#top .stage{display:none}}
</style>
</head>
<body>
<header><b>FLOWAY</b><nav aria-label="페이지 메뉴"><a href="#problem">문제</a><a href="#how">작동 원리</a><a href="#product">제품</a><a href="#flow">이용 과정</a><a href="#scale">설치</a><a href="#design">디자인</a></nav><button class="hd-menu" id="mo">Menu</button></header>
<div id="bar"></div>
<div class="mnav" id="mn"><button id="mc">Close</button><a href="#problem">문제</a><a href="#how">작동 원리</a><a href="#product">제품</a><a href="#flow">이용 과정</a><a href="#design">디자인</a></div>
<main>
<section class="pin" id="top" data-pin style="--h:460"><div class="sticky"><canvas id="cv" aria-hidden="true"></canvas><div class="hero">
 <div>
  <h1>FLOWAY<span>붐비는 길 대신, 지금 흐르는 길을 안내한다</span></h1>
  <p class="lead" data-at=".3">같은 거리를 두 개의 지도로 보여 주고, 혼잡을 서로 다르게 해석해 인파를 자연스럽게 분산시킵니다.</p>
  <div class="seg" data-at=".38" role="group" aria-label="방문자 모드 선택"><button id="mT" aria-pressed="true">관광객 모드</button><button id="mL" aria-pressed="false">내국인 모드</button></div>
  <p class="hint" data-at=".44">모드를 바꿔 보세요. 단말기 화면이 같은 데이터를 다르게 보여 줍니다.</p>
 </div>
 <div class="stage" aria-label="안내 단말기 일러스트">
  <svg viewBox="0 0 300 500" role="img" aria-label="화면, 세 개의 버튼, 곡선형 본체를 가진 안내 단말기">
   <path d="M92 250 C80 320 96 380 92 490 H208 C204 380 220 320 208 250Z" fill="#f7f5e8" stroke="#292929" stroke-width="2.5"/>
   <path d="M208 250 C220 320 204 380 208 490" fill="none" stroke="#e9be5f" stroke-width="7"/>
   <path d="M56 70 Q56 22 104 22 H226 Q252 22 252 48 V58 H236 V50 H104 V70Z" fill="#292929"/>
   <rect x="56" y="22" width="26" height="198" rx="6" fill="#292929"/>
   <rect x="82" y="62" width="148" height="152" rx="6" fill="#f7f5e8" stroke="#292929" stroke-width="2"/>
   <path d="M90 190 Q130 150 160 168 T222 92" fill="none" stroke="#646661" stroke-width="3" stroke-dasharray="3 6" id="routeLine"/>
   <circle class="dot" id="d1" cx="130" cy="150" r="14" fill="#e9be5f"/>
   <circle class="dot" id="d2" cx="180" cy="118" r="22" fill="#292929"/>
   <circle class="dot" id="d3" cx="112" cy="104" r="10" fill="#e9be5f"/>
   <text id="scrText" x="156" y="82" text-anchor="middle" font-size="11" font-weight="700" fill="#292929">필수 코스</text>
   <text id="scrSub" x="156" y="204" text-anchor="middle" font-size="10" fill="#646661">대체 스팟과 함께 안내</text>
   <rect x="56" y="222" width="190" height="16" rx="8" fill="#f5e7b6" stroke="#292929" stroke-width="2"/>
   <rect x="82" y="225" width="14" height="10" rx="3" fill="#fff" stroke="#292929"/>
   <circle cx="151" cy="230" r="8" fill="#e9be5f" stroke="#292929" stroke-width="2"/>
   <circle cx="208" cy="230" r="6" fill="#fff" stroke="#292929"/>
   <ellipse cx="150" cy="492" rx="80" ry="7" fill="#292929" opacity=".15"/>
  </svg>
 </div>
</div><div class="cue" aria-hidden="true">SCROLL</div></div></section>

<section id="how"><div class="wrap">
 <h2>Sense. Decide. Respond.</h2>
 <p class="lead">세 가지 정보를 합쳐, 지금 흐르는 길을 골라 줍니다.</p>
 <div class="trio">
  <div><small>입력 정보</small><h3>언어 선택 · 혼잡 센서 · 가게 주문 데이터(POS)</h3><p>누가 왔는지, 거리가 얼마나 붐비는지, 가게가 얼마나 바쁜지를 한꺼번에 읽습니다.</p></div>
  <div><small>AI 판단</small><h3>관광객 · 내국인에 맞춰 경로를 나눠 고른다</h3><p>붐비는 구간을 피한 경로를 방문자 유형별로 나눠 고릅니다.</p></div>
  <div><small>물리적 반응</small><h3>화면에 길을 그리고, QR로 휴대폰에 옮겨 준다</h3><p>단말기 앞에서는 길을 보여 주고, 이동 중에는 휴대폰이 이어받습니다.</p></div>
 </div>
</div></section>

<section class="problem pin" id="problem" data-pin style="--h:300"><div class="sticky"><div class="wrap">
 <h2>When everyone goes the same way, the street clogs.</h2>
 <p class="lead">명동에서는 인기 가게와 포토스팟 앞이 통행로까지 이어집니다. 누구도 나쁘지 않은데 모두가 불편해집니다.</p>
 <div class="situ">
  <p data-at=".2"><small>관광객</small>인기 가게와 포토스팟에 몰려 통행로가 막힘</p>
  <p data-at=".45"><small>내국인</small>혼잡 구간을 피해 가는 방법을 알기 어려움</p>
  <p data-at=".7"><small>상인</small>조리, 계산, 응대로 바빠 주변 상황을 살필 여유가 없음</p>
 </div>
</div></div></section>

<section id="issues"><div class="wrap">
 <h2>Guidance should never create a new crowd.</h2>
 <p class="lead">안내 제품이 오히려 병목이 될 수 있습니다. 네 가지 위험을 설계 단계에서 먼저 풀었습니다.</p>
 <div class="rows">
  <div class="row head"><span>문제점</span><span>왜 문제인가</span><span>해결 방향</span></div>
  <div class="row"><h3>단말기 앞 쏠림</h3><p>혼잡을 줄이는 제품이 통행로에 줄과 정체를 만든다.</p><p class="fix">여러 입구에 분산 배치</p></div>
  <div class="row"><h3>상인 추가 부담</h3><p>불빛 상태를 직접 바꾸면 바쁜 상인에게 일만 늘고, 인기 가게는 노출이 줄 수 있다.</p><p class="fix">주문 연동 자동화, 시간대별 순환 추천</p></div>
  <div class="row"><h3>경로 쏠림</h3><p>모두에게 같은 우회로를 알려주면 그곳이 다시 혼잡해진다.</p><p class="fix">단말기 간 연동으로 우회로 수용 인원을 계산해 사람마다 다른 경로 배분</p></div>
  <div class="row"><h3>이동 중 안내 단절</h3><p>단말기 앞에서만 안내되고 이후 동선은 도움이 없다.</p><p class="fix">QR로 개인 휴대폰에 경로 전달, 상황 변화 시 알림으로 재안내</p></div>
 </div>
</div></section>

<section id="product" style="background:var(--sand)"><div class="wrap">
 <h2>Two maps of one street.</h2>
 <p class="lead">같은 거리를 두 개의 지도로 보여 주고, 혼잡을 서로 다르게 해석해 인파를 자연스럽게 분산시키는 거리 안내 단말기입니다.</p>
 <div class="four">
  <div><h3>거리 혼잡도 분석</h3><p>익명 센서와 가게 불빛 상태를 합쳐 거리 구간별 혼잡도를 실시간으로 판단합니다.</p></div>
  <div><h3>방문자 유형별 지도</h3><p>언어 선택에 따라 관광객 모드와 내국인 모드로 시작하고, 같은 데이터를 다르게 해석해 보여 줍니다.</p></div>
  <div><h3>분산 경로 추천</h3><p>혼잡한 구간은 대체 스팟과 우회 경로를 함께 안내해 인파를 자연스럽게 나눕니다.</p></div>
  <div><h3>상인 부담 감소</h3><p>가게 주변이 혼잡해지지 않습니다.</p></div>
 </div>
</div></section>

<section class="flow pin" id="flow" data-pin style="--h:520"><div class="sticky"><div class="wrap fl">
 <h2>Ten seconds at the kiosk. The rest on your phone.</h2>
 <div class="ks" id="ks"><div><small id="ksT"></small><b id="ksM"></b></div><div class="kr"><div class="bars" id="bars"><i></i><i></i><i></i><i></i><i></i></div><div class="qr" id="qr"></div></div></div>
 <ol class="steps">
  <li><h3>안내 필요 발생</h3><p>방문자가 입구에서 길과 먹거리를 찾으려 한다. 단말기는 통행로 옆에 여러 곳 분산 설치되어 있어 줄 없이 접근할 수 있다.</p></li>
  <li><h3>모드 선택</h3><p>원터치로 언어와 방문자 모드(관광객/내국인)를 각각 고른다. 선택은 10초 안에 끝난다.</p></li>
  <li><h3>혼잡 상태 분석</h3><p>단말기가 센서와 가게 주문 데이터(POS)를 합쳐 구간별 혼잡도를 확인한다. 상인이 따로 조작할 필요가 없다.</p></li>
  <li><h3>분산 경로 추천</h3><p>관광객에게는 필수 코스와 대체 스팟을, 내국인에게는 우회 경로와 한산한 가게를 보여 준다. 우회로 수용 인원을 계산해 사람마다 다른 경로를 배분한다.</p></li>
  <li><h3>휴대폰 연동과 이동</h3><p>추천 경로를 QR로 휴대폰에 넘기고 단말기 앞을 바로 떠난다. 이동 중 혼잡이 바뀌면 알림으로 경로를 다시 제안한다.</p></li>
  <li><h3>상태 갱신</h3><p>사용이 끝나면 화면이 초기화되고, 가게 주문 상황이 지도에 자동 반영된다. 인기 가게와 한산한 가게는 시간대별로 번갈아 추천된다.</p></li>
 </ol>
</div></div></section>

<section id="scale"><div class="wrap scale">
 <div>
  <h2>Two sizes to cover the whole street.</h2>
  <p class="lead">소형은 촘촘하게, 대형은 핵심 지점에만 둡니다.</p>
  <div class="seg" style="margin-top:26px" role="group" aria-label="설치 규모 선택"><button id="sS" aria-pressed="true">소형</button><button id="sL" aria-pressed="false">대형</button></div>
 </div>
 <dl id="specs" aria-live="polite"></dl>
</div></section>

<section class="cmf" id="design"><div class="wrap">
 <h2>Contrast, set on a curve.</h2>
 <div class="kw"><span>Organic 유기적인</span><span>Fluid 유동적인</span><span>Dynamic 역동적인</span><span>Contrasting 대조적인</span></div>
 <div class="sw" role="list" aria-label="색상 팔레트">
  <div role="listitem" style="background:#292929;border:1px solid #646661;color:#f7f5e8">292929</div>
  <div role="listitem" style="background:#646661;color:#f7f5e8">646661</div>
  <div role="listitem" style="background:#e9be5f">E9BE5F</div>
  <div role="listitem" style="background:#f5e7b6">F5E7B6</div>
  <div role="listitem" style="background:#f7f5e8">F7F5E8</div>
 </div>
 <p>유기적인 곡면 형상에 차콜 프레임과 아이보리 본체를 대비시키고, 골드 포인트로 조작부를 찾기 쉽게 만들었습니다.</p>
</div></section>

<section><div class="wrap model">
 <svg viewBox="0 0 300 380" role="img" aria-label="단말기 조작부 확대: QR 생성, 메인 액션, 언어 변경 버튼">
  <rect x="30" y="140" width="240" height="70" rx="35" fill="#f5e7b6" stroke="#292929" stroke-width="3"/>
  <rect x="62" y="160" width="32" height="30" rx="8" fill="#fff" stroke="#292929" stroke-width="3"/>
  <rect x="70" y="167" width="16" height="16" fill="none" stroke="#292929" stroke-width="2"/>
  <circle cx="150" cy="175" r="26" fill="#e9be5f" stroke="#292929" stroke-width="3"/>
  <circle cx="150" cy="175" r="16" fill="#f3cf7a"/>
  <rect x="206" y="160" width="32" height="30" rx="8" fill="#fff" stroke="#292929" stroke-width="3"/>
  <path d="M214 172 a8 8 0 0 1 14 -2 M230 178 a8 8 0 0 1 -14 2" fill="none" stroke="#292929" stroke-width="2"/>
  <text x="78" y="240" text-anchor="middle" font-size="13" font-weight="700" fill="#292929">QR 생성</text>
  <text x="150" y="252" text-anchor="middle" font-size="13" font-weight="700" fill="#292929">메인 액션</text>
  <text x="222" y="240" text-anchor="middle" font-size="13" font-weight="700" fill="#292929">언어 변경</text>
 </svg>
 <div>
  <h2>Just three buttons.</h2>
  <ul class="btns">
   <li><i>QR</i>QR 생성 — 추천 경로를 내 휴대폰으로 가져갑니다.</li>
   <li><i></i>메인 액션 — 큰 골드 버튼으로 안내를 시작하고 확정합니다.</li>
   <li><i>A</i>언어 변경 — 언어를 바꾸면 방문자 모드도 함께 정해집니다.</li>
  </ul>
 </div>
</div></section>
</main>
<footer><h2>Same street, different paths.</h2><p>FLOWAY</p></footer>
<script>
const $=id=>document.getElementById(id);
const modes={
 T:{t:'필수 코스',s:'대체 스팟과 함께 안내',c:['#e9be5f','#292929','#e9be5f'],r:['14','22','10']},
 L:{t:'우회 경로',s:'한산한 가게 먼저 안내',c:['#292929','#e9be5f','#f5e7b6'],r:['22','12','16']}
};
function setMode(k){
 const m=modes[k];
 $('scrText').textContent=m.t;$('scrSub').textContent=m.s;
 ['d1','d2','d3'].forEach((id,i)=>{$(id).setAttribute('fill',m.c[i]);$(id).setAttribute('r',m.r[i])});
 $('mT').setAttribute('aria-pressed',k==='T');$('mL').setAttribute('aria-pressed',k==='L');
}
$('mT').onclick=()=>setMode('T');$('mL').onclick=()=>setMode('L');
const spec={
 S:[['역할','현재 위치 확인과 빠른 안내'],['설치 위치','골목 안쪽, 가게 앞, 갈림길'],['화면 구성','현재 구간 혼잡도, 가까운 한산한 가게'],['이용 방식','5초 확인, 서서 보는 시간 최소화'],['QR 연동','현재 구간 정보만 전달'],['설치 밀도','많이 (촘촘하게)']],
 L:[['역할','거리 전체 혼잡 현황과 종합 안내'],['설치 위치','거리 입구, 지하철역 출구, 주요 광장'],['화면 구성','거리 전체 지도, 두 모드 지도 동시 표시'],['이용 방식','여러 명이 함께 보는 대형 화면'],['QR 연동','전체 코스 전달'],['설치 밀도','적게 (핵심 지점만)']]
};
function setScale(k){
 $('specs').innerHTML=spec[k].map(r=>'<div><dt>'+r[0]+'</dt><dd>'+r[1]+'</dd></div>').join('');
 $('sS').setAttribute('aria-pressed',k==='S');$('sL').setAttribute('aria-pressed',k==='L');
}
$('sS').onclick=()=>setScale('S');$('sL').onclick=()=>setScale('L');
setScale('S');

</script>
<script>
(()=>{
const g=id=>document.getElementById(id),R=matchMedia('(prefers-reduced-motion:reduce)').matches;
if(R)document.documentElement.classList.add('st');
const E=(a,b,x)=>{x=Math.min(1,Math.max(0,(x-a)/(b-a)));return x*x*(3-2*x)};
const pins=[...document.querySelectorAll('[data-pin]')].map(el=>({el,n:[...el.querySelectorAll('[data-at]')]}));
const hd=document.querySelector('header'),bar=g('bar'),dk=[...document.querySelectorAll('.problem,.cmf')],top=g('top');
let K=R?1:0,S=R?1:0,lane=0,cur=-1;
/* dot street */
const cv=g('cv'),cx=cv.getContext('2d');let W=0,H=0;
const D=Array.from({length:120},(_,i)=>({x:Math.random(),o:Math.random()*2-1,v:.5+Math.random()*.7,l:i%2}));
const rs=()=>{const r=devicePixelRatio||1;W=cv.clientWidth;H=cv.clientHeight;cv.width=W*r;cv.height=H*r;cx.setTransform(r,0,0,r,0,0)};
addEventListener('resize',rs);rs();
g('mT').addEventListener('click',()=>lane=0);g('mL').addEventListener('click',()=>lane=1);
let last=0;
function draw(t){
 const dt=R?0:Math.min(.05,(t-last)/1000||0);last=t;cx.clearRect(0,0,W,H);
 const yc=H-70,yb=H-140,r=Math.round(247-206*K),gg=Math.round(245-204*K),b=Math.round(232-191*K),col=r+','+gg+','+b;
 cx.lineWidth=1;cx.strokeStyle='rgba('+col+',.22)';
 cx.beginPath();cx.moveTo(0,yc-26);cx.lineTo(W,yc-26);cx.moveTo(0,yc+26);cx.lineTo(W,yc+26);cx.stroke();
 cx.setLineDash([4,8]);cx.strokeStyle='rgba(233,190,95,'+.7*S+')';cx.beginPath();cx.moveTo(0,yb);cx.lineTo(W,yb);cx.stroke();cx.setLineDash([]);
 D.forEach(d=>{
  d.x=(d.x+dt*(.015+.06*S)*d.v)%1;
  const y=yc+d.l*(yb-yc)*S+d.o*(22-12*S),a=1-(1-(d.l===lane?1:.28))*S;
  cx.globalAlpha=a;cx.fillStyle=d.l?'rgb('+col+')':'#e9be5f';
  cx.beginPath();cx.arc(d.x*(W+40)-20,y,4.5,0,6.283);cx.fill();
 });cx.globalAlpha=1;
}
/* kiosk steps */
const F=[['01 안내 필요','길과 먹거리를 찾는 방문자',[30,45,80,40,55],0],['02 모드 선택','한국어 · 관광객 모드',[30,45,80,40,55],0],['03 혼잡 분석','센서 + POS로 구간별 혼잡도',[35,90,60,25,70],0],['04 경로 추천','붐비는 구간은 대체 스팟으로',[35,90,35,25,40],0],['05 QR 전송','추천 경로가 휴대폰으로',[35,60,35,25,40],1],['06 상태 갱신','화면 초기화, 시간대별 순환 추천',[40,45,50,40,45],0]];
const li=[...document.querySelectorAll('.flow .steps li')],bars=[...g('bars').children];
g('qr').innerHTML=Array.from({length:25},(_,i)=>'<i'+([1,3,6,8,12,16,18,20,22,24].includes(i)?' class="z"':'')+'></i>').join('');
function flow(i){
 if(i===cur)return;cur=i;const f=F[i];
 li.forEach((l,j)=>l.classList.toggle('on',j===i));
 g('ksT').textContent=f[0];g('ksM').textContent=f[1];
 g('ksM').animate([{opacity:0,transform:'translateY(10px)'},{opacity:1,transform:'none'}],{duration:400});
 bars.forEach((e,j)=>{e.style.height=f[2][j]+'%';e.style.background=f[2][j]>=80?'#f7f5e8':''});
 g('ks').classList.toggle('q',!!f[3]);
}
flow(0);
function tick(t){
 const vh=innerHeight;
 pins.forEach(({el,n})=>{
  const r=el.getBoundingClientRect();if(r.bottom<-50||r.top>vh+50)return;
  const p=R?1:Math.min(1,Math.max(0,-r.top/(r.height-vh)));
  el.style.setProperty('--p',p);
  n.forEach(e=>e.classList.toggle('on',R||p>=+e.dataset.at));
  if(el===top){K=R?1:E(.12,.45,p);S=R?1:E(.45,.85,p);el.style.setProperty('--k',K);el.style.setProperty('--t',R?1:E(.08,.4,p))}
  if(el.id==='flow'&&!R)flow(Math.min(5,Math.floor(p*6)));
 });
 const tr=top.getBoundingClientRect();
 if(tr.bottom>0)draw(t);
 hd.classList.toggle('dk',(tr.top<=30&&tr.bottom>30&&K<.5)||dk.some(e=>{const q=e.getBoundingClientRect();return q.top<=30&&q.bottom>30}));
 bar.style.transform='scaleX('+scrollY/Math.max(1,document.documentElement.scrollHeight-innerHeight)+')';
 requestAnimationFrame(tick);
}
requestAnimationFrame(tick);
/* menu */
const mn=g('mn');g('mo').onclick=()=>mn.classList.add('o');g('mc').onclick=()=>mn.classList.remove('o');mn.querySelectorAll('a').forEach(a=>a.onclick=()=>mn.classList.remove('o'));
/* three buttons pulse in turn */
if(!R){
 const L=[...document.querySelectorAll('.btns li')],tg=['rect[x="62"]','circle[r="26"]','rect[x="206"]'].map(q=>document.querySelector('.model svg '+q));
 let vis=false,c=0;new IntersectionObserver(e=>vis=e[0].isIntersecting).observe(document.querySelector('.model'));
 setInterval(()=>{if(!vis)return;L.forEach((l,i)=>l.classList.toggle('hl',i===c));tg.forEach((e,i)=>{e.classList.remove('pop');if(i===c){void e.getBoundingClientRect();e.classList.add('pop')}});c=(c+1)%3},1700);
}
})();
</script>
</body>
</html>
