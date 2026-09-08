
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DECOR GO - طلب خدمة</title>

    <style>
        body {
            margin: 0;
            font-family: Arial, sans-serif;
            background: #f5f5f5;
            color: #222;
        }

        header {
            background: #111;
            color: white;
            text-align: center;
            padding: 25px;
        }

        header h1 {
            margin: 0;
            font-size: 32px;
        }

        header span {
            color: #c9a227;
        }

        .container {
            max-width: 600px;
            margin: 40px auto;
            background: white;
            padding: 30px;
            border-radius: 15px;
            box-shadow: 0 5px 20px rgba(0,0,0,0.08);
        }

        h2 {
            text-align: center;
            margin-bottom: 25px;
        }

        label {
            display: block;
            margin-bottom: 8px;
            font-weight: bold;
        }

        input,
        select {
            width: 100%;
            box-sizing: border-box;
            padding: 14px;
            margin-bottom: 20px;
            border: 1px solid #ddd;
            border-radius: 8px;
            font-size: 16px;
        }

        button {
            width: 100%;
            padding: 15px;
            border: none;
            border-radius: 8px;
            background: #25D366;
            color: white;
            font-size: 18px;
            font-weight: bold;
            cursor: pointer;
        }

        button:hover {
            opacity: 0.9;
        }

        .back {
            display: block;
            text-align: center;
            margin-top: 20px;
            color: #555;
            text-decoration: none;
        }
    </style>
</head>

<body>

<header>
    <h1>DECOR <span>GO</span></h1>
</header>

<div class="container">

    <h2>اطلب خدمتك</h2>

    <form onsubmit="sendToWhatsApp(event)">

        <label for="name">الاسم</label>
        <input
            type="text"
            id="name"
            placeholder="اكتب اسمك"
            required
        >

        <label for="service">نوع الخدمة</label>
        <select id="service" required>
            <option value="">اختر نوع الخدمة</option>
            <option>ديكور داخلي</option>
            <option>إكساء</option>
            <option>بديل رخام</option>
            <option>بديل خشب</option>
            <option>ورق جدران</option>
            <option>أسقف معلقة</option>
            <option>تصميم وتنفيذ</option>
            <option>خدمة أخرى</option>
        </select>

        <label for="address">العنوان</label>
        <input
            type="text"
            id="address"
            placeholder="اكتب عنوانك"
            required
        >

        <label for="phone">رقم الهاتف</label>
        <input
            type="tel"
            id="phone"
            placeholder="09xxxxxxxx"
            required
        >

        <button type="submit">
            إرسال إلى واتساب
        </button>

    </form>

    <a class="back" href="index.html">
        العودة إلى الصفحة الرئيسية
    </a>

</div>

<script>
function sendToWhatsApp(event) {

    event.preventDefault();

    const name = document.getElementById("name").value;
    const service = document.getElementById("service").value;
    const address = document.getElementById("address").value;
    const phone = document.getElementById("phone").value;

    const message =
        "طلب خدمة جديد - DECOR GO%0A%0A" +
        "الاسم: " + encodeURIComponent(name) + "%0A" +
        "نوع الخدمة: " + encodeURIComponent(service) + "%0A" +
        "العنوان: " + encodeURIComponent(address) + "%0A" +
        "رقم الهاتف: " + encodeURIComponent(phone);

    const whatsappNumber = "963998574957";

    const whatsappURL =
        "https://wa.me/" + whatsappNumber + "?text=" + message;

    window.open(whatsappURL, "_blank");
}
</script>

</body>
</html>
