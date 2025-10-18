# Rocky-wepsitee
<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Rocky Site - ❤️</title>
    <link rel="stylesheet" href="style.css"> 
</head>
<body>

    <div id="heart-container" onclick="toggleIcon()">
        <span id="icon" class="heart-icon">❤️</span> 
        <span id="middle-finger-icon" class="middle-finger-icon">🖕🏻</span> 
    </div>

    <script src="script.js"></script> 

</body>
</html>
/* كود CSS للتصميم */
body {
    /* خلفية بيضاء بالكامل */
    background-color: white; 
    /* توسيط المحتوى في المنتصف */
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh; /* جعل الارتفاع 100% من الشاشة */
    margin: 0;
    overflow: hidden; /* لمنع ظهور أشرطة التمرير */
}

#heart-container {
    /* حاوية لتوسيط وتحديد موضع القلب */
    position: relative;
    cursor: pointer; /* تغيير شكل المؤشر ليشير إلى أنه زر */
    transition: transform 0.3s ease; /* إضافة تأثير انتقال ناعم */
}

#icon, #middle-finger-icon {
    font-size: 150px; /* حجم الأيقونات المبدئي */
    line-height: 1;
    /* تأثير الحركة المبدئي (مخفي) */
    transition: transform 0.3s ease, font-size 0.3s ease;
    /* تأكد من أن كليهما لهما نفس الخصائص الأساسية */
}

.heart-icon {
    color: red; /* لون القلب */
}

.middle-finger-icon {
    color: black; /* لون الشكل الجديد */
    display: none; /* إخفاء الشكل الجديد مبدئياً */
}

/* فئات JavaScript لتطبيق التغيرات الديناميكية (الحركة والتكبير/التصغير) */

.transformed {
    /* حجم كبير وميلان خفيف عند الضغط */
    transform: rotate(5deg) scale(1.5);
    font-size: 200px !important; 
}

.small {
    /* حجم صغير بعد فترة وجيزة */
    transform: rotate(-5deg) scale(0.8);
    font-size: 100px !important;
}
// كود JavaScript للتفاعل
const heartContainer = document.getElementById('heart-container');
const heartIcon = document.getElementById('icon');
const middleFingerIcon = document.getElementById('middle-finger-icon');
let isHeart = true;
let timeoutId;

function toggleIcon() {
    // مسح أي مؤقت سابق لمنع التداخل في الحركات
    clearTimeout(timeoutId);

    if (isHeart) {
        // 1. التغيير إلى الشكل الجديد (الإصبع)
        heartIcon.style.display = 'none';
        middleFingerIcon.style.display = 'block';
        isHeart = false;
        
        // 2. تطبيق تأثير التكبير (التصنيف: transformed)
        middleFingerIcon.classList.add('transformed');

        // 3. التغيير إلى الحجم الأصغر بعد 500 مللي ثانية
        timeoutId = setTimeout(() => {
            middleFingerIcon.classList.remove('transformed');
            middleFingerIcon.classList.add('small');

            // 4. العودة إلى القلب الأحمر بعد 1000 مللي ثانية
            setTimeout(() => {
                middleFingerIcon.classList.remove('small');
                middleFingerIcon.style.display = 'none';
                heartIcon.style.display = 'block';
                isHeart = true;
            }, 1000);

        }, 500);

    } else {
        // إذا كان الشكل الجديد مرئياً، نعود إلى القلب فوراً
        middleFingerIcon.classList.remove('transformed');
        middleFingerIcon.classList.remove('small');
        middleFingerIcon.style.display = 'none';
        heartIcon.style.display = 'block';
        isHeart = true;
    }
}
