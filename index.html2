```html
<!DOCTYPE html>
<html lang="th">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Sweet Bakery Gallery</title>

<link href="https://fonts.googleapis.com/css2?family=Kanit:wght@300;400;500;600&family=Playfair+Display:wght@600;700&display=swap" rel="stylesheet">

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    scroll-behavior: smooth;
}

body {
    font-family: 'Kanit', sans-serif;
    background: #fffafd;
    color: #64798b;
}

/* HEADER */
header {
    background: linear-gradient(120deg, #f9dce8, #dceffc);
    text-align: center;
    padding: 75px 20px;
}

header h1 {
    font-family: 'Playfair Display', serif;
    font-size: 52px;
    color: #cf86a7;
    margin-bottom: 12px;
}

header p {
    font-size: 17px;
    color: #718da5;
}

header .subtitle {
    margin-top: 10px;
    font-size: 14px;
}

/* FILTER */
.filter-section {
    text-align: center;
    padding: 50px 20px 30px;
}

.filter-section h2 {
    font-family: 'Playfair Display', serif;
    font-size: 34px;
    color: #cf86a7;
    margin-bottom: 25px;
}

.filter-buttons {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    gap: 12px;
}

.filter-btn {
    padding: 11px 28px;
    border: 1px solid #e9c5d6;
    border-radius: 30px;
    background: white;
    color: #7893a8;
    cursor: pointer;
    font-family: inherit;
    font-size: 15px;
    transition: .3s;
}

.filter-btn:hover,
.filter-btn.active {
    background: #e6a7c1;
    color: white;
    border-color: #e6a7c1;
    transform: translateY(-3px);
}

/* GALLERY */
.gallery-section {
    padding: 25px 8% 80px;
}

.gallery {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
    gap: 28px;
}

.card {
    background: white;
    border-radius: 20px;
    overflow: hidden;
    box-shadow: 0 5px 20px #9ab9d322;
    transition: .4s;
    animation: appear .5s ease;
}

.card:hover {
    transform: translateY(-10px);
    box-shadow: 0 12px 28px #dba4c455;
}

.card img {
    width: 100%;
    height: 220px;
    object-fit: cover;
    transition: .5s;
}

.card:hover img {
    transform: scale(1.06);
}

.card-content {
    padding: 20px;
    text-align: center;
}

.card h3 {
    color: #ce83a5;
    font-size: 21px;
    margin-bottom: 8px;
}

.card p {
    color: #829caf;
    font-size: 14px;
    line-height: 1.7;
}

.category {
    display: inline-block;
    margin-top: 12px;
    padding: 5px 16px;
    border-radius: 20px;
    background: #e7f3fb;
    color: #739ab8;
    font-size: 12px;
}

.card.hide {
    display: none;
}

/* ABOUT */
.about {
    background: linear-gradient(120deg, #fce8ef, #e4f2fb);
    padding: 65px 15%;
    text-align: center;
}

.about h2 {
    font-family: 'Playfair Display', serif;
    color: #ce83a5;
    font-size: 34px;
    margin-bottom: 15px;
}

.about p {
    line-height: 2;
    max-width: 650px;
    margin: auto;
}

/* FOOTER */
footer {
    background: #dba1b9;
    text-align: center;
    padding: 25px;
    color: white;
}

/* ANIMATION */
@keyframes appear {
    from {
        opacity: 0;
        transform: translateY(20px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}

/* RESPONSIVE */
@media(max-width: 600px) {
    header {
        padding: 55px 15px;
    }

    header h1 {
        font-size: 38px;
    }

    .filter-section h2 {
        font-size: 28px;
    }

    .gallery-section {
        padding: 20px 6% 60px;
    }

    .gallery {
        grid-template-columns: repeat(2, minmax(0, 1fr));
        gap: 12px;
    }

    .card img {
        height: 145px;
    }

    .card-content {
        padding: 12px 8px;
    }

    .card h3 {
        font-size: 16px;
    }

    .card p {
        font-size: 12px;
    }

    .filter-btn {
        padding: 9px 17px;
        font-size: 13px;
    }
}

@media(max-width: 360px) {
    .gallery {
        grid-template-columns: 1fr;
    }
}
</style>
</head>

<body>

<!-- HEADER -->
<header>
    <h1>Sweet Bakery ♡</h1>
    <p>Welcome to our little bakery</p>
    <p class="subtitle">
        รวมขนมเบเกอรี่แสนอร่อยที่คุณชื่นชอบ
        สดใหม่ หอมหวาน และเต็มไปด้วยความสุข
    </p>
</header>

<!-- FILTER BUTTONS -->
<section class="filter-section">
    <h2>Our Bakery Gallery</h2>
    <div class="filter-buttons">

        <button class="filter-btn active" onclick="filterItems('all', this)">
            ทั้งหมด
        </button>

        <button class="filter-btn" onclick="filterItems('cake', this)">
            เค้ก
        </button>

        <button class="filter-btn" onclick="filterItems('bread', this)">
            ขนมปัง
        </button>

        <button class="filter-btn" onclick="filterItems('sweet', this)">
            คุกกี้และโดนัท
        </button>

    </div>
</section>

<!-- GALLERY -->
<section class="gallery-section">
    <div class="gallery" id="gallery">

        <!-- CAKE -->
        <div class="card" data-category="cake">
            <img src="images/cake.jpg" alt="Strawberry Cake">
            <div class="card-content">
                <h3>Strawberry Cake</h3>
                <p>เค้กสตรอว์เบอร์รีครีมสด หวานละมุน</p>
                <span class="category">เค้ก</span>
            </div>
        </div>

        <div class="card" data-category="cake">
            <img src="images/chocolatecake.jpg" alt="Chocolate Cake">
            <div class="card-content">
                <h3>Chocolate Cake</h3>
                <p>เค้กช็อกโกแลตเข้มข้น นุ่มละลายในปาก</p>
                <span class="category">เค้ก</span>
            </div>
        </div>

        <div class="card" data-category="cake">
            <img src="images/cheesecake.jpg" alt="Cheesecake">
            <div class="card-content">
                <h3>Cheesecake</h3>
                <p>ชีสเค้กเนื้อเนียน หอมชีส</p>
                <span class="category">เค้ก</span>
            </div>
        </div>

        <!-- BREAD -->
        <div class="card" data-category="bread">
            <img src="images/croissant.jpg" alt="Croissant">
            <div class="card-content">
                <h3>Butter Croissant</h3>
                <p>ครัวซองต์เนยสด กรอบนอกนุ่มใน</p>
                <span class="category">ขนมปัง</span>
            </div>
        </div>

        <div class="card" data-category="bread">
            <img src="images/bread.jpg" alt="Bread">
            <div class="card-content">
                <h3>Milk Bread</h3>
                <p>ขนมปังนมสด เนื้อนุ่ม หอมหวาน</p>
                <span class="category">ขนมปัง</span>
            </div>
        </div>

        <!-- SWEET -->
        <div class="card" data-category="sweet">
            <img src="images/donut.jpg" alt="Donut">
            <div class="card-content">
                <h3>Sweet Donut</h3>
                <p>โดนัทเคลือบช็อกโกแลตแสนอร่อย</p>
                <span class="category">โดนัท</span>
            </div>
        </div>

        <div class="card" data-category="sweet">
            <img src="images/cookie.jpg" alt="Cookie">
            <div class="card-content">
                <h3>Chocolate Cookie</h3>
                <p>คุกกี้ช็อกโกแลตชิพกรุบกรอบ</p>
                <span class="category">คุกกี้</span>
            </div>
        </div>

        <div class="card" data-category="sweet">
            <img src="images/brownie.jpg" alt="Brownie">
            <div class="card-content">
                <h3>Chocolate Brownie</h3>
                <p>บราวนี่ช็อกโกแลตเข้มข้น</p>
                <span class="category">ขนมหวาน</span>
            </div>
        </div>

    </div>
</section>

<!-- ABOUT -->
<section class="about">
    <h2>About Sweet Bakery ♡</h2>
    <p>
        Sweet Bakery คือเว็บไซต์แนะนำขนมเบเกอรี่
        ที่รวบรวมขนมหลากหลายชนิดไว้ในที่เดียว
        สามารถเลือกชมขนมตามหมวดหมู่ที่สนใจได้
        เราเชื่อว่าขนมหวานสามารถเติมเต็มความสุข
        ให้กับทุกวันของคุณได้
    </p>
</section>

<!-- FOOTER -->
<footer>
    <p>© 2026 Sweet Bakery</p>
    <p>Made with Love ♡</p>
</footer>

<!-- JAVASCRIPT FILTER -->
<script>
function filterItems(category, button) {

    const cards = document.querySelectorAll('.card');
    const buttons = document.querySelectorAll('.filter-btn');

    // เปลี่ยนสีปุ่มที่ถูกเลือก
    buttons.forEach(btn => {
        btn.classList.remove('active');
    });

    button.classList.add('active');

    // กรองหมวดหมู่สินค้า
    cards.forEach(card => {

        const itemCategory = card.dataset.category;

        if (category === 'all' || itemCategory === category) {
            card.classList.remove('hide');
        } else {
            card.classList.add('hide');
        }

    });
}
</script>

</body>
</html>
```
