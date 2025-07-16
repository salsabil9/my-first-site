# almanzilallamin
موقع المنزل الآمن 
<!DOCTYPE html><html lang="ar">
<head>
  <meta charset="UTF-8">
  <title>المنزل الآمن لتشافي صدمات الطفولة</title>
  <style>
    body {
      font-family: 'Arial', sans-serif;
      direction: rtl;
      background-color: #fdf6f0;
      margin: 0;
      padding: 0;
    }
    header, nav, main, section {
      padding: 20px;
    }
    header {
      background-color: #f4c6a1;
      color: white;
      text-align: center;
    }
    nav {
      background-color: #fde6d0;
      display: flex;
      justify-content: space-around;
    }
    nav a {
      color: #7a4d3b;
      text-decoration: none;
      font-weight: bold;
    }
    section {
      background-color: #fff;
      margin: 10px;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
    }
    button {
      padding: 10px;
      background-color: #7a4d3b;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }
    button:hover {
      background-color: #5c392c;
    }
    .result {
      font-weight: bold;
      color: #5c392c;
      margin-top: 15px;
    }
  </style>
</head>
<body>
  <header>
    <h1>المنزل الآمن لتشافي صدمات الطفولة</h1>
  </header>  <nav>
    <a href="#home">المنزل الآمن</a>
    <a href="#female-tasks">مهمات الإناث</a>
    <a href="#male-tasks">مهمات الذكور</a>
    <a href="#progress">تقدم التشافي</a>
  </nav>  <main>
    <section id="home">
      <h2>مقدمة الموقع</h2>
      <p>هذا الموقع مخصص لمن يسعون إلى تشافي صدمات الطفولة. ستجدون هنا اختبارات نفسية، مهمات مصممة خصيصًا لدعم الإناث والذكور، بالإضافة إلى نظام نقاط لتتبع تقدمكم ودرجة التشافي المتوقعة.</p>
    </section><section id="test">
  <h2>اختبار الحالة النفسية</h2>
  <p>اختر أكثر عرض تعاني منه حاليًا:</p>
  <select id="disorder">
    <option value="">-- اختر --</option>
    <option value="الاكتئاب">أشعر بالحزن المستمر وفقدان الشغف</option>
    <option value="القلق">أشعر بالتوتر والخوف المتكرر</option>
    <option value="اضطراب الهوية">أشعر بأني لا أعرف من أنا</option>
    <option value="التعلق المرضي">أشعر أنني أعتمد على الآخرين بشكل مبالغ فيه</option>
  </select>
  <br><br>
  <button onclick="showResult()">اعرض النتيجة</button>
  <p class="result" id="result"></p>
</section>

<section id="female-tasks">
  <h2>مهمات الإناث</h2>
  <ul>
    <li>تمرين الكتابة الشعورية اليومية (5 نقاط)</li>
    <li>تأمل داخلي لمدة 10 دقائق (3 نقاط)</li>
    <li>تمرين استرجاع لحظة أمان طفولية (7 نقاط)</li>
  </ul>
</section>

<section id="male-tasks">
  <h2>مهمات الذكور</h2>
  <ul>
    <li>مشي تأملي في الطبيعة لمدة 15 دقيقة (5 نقاط)</li>
    <li>محادثة داخلية حول مشاعر مكبوتة (4 نقاط)</li>
    <li>مهمة بناء روتين صباحي ثابت (6 نقاط)</li>
  </ul>
</section>

<section id="progress">
  <h2>تقدم التشافي</h2>
  <p>مجموع نقاطك حتى الآن: <span id="points">0</span> نقطة</p>
  <p>درجة التشافي المتوقعة: <span id="level">جاري التقييم...</span></p>
  <br>
  <button onclick="updateProgress()">تحديث التقدم</button>
</section>

  </main>  <script>
    function showResult() {
      const disorder = document.getElementById("disorder").value;
      const result = document.getElementById("result");
      if (disorder === "") {
        result.innerText = "المرجو اختيار أحد الأعراض لتحديد النتيجة.";
        return;
      }
      result.innerText = `تشير الأعراض إلى احتمال وجود: ${disorder}`;
    }

    let totalPoints = 0;
    function updateProgress() {
      totalPoints += 5; // مثال بسيط فقط، يمكن تطويره لاحقًا حسب المهام المنجزة
      document.getElementById("points").innerText = totalPoints;
      let level = "";
      if (totalPoints < 10) level = "مبتدئ في التشافي";
      else if (totalPoints < 20) level = "في طريق التشافي";
      else level = "تشافي عميق";
      document.getElementById("level").innerText = level;
    }
  </script></body>
</html>
