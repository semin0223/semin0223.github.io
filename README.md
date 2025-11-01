<!DOCTYPE html>
<html lang="ko">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>흥해라흥 픽쳐스</title>
<link href="https://fonts.googleapis.com/css2?family=Nanum+Gothic:wght@400;700&display=swap" rel="stylesheet">
<style>
body {
  font-family: 'Nanum Gothic', Arial, sans-serif;
  margin:0;
  padding:0;
  background: linear-gradient(135deg, #fdf6f0, #e0f7fa);
  color:#222;
}

/* 헤더 */
h1 {
  text-align:center;
  margin-top:20px;
  font-size:2.5em;
  text-shadow: 1px 1px 2px rgba(0,0,0,0.2);
}
h2 {
  margin-bottom:15px;
  font-size:1.8em;
  color:#e11d48;
}

/* 섹션 */
.section {
  display:none;
  padding:40px 20px;
  margin:20px auto;
  max-width:900px;
  background:#fff;
  border-radius:12px;
  box-shadow:0 6px 20px rgba(0,0,0,0.1);
  transition: all 0.3s ease-in-out;
}
.section.active { display:block; }

/* 네비게이션 */
nav {
  position:fixed; top:15px; right:20px;
  background:#fff;
  padding:12px 18px;
  border-radius:12px;
  box-shadow:0 4px 12px rgba(0,0,0,0.15);
  z-index:1000;
}
nav a {
  margin:0 10px;
  text-decoration:none;
  color:#e11d48;
  font-weight:bold;
  cursor:pointer;
  transition: color 0.3s;
}
nav a:hover { color:#b91c1c; }

/* 영상 */
iframe {
  width:100%;
  height:315px;
  border-radius:10px;
  margin-bottom:20px;
  box-shadow:0 4px 12px rgba(0,0,0,0.1);
}

/* 굿즈 */
.product {
  border:1px solid #ddd;
  padding:20px;
  border-radius:10px;
  text-align:center;
  display:inline-block;
  margin:15px;
  background:#fafafa;
  min-width:220px;
  box-shadow:0 4px 12px rgba(0,0,0,0.08);
  transition: transform 0.3s, box-shadow 0.3s;
}
.product:hover {
  transform: translateY(-5px);
  box-shadow:0 8px 20px rgba(0,0,0,0.15);
}
.btn {
  display:inline-block;
  padding:10px 15px;
  background:#e11d48;
  color:#fff;
  border-radius:6px;
  text-decoration:none;
  margin-top:10px;
  font-weight:bold;
  transition: background 0.3s, transform 0.2s;
}
.btn:hover {
  background:#b91c1c;
  transform: scale(1.05);
}

/* 반응형 */
@media (max-width:768px){
  iframe { height:220px; }
}
@media (max-width:480px){
  .product { min-width:150px; margin:10px; padding:15px; }
}
</style>
</head>
<body>

<h1>흥해라흥 픽쳐스</h1>

<nav>
  <a onclick="showSection('about')">소개</a>
  <a onclick="showSection('video')">영상</a>
  <a onclick="showSection('shop')">굿즈 샵</a>
</nav>

<section id="about" class="section active">
  <h2>소개 / About</h2>
  <p>안녕하세요! 흥해라흥 픽쳐스입니다. 저희는 다양한 영상 콘텐츠를 제작하고 있으며, 여러분께 즐거움을 선사하고자 합니다. 아래에서 저희의 영상을 만나보세요!</p>
</section>

<section id="video" class="section">
  <h2>영상 / Video</h2>
  <iframe src="https://www.youtube.com/embed/6hY1AJ_cVMO" title="흥해라흥 영상 1" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
  <iframe src="https://www.youtube.com/embed/3DNaj8R4HJg" title="흥해라흥 영상 2" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</section>

<section id="shop" class="section">
  <h2>Shop / 굿즈 샵</h2>
  <div class="product">
    <p>호팔이 마그넷</p>
    <a href="https://www.coupang.com/vp/products/8468475865?itemId=24501252472&vendorItemId=91514332584" class="btn" target="_blank">구매 / Buy</a>
  </div>
</section>

<script>
function showSection(id) {
  const sections = document.querySelectorAll('.section');
  sections.forEach(sec => sec.classList.remove('active'));
  document.getElementById(id).classList.add('active');
}
</script>

</body>
</html>
