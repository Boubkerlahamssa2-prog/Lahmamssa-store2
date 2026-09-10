<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>ملبس — كلشي للعائلة</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Lalezar&family=Almarai:wght@300;400;700;800&display=swap" rel="stylesheet">
<style>
  :root{
    --charcoal:#1c1a17;
    --charcoal-2:#2a2521;
    --stone:#efe9df;
    --cream:#f9f6f0;
    --ochre:#c98a2c;
    --ochre-dark:#a86f1e;
    --rust:#8b3a2b;
    --line:#d8cfbf;
  }
  *{margin:0;padding:0;box-sizing:border-box;}
  body{
    font-family:'Almarai',sans-serif;
    background:var(--cream);
    color:var(--charcoal);
    line-height:1.7;
  }
  h1,h2,h3,.brand{font-family:'Lalezar',sans-serif; font-weight:400; letter-spacing:.5px;}

  /* ===== TOP BAR ===== */
  .topbar{
    background:var(--charcoal);
    color:var(--stone);
    font-size:.85rem;
    text-align:center;
    padding:.5rem 1rem;
  }

  /* ===== HEADER ===== */
  header{
    background:var(--cream);
    border-bottom:2px solid var(--charcoal);
    padding:1.2rem 1.5rem;
    display:flex;
    align-items:center;
    justify-content:space-between;
    flex-wrap:wrap;
    gap:1rem;
  }
  .brand{font-size:2rem; color:var(--charcoal);}
  nav{display:flex; gap:1.8rem; font-weight:700; font-size:1rem;}
  nav a{color:var(--charcoal); text-decoration:none; border-bottom:2px solid transparent; padding-bottom:2px; transition:border-color .15s;}
  nav a:hover{border-color:var(--ochre);}

  /* ===== HERO ===== */
  .hero{
    background:
      repeating-linear-gradient(135deg, var(--charcoal-2) 0 2px, var(--charcoal) 2px 40px);
    color:var(--cream);
    padding:5rem 1.5rem 4rem;
    text-align:center;
    position:relative;
    overflow:hidden;
  }
  .hero h1{
    font-size:clamp(2.6rem, 7vw, 5rem);
    color:var(--stone);
    line-height:1.15;
  }
  .hero h1 em{font-style:normal; color:var(--ochre);}
  .hero p{
    max-width:520px;
    margin:1.2rem auto 2rem;
    font-size:1.15rem;
    color:#cfc6b8;
  }
  .hero .cta-row{display:flex; gap:1rem; justify-content:center; flex-wrap:wrap;}
  .btn{
    display:inline-block;
    padding:.9rem 1.8rem;
    border-radius:2px;
    font-weight:700;
    text-decoration:none;
    font-size:1rem;
    transition:transform .15s, background .15s;
  }
  .btn-solid{background:var(--ochre); color:var(--charcoal);}
  .btn-solid:hover{background:var(--stone); transform:translateY(-2px);}
  .btn-outline{border:2px solid var(--stone); color:var(--stone);}
  .btn-outline:hover{background:var(--stone); color:var(--charcoal);}

  /* ===== TRUST STRIP ===== */
  .trust{
    display:flex; flex-wrap:wrap; justify-content:center; gap:0;
    background:var(--stone);
    border-bottom:2px solid var(--charcoal);
  }
  .trust div{
    flex:1 1 220px;
    text-align:center;
    padding:1rem .8rem;
    font-weight:700;
    font-size:.95rem;
    border-left:1px solid var(--line);
  }

  /* ===== CATEGORIES ===== */
  .categories{
    max-width:1200px;
    margin:0 auto;
    padding:4rem 1.5rem 2rem;
  }
  .categories h2{font-size:2.2rem; margin-bottom:.4rem;}
  .categories .lead{color:#5c5347; margin-bottom:2.2rem; max-width:480px;}
  .cat-grid{
    display:grid;
    grid-template-columns:2fr 1fr;
    grid-template-rows:auto auto;
    gap:1.2rem;
  }
  .cat-card{
    position:relative;
    border-radius:4px;
    overflow:hidden;
    min-height:220px;
    display:flex; align-items:flex-end;
    padding:1.6rem;
    color:var(--cream);
  }
  .cat-card::after{
    content:'';
    position:absolute; inset:0;
    background:linear-gradient(0deg, rgba(0,0,0,.55), rgba(0,0,0,.05));
    z-index:0;
  }
  .cat-card span{position:relative; z-index:1; font-family:'Lalezar',sans-serif; font-size:1.6rem;}
  .cat-men{background:var(--charcoal); grid-row:1 / 3;}
  .cat-women{background:var(--rust);}
  .cat-kids{background:var(--ochre-dark);}

  /* ===== PRODUCTS ===== */
  .products{
    background:var(--stone);
    padding:4rem 1.5rem;
  }
  .products-inner{max-width:1200px; margin:0 auto;}
  .products h2{font-size:2.2rem; margin-bottom:2rem; text-align:center;}
  .product-grid{
    display:grid;
    grid-template-columns:repeat(auto-fit, minmax(230px, 1fr));
    gap:1.6rem;
  }
  .product{
    background:var(--cream);
    border:1px solid var(--line);
  }
  .swatch{
    height:220px;
    display:flex; align-items:center; justify-content:center;
    font-size:3rem;
  }
  .swatch-1{background:#7c6a55;}
  .swatch-2{background:#a13d2b;}
  .swatch-3{background:#33463b;}
  .swatch-4{background:#2c3e50;}
  .swatch-5{background:#c9a15f;}
  .swatch-6{background:#4a3b52;}
  .product-info{padding:1rem 1.1rem 1.3rem;}
  .product-info h3{font-family:'Almarai',sans-serif; font-weight:700; font-size:1.05rem; margin-bottom:.3rem;}
  .product-info .price{color:var(--ochre-dark); font-weight:800; font-size:1.15rem; margin-bottom:.7rem;}
  .order-btn{
    display:block;
    text-align:center;
    background:var(--charcoal);
    color:var(--cream);
    padding:.6rem;
    text-decoration:none;
    font-weight:700;
    font-size:.9rem;
  }
  .order-btn:hover{background:var(--ochre-dark);}

  /* ===== HOW IT WORKS ===== */
  .how{
    max-width:900px;
    margin:0 auto;
    padding:4rem 1.5rem;
  }
  .how h2{text-align:center; font-size:2.2rem; margin-bottom:2.5rem;}
  .steps{display:flex; flex-wrap:wrap; gap:1.5rem; justify-content:center;}
  .step{flex:1 1 220px; text-align:center;}
  .step .n{
    width:46px; height:46px; border-radius:50%;
    background:var(--ochre); color:var(--charcoal);
    display:flex; align-items:center; justify-content:center;
    font-weight:800; margin:0 auto .8rem;
  }

  /* ===== FOOTER ===== */
  footer{
    background:var(--charcoal);
    color:#cfc6b8;
    padding:3rem 1.5rem 1.5rem;
    text-align:center;
  }
  footer .brand{color:var(--cream); font-size:1.6rem; margin-bottom:.5rem;}
  footer .wa{
    display:inline-block; margin:1rem 0 2rem;
    background:var(--ochre); color:var(--charcoal);
    padding:.8rem 2rem; text-decoration:none; font-weight:700;
  }
  footer small{display:block; margin-top:1.5rem; color:#8a8276; border-top:1px solid #3a352e; padding-top:1.2rem;}

  @media (max-width:640px){
    nav{gap:1rem; font-size:.9rem; width:100%; justify-content:center;}
    .cat-grid{grid-template-columns:1fr;}
    .cat-men{grid-row:auto;}
    .trust div{border-left:none; border-bottom:1px solid var(--line);}
  }
</style>
</head>
<body>

<div class="topbar">توصيل لجميع مدن المغرب 🚚 — الدفع عند الاستلام متوفر</div>

<header>
  <div class="brand">ملبس</div>
  <nav>
    <a href="#men">رجال</a>
    <a href="#women">نساء</a>
    <a href="#kids">أطفال</a>
    <a href="#contact">تواصل معنا</a>
  </nav>
</header>

<section class="hero">
  <h1>لباس <em>لكل</em><br>أفراد العائلة</h1>
  <p>قطع مختارة بعناية، بأسعار فالمتناول، وتوصيل لباب الدار فجميع المدن المغربية.</p>
  <div class="cta-row">
    <a href="#products" class="btn btn-solid">شوف المنتجات</a>
    <a href="#contact" class="btn btn-outline">تواصل معنا</a>
  </div>
</section>

<div class="trust">
  <div>✅ جودة مضمونة</div>
  <div>💵 الدفع عند الاستلام</div>
  <div>🚚 توصيل سريع</div>
  <div>🔄 إمكانية التبديل</div>
</div>

<section class="categories">
  <h2>تسوق حسب الفئة</h2>
  <p class="lead">مجموعات مختارة للرجال، النساء، والأطفال — تحدث بانتظام.</p>
  <div class="cat-grid">
    <a class="cat-card cat-men" href="#men"><span>ملابس رجالية</span></a>
    <a class="cat-card cat-women" href="#women"><span>ملابس نسائية</span></a>
    <a class="cat-card cat-kids" href="#kids"><span>ملابس أطفال</span></a>
  </div>
</section>

<section class="products" id="products">
  <div class="products-inner">
    <h2>الأكثر طلبًا هاد الأسبوع</h2>
    <div class="product-grid">

      <div class="product">
        <div class="swatch swatch-1">👕</div>
        <div class="product-info">
          <h3>قميص رجالي كاجوال</h3>
          <div class="price">149 درهم</div>
          <a class="order-btn" href="#contact">اطلب عبر واتساب</a>
        </div>
      </div>

      <div class="product">
        <div class="swatch swatch-2">👗</div>
        <div class="product-info">
          <h3>فستان صيفي نسائي</h3>
          <div class="price">219 درهم</div>
          <a class="order-btn" href="#contact">اطلب عبر واتساب</a>
        </div>
      </div>

      <div class="product">
        <div class="swatch swatch-3">🧥</div>
        <div class="product-info">
          <h3>جاكيت شتوي</h3>
          <div class="price">329 درهم</div>
          <a class="order-btn" href="#contact">اطلب عبر واتساب</a>
        </div>
      </div>

      <div class="product">
        <div class="swatch swatch-4">👖</div>
        <div class="product-info">
          <h3>سروال جينز رجالي</h3>
          <div class="price">179 درهم</div>
          <a class="order-btn" href="#contact">اطلب عبر واتساب</a>
        </div>
      </div>

      <div class="product">
        <div class="swatch swatch-5">🧒</div>
        <div class="product-info">
          <h3>طقم أطفال (2 قطع)</h3>
          <div class="price">99 درهم</div>
          <a class="order-btn" href="#contact">اطلب عبر واتساب</a>
        </div>
      </div>

      <div class="product">
        <div class="swatch swatch-6">🧣</div>
        <div class="product-info">
          <h3>وشاح + قفازات</h3>
          <div class="price">89 درهم</div>
          <a class="order-btn" href="#contact">اطلب عبر واتساب</a>
        </div>
      </div>

    </div>
  </div>
</section>

<section class="how">
  <h2>كيفاش تطلب؟</h2>
  <div class="steps">
    <div class="step">
      <div class="n">1</div>
      <p>اختار القطعة اللي عجبتك من المنتجات</p>
    </div>
    <div class="step">
      <div class="n">2</div>
      <p>تواصل معنا عبر واتساب وأعطينا المقاس والمدينة</p>
    </div>
    <div class="step">
      <div class="n">3</div>
      <p>خلص عند التوصيل — بلا مخاطرة</p>
    </div>
  </div>
</section>

<footer id="contact">
  <div class="brand">ملبس</div>
  <p>عندك سؤال على مقاس أو منتج؟ راسلنا مباشرة.</p>
  <a class="wa" href="https://wa.me/212600000000" target="_blank">تواصل عبر واتساب 💬</a>
  <small>© 2026 ملبس — جميع الحقوق محفوظة</small>
</footer>

</body>
</html>
