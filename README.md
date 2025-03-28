# socialmedia-news
<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="أكبر موقع إخباري لمتابعة كل جديد في عالم السوشيال ميديا">
    <meta name="keywords" content="أخبار, سوشيال ميديا, فيسبوك, تويتر, يوتيوب, إنستجرام">
    <meta name="author" content="أخبار السوشيال ميديا">
    <title>أخبار السوشيال ميديا</title>
    <link rel="stylesheet" href="style.css">
    <script defer src="script.js"></script>
</head>
<body>

    <!-- شريط الأخبار المتحرك -->
    <div class="news-ticker">
        <marquee>🚀 عاجل: تحديثات جديدة في فيسبوك! - تويتر تعلن عن ميزة جديدة - يوتيوب تحظر بعض القنوات 🔥</marquee>
    </div>

    <!-- الهيدر -->
    <header>
        <h1>أخبار السوشيال ميديا</h1>
        <form class="search-bar">
            <input type="text" placeholder="ابحث عن خبر...">
            <button type="submit">🔍</button>
        </form>
    </header>

    <!-- القائمة الرئيسية -->
    <nav>
        <ul>
            <li><a href="#">الرئيسية</a></li>
            <li><a href="#">فيسبوك</a></li>
            <li><a href="#">تويتر</a></li>
            <li><a href="#">يوتيوب</a></li>
            <li><a href="#">إنستجرام</a></li>
            <li><a href="#">تيك توك</a></li>
            <li><a href="#">المزيد ⬇</a>
                <ul class="dropdown">
                    <li><a href="#">سناب شات</a></li>
                    <li><a href="#">لينكد إن</a></li>
                    <li><a href="#">تطبيقات جديدة</a></li>
                </ul>
            </li>
        </ul>
    </nav>

    <!-- قسم الأخبار -->
    <section class="news-container">
        <article class="news">
            <img src="news1.jpg" alt="تحديث فيسبوك">
            <h2>🔵 تحديث ضخم في فيسبوك يغير قواعد اللعبة!</h2>
            <p>أعلنت ميتا عن تحديث جديد في فيسبوك يشمل تغييرات في نظام الإعجابات والتفاعل...</p>
            <a href="#">اقرأ المزيد</a>
        </article>

        <article class="news">
            <img src="news2.jpg" alt="يوتيوب تطلق ميزة جديدة">
            <h2>🔴 يوتيوب تضيف أدوات قوية لصناع المحتوى!</h2>
            <p>أطلقت يوتيوب أداة تحليل متطورة لمراقبة أداء الفيديوهات...</p>
            <a href="#">اقرأ المزيد</a>
        </article>

        <article class="news">
            <img src="news3.jpg" alt="تيك توك">
            <h2>🟣 تيك توك ينافس يوتيوب بفيديوهات أطول!</h2>
            <p>تيك توك يبدأ في اختبار فيديوهات تصل إلى 30 دقيقة لمنافسة يوتيوب...</p>
            <a href="#">اقرأ المزيد</a>
        </article>
    </section>

    <!-- الفوتر -->
    <footer>
        <p>© 2025 أخبار السوشيال ميديا - جميع الحقوق محفوظة.</p>
    </footer>

</body>
</html>/* ضبط الخطوط والألوان */
body {
    font-family: 'Arial', sans-serif;
    background-color: #3b0a1b;
    color: white;
    margin: 0;
    padding: 0;
}

/* شريط الأخبار */
.news-ticker {
    background-color: #660f29;
    padding: 10px;
    font-weight: bold;
    text-align: center;
}

/* الهيدر */
header {
    text-align: center;
    background-color: #50081c;
    padding: 20px;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

header h1 {
    margin: 0;
    font-size: 24px;
}

/* شريط البحث */
.search-bar input {
    padding: 8px;
    border: none;
    border-radius: 5px;
}

.search-bar button {
    padding: 8px;
    border: none;
    background-color: white;
    cursor: pointer;
}

/* القائمة */
nav ul {
    list-style: none;
    padding: 10px;
    background-color: #661026;
    display: flex;
    justify-content: center;
}

nav ul li {
    position: relative;
    margin: 0 15px;
}

nav ul li a {
    color: white;
    text-decoration: none;
}

/* القائمة المنسدلة */
.dropdown {
    display: none;
    position: absolute;
    background-color: #750d28;
    list-style: none;
    padding: 10px;
}

nav ul li:hover .dropdown {
    display: block;
}

/* قسم الأخبار */
.news-container {
    display: flex;
    justify-content: center;
    gap: 20px;
    padding: 20px;
}

.news {
    background-color: #750d28;
    padding: 15px;
    border-radius: 8px;
    width: 300px;
    text-align: center;
}

.news img {
    width: 100%;
    border-radius: 8px;
}

.news h2 {
    font-size: 18px;
}

.news p {
    font-size: 14px;
}

/* الفوتر */
footer {
    text-align: center;
    padding: 10px;
    background-color: #50081c;
    margin-top: 20px;
}document.querySelector('.search-bar').addEventListener('submit', function(event) {
    event.preventDefault();
    let searchQuery = event.target.querySelector('input').value;
    alert("جارٍ البحث عن: " + searchQuery);
});

// إضافة تأثير عند تمرير الماوس على الأخبار
document.querySelectorAll('.news').forEach(news => {
    news.addEventListener('mouseenter', () => news.style.transform = "scale(1.05)");
    news.addEventListener('mouseleave', () => news.style.transform = "scale(1)");
});
