<!DOCTYPE html>
<html lang="ru"><head>
  <meta charset="UTF-8">
  <title>Мир хомяков</title>
  <style>
    *,*::before,*::after{margin:0;padding:0;box-sizing:border-box;}
    body{font-family:'Segoe UI',sans-serif;background:linear-gradient(135deg,#f9d4c3,#f5b78f);color:#554236;line-height:1.6;min-height:100vh;padding-bottom:60px;}
    header{text-align:center;padding:2rem 1rem;background:rgba(255,215,175,0.9);border-bottom:3px solid #e6a173;}
    h1{font-size:2.5rem;color:#8c5e4c;text-shadow:1px 1px 2px rgba(0,0,0,0.1);}
    h2{color:#a67c52;margin:1.5rem 0 1rem;font-size:1.4rem;}
    .container{max-width:1100px;margin:0 auto;padding:0 1rem;}
    .section{background:rgba(255,255,255,0.85);border-radius:15px;padding:1.5rem;margin:1.5rem 0;box-shadow:0 5px 15px rgba(0,0,0,0.1);animation:fadeUp 0.8s ease forwards;opacity:0;}
    @keyframes fadeUp{to{opacity:1;transform:translateY(0);}}
    p{margin-bottom:1rem;}
    ul{padding-left:1.2rem;margin:1rem 0;}
    li{margin:0.5rem 0;}
    .grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:1.2rem;margin:1.2rem 0;}
    .card{border-radius:12px;overflow:hidden;box-shadow:0 4px 10px rgba(0,0,0,0.15);transition:transform 0.3s,box-shadow 0.3s;}
    .card:hover{transform:translateY(-5px);box-shadow:0 8px 20px rgba(0,0,0,0.2);}
    .card img{width:100%;height:180px;object-fit:cover;}
    .card-content{padding:1rem;background:#fff;}
    footer{text-align:center;padding:1.5rem;background:#8c5e4c;color:white;position:fixed;bottom:0;width:100%;}
    .seeds{position:fixed;top:0;left:0;width:100%;height:100%;pointer-events:none;z-index:-1;}
    .seed{position:absolute;color:#d4b17a;font-size:16px;opacity:0.7;animation:fallSeed 6s linear infinite;}
    @keyframes fallSeed{0%{transform:translateY(-10%) rotate(0deg);opacity:0;}10%{opacity:0.7;}90%{opacity:0.7;}100%{transform:translateY(110%) rotate(360deg);opacity:0;}}
  </style>
</head>
<body>
  <div class="seeds" id="seedContainer"></div>
  <header>
    <h1>Мир хомяков</h1>
    <p>Всё о милых пушистых питомцах</p>
  </header>
  <div class="container">
    <section class="section">
      <h2>Кто такие хомяки?</h2>
      <p>Хомяки — небольшие грызуны, популярные как домашние питомцы. Они активны, любопытны и очень обаятельны.</p>
      <p>В природе обитают в степях, полупустынях и горах. В домашних условиях живут 2–4 года.</p>
    </section>
    <section class="section">
      <h2>Популярные породы</h2>
      <div class="grid">
        <div class="card">
          <img src="https://avatars.mds.yandex.net/i?id=e9dfc93d97ddf722b9343bb3fae63f094aa866b3-12421657-images-thumbs&n=13" alt="Сирийский хомяк">
          <div class="card-content">
            <h3>Сирийский хомяк</h3>
            <p>Крупный, пушистый, чаще золотистого окраса. Самый популярный домашний вид.</p>
          </div>
        </div>
        <div class="card">
          <img src="https://avatars.mds.yandex.net/i?id=516228ae795f4c9902f3d8bec904f660991a217f-4614052-images-thumbs&n=13" alt="Джунгарский хомяк">
          <div class="card-content">
            <h3>Джунгарский хомяк</h3>
                <p>Маленький, с тёмной полоской на спине. Хорошо подходит для небольших квартир.</p>
          </div>
        </div>
        <div class="card">
          <img src="https://avatars.mds.yandex.net/i?id=a44e8dbf6f61d1d453bc9843b518dc8985af5e1a-16401250-images-thumbs&n=13" alt="Хомяк Роборовского">
          <div class="card-content">
            <h3>Хомяк Роборовского</h3>
            <p>Самый маленький вид. Часто живут группами, очень подвижные.</p>
          </div>
        </div>
      </div>
    </section>
    <section class="section">
      <h2>Уход за хомяком</h2>
      <ul>
        <li>Клетка не менее 50 × 30 см с глубоким поддоном</li>
        <li>Наполнитель (древесные гранулы, бумага, сено)</li>
        <li>Колесо для бега (сплошное, чтобы не травмировало лапки)</li>
        <li>Кормушка и поилка</li>
        <li>Укрытие (домик или норка)</li>
        <li>Свежая вода и сбалансированный корм ежедневно</li>
      </ul>
      <p>Чистить клетку нужно 1–2 раза в неделю, не тревожа запасы хомяка.</p>
    </section>
    <section class="section">
      <h2>Чем кормить?</h2>
      <p>Основа рациона — специализированный корм для хомяков. Дополнительно можно давать:</p>
      <ul>
        <li>Свежие овощи (морковь, огурец, кабачок)</li>
        <li>Фрукты (яблоко, груша — немного)</li>
        <li>Зелень (листья салата, петрушка)</li>
        <li>Белковую пищу (варёное яйцо, нежирный творог — 1–2 раза в неделю)</li>
      </ul>
    </section>
  </div>
  <footer><p>© 2025 Любители хомяков</p></footer>
  <script>
    const seedContainer = document.getElementById('seedContainer');
    function createSeed() {
      const seed = document.createElement('div');
      seed.className = 'seed';
      seed.textContent = '•';
      seed.style.left = Math.random() * 100 + 'vw';
      seed.style.top = '-10%';
      seedContainer.appendChild(seed);
      setTimeout(() => seed.remove(), 6000);
    }
    setInterval(createSeed, 300);
  </script>
</body></html>
