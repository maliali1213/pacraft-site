body {
    margin: 0;
    font-family: 'Vazirmatn', sans-serif;
    color: #fff;
    text-align: center;
    overflow-x: hidden; /* جلوگیری از اسکرول افقی */
    background-image: url('image_gen_5db5c5ab-fa78-4b9f-aa74-c9cee110c206_0.png'); /* تصویر پس زمینه ماینکرافتی شما */
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
    background-attachment: fixed; /* ثابت ماندن پس‌زمینه هنگام اسکرول */
    min-height: 100vh;
    display: flex;
    flex-direction: column; /* چیدمان ستونی برای هدر، محتوا و فوتر */
    justify-content: space-between; /* پخش شدن محتوا در کل صفحه */
}

.header {
    background-color: rgba(0, 0, 0, 0.7); /* پس‌زمینه نیمه‌شفاف تیره برای هدر */
    padding: 30px 20px;
    margin-bottom: 20px;
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.5);
    border-bottom-left-radius: 15px;
    border-bottom-right-radius: 15px;
}

h1 {
    font-size: 4.5em; /* بزرگتر کردن عنوان */
    margin-bottom: 10px;
    color: #ffd700; /* رنگ طلایی */
    text-shadow: 3px 3px 7px rgba(0, 0, 0, 0.8);
    letter-spacing: 2px; /* فاصله بین حروف برای جلوه بهتر */
}

.tagline {
    font-size: 1.8em;
    color: #aaffaa; /* رنگ سبز روشن برای جمله "امکانات روز دنیا" */
    text-shadow: 1px 1px 4px rgba(0, 0, 0, 0.7);
    margin-top: 0;
}

.content-wrapper {
    flex-grow: 1; /* اجازه می‌دهد این بخش فضای موجود را پر کند */
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 20px;
    gap: 30px; /* فاصله بین بخش‌های مختلف */
}

.section {
    background-color: rgba(0, 0, 0, 0.6);
    padding: 30px 40px;
    border-radius: 15px;
    box-shadow: 0 8px 25px rgba(0, 0, 0, 0.5);
    max-width: 900px;
    width: 95%;
    backdrop-filter: blur(5px); /* افکت بلور برای پس‌زمینه نیمه‌شفاف */
    border: 1px solid rgba(255, 255, 255, 0.1); /* حاشیه کمرنگ */
}

.section h2 {
    font-size: 2.8em;
    color: #ffd700;
    margin-bottom: 25px;
    text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.7);
}

.staff-list ul {
    list-style: none; /* حذف دایره‌های لیست */
    padding: 0;
    font-size: 1.4em;
    line-height: 1.8;
    text-align: right; /* راست‌چین کردن لیست */
}

.staff-list ul li {
    margin-bottom: 10px;
    padding-right: 20px; /* برای فاصله از سمت راست */
    position: relative;
}

.staff-list ul li::before {
    content: "⛏️"; /* آیکون کلنگ ماینکرافت */
    position: absolute;
    right: 0;
    color: #ffd700;
}

.gamemode-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(150px, 1fr)); /* چیدمان گرید برای گیم‌مودها */
    gap: 15px;
    margin-top: 20px;
    text-align: center;
}

.gamemode-grid span {
    background-color: rgba(76, 175, 80, 0.8); /* سبز ماینکرافتی با شفافیت */
    padding: 12px 15px;
    border-radius: 8px;
    font-size: 1.2em;
    font-weight: bold;
    color: #fff;
    box-shadow: 0 3px 10px rgba(0, 0, 0, 0.4);
    transition: background-color 0.3s ease, transform 0.2s ease;
}

.gamemode-grid span:hover {
    background-color: #45a049;
    transform: translateY(-5px);
}

.footer {
    background-color: rgba(0, 0, 0, 0.7);
    padding: 20px;
    margin-top: 30px;
    box-shadow: 0 -5px 15px rgba(0, 0, 0, 0.5);
    border-top-left-radius: 15px;
    border-top-right-radius: 15px;
    text-align: right; /* راست‌چین کردن فوتر */
    padding-right: 40px; /* کمی فاصله از سمت راست */
}

.footer p {
    font-size: 1.1em;
    color: #bbb;
    margin: 0;
    text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.5);
}

/* واکنش‌گرا کردن برای موبایل و تبلت */
@media (max-width: 768px) {
    h1 {
        font-size: 3.5em;
    }
    .tagline {
        font-size: 1.5em;
    }
    .section h2 {
        font-size: 2.2em;
    }
    .staff-list ul {
        font-size: 1.2em;
    }
    .gamemode-grid {
        grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
    }
    .gamemode-grid span {
        font-size: 1em;
    }
    .footer {
        padding-right: 20px;
    }
}

@media (max-width: 480px) {
    h1 {
        font-size: 2.8em;
    }
    .tagline {
        font-size: 1.2em;
    }
    .header {
        padding: 20px 10px;
    }
    .section {
        padding: 20px;
        width: 98%;
    }
    .section h2 {
        font-size: 1.8em;
        margin-bottom: 15px;
    }
    .staff-list ul {
        font-size: 1em;
        text-align: center; /* در موبایل وسط‌چین */
    }
    .staff-list ul li::before {
        display: none; /* آیکون را در موبایل حذف می‌کنیم */
    }
    .gamemode-grid {
        grid-template-columns: 1fr; /* در موبایل هر گیم‌مود در یک خط */
    }
    .gamemode-grid span {
        padding: 10px;
    }
    .footer {
        padding-left: 10px;
        padding-right: 10px;
        text-align: center; /* در موبایل وسط‌چین */
    }
}
