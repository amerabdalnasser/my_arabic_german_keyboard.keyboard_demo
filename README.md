my_arabic_german_keyboard
keyboard.html
<!DOCTYPE html>
<html lang="ar"> <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>لوحة مفاتيح ألمانية-عربية</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            background-color: #f0f2f5;
            margin: 0;
            padding: 20px;
            box-sizing: border-box;
            flex-direction: column;
        }

        .keyboard-container {
            background-color: #ffffff;
            border-radius: 10px;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
            padding: 20px;
            display: flex;
            flex-direction: column;
            gap: 10px;
            max-width: 900px;
            width: 100%;
        }

        .keyboard-row {
            display: flex;
            gap: 8px;
            justify-content: center;
            /* لم نعد نستخدم direction: rtl; هنا، لذا الصفوف ستكون LTR افتراضياً */
        }

        .key {
            flex-grow: 1;
            flex-basis: 0;
            background-color: #e0e0e0;
            border-radius: 6px;
            height: 50px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            font-size: 1.2em;
            font-weight: bold;
            color: #333;
            cursor: pointer;
            transition: background-color 0.1s ease, transform 0.05s ease;
            position: relative;
            user-select: none; /* Prevent text selection */
            min-width: 40px; /* Ensure a minimum width for small screens */
            padding: 5px;
            box-sizing: border-box;
            /* text-align: center; هذا يمكن أن يتعارض مع محاذاة alt-char و main-char */
        }

        .key:hover {
            background-color: #d0d0d0;
        }

        .key:active {
            background-color: #c0c0c0;
            transform: scale(0.98);
        }

        .key .main-char {
            font-size: 1.4em;
            color: #222;
            direction: rtl; /* لجعل الحرف الرئيسي (العربي) من اليمين لليسار */
            text-align: right; /* لمحاذاة الحرف الرئيسي لليمين داخل الزر */
            width: 100%; /* للتأكد من أن النص يأخذ العرض الكامل للمفتاح */
            box-sizing: border-box; /* لضمان عدم وجود مشاكل في العرض */
        }

        .key .alt-char {
            font-size: 0.8em;
            color: #666;
            position: absolute;
            top: 5px;
            left: 5px;
            direction: ltr; /* لضمان أن الحرف الألماني يُقرأ من اليسار لليمين */
            text-align: left; /* لمحاذاة الحرف الألماني لليسار */
            width: 100%; /* للتأكد من أن النص يأخذ العرض الكامل للمفتاح */
            box-sizing: border-box;
        }
        
        .key .special-key {
            font-size: 0.9em;
            color: #444;
            /* لا داعي لـ direction هنا، سيتخذ الافتراضي (LTR) */
        }

        /* Specific key widths - no change needed here */
        .key.tab, .key.backspace {
            flex-basis: 5%; /* Adjust as needed */
            min-width: 70px;
        }
        .key.capslock, .key.enter {
            flex-basis: 7%; /* Adjust as needed */
            min-width: 90px;
        }
        .key.shift {
            flex-basis: 10%; /* Adjust as needed */
            min-width: 120px;
        }
        .key.space {
            flex-grow: 4;
            min-width: 250px;
        }
        .key.ctrl, .key.alt {
            flex-basis: 4%;
            min-width: 60px;
        }
        .key.wide {
             flex-basis: 2%; /* Make these slightly wider than regular keys */
             min-width: 50px;
        }

        @media (max-width: 768px) {
            .keyboard-container {
                padding: 15px;
                gap: 8px;
            }
            .keyboard-row {
                gap: 6px;
            }
            .key {
                height: 45px;
                font-size: 1em;
                min-width: 35px;
            }
            .key .main-char {
                font-size: 1.2em;
            }
            .key .alt-char {
                font-size: 0.7em;
                top: 3px;
                left: 3px;
            }
            .key .special-key {
                font-size: 0.8em;
            }
            .key.tab, .key.backspace, .key.capslock, .key.enter, .key.shift, .key.ctrl, .key.alt {
                min-width: unset; /* Allow flexible sizing */
                flex-basis: auto;
                flex-grow: 1; /* Make them grow proportionally */
            }
        }
    </style>
</head>
<body>
    <h1 dir="rtl">لوحة مفاتيح ألمانية-عربية (افتراضية)</h1> <div class="keyboard-container">
        <div class="keyboard-row">
            <div class="key wide"><span class="main-char">ء</span><span class="alt-char">^</span></div>
            <div class="key"><span class="main-char">١</span><span class="alt-char">1</span></div>
            <div class="key"><span class="main-char">٢</span><span class="alt-char">2</span></div>
            <div class="key"><span class="main-char">٣</span><span class="alt-char">3</span></div>
            <div class="key"><span class="main-char">٤</span><span class="alt-char">4</span></div>
            <div class="key"><span class="main-char">٥</span><span class="alt-char">5</span></div>
            <div class="key"><span class="main-char">٦</span><span class="alt-char">6</span></div>
            <div class="key"><span class="main-char">٧</span><span class="alt-char">7</span></div>
            <div class="key"><span class="main-char">٨</span><span class="alt-char">8</span></div>
            <div class="key"><span class="main-char">٩</span><span class="alt-char">9</span></div>
            <div class="key"><span class="main-char">٠</span><span class="alt-char">0</span></div>
            <div class="key wide"><span class="main-char">ص</span><span class="alt-char">ß</span></div>
            <div class="key wide"><span class="main-char">ض</span><span class="alt-char">´</span></div>
            <div class="key backspace"><span class="special-key">مسافة للخلف</span></div>
        </div>

        <div class="keyboard-row">
            <div class="key tab"><span class="special-key">Tab</span></div>
            <div class="key"><span class="main-char">ق</span><span class="alt-char">Q</span></div>
            <div class="key"><span class="main-char">و</span><span class="alt-char">W</span></div>
            <div class="key"><span class="main-char">ه</span><span class="alt-char">E</span></div>
            <div class="key"><span class="main-char">ر</span><span class="alt-char">R</span></div>
            <div class="key"><span class="main-char">ت</span><span class="alt-char">T</span></div>
            <div class="key"><span class="main-char">ي</span><span class="alt-char">Z</span></div> <div class="key"><span class="main-char">و</span><span class="alt-char">U</span></div>
            <div class="key"><span class="main-char">ط</span><span class="alt-char">I</span></div>
            <div class="key"><span class="main-char">ج</span><span class="alt-char">O</span></div>
            <div class="key"><span class="main-char">د</span><span class="alt-char">P</span></div>
            <div class="key wide"><span class="main-char">ذ</span><span class="alt-char">Ü</span></div> <div class="key wide"><span class="main-char">ج</span><span class="alt-char">+</span></div>
            <div class="key wide"><span class="main-char">\</span><span class="alt-char">#</span></div>
        </div>

        <div class="keyboard-row">
            <div class="key capslock"><span class="special-key">Caps Lock</span></div>
            <div class="key"><span class="main-char">ش</span><span class="alt-char">A</span></div>
            <div class="key"><span class="main-char">س</span><span class="alt-char">S</span></div>
            <div class="key"><span class="main-char">ي</span><span class="alt-char">D</span></div>
            <div class="key"><span class="main-char">ب</span><span class="alt-char">F</span></div>
            <div class="key"><span class="main-char">ل</span><span class="alt-char">G</span></div>
            <div class="key"><span class="main-char">ا</span><span class="alt-char">H</span></div>
            <div class="key"><span class="main-char">ك</span><span class="alt-char">J</span></div>
            <div class="key"><span class="main-char">م</span><span class="alt-char">K</span></div>
            <div class="key"><span class="main-char">ن</span><span class="alt-char">L</span></div>
            <div class="key wide"><span class="main-char">ة</span><span class="alt-char">Ö</span></div> <div class="key wide"><span class="main-char">ى</span><span class="alt-char">Ä</span></div> <div class="key enter"><span class="special-key">Enter</span></div>
        </div>

        <div class="keyboard-row">
            <div class="key shift"><span class="special-key">Shift</span></div>
            <div class="key"><span class="main-char">ئ</span><span class="alt-char">Y</span></div> <div class="key"><span class="main-char">ؤ</span><span class="alt-char">X</span></div>
            <div class="key"><span class="main-char">ر</span><span class="alt-char">C</span></div>
            <div class="key"><span class="main-char">ز</span><span class="alt-char">V</span></div>
            <div class="key"><span class="main-char">ع</span><span class="alt-char">B</span></div>
            <div class="key"><span class="main-char">غ</span><span class="alt-char">N</span></div>
            <div class="key"><span class="main-char">ب</span><span class="alt-char">M</span></div>
            <div class="key wide"><span class="main-char">و</span><span class="alt-char">,</span></div>
            <div class="key wide"><span class="main-char">.</span><span class="alt-char">.</span></div>
            <div class="key wide"><span class="main-char">/</span><span class="alt-char">-</span></div>
            <div class="key shift"><span class="special-key">Shift</span></div>
        </div>

        <div class="keyboard-row">
            <div class="key ctrl"><span class="special-key">Ctrl</span></div>
            <div class="key wide"><span class="alt-char">Win</span></div>
            <div class="key alt"><span class="special-key">Alt</span></div>
            <div class="key space"><span class="main-char"></span></div> <div class="key alt"><span class="special-key">Alt Gr</span></div>
            <div class="key wide"><span class="alt-char">Win</span></div>
            <div class="key ctrl"><span class="special-key">Ctrl</span></div>
        </div>
    </div>

    <script>
        // Optional: Add some basic interaction if needed in the future
        // For now, this is purely visual.
        document.querySelectorAll('.key').forEach(key => {
            key.addEventListener('click', () => {
                const mainChar = key.querySelector('.main-char') ? key.querySelector('.main-char').textContent : '';
                const altChar = key.querySelector('.alt-char') ? key.querySelector('.alt-char').textContent : '';
                const specialKey = key.querySelector('.special-key') ? key.querySelector('.special-key').textContent : '';

                let charToDisplay = '';
                if (mainChar) charToDisplay += mainChar;
                if (altChar) charToDisplay += ` (${altChar})`;
                if (specialKey) charToDisplay = specialKey;

                console.log(`Key pressed: ${charToDisplay.trim()}`);
                // In a real application, you would send this character to an input field
            });
        });
    </script>
</body>
</html>
