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

/* =========================
   الهيدر
   ========================= */

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


/* =========================
   القائمة
   ========================= */

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


/* =========================
   الصفحات
   ========================= */

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


/* =========================
   الأزرار
   ========================= */

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


/* =========================
   النماذج
   ========================= */

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


/* =========================
   منشور السحب
   ========================= */

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


/* =========================
   صندوق الدعوات
   ========================= */

.invite-box {
    background: #fafafa;
    border: 1px solid #e2e2e2;
    border-radius: 14px;
    padding: 20px;
    margin: 20px 0;
    line-height: 2;
}

.invite-title {
    font-size: 20px;
    font-weight: bold;
    margin-bottom: 10px;
}

.invite-highlight {
    background: #fff8df;
    border-right: 5px solid #d4a017;
    padding: 15px;
    border-radius: 8px;
    margin: 15px 0;
    line-height: 1.9;
}


/* =========================
   تنسيق نص الدعوة
   ========================= */

.invitation-message-box {
    background: #fff8e6;
    border-right: 5px solid #d4a017;
    border-radius: 12px;
    padding: 18px;
    margin: 20px 0;
    line-height: 2;
    text-align: right;
}

.invitation-message-box .invitation-title {
    font-size: 18px;
    font-weight: bold;
    color: #8a6500;
    margin-bottom: 12px;
}

.invitation-message-box p {
    margin-bottom: 10px;
}


/* زر النسخ */

.copy-invite-button {
    background: #6c757d;
    color: white;
}

.copy-invite-button:hover {
    opacity: 0.85;
}

.invite-share-hint {
    text-align: center;
    color: #777;
    font-size: 13px;
    line-height: 1.8;
    margin-top: 12px;
}


/* =========================
   التحميل
   ========================= */

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


/* ==================================================
   حاسبة كميات المواد - DECOR GO
   ================================================== */

.quantity-intro {
    background: #fff8df;
    border-right: 5px solid #d4a017;
    padding: 15px;
    border-radius: 10px;
    line-height: 1.9;
    margin-bottom: 20px;
}

.quantity-note {
    color: #777;
    font-size: 13px;
    line-height: 1.8;
    margin-top: 8px;
}

.quantity-result {
    display: none;
    margin-top: 25px;
}

.quantity-wall-info {
    background: #f8f8f8;
    border: 1px solid #e2e2e2;
    border-radius: 12px;
    padding: 15px;
    line-height: 2;
    margin-bottom: 15px;
}

.quantity-option {
    background: #fafafa;
    border: 1px solid #ddd;
    border-radius: 13px;
    padding: 18px;
    margin-bottom: 15px;
}

.quantity-option h3 {
    color: #8a6500;
    margin-bottom: 13px;
    font-size: 19px;
}

.quantity-material {
    line-height: 1.9;
}

.quantity-material-name {
    font-weight: bold;
    color: #222;
    font-size: 16px;
}

.quantity-number {
    color: #8a6500;
    font-weight: bold;
    font-size: 17px;
}

.quantity-area {
    color: #777;
    font-size: 13px;
}

.quantity-adhesive {
    color: #8a6500;
    font-weight: bold;
    margin-top: 3px;
}

.quantity-divider {
    border: 0;
    border-top: 1px solid #ddd;
    margin: 14px 0;
}

.quantity-warning {
    background: #fff8df;
    border-right: 5px solid #d4a017;
    border-radius: 10px;
    padding: 15px;
    line-height: 1.9;
}

.quantity-creator {
    text-align: center;
    font-size: 24px;
    font-weight: bold;
    color: #8a6500;
    margin-top: 28px;
    padding-top: 20px;
    border-top: 1px solid #ddd;
}

.quantity-whatsapp {
    display: block;
    text-decoration: none;
    text-align: center;
    background: #168c3b;
    color: white;
    padding: 14px;
    border-radius: 10px;
    font-size: 16px;
    font-weight: bold;
    margin-top: 15px;
}


/* =========================
   الفوتر
   ========================= */

footer {
    text-align: center;
    background: #111;
    color: #ddd;
    padding: 25px;
    margin-top: 30px;
    line-height: 1.8;
}


/* =========================
   الهاتف
   ========================= */

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


<!-- =========================
     الهيدر
     ========================= -->

<header>

    <div class="logo">
        DECOR <span>GO</span>
    </div>

    <div class="subtitle">
        منصة خدمات الإكساء والديكور
    </div>

</header>


<!-- =========================
     القائمة
     ========================= -->

<nav>

    <button onclick="showPage('home', this)">
        🏠 الرئيسية
    </button>

    <button onclick="showPage('service', this)">
        🛠️ اطلب خدمة
    </button>

    <button onclick="showPage('inspection', this)">
        📐 معاينة مجانية
    </button>

    <!-- التبويبة الجديدة -->

    <button onclick="showPage('quantities', this)">
        📐 احسب كميات المواد
    </button>

    <button onclick="showPage('contest', this)">
        🎁 ادخل السحب
    </button>

    <button onclick="showPage('invite', this)">
        👥 ادعُ أصدقاءك
    </button>

    <button onclick="showPage('download', this)">
        📲 تحميل التطبيق
    </button>

    <button onclick="showPage('rubble', this)">
        🚚 ترحيل ردم
    </button>

</nav>



<!-- ==================================================
     الرئيسية
     ================================================== -->

<section id="home" class="page active">

    <div class="card">

        <h2>
            أهلاً وسهلاً بك في DECOR GO
        </h2>

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


        <button
            class="main-button gold-button home-button"
            onclick="showPageById('inspection')"
        >
            📐 اطلب معاينة مجانية
        </button>


        <button
            class="main-button home-button download-home"
            onclick="showPageById('download')"
        >
            📲 تحميل التطبيق
        </button>


        <button
            class="main-button contest-home"
            onclick="showPageById('contest')"
        >
            🎁 ادخل السحب
        </button>

    </div>

</section>



<!-- ==================================================
     طلب خدمة
     ================================================== -->

<section id="service" class="page">

    <div class="card">

        <h2>🛠️ اطلب خدمة</h2>

        <p class="description">
            املأ المعلومات التالية وسنتواصل معك عبر واتساب.
        </p>


        <form onsubmit="sendService(event)">

            <label>الاسم</label>

            <input
                type="text"
                id="serviceName"
                required
            >


            <label>نوع الخدمة</label>

            <select
                id="serviceType"
                required
            >

                <option value="">
                    اختر الخدمة
                </option>

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

            <input
                type="text"
                id="serviceAddress"
                required
            >


            <label>رقم الهاتف</label>

            <input
                type="tel"
                id="servicePhone"
                required
            >


            <button
                class="main-button"
                type="submit"
            >
                📲 إرسال الطلب إلى واتساب
            </button>

        </form>

    </div>

</section>



<!-- ==================================================
     معاينة مجانية
     ================================================== -->

<section id="inspection" class="page">

    <div class="card">

        <h2>📐 اطلب معاينة مجانية</h2>

        <p class="description">
            اطلب معاينة مجانية لمشروعك وسنتواصل معك لتحديد التفاصيل.
        </p>


        <form onsubmit="sendInspection(event)">

            <label>المنطقة</label>

            <select
                id="inspectionArea"
                required
            >

                <option value="">
                    اختر المنطقة
                </option>

                <option>دمشق</option>
                <option>ريف دمشق</option>

            </select>


            <label>الاسم</label>

            <input
                type="text"
                id="inspectionName"
                required
            >


            <label>رقم الهاتف</label>

            <input
                type="tel"
                id="inspectionPhone"
                required
            >


            <label>العنوان بالتفصيل</label>

            <textarea
                id="inspectionAddress"
                required
            ></textarea>


            <button
                class="main-button"
                type="submit"
            >
                📲 طلب المعاينة عبر واتساب
            </button>

        </form>

    </div>

</section>



<!-- ==================================================
     احسب كميات المواد
     ================================================== -->

<section id="quantities" class="page">

    <div class="card">

        <h2>📐 احسب كميات المواد</h2>

        <p class="description">
            احسب كمية مواد التكسية المطلوبة لحائط واحد
            بطريقة سهلة وسريعة.
        </p>


        <div class="quantity-intro">

            📏 أدخل طول الحائط وارتفاعه،
            ثم اختر المواد التي تريد استخدامها.

            <br>

            📐 التطبيق يحسب لك الكميات حسب مساحة الحائط،
            ويحسب اللاصق للمواد التي تم تحديد قاعدة اللاصق لها.

        </div>


        <!-- نوع الغرفة -->

        <label>
            نوع الغرفة
        </label>

        <select id="quantityRoomType">

            <option value="">
                اختر نوع الغرفة
            </option>

            <option>غرفة نوم</option>
            <option>غرفة أطفال</option>
            <option>غرفة ضيوف</option>
            <option>صالون</option>
            <option>غرفة معيشة</option>
            <option>مدخل</option>
            <option>ديكور شاشة</option>
            <option>مكتب</option>
            <option>محل</option>
            <option>أخرى</option>

        </select>


        <!-- طول الحائط -->

        <label>
            طول الحائط بالمتر
        </label>

        <input
            type="number"
            id="quantityWallLength"
            min="0.01"
            step="0.01"
            placeholder="مثال: 3"
        >


        <!-- ارتفاع الحائط -->

        <label>
            ارتفاع الحائط بالمتر
        </label>

        <input
            type="number"
            id="quantityWallHeight"
            min="0.01"
            step="0.01"
            placeholder="مثال: 2.80"
        >


        <!-- المادة الأولى -->

        <label>
            المادة الأولى
        </label>

        <select id="quantityMaterial1">

            <option value="">
                اختر المادة الأولى
            </option>

        </select>


        <!-- المادة الثانية -->

        <label>
            المادة الثانية
            <span style="color:#999;">
                (اختياري)
            </span>
        </label>

        <select id="quantityMaterial2">

            <option value="">
                بدون مادة ثانية
            </option>

        </select>


        <!-- المادة الثالثة -->

        <label>
            المادة الثالثة
            <span style="color:#999;">
                (اختياري)
            </span>
        </label>

        <select id="quantityMaterial3">

            <option value="">
                بدون مادة ثالثة
            </option>

        </select>


        <div class="quantity-note">

            عند اختيار مادتين:
            يتم إعطاء خيارات من لوح واحد أو لوحين من المادة الأولى،
            والباقي من المادة الثانية.

            <br><br>

            عند المساحات الكبيرة يمكن أن يصل عدد ألواح المادة الأولى
            إلى ثلاثة ألواح.

        </div>


        <button
            class="main-button gold-button"
            type="button"
            onclick="calculateQuantities()"
        >
            📊 احسب الكميات
        </button>


        <!-- =========================
             النتائج
             ========================= -->

        <div
            id="quantityResult"
            class="quantity-result"
        >

            <h3
                style="
                    color:#8a6500;
                    margin-bottom:15px;
                    font-size:22px;
                "
            >
                📊 نتيجة الحساب
            </h3>


            <div
                id="quantityWallInfo"
                class="quantity-wall-info"
            ></div>


            <div
                id="quantityResultsContainer"
            ></div>


            <div class="quantity-creator">
                يحيى آغا / Yahea Agha
            </div>


            <a
                class="quantity-whatsapp"
                href="https://wa.me/963998574957"
                target="_blank"
            >
                💬 للتوصية أو التواصل عبر واتساب
            </a>

        </div>

    </div>

</section>



<!-- ==================================================
     السحب
     ================================================== -->

<section id="contest" class="page">

    <div class="card">

        <h2>🎁 ادخل السحب</h2>

        <p class="description">
            اقرأ المنشور، ثم شاركه وسجل معلوماتك للدخول في السحب.
        </p>


        <div
            id="contestText"
            class="contest-post"
        >

🏠 ليش تجيب فني وتخجل منه بمعاينته وتبلش تنفيذ معه، وإنت فقط كنت بدك تعرف شو التكلفة أو شو بيتك بده مواد؟

مع ديكور غو نحنا منجي لعندك ونعمل المعاينة مجاناً، وما في أي التزام عليك بالتنفيذ معنا.

أنت تعرف احتياجات بيتك وتأخذ قرارك براحتك.

🔹 عاين… احسب… وبعدها قرر.

ديكور غو مو تطبيق بيربط الفني بالعميل. نحنا مسؤولين عن العمل من بدايته حتى آخر مرحلة من التشطيب.

وكمان السوق كله صار بين إيديك 📱 تصفح المواد، احسب تكلفتها واعمل فاتورتك بنفسك.

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


        <button
            class="main-button gold-button"
            onclick="copyContest()"
        >
            📋 نسخ منشور السحب
        </button>


        <div class="info-box">

            بعد مشاركة المنشور، اكتب اسمك ورقم هاتفك
            وأرسل المعلومات عبر واتساب.

        </div>


        <form onsubmit="sendContest(event)">

            <label>الاسم</label>

            <input
                type="text"
                id="contestName"
                required
            >


            <label>رقم الهاتف</label>

            <input
                type="tel"
                id="contestPhone"
                required
            >


            <button
                class="main-button"
                type="submit"
            >
                🎁 إرسال بيانات الدخول للسحب
            </button>

        </form>

    </div>

</section>



<!-- ==================================================
     دعوات الأصدقاء
     ================================================== -->

<section id="invite" class="page">

    <div class="card">

        <h2>👥 ادعُ أصدقاءك</h2>


        <p class="description">

            شارك ديكور غو مع أصدقائك،
            وساعدهم على الوصول إلى خدمات الإكساء والديكور
            والاستفادة من عروضنا وخدماتنا.

        </p>


        <div class="invitation-message-box">

            <div class="invitation-title">
                🎁 رسالة الدعوة
            </div>


            <p>
                يمكنك إرسال الدعوة مباشرة عبر واتساب،
                أو نسخها وإرسالها عبر Messenger أو Telegram
                أو أي تطبيق تواصل آخر.
            </p>

        </div>


        <button
            class="main-button gold-button"
            onclick="shareInvite()"
        >
            📲 إرسال الدعوة عبر واتساب
        </button>


        <button
            class="main-button copy-invite-button"
            onclick="copyInvite()"
        >
            📋 نسخ الدعوة
        </button>


        <div class="invite-share-hint">

            بعد نسخ الدعوة، يمكنك لصقها وإرسالها
            عبر واتساب أو Messenger أو Telegram
            أو أي تطبيق آخر.

        </div>


        <div class="invite-box">

            <div class="invite-title">
                📝 هل دعاك أحد إلى ديكور غو؟
            </div>


            <p class="description">

                إذا سجلت في ديكور غو عن طريق أحد أصدقائك،
                اكتب اسمه ورقم هاتفه حتى نستطيع تسجيل الدعوة.

            </p>


            <form onsubmit="sendInvite(event)">

                <label>
                    اسم الشخص الذي دعاك
                </label>

                <input
                    type="text"
                    id="inviterName"
                    placeholder="اكتب اسم الشخص"
                    required
                >


                <label>
                    رقم هاتف الشخص الذي دعاك
                </label>

                <input
                    type="tel"
                    id="inviterPhone"
                    placeholder="مثال: 099xxxxxxx"
                    required
                >


                <button
                    class="main-button"
                    type="submit"
                >
                    📲 إرسال بيانات الدعوة عبر واتساب
                </button>

            </form>

        </div>


        <div class="info-box">

            ℹ️ لا تحتاج إلى تعديل نظام تسجيل الدخول.
            هذه التبويبة مستقلة، ويتم إرسال معلومات الدعوة عبر واتساب
            ليتم تنظيمها ومراجعتها بشكل يدوي.

        </div>

    </div>

</section>



<!-- ==================================================
     تحميل التطبيق
     ================================================== -->

<section id="download" class="page">

    <div class="card">

        <h2>📲 تحميل تطبيق DECOR GO</h2>

        <p class="description">

            حمّل تطبيق ديكور غو بسهولة من خلال أحد الخيارين التاليين:

        </p>


        <div class="download-box">


            <a
                class="download-button"
                href="https://www.appcreator24.com/app4030820-alhd2n"
                target="_blank"
            >
                📲 تحميل التطبيق مباشرة
            </a>


            <a
                class="download-button telegram"
                href="https://t.me/DecorGoagha"
                target="_blank"
            >
                ✈️ تحميل التطبيق عبر تلغرام
            </a>


        </div>


        <div class="info-box">

            إذا واجهتك مشكلة في التحميل،
            تواصل معنا عبر واتساب.

        </div>

    </div>

</section>



<!-- ==================================================
     ترحيل ردم
     ================================================== -->

<section id="rubble" class="page">

    <div class="card">

        <h2>🚚 ترحيل ردم</h2>

        <p class="description">

            املأ المعلومات التالية وسنتواصل معك عبر واتساب
            لتنسيق خدمة ترحيل الردم.

        </p>


        <form onsubmit="sendRubble(event)">

            <label>الاسم</label>

            <input
                type="text"
                id="rubbleName"
                required
            >


            <label>العنوان</label>

            <input
                type="text"
                id="rubbleAddress"
                required
            >


            <label>العنوان بالتفصيل</label>

            <textarea
                id="rubbleDetailedAddress"
                required
            ></textarea>


            <button
                class="main-button"
                type="submit"
            >
                📲 إرسال المعلومات إلى واتساب
            </button>

        </form>

    </div>

</section>



<!-- ==================================================
     الفوتر
     ================================================== -->

<footer>

    <strong>DECOR GO</strong>

    <br>

    منصة خدمات الإكساء والديكور

    <br>

    جميع الحقوق محفوظة © 2026

</footer>



<script>

const whatsappNumber = "963998574957";


/* =================================================
   تبديل الصفحات
   ================================================= */

function showPage(pageId, button) {

    document
        .querySelectorAll(".page")
        .forEach(function(page) {

            page.classList.remove("active");

        });


    document
        .getElementById(pageId)
        .classList.add("active");


    document
        .querySelectorAll("nav button")
        .forEach(function(btn) {

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


/* =================================================
   فتح صفحة من زر داخل الصفحة
   ================================================= */

function showPageById(pageId) {

    document
        .querySelectorAll(".page")
        .forEach(function(page) {

            page.classList.remove("active");

        });


    document
        .getElementById(pageId)
        .classList.add("active");


    document
        .querySelectorAll("nav button")
        .forEach(function(btn) {

            btn.classList.remove("active");

        });


    window.scrollTo({
        top: 0,
        behavior: "smooth"
    });

}


/* =================================================
   إرسال طلب خدمة
   ================================================= */

function sendService(event) {

    event.preventDefault();

    const name =
        document.getElementById("serviceName").value;

    const service =
        document.getElementById("serviceType").value;

    const address =
        document.getElementById("serviceAddress").value;

    const phone =
        document.getElementById("servicePhone").value;


    const message =
        "🛠️ طلب خدمة جديد - DECOR GO\n\n" +

        "الاسم: " +
        name +
        "\n" +

        "نوع الخدمة: " +
        service +
        "\n" +

        "العنوان: " +
        address +
        "\n" +

        "رقم الهاتف: " +
        phone;


    openWhatsApp(message);

}


/* =================================================
   إرسال طلب معاينة
   ================================================= */

function sendInspection(event) {

    event.preventDefault();

    const area =
        document.getElementById("inspectionArea").value;

    const name =
        document.getElementById("inspectionName").value;

    const phone =
        document.getElementById("inspectionPhone").value;

    const address =
        document.getElementById("inspectionAddress").value;


    const message =
        "📐 طلب معاينة مجانية - DECOR GO\n\n" +

        "المنطقة: " +
        area +
        "\n" +

        "الاسم: " +
        name +
        "\n" +

        "رقم الهاتف: " +
        phone +
        "\n" +

        "العنوان بالتفصيل: " +
        address;


    openWhatsApp(message);

}


/* =================================================
   إرسال بيانات السحب
   ================================================= */

function sendContest(event) {

    event.preventDefault();

    const name =
        document.getElementById("contestName").value;

    const phone =
        document.getElementById("contestPhone").value;


    const message =
        "🎁 تسجيل في السحب الشهري - DECOR GO\n\n" +

        "الاسم: " +
        name +
        "\n" +

        "رقم الهاتف: " +
        phone;


    openWhatsApp(message);

}


/* =================================================
   نص دعوة الأصدقاء
   ================================================= */

function getInviteMessage() {

    return `🎁 جوائز نقدية، إكساء منزلك مجانًا وخصومات على خدماتنا قد تكون من نصيبك من خلال دعوة أصدقائك.

🏠 إذا كنت مهتمًا بالديكور والإكساء، حابب عرّفك على «ديكور غو».

✨ مع ديكور غو فيك:

📐 تخطط وتحسب تكلفة مشروعك
🛍️ تتصفح خدمات ومواد الديكور
👷 تطلب معاينة مجانية
📱 وتتابع كل شيء من موبايلك

📲 حمّل تطبيق ديكور غو:
https://apk.e-droid.net/apk/app4030820-alhd2n.apk?v=4

🌐 منصة ديكور غو:
https://yyalmaz-prog.github.io/Decor-Go/index.html

📢 تابعنا على تيليجرام:
https://t.me/DecorGoagha

🎁 وإذا وصلت إلى ديكور غو عن طريقي،
ادخل إلى تبويبة «ادعُ أصدقاءك»
واختر:

«نعم، تمت دعوتي عن طريق صديق»

ثم اكتب اسمي ورقم هاتفي،
لتدخل السحب وتزيد فرصك في الربح.

❤️ أهلاً وسهلاً فيك مع ديكور غو`;

}


/* =================================================
   مشاركة دعوة عبر واتساب
   ================================================= */

function shareInvite() {

    const message =
        getInviteMessage();


    const url =
        "https://wa.me/?text=" +
        encodeURIComponent(message);


    window.open(
        url,
        "_blank"
    );

}


/* =================================================
   نسخ الدعوة
   ================================================= */

function copyInvite() {

    const message =
        getInviteMessage();


    if (
        navigator.clipboard &&
        navigator.clipboard.writeText
    ) {

        navigator.clipboard
            .writeText(message)
            .then(function() {

                alert(
                    "✅ تم نسخ الدعوة بنجاح!\n\nيمكنك الآن لصقها وإرسالها عبر واتساب أو Messenger أو Telegram أو أي تطبيق آخر."
                );

            })
            .catch(function() {

                fallbackCopyInvite(message);

            });

    } else {

        fallbackCopyInvite(message);

    }

}


function fallbackCopyInvite(message) {

    const textarea =
        document.createElement("textarea");


    textarea.value =
        message;


    textarea.style.position =
        "fixed";


    textarea.style.left =
        "-9999px";


    document.body.appendChild(
        textarea
    );


    textarea.focus();

    textarea.select();


    try {

        document.execCommand("copy");


        alert(
            "✅ تم نسخ الدعوة بنجاح!\n\nيمكنك الآن لصقها وإرسالها عبر واتساب أو Messenger أو Telegram أو أي تطبيق آخر."
        );

    }

    catch (error) {

        alert(
            "⚠️ لم يتم النسخ تلقائيًا.\n\nيرجى نسخ الدعوة يدويًا."
        );

    }


    document.body.removeChild(
        textarea
    );

}


/* =================================================
   إرسال بيانات الشخص الذي دعاك
   ================================================= */

function sendInvite(event) {

    event.preventDefault();


    const inviterName =
        document
            .getElementById("inviterName")
            .value
            .trim();


    const inviterPhone =
        document
            .getElementById("inviterPhone")
            .value
            .trim();


    if (!inviterName) {

        alert(
            "يرجى كتابة اسم الشخص الذي دعاك."
        );

        return;

    }


    if (!inviterPhone) {

        alert(
            "يرجى كتابة رقم هاتف الشخص الذي دعاك."
        );

        return;

    }


    const message =
        "👥 دعوات الأصدقاء - DECOR GO\n\n" +

        "تمت دعوتي عن طريق صديق.\n\n" +

        "👤 اسم الشخص الذي دعاني:\n" +
        inviterName +
        "\n\n" +

        "📱 رقم هاتف الشخص الذي دعاني:\n" +
        inviterPhone;


    openWhatsApp(message);

}


/* =================================================
   إرسال طلب ترحيل ردم
   ================================================= */

function sendRubble(event) {

    event.preventDefault();


    const name =
        document.getElementById("rubbleName").value;

    const address =
        document.getElementById("rubbleAddress").value;

    const detailedAddress =
        document.getElementById("rubbleDetailedAddress").value;


    const message =
        "🚚 طلب ترحيل ردم - DECOR GO\n\n" +

        "الاسم: " +
        name +
        "\n" +

        "العنوان: " +
        address +
        "\n" +

        "العنوان بالتفصيل: " +
        detailedAddress;


    openWhatsApp(message);

}


/* =================================================
   واتساب
   ================================================= */

function openWhatsApp(message) {

    const url =
        "https://wa.me/" +
        whatsappNumber +
        "?text=" +
        encodeURIComponent(message);


    window.open(
        url,
        "_blank"
    );

}


/* =================================================
   نسخ منشور السحب
   ================================================= */

function copyContest() {

    const text =
        document
            .getElementById("contestText")
            .innerText;


    if (
        navigator.clipboard &&
        navigator.clipboard.writeText
    ) {

        navigator.clipboard
            .writeText(text)
            .then(function() {

                alert(
                    "✅ تم نسخ منشور السحب بنجاح"
                );

            })
            .catch(function() {

                alert(
                    "❌ لم يتم النسخ. يمكنك تحديد النص ونسخه يدوياً."
                );

            });

    } else {

        alert(
            "❌ لم يتم النسخ. يمكنك تحديد النص ونسخه يدوياً."
        );

    }

}


/* =================================================
   =================================================
   حاسبة كميات المواد
   =================================================
   ================================================= */


/* =========================
   بيانات المواد
   ========================= */

const quantityMaterials = {

    wood16: {
        name: "بديل الخشب 16 سم × 290 سم",
        width: 0.16,
        height: 2.90,
        type: "wood16"
    },

    wood20: {
        name: "بديل الخشب 20 سم × 290 سم",
        width: 0.20,
        height: 2.90,
        type: "wood20"
    },

    wood30: {
        name: "بديل الخشب 30 سم × 290 سم",
        width: 0.30,
        height: 2.90,
        type: "wood30"
    },

    flexibleWood60: {
        name: "بديل الخشب 60 سم خشب مرن × 280 سم",
        width: 0.60,
        height: 2.80,
        type: "flexibleWood60"
    },

    marble120x290: {
        name: "بديل رخام 120 × 290 سم",
        width: 1.20,
        height: 2.90,
        type: "panel2adhesive"
    },

    marble120x280: {
        name: "بديل رخام 120 × 280 سم",
        width: 1.20,
        height: 2.80,
        type: "panel2adhesive"
    },

    marbleRoll120x290: {
        name: "رول بديل رخام 120 × 290 سم",
        width: 1.20,
        height: 2.90,
        type: "roll"
    },

    stoneRoll120x290: {
        name: "رول بديل حجر 120 × 290 سم",
        width: 1.20,
        height: 2.90,
        type: "roll"
    },

    travertino130x290: {
        name: "لوح ترافلتينو 130 × 290 سم",
        width: 1.30,
        height: 2.90,
        type: "panel2adhesive"
    },

    stone60x120: {
        name: "بديل الحجر 60 × 120 سم",
        width: 0.60,
        height: 1.20,
        type: "stone"
    }

};


/* =========================
   تعبئة قوائم المواد
   ========================= */

function loadQuantityMaterials() {

    const selects = [
        document.getElementById("quantityMaterial1"),
        document.getElementById("quantityMaterial2"),
        document.getElementById("quantityMaterial3")
    ];


    selects.forEach(function(select) {

        Object.keys(quantityMaterials)
            .forEach(function(key) {

                const option =
                    document.createElement("option");

                option.value = key;

                option.textContent =
                    quantityMaterials[key].name;

                select.appendChild(option);

            });

    });

}


/* =========================
   حساب اللاصق
   ========================= */

function getQuantityAdhesive(
    material,
    quantity
) {

    if (quantity <= 0) {
        return "";
    }


    /*
       بديل الخشب 16:
       كل 3 قطع = لاصق واحد
    */

    if (material.type === "wood16") {

        return Math.ceil(quantity / 3)
            + " لاصق سندويش كبير";

    }


    /*
       بديل الخشب 30:
       كل قطعتين = لاصق واحد
    */

    if (material.type === "wood30") {

        return Math.ceil(quantity / 2)
            + " لاصق سندويش كبير";

    }


    /*
       بديل الرخام والترافلتينو:
       كل لوح = 2 لاصق
    */

    if (material.type === "panel2adhesive") {

        return (quantity * 2)
            + " لاصق سندويش كبير";

    }


    return "";

}


/* =========================
   عرض مادة
   ========================= */

function quantityMaterialHTML(
    material,
    quantity
) {

    if (quantity <= 0) {
        return "";
    }


    const materialArea =
        material.width *
        material.height;


    const coveredArea =
        quantity *
        materialArea;


    let html = `

        <div class="quantity-material">

            <div class="quantity-material-name">
                ${material.name}
            </div>

            <div>
                الكمية:
                <span class="quantity-number">
                    ${quantity}
                </span>
            </div>

            <div class="quantity-area">
                المساحة المغطاة تقريباً:
                ${coveredArea.toFixed(2)} م²
            </div>

    `;


    const adhesive =
        getQuantityAdhesive(
            material,
            quantity
        );


    if (adhesive) {

        html += `

            <div class="quantity-adhesive">
                🧴 ${adhesive}
            </div>

        `;

    }


    html += `
        </div>
    `;


    return html;

}


/* =========================
   حساب مادة واحدة
   ========================= */

function calculateSingleQuantity(
    wallArea,
    material
) {

    const materialArea =
        material.width *
        material.height;


    return Math.ceil(
        wallArea / materialArea
    );

}


/* =========================
   حساب الكمية المتبقية
   ========================= */

function calculateRemainingQuantity(
    remainingArea,
    material
) {

    if (remainingArea <= 0) {
        return 0;
    }


    const materialArea =
        material.width *
        material.height;


    return Math.ceil(
        remainingArea / materialArea
    );

}


/* =================================================
   خيار مادتين
   ================================================= */

function createTwoMaterialOption(
    wallArea,
    material1,
    material2,
    panelCount,
    optionNumber
) {

    const material1Area =
        material1.width *
        material1.height;


    const usedArea =
        panelCount *
        material1Area;


    /*
       إذا الألواح غطت الحائط كله،
       لا نعرض هذا الخيار.

       وهذا مهم جداً حسب الاتفاق:
       إذا لوحان غطوا كامل الحائط،
       يبقى خيار لوح واحد + المادة الثانية.
    */

    if (usedArea >= wallArea) {
        return "";
    }


    const remainingArea =
        wallArea - usedArea;


    const material2Quantity =
        calculateRemainingQuantity(
            remainingArea,
            material2
        );


    let html = `

        <div class="quantity-option">

            <h3>
                الخيار ${optionNumber}
            </h3>

            ${quantityMaterialHTML(
                material1,
                panelCount
            )}

            <hr class="quantity-divider">

            ${quantityMaterialHTML(
                material2,
                material2Quantity
            )}

        </div>

    `;


    return html;

}


/* =================================================
   خيار 3 مواد
   ================================================= */

function createThreeMaterialOption(
    wallArea,
    material1,
    material2,
    material3,
    panelCount,
    optionNumber
) {

    const material1Area =
        material1.width *
        material1.height;


    const firstArea =
        panelCount *
        material1Area;


    /*
       لا نعرض الخيار إذا الألواح
       تغطي الحائط كاملاً.
    */

    if (firstArea >= wallArea) {
        return "";
    }


    let remainingArea =
        wallArea - firstArea;


    let html = `

        <div class="quantity-option">

            <h3>
                الخيار ${optionNumber}
            </h3>

            ${quantityMaterialHTML(
                material1,
                panelCount
            )}

    `;


    /*
       في حالة 3 مواد:
       نستخدم قطعة واحدة من المادة الثانية
       إذا بقيت مساحة كافية،
       ثم المادة الثالثة تكمل الباقي.

       الهدف أن يبقى عدد الألواح الديكورية
       محدوداً ومنطقياً.
    */

    const material2Area =
        material2.width *
        material2.height;


    if (remainingArea > material2Area) {

        html += `

            <hr class="quantity-divider">

            ${quantityMaterialHTML(
                material2,
                1
            )}

        `;


        remainingArea -= material2Area;


        const material3Quantity =
            calculateRemainingQuantity(
                remainingArea,
                material3
            );


        if (material3Quantity > 0) {

            html += `

                <hr class="quantity-divider">

                ${quantityMaterialHTML(
                    material3,
                    material3Quantity
                )}

            `;

        }

    } else {

        const material3Quantity =
            calculateRemainingQuantity(
                remainingArea,
                material3
            );


        html += `

            <hr class="quantity-divider">

            ${quantityMaterialHTML(
                material3,
                material3Quantity
            )}

        `;

    }


    html += `
        </div>
    `;


    return html;

}


/* =================================================
   الحساب الرئيسي
   ================================================= */

function calculateQuantities() {

    const roomType =
        document
            .getElementById("quantityRoomType")
            .value;


    const wallLength =
        parseFloat(
            document
                .getElementById("quantityWallLength")
                .value
        );


    const wallHeight =
        parseFloat(
            document
                .getElementById("quantityWallHeight")
                .value
        );


    const material1Key =
        document
            .getElementById("quantityMaterial1")
            .value;


    const material2Key =
        document
            .getElementById("quantityMaterial2")
            .value;


    const material3Key =
        document
            .getElementById("quantityMaterial3")
            .value;


    /* =========================
       التحقق
       ========================= */

    if (!roomType) {

        alert(
            "يرجى اختيار نوع الغرفة."
        );

        return;

    }


    if (!wallLength || wallLength <= 0) {

        alert(
            "يرجى إدخال طول الحائط بشكل صحيح."
        );

        return;

    }


    if (!wallHeight || wallHeight <= 0) {

        alert(
            "يرجى إدخال ارتفاع الحائط بشكل صحيح."
        );

        return;

    }


    if (!material1Key) {

        alert(
            "يرجى اختيار المادة الأولى."
        );

        return;

    }


    /*
       منع تكرار المادة
    */

    const selectedKeys = [
        material1Key,
        material2Key,
        material3Key
    ].filter(Boolean);


    const uniqueKeys =
        [...new Set(selectedKeys)];


    if (
        uniqueKeys.length !==
        selectedKeys.length
    ) {

        alert(
            "يرجى اختيار مواد مختلفة."
        );

        return;

    }


    /* =========================
       مساحة الحائط
       ========================= */

    const wallArea =
        wallLength *
        wallHeight;


    const selectedMaterials =
        uniqueKeys.map(function(key) {

            return quantityMaterials[key];

        });


    /* =========================
       معلومات الحائط
       ========================= */

    document
        .getElementById("quantityWallInfo")
        .innerHTML = `

            <strong>
                نوع الغرفة:
            </strong>
            ${roomType}

            <br>

            <strong>
                طول الحائط:
            </strong>
            ${wallLength.toFixed(2)} م

            <br>

            <strong>
                ارتفاع الحائط:
            </strong>
            ${wallHeight.toFixed(2)} م

            <br>

            <strong>
                مساحة الحائط:
            </strong>
            ${wallArea.toFixed(2)} م²

        `;


    let resultsHTML = "";


    /* =================================================
       مادة واحدة
       ================================================= */

    if (selectedMaterials.length === 1) {

        const material =
            selectedMaterials[0];


        const quantity =
            calculateSingleQuantity(
                wallArea,
                material
            );


        resultsHTML = `

            <div class="quantity-option">

                <h3>
                    📦 الكمية المطلوبة
                </h3>

                ${quantityMaterialHTML(
                    material,
                    quantity
                )}

            </div>

        `;

    }


    /* =================================================
       مادتان
       ================================================= */

    else if (selectedMaterials.length === 2) {

        const material1 =
            selectedMaterials[0];

        const material2 =
            selectedMaterials[1];


        /*
           خيار لوح واحد
        */

        resultsHTML +=
            createTwoMaterialOption(
                wallArea,
                material1,
                material2,
                1,
                1
            );


        /*
           خيار لوحين
        */

        resultsHTML +=
            createTwoMaterialOption(
                wallArea,
                material1,
                material2,
                2,
                2
            );


        if (!resultsHTML) {

            resultsHTML = `

                <div class="quantity-warning">

                    مساحة الحائط لا تسمح بتوزيع المواد
                    وفق الخيارات المحددة.

                </div>

            `;

        }

    }


    /* =================================================
       3 مواد
       ================================================= */

    else if (selectedMaterials.length === 3) {

        const material1 =
            selectedMaterials[0];

        const material2 =
            selectedMaterials[1];

        const material3 =
            selectedMaterials[2];


        /*
           خيار لوح واحد
        */

        resultsHTML +=
            createThreeMaterialOption(
                wallArea,
                material1,
                material2,
                material3,
                1,
                1
            );


        /*
           خيار لوحين
        */

        resultsHTML +=
            createThreeMaterialOption(
                wallArea,
                material1,
                material2,
                material3,
                2,
                2
            );


        /*
           خيار 3 ألواح للمساحات الكبيرة
        */

        resultsHTML +=
            createThreeMaterialOption(
                wallArea,
                material1,
                material2,
                material3,
                3,
                3
            );


        if (!resultsHTML) {

            resultsHTML = `

                <div class="quantity-warning">

                    مساحة الحائط لا تسمح باستخدام
                    الألواح المختارة بهذه الطريقة.

                </div>

            `;

        }

    }


    /* =========================
       عرض النتائج
       ========================= */

    document
        .getElementById("quantityResultsContainer")
        .innerHTML =
        resultsHTML;


    document
        .getElementById("quantityResult")
        .style.display =
        "block";


    document
        .getElementById("quantityResult")
        .scrollIntoView({
            behavior: "smooth",
            block: "start"
        });

}


/* =================================================
   تشغيل حاسبة المواد
   ================================================= */

loadQuantityMaterials();

</script>

</body>
</html>
