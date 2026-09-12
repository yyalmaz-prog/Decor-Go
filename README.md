<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>DECOR GO - ديكور غو</title>

<style>
* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

body {
    font-family: Arial, Tahoma, sans-serif;
    background: #f5f5f5;
    color: #222;
}

/* الهيدر */
header {
    background: #111;
    color: white;
    padding: 18px 20px;
    text-align: center;
    position: sticky;
    top: 0;
    z-index: 1000;
}

.logo {
    font-size: 30px;
    font-weight: bold;
    letter-spacing: 1px;
}

.logo span {
    color: #d4a017;
}

.subtitle {
    font-size: 13px;
    margin-top: 5px;
    color: #ddd;
}

/* القائمة */
nav {
    background: white;
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    gap: 8px;
    padding: 12px;
    box-shadow: 0 2px 8px rgba(0,0,0,0.08);
}

nav button {
    border: none;
    background: #f0f0f0;
    padding: 12px 18px;
    border-radius: 10px;
    cursor: pointer;
    font-size: 15px;
    font-weight: bold;
}

nav button:hover,
nav button.active {
    background: #111;
    color: white;
}

/* الصفحات */
.page {
    display: none;
    max-width: 900px;
    margin: 30px auto;
    padding: 25px;
}

.page.active {
    display: block;
}

.card {
    background: white;
    border-radius: 18px;
    padding: 30px;
    box-shadow: 0 5px 20px rgba(0,0,0,0.08);
}

h2 {
    margin-bottom: 15px;
    font-size: 27px;
}

.description {
    line-height: 1.9;
    color: #555;
    margin-bottom: 25px;
}

/* أزرار */
.main-button {
    display: inline-block;
    width: 100%;
    border: none;
    background: #111;
    color: white;
    padding: 15px;
    border-radius: 10px;
    font-size: 17px;
    font-weight: bold;
    cursor: pointer;
    margin-top: 10px;
}

.main-button:hover {
    opacity: 0.85;
}

.gold-button {
    background: #d4a017;
    color: #111;
}

/* أزرار الواجهة الرئيسية */
.home-button {
    margin-top: 12px;
}

.home-button.download-home {
    background: #111;
    color: white;
}

.home-button.contest-home {
    background: #d4a017;
    color: #111;
}

/* النماذج */
label {
    display: block;
    margin-top: 15px;
    margin-bottom: 7px;
    font-weight: bold;
}

input,
select,
textarea {
    width: 100%;
    padding: 13px;
    border: 1px solid #ddd;
    border-radius: 9px;
    font-size: 16px;
    background: white;
}

textarea {
    min-height: 100px;
    resize: vertical;
}

/* منشور السحب */
.contest-post {
    background: #fafafa;
    border: 1px solid #ddd;
    border-radius: 12px;
    padding: 20px;
    line-height: 2;
    white-space: pre-line;
    margin: 20px 0;
}

.info-box {
    background: #fff8df;
    border-right: 5px solid #d4a017;
    padding: 15px;
    border-radius: 8px;
    margin: 15px 0;
    line-height: 1.8;
}

/* التحميل */
.download-box {
    display: grid;
    gap: 15px;
    margin-top: 25px;
}

.download-button {
    display: block;
    text-align: center;
    text-decoration: none;
    background: #111;
    color: white;
    padding: 16px;
    border-radius: 10px;
    font-size: 17px;
    font-weight: bold;
}

.download-button.telegram {
    background: #229ED9;
}

.download-button:hover {
    opacity: 0.85;
}

/* الفوتر */
footer {
    text-align: center;
    background: #111;
    color: #ddd;
    padding: 25px;
    margin-top: 30px;
    line-height: 1.8;
}

/* الهاتف */
@media (max-width: 600px) {

    .logo {
        font-size: 25px;
    }

    nav {
        gap: 5px;
    }

    nav button {
        padding: 10px 11px;
        font-size: 13px;
    }

    .page {
        margin: 15px auto;
        padding: 12px;
    }

    .card {
        padding: 20px 15px;
    }

    h2 {
        font-size: 23px;
    }
}
</style>
</head>

<body>

<header>
    <div class="logo">DECOR <span>GO</span></div>
    <div class="subtitle">منصة خدمات الإكساء والديكور</div>
</header>

<nav>
    <button class="active" onclick="showPage('home', this)">🏠 الرئيسية</button>
    <button onclick="showPage('service', this)">🛠️ اطلب خدمة</button>
    <button onclick="showPage('inspection', this)">📐 معاينة مجانية</button>
    <button onclick="showPage('contest', this)">🎁 ادخل السحب</button>
    <button onclick="showPage('download', this)">📲 تحميل التطبيق</button>
</nav>


<!-- الرئيسية -->
<section id="home" class="page active">

    <div class="card">

        <h2>أهلاً وسهلاً بك في DECOR GO</h2>

        <p class="description">
            منصة ديكور غو تساعدك في الوصول إلى خدمات الإكساء والديكور،
            وطلب الفنيين، والحصول على معاينة مجانية لمشروعك.
            كل ذلك بطريقة سهلة وسريعة.
        </p>

        <div class="info-box">
            🔨 خدمات إكساء وديكور<br>
            👷 فنيين وخدمات أمامك<br>
            📐 معاينة مجانية<br>
            💰 حساب تقديري للتكاليف<br>
            🎁 سحب شهري على جوائز نقدية
        </div>

        <!-- معاينة مجانية -->
        <button class="main-button gold-button home-button"
                onclick="showPageById('inspection')">
            📐 اطلب معاينة مجانية
        </button>

        <!-- تحميل التطبيق -->
        <button class="main-button home-button download-home"
                onclick="showPageById('download')">
            📲 تحميل التطبيق
        </button>

        <!-- السحب -->
        <button class="main-button home-button contest-home"
                onclick="showPageById('contest')">
            🎁 ادخل السحب
        </button>

    </div>

</section>


<!-- طلب خدمة -->
<section id="service" class="page">

    <div class="card">

        <h2>🛠️ اطلب خدمة</h2>

        <p class="description">
            املأ المعلومات التالية وسنتواصل معك عبر واتساب.
        </p>

        <form onsubmit="sendService(event)">

            <label>الاسم</label>
            <input type="text" id="serviceName" required>

            <label>نوع الخدمة</label>
            <select id="serviceType" required>
                <option value="">اختر الخدمة</option>
                <option>إكساء كامل</option>
                <option>ديكور داخلي</option>
                <option>دهان</option>
                <option>جبس بورد</option>
                <option>بديل رخام</option>
                <option>بديل خشب</option>
                <option>ورق جدران</option>
                <option>أسقف مستعارة</option>
                <option>أعمال كهرباء</option>
                <option>أعمال صحية</option>
                <option>خدمة أخرى</option>
            </select>

            <label>العنوان</label>
            <input type="text" id="serviceAddress" required>

            <label>رقم الهاتف</label>
            <input type="tel" id="servicePhone" required>

            <button class="main-button" type="submit">
                📲 إرسال الطلب إلى واتساب
            </button>

        </form>

    </div>

</section>


<!-- المعاينة -->
<section id="inspection" class="page">

    <div class="card">

        <h2>📐 اطلب معاينة مجانية</h2>

        <p class="description">
            اطلب معاينة مجانية لمشروعك وسنتواصل معك لتحديد التفاصيل.
        </p>

        <form onsubmit="sendInspection(event)">

            <label>المنطقة</label>

            <select id="inspectionArea" required>
                <option value="">اختر المنطقة</option>
                <option>دمشق</option>
                <option>ريف دمشق</option>
            </select>

            <label>الاسم</label>
            <input type="text" id="inspectionName" required>

            <label>رقم الهاتف</label>
            <input type="tel" id="inspectionPhone" required>

            <label>العنوان بالتفصيل</label>
            <textarea id="inspectionAddress" required></textarea>

            <button class="main-button" type="submit">
                📲 طلب المعاينة عبر واتساب
            </button>

        </form>

    </div>

</section>


<!-- السحب -->
<section id="contest" class="page">

    <div class="card">

        <h2>🎁 ادخل السحب</h2>

        <p class="description">
            اقرأ المنشور، ثم شاركه وسجل معلوماتك للدخول في السحب.
        </p>

        <div id="contestText" class="contest-post">
🏠 ليش تجيب فني وتخجل منه بمعاينته وتبلش تنفيذ معه، وإنت فقط كنت بدك تعرف شو التكلفة أو شو بيتك بده مواد؟

مع ديكور غو نحنا منجي لعندك ونعمل المعاينة مجاناً، وما في أي التزام عليك بالتنفيذ معنا.

أنت تعرف احتياجات بيتك وتأخذ قرارك براحتك.

🔹 عاين… احسب… وبعدها قرر.

ديكور غو مو تطبيق بيربط الفني بالعميل.
نحنا مسؤولين عن العمل من بدايته حتى آخر مرحلة من التشطيب.

وكمان السوق كله صار بين إيديك 📱
تصفح المواد، احسب تكلفتها واعمل فاتورتك بنفسك.

📲 حمل تطبيق ديكور غو مباشرة من الرابط.
🌐 جرب منصتنا.
📱 وتابع قناتنا على تيليجرام.

ديكور غو — قبل ما تدفع احسبها صح.

🔗 التحميل المباشر:
https://apk.e-droid.net/apk/app4030820-alhd2n.apk?v=4

🌐 منصة ديكور غو:
https://yyalmaz-prog.github.io/Decor-Go/index.html

📲 قناة تيليجرام:
https://t.me/DecorGoagha
        </div>

        <button class="main-button gold-button"
                onclick="copyContest()">
            📋 نسخ منشور السحب
        </button>

        <div class="info-box">
            بعد مشاركة المنشور، اكتب اسمك ورقم هاتفك
            وأرسل المعلومات عبر واتساب.
        </div>

        <form onsubmit="sendContest(event)">

            <label>الاسم</label>
            <input type="text" id="contestName" required>

            <label>رقم الهاتف</label>
            <input type="tel" id="contestPhone" required>

            <button class="main-button" type="submit">
                🎁 إرسال بيانات الدخول للسحب
            </button>

        </form>

    </div>

</section>


<!-- تحميل التطبيق -->
<section id="download" class="page">

    <div class="card">

        <h2>📲 تحميل تطبيق DECOR GO</h2>

        <p class="description">
            حمّل تطبيق ديكور غو بسهولة من خلال أحد الخيارين التاليين:
        </p>

        <div class="download-box">

            <!-- التحميل المباشر -->
            <a class="download-button"
               href="https://www.appcreator24.com/app4030820-alhd2n"
               target="_blank">
                📲 تحميل التطبيق مباشرة
            </a>

            <!-- التحميل من تلغرام -->
            <a class="download-button telegram"
               href="https://t.me/DecorGoagha"
               target="_blank">
                ✈️ تحميل التطبيق عبر تلغرام
            </a>

        </div>

        <div class="info-box">
            إذا واجهتك مشكلة في التحميل، تواصل معنا عبر واتساب.
        </div>

    </div>

</section>


<footer>
    <strong>DECOR GO</strong><br>
    منصة خدمات الإكساء والديكور<br>
    جميع الحقوق محفوظة © 2026
</footer>


<script>

const whatsappNumber = "963998574957";


/* تبديل الصفحات */

function showPage(pageId, button) {

    document.querySelectorAll(".page").forEach(function(page) {
        page.classList.remove("active");
    });

    document.getElementById(pageId).classList.add("active");

    document.querySelectorAll("nav button").forEach(function(btn) {
        btn.classList.remove("active");
    });

    if (button) {
        button.classList.add("active");
    }

    window.scrollTo({
        top: 0,
        behavior: "smooth"
    });
}


/* فتح صفحة من زر داخل الصفحة */

function showPageById(pageId) {

    document.querySelectorAll(".page").forEach(function(page) {
        page.classList.remove("active");
    });

    document.getElementById(pageId).classList.add("active");

    document.querySelectorAll("nav button").forEach(function(btn) {
        btn.classList.remove("active");
    });

    window.scrollTo({
        top: 0,
        behavior: "smooth"
    });
}


/* إرسال طلب خدمة */

function sendService(event) {

    event.preventDefault();

    const name = document.getElementById("serviceName").value;
    const service = document.getElementById("serviceType").value;
    const address = document.getElementById("serviceAddress").value;
    const phone = document.getElementById("servicePhone").value;

    const message =
        "🛠️ طلب خدمة جديد - DECOR GO\n\n" +
        "الاسم: " + name + "\n" +
        "نوع الخدمة: " + service + "\n" +
        "العنوان: " + address + "\n" +
        "رقم الهاتف: " + phone;

    openWhatsApp(message);
}


/* إرسال طلب معاينة */

function sendInspection(event) {

    event.preventDefault();

    const area = document.getElementById("inspectionArea").value;
    const name = document.getElementById("inspectionName").value;
    const phone = document.getElementById("inspectionPhone").value;
    const address = document.getElementById("inspectionAddress").value;

    const message =
        "📐 طلب معاينة مجانية - DECOR GO\n\n" +
        "المنطقة: " + area + "\n" +
        "الاسم: " + name + "\n" +
        "رقم الهاتف: " + phone + "\n" +
        "العنوان بالتفصيل: " + address;

    openWhatsApp(message);
}


/* إرسال بيانات السحب */

function sendContest(event) {

    event.preventDefault();

    const name = document.getElementById("contestName").value;
    const phone = document.getElementById("contestPhone").value;

    const message =
        "🎁 تسجيل في السحب الشهري - DECOR GO\n\n" +
        "الاسم: " + name + "\n" +
        "رقم الهاتف: " + phone;

    openWhatsApp(message);
}


/* واتساب */

function openWhatsApp(message) {

    const url =
        "https://wa.me/" +
        whatsappNumber +
        "?text=" +
        encodeURIComponent(message);

    window.open(url, "_blank");
}


/* نسخ منشور السحب */

function copyContest() {

    const text = document.getElementById("contestText").innerText;

    navigator.clipboard.writeText(text).then(function() {

        alert("✅ تم نسخ منشور السحب بنجاح");

    }).catch(function() {

        alert("❌ لم يتم النسخ. يمكنك تحديد النص ونسخه يدوياً.");

    });
}

</script>

</body>
</html>
