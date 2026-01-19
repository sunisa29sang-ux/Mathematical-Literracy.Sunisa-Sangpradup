<html lang="th" class="h-full">
 <head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>คณิตศาสตร์การเงิน ป.5</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <script src="/_sdk/element_sdk.js"></script>
  <link href="https://fonts.googleapis.com/css2?family=Kanit:wght@300;400;500;600;700&amp;display=swap" rel="stylesheet">
  <style>
    body {
      box-sizing: border-box;
      font-family: 'Kanit', sans-serif;
    }
    
    .coin-bounce {
      animation: bounce 2s infinite;
    }
    
    @keyframes bounce {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-10px); }
    }
    
    .sparkle {
      animation: sparkle 1.5s infinite;
    }
    
    @keyframes sparkle {
      0%, 100% { opacity: 1; transform: scale(1); }
      50% { opacity: 0.5; transform: scale(1.2); }
    }
    
    .correct-answer {
      animation: celebrate 0.5s ease-out;
    }
    
    @keyframes celebrate {
      0% { transform: scale(1); }
      50% { transform: scale(1.1); }
      100% { transform: scale(1); }
    }
    
    .wrong-answer {
      animation: shake 0.5s ease-out;
    }
    
    @keyframes shake {
      0%, 100% { transform: translateX(0); }
      25% { transform: translateX(-5px); }
      75% { transform: translateX(5px); }
    }
    
    .money-card {
      transition: all 0.3s ease;
    }
    
    .money-card:hover {
      transform: translateY(-5px);
    }
    
    .tab-active {
      background: linear-gradient(135deg, #10b981, #059669);
      color: white;
    }
  </style>
  <style>@view-transition { navigation: auto; }</style>
  <script src="/_sdk/data_sdk.js" type="text/javascript"></script>
 </head>
 <body class="h-full bg-white">
  <div id="app" class="h-full overflow-auto"><!-- Header -->
   <header class="bg-gradient-to-r from-emerald-500 to-teal-600 text-white py-6 px-4 shadow-lg">
    <div class="max-w-4xl mx-auto text-center">
     <div class="flex justify-center items-center gap-3 mb-2"><span class="text-4xl coin-bounce">💰</span>
      <h1 id="main-title" class="text-2xl md:text-3xl font-bold">คณิตศาสตร์การเงิน ป.5</h1><span class="text-4xl coin-bounce" style="animation-delay: 0.5s;">🪙</span>
     </div>
     <p id="welcome-text" class="text-emerald-100 text-lg">มาเรียนรู้เรื่องเงินกันเถอะ!</p>
    </div>
   </header><!-- Navigation Tabs -->
   <nav class="max-w-4xl mx-auto px-4 mt-6">
    <div class="flex flex-wrap gap-2 bg-white rounded-2xl p-2 shadow-md"><button onclick="showSection('learn')" id="tab-learn" class="tab-btn flex-1 min-w-[120px] py-3 px-4 rounded-xl font-medium transition-all tab-active"> 📚 เรียนรู้ </button> <button onclick="showSection('practice')" id="tab-practice" class="tab-btn flex-1 min-w-[120px] py-3 px-4 rounded-xl font-medium transition-all bg-gray-100 text-gray-600 hover:bg-gray-200"> ✏️ แบบฝึกหัด </button> <button onclick="showSection('game')" id="tab-game" class="tab-btn flex-1 min-w-[120px] py-3 px-4 rounded-xl font-medium transition-all bg-gray-100 text-gray-600 hover:bg-gray-200"> 🎮 เกม </button>
    </div>
   </nav><!-- Main Content -->
   <main class="max-w-4xl mx-auto px-4 py-6 pb-20"><!-- Learning Section -->
    <section id="section-learn" class="space-y-6">
     <h2 class="text-xl font-bold text-emerald-800 flex items-center gap-2"><span class="sparkle">⭐</span> รู้จักเงินไทย</h2><!-- Coins -->
     <div class="bg-white rounded-2xl p-6 shadow-md">
      <h3 class="text-lg font-semibold text-gray-800 mb-4 flex items-center gap-2">🪙 เหรียญกษาปณ์</h3>
      <div class="grid grid-cols-2 md:grid-cols-5 gap-4">
       <div class="money-card bg-gradient-to-br from-gray-100 to-slate-200 rounded-xl p-4 text-center shadow-sm">
        <div class="w-12 h-12 mx-auto bg-gradient-to-br from-slate-300 to-slate-400 rounded-full flex items-center justify-center text-gray-700 font-bold text-sm mb-2 shadow-md">
         25ส.
        </div>
        <p class="font-medium text-slate-700">25 สตางค์</p>
        <p class="text-xs text-slate-500">0.25 บาท</p>
       </div>
       <div class="money-card bg-gradient-to-br from-gray-100 to-slate-200 rounded-xl p-4 text-center shadow-sm">
        <div class="w-12 h-12 mx-auto bg-gradient-to-br from-slate-300 to-slate-400 rounded-full flex items-center justify-center text-gray-700 font-bold text-sm mb-2 shadow-md">
         50ส.
        </div>
        <p class="font-medium text-slate-700">50 สตางค์</p>
        <p class="text-xs text-slate-500">0.50 บาท</p>
       </div>
       <div class="money-card bg-gradient-to-br from-gray-100 to-slate-200 rounded-xl p-4 text-center shadow-sm">
        <div class="w-14 h-14 mx-auto bg-gradient-to-br from-slate-200 to-slate-300 rounded-full flex items-center justify-center text-gray-700 font-bold mb-2 shadow-md">
         1
        </div>
        <p class="font-medium text-slate-700">1 บาท</p>
       </div>
       <div class="money-card bg-gradient-to-br from-yellow-100 to-amber-100 rounded-xl p-4 text-center shadow-sm">
        <div class="w-14 h-14 mx-auto bg-gradient-to-br from-yellow-400 to-yellow-500 rounded-full flex items-center justify-center text-yellow-900 font-bold mb-2 shadow-md">
         2
        </div>
        <p class="font-medium text-yellow-800">2 บาท</p>
       </div>
       <div class="money-card bg-gradient-to-br from-gray-100 to-slate-200 rounded-xl p-4 text-center shadow-sm">
        <div class="w-14 h-14 mx-auto bg-gradient-to-br from-slate-200 to-slate-300 rounded-full flex items-center justify-center text-gray-700 font-bold mb-2 shadow-md">
         5
        </div>
        <p class="font-medium text-slate-700">5 บาท</p>
       </div>
       <div class="money-card bg-gradient-to-br from-amber-100 to-yellow-100 rounded-xl p-4 text-center shadow-sm col-span-2 md:col-span-1">
        <div class="w-16 h-16 mx-auto rounded-full flex items-center justify-center font-bold mb-2 border-4 border-amber-400 bg-gradient-to-br from-gray-300 to-gray-400 text-gray-700">
         10
        </div>
        <p class="font-medium text-gray-800">10 บาท</p>
        <p class="text-xs text-gray-500">เหรียญสองสี</p>
       </div>
      </div>
     </div><!-- Banknotes -->
     <div class="bg-white rounded-2xl p-6 shadow-md">
      <h3 class="text-lg font-semibold text-gray-800 mb-4 flex items-center gap-2">💵 ธนบัตร</h3>
      <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
       <div class="money-card bg-gradient-to-r from-green-400 to-green-500 rounded-xl p-4 text-white shadow-sm">
        <div class="flex justify-between items-center"><span class="text-3xl font-bold">฿20</span> <span class="text-green-100">ธนบัตรสีเขียว</span>
        </div>
       </div>
       <div class="money-card bg-gradient-to-r from-purple-400 to-purple-500 rounded-xl p-4 text-white shadow-sm">
        <div class="flex justify-between items-center"><span class="text-3xl font-bold">฿50</span> <span class="text-purple-100">ธนบัตรสีม่วง</span>
        </div>
       </div>
       <div class="money-card bg-gradient-to-r from-red-400 to-red-500 rounded-xl p-4 text-white shadow-sm">
        <div class="flex justify-between items-center"><span class="text-3xl font-bold">฿100</span> <span class="text-red-100">ธนบัตรสีแดง</span>
        </div>
       </div>
       <div class="money-card bg-gradient-to-r from-blue-400 to-blue-500 rounded-xl p-4 text-white shadow-sm">
        <div class="flex justify-between items-center"><span class="text-3xl font-bold">฿500</span> <span class="text-blue-100">ธนบัตรสีน้ำเงิน</span>
        </div>
       </div>
       <div class="money-card bg-gradient-to-r from-amber-400 to-amber-500 rounded-xl p-4 text-white shadow-sm md:col-span-2">
        <div class="flex justify-between items-center"><span class="text-3xl font-bold">฿1,000</span> <span class="text-amber-100">ธนบัตรสีน้ำตาล (ราคาสูงสุด)</span>
        </div>
       </div>
      </div>
     </div><!-- Conversion Tips -->
     <div class="bg-gradient-to-r from-emerald-500 to-teal-500 rounded-2xl p-6 text-white shadow-md">
      <h3 class="text-lg font-semibold mb-4 flex items-center gap-2">💡 ความรู้สำคัญ</h3>
      <ul class="space-y-3">
       <li class="flex items-start gap-3"><span class="bg-white/20 rounded-full w-6 h-6 flex items-center justify-center text-sm flex-shrink-0">1</span> <span>1 บาท = 100 สตางค์</span></li>
       <li class="flex items-start gap-3"><span class="bg-white/20 rounded-full w-6 h-6 flex items-center justify-center text-sm flex-shrink-0">2</span> <span>25 สตางค์ = 0.25 บาท (หนึ่งในสี่ของบาท)</span></li>
       <li class="flex items-start gap-3"><span class="bg-white/20 rounded-full w-6 h-6 flex items-center justify-center text-sm flex-shrink-0">3</span> <span>50 สตางค์ = 0.50 บาท (ครึ่งบาท)</span></li>
       <li class="flex items-start gap-3"><span class="bg-white/20 rounded-full w-6 h-6 flex items-center justify-center text-sm flex-shrink-0">4</span> <span>เงินทอน = เงินที่จ่าย - ราคาสินค้า</span></li>
      </ul>
     </div>
    </section><!-- Practice Section -->
    <section id="section-practice" class="space-y-6 hidden">
     <h2 class="text-xl font-bold text-emerald-800 flex items-center gap-2"><span class="sparkle">✏️</span> แบบฝึกหัด</h2><!-- Practice Type Selection -->
     <div class="grid grid-cols-1 md:grid-cols-3 gap-4"><button onclick="startPractice('addition')" class="bg-white rounded-2xl p-6 shadow-md hover:shadow-lg transition-all text-left group">
       <div class="text-4xl mb-3 group-hover:scale-110 transition-transform">
        ➕
       </div><h3 class="font-bold text-gray-800">บวกเงิน</h3><p class="text-sm text-gray-500">รวมเงินหลายจำนวน</p></button> <button onclick="startPractice('subtraction')" class="bg-white rounded-2xl p-6 shadow-md hover:shadow-lg transition-all text-left group">
       <div class="text-4xl mb-3 group-hover:scale-110 transition-transform">
        ➖
       </div><h3 class="font-bold text-gray-800">ลบเงิน (เงินทอน)</h3><p class="text-sm text-gray-500">คำนวณเงินทอน</p></button> <button onclick="startPractice('mixed')" class="bg-white rounded-2xl p-6 shadow-md hover:shadow-lg transition-all text-left group">
       <div class="text-4xl mb-3 group-hover:scale-110 transition-transform">
        🔀
       </div><h3 class="font-bold text-gray-800">โจทย์รวม</h3><p class="text-sm text-gray-500">ฝึกทั้งบวกและลบ</p></button>
     </div><!-- Practice Area -->
     <div id="practice-area" class="hidden">
      <div class="bg-white rounded-2xl p-6 shadow-md">
       <div class="flex justify-between items-center mb-4"><span id="practice-type-label" class="bg-emerald-100 text-emerald-700 px-4 py-1 rounded-full text-sm font-medium">บวกเงิน</span> <span id="practice-score" class="text-gray-600">คะแนน: <span class="font-bold text-emerald-600">0</span>/10</span>
       </div>
       <div id="practice-question" class="text-center py-8">
        <p class="text-lg text-gray-600 mb-4" id="question-text">ราคาสมุด 15 บาท และดินสอ 8 บาท รวมเป็นเงินเท่าไร?</p>
        <div class="flex justify-center items-center gap-4 text-3xl font-bold text-emerald-700" id="question-visual">
         15 + 8 = ?
        </div>
       </div>
       <div class="flex flex-col items-center gap-4">
        <div class="flex items-center gap-2"><input type="number" id="practice-answer" class="w-32 text-center text-2xl font-bold border-2 border-emerald-300 rounded-xl py-3 focus:border-emerald-500 focus:outline-none" placeholder="?"> <span class="text-xl text-gray-600">บาท</span>
        </div><button onclick="checkPracticeAnswer()" class="bg-gradient-to-r from-emerald-500 to-teal-500 text-white px-8 py-3 rounded-xl font-medium hover:from-emerald-600 hover:to-teal-600 transition-all shadow-md"> ตรวจคำตอบ </button>
       </div>
       <div id="practice-feedback" class="mt-4 text-center hidden">
        <p id="feedback-text" class="text-lg font-medium"></p>
       </div>
      </div>
     </div>
    </section><!-- Game Section -->
    <section id="section-game" class="space-y-6 hidden">
     <h2 class="text-xl font-bold text-emerald-800 flex items-center gap-2"><span class="sparkle">🎮</span> เกมซื้อของ</h2>
     <div class="bg-white rounded-2xl p-6 shadow-md">
      <div class="flex justify-between items-center mb-6">
       <div class="flex items-center gap-2"><span class="text-2xl">👛</span> <span class="text-lg">เงินของฉัน:</span> <span id="my-money" class="text-2xl font-bold text-emerald-600">100 บาท</span>
       </div><button onclick="resetGame()" class="text-gray-500 hover:text-gray-700 text-sm underline">เริ่มใหม่</button>
      </div><!-- Shop Items -->
      <div class="grid grid-cols-2 md:grid-cols-4 gap-4 mb-6">
       <div class="shop-item bg-gradient-to-br from-pink-50 to-pink-100 rounded-xl p-4 text-center cursor-pointer hover:shadow-md transition-all" onclick="buyItem('ไอศกรีม', 15)">
        <div class="text-4xl mb-2">
         🍦
        </div>
        <p class="font-medium text-gray-800">ไอศกรีม</p>
        <p class="text-emerald-600 font-bold">15 บาท</p>
       </div>
       <div class="shop-item bg-gradient-to-br from-blue-50 to-blue-100 rounded-xl p-4 text-center cursor-pointer hover:shadow-md transition-all" onclick="buyItem('น้ำดื่ม', 10)">
        <div class="text-4xl mb-2">
         💧
        </div>
        <p class="font-medium text-gray-800">���้ำดื่ม</p>
        <p class="text-emerald-600 font-bold">10 บาท</p>
       </div>
       <div class="shop-item bg-gradient-to-br from-yellow-50 to-yellow-100 rounded-xl p-4 text-center cursor-pointer hover:shadow-md transition-all" onclick="buyItem('ขนมปัง', 25)">
        <div class="text-4xl mb-2">
         🍞
        </div>
        <p class="font-medium text-gray-800">ขนมปัง</p>
        <p class="text-emerald-600 font-bold">25 บาท</p>
       </div>
       <div class="shop-item bg-gradient-to-br from-orange-50 to-orange-100 rounded-xl p-4 text-center cursor-pointer hover:shadow-md transition-all" onclick="buyItem('ส้ม', 8)">
        <div class="text-4xl mb-2">
         🍊
        </div>
        <p class="font-medium text-gray-800">ส้ม</p>
        <p class="text-emerald-600 font-bold">8 บาท</p>
       </div>
       <div class="shop-item bg-gradient-to-br from-red-50 to-red-100 rounded-xl p-4 text-center cursor-pointer hover:shadow-md transition-all" onclick="buyItem('แอปเปิ้ล', 12)">
        <div class="text-4xl mb-2">
         🍎
        </div>
        <p class="font-medium text-gray-800">แอปเปิ้ล</p>
        <p class="text-emerald-600 font-bold">12 บาท</p>
       </div>
       <div class="shop-item bg-gradient-to-br from-purple-50 to-purple-100 rounded-xl p-4 text-center cursor-pointer hover:shadow-md transition-all" onclick="buyItem('นม', 18)">
        <div class="text-4xl mb-2">
         🥛
        </div>
        <p class="font-medium text-gray-800">นม</p>
        <p class="text-emerald-600 font-bold">18 บาท</p>
       </div>
       <div class="shop-item bg-gradient-to-br from-green-50 to-green-100 rounded-xl p-4 text-center cursor-pointer hover:shadow-md transition-all" onclick="buyItem('สมุด', 20)">
        <div class="text-4xl mb-2">
         📓
        </div>
        <p class="font-medium text-gray-800">สมุด</p>
        <p class="text-emerald-600 font-bold">20 บาท</p>
       </div>
       <div class="shop-item bg-gradient-to-br from-indigo-50 to-indigo-100 rounded-xl p-4 text-center cursor-pointer hover:shadow-md transition-all" onclick="buyItem('ดินสอ', 5)">
        <div class="text-4xl mb-2">
         ✏️
        </div>
        <p class="font-medium text-gray-800">ดินสอ</p>
        <p class="text-emerald-600 font-bold">5 บาท</p>
       </div>
      </div><!-- Shopping Cart -->
      <div class="bg-gray-50 rounded-xl p-4">
       <h3 class="font-semibold text-gray-700 mb-3 flex items-center gap-2">🛒 ตะกร้าสินค้า</h3>
       <div id="cart-items" class="space-y-2 mb-4 min-h-[60px]">
        <p class="text-gray-400 text-center py-4">ยังไม่มีสินค���าในตะกร้า</p>
       </div>
       <div class="flex justify-between items-center pt-4 border-t border-gray-200"><span class="font-medium text-gray-700">รวมทั้งหมด:</span> <span id="cart-total" class="text-xl font-bold text-emerald-600">0 บาท</span>
       </div>
      </div><!-- Game Message -->
      <div id="game-message" class="mt-4 text-center hidden">
       <p id="game-message-text" class="text-lg font-medium py-4 rounded-xl"></p>
      </div>
     </div>
    </section>
   </main><!-- Footer - Creator Info -->
   <footer class="bg-gradient-to-r from-emerald-500 to-teal-600 text-white py-6 px-4 mt-12">
    <div class="max-w-4xl mx-auto text-center">
     <div class="bg-white/10 backdrop-blur-sm rounded-2xl p-6 inline-block">
      <p class="text-emerald-100 text-sm mb-2">👩‍🎓 ผู้สร้างเกม</p>
      <h3 class="text-xl md:text-2xl font-bold mb-2">เ��็กหญิงสุนิสา แสงประดับ</h3>
      <div class="flex justify-center items-center gap-3 flex-wrap"><span class="bg-white/20 px-4 py-1 rounded-full text-sm font-medium">ปีที่ 5/5</span> <span class="bg-white/20 px-4 py-1 rounded-full text-sm font-medium">สาย MEP</span>
      </div>
     </div>
    </div>
   </footer>
  </div>
  <script>
    // Configuration
    const defaultConfig = {
      app_title: 'คณิตศาสตร์การเงิน ป.5',
      welcome_message: 'มาเรียนรู้เรื่องเงินกันเถอะ!',
      background_color: '#ffffff',
      primary_color: '#10b981',
      text_color: '#1f2937',
      secondary_surface_color: '#f3f4f6',
      accent_color: '#0d9488'
    };

    let config = { ...defaultConfig };

    // Practice state
    let practiceType = '';
    let practiceScore = 0;
    let practiceQuestion = 0;
    let currentAnswer = 0;

    // Game state
    let myMoney = 100;
    let cart = [];

    // Section navigation
    function showSection(section) {
      document.querySelectorAll('[id^="section-"]').forEach(el => el.classList.add('hidden'));
      document.getElementById(`section-${section}`).classList.remove('hidden');
      
      document.querySelectorAll('.tab-btn').forEach(btn => {
        btn.classList.remove('tab-active');
        btn.classList.add('bg-gray-100', 'text-gray-600');
      });
      
      const activeTab = document.getElementById(`tab-${section}`);
      activeTab.classList.add('tab-active');
      activeTab.classList.remove('bg-gray-100', 'text-gray-600');
    }

    // Practice functions
    function startPractice(type) {
      practiceType = type;
      practiceScore = 0;
      practiceQuestion = 0;
      
      const labels = {
        addition: 'บวกเงิน',
        subtraction: 'ลบเงิน (เงินทอน)',
        mixed: 'โจทย์รวม'
      };
      
      document.getElementById('practice-type-label').textContent = labels[type];
      document.getElementById('practice-area').classList.remove('hidden');
      updateScore();
      generateQuestion();
    }

    function generateQuestion() {
      const items = [
        { name: 'สมุด', emoji: '📓' },
        { name: 'ดินสอ', emoji: '✏️' },
        { name: 'ยางลบ', emoji: '🧽' },
        { name: 'ไม้บรรทัด', emoji: '📏' },
        { name: 'ขนม', emoji: '🍪' },
        { name: 'น้ำ', emoji: '💧' },
        { name: 'นม', emoji: '🥛' },
        { name: 'แอปเปิ้ล', emoji: '🍎' }
      ];

      let questionType = practiceType;
      if (practiceType === 'mixed') {
        questionType = Math.random() > 0.5 ? 'addition' : 'subtraction';
      }

      const item1 = items[Math.floor(Math.random() * items.length)];
      const item2 = items[Math.floor(Math.random() * items.length)];
      const price1 = Math.floor(Math.random() * 40) + 5;
      const price2 = Math.floor(Math.random() * 30) + 5;

      let questionText, visualText;

      if (questionType === 'addition') {
        currentAnswer = price1 + price2;
        questionText = `ราคา${item1.name} ${price1} บาท และ${item2.name} ${price2} บาท รวมเป็นเงินเท่าไร?`;
        visualText = `${item1.emoji} ${price1} + ${item2.emoji} ${price2} = ?`;
      } else {
        const paid = Math.ceil((price1 + 10) / 10) * 10;
        currentAnswer = paid - price1;
        questionText = `ซื้อ${item1.name}ราคา ${price1} บาท จ่ายเงิ�� ${paid} บาท ได้เงินทอนเท่าไร?`;
        visualText = `💵 ${paid} - ${item1.emoji} ${price1} = ?`;
      }

      document.getElementById('question-text').textContent = questionText;
      document.getElementById('question-visual').textContent = visualText;
      document.getElementById('practice-answer').value = '';
      document.getElementById('practice-feedback').classList.add('hidden');
    }

    function checkPracticeAnswer() {
      const userAnswer = parseInt(document.getElementById('practice-answer').value);
      const feedbackEl = document.getElementById('practice-feedback');
      const feedbackText = document.getElementById('feedback-text');
      const questionEl = document.getElementById('practice-question');

      feedbackEl.classList.remove('hidden');

      if (userAnswer === currentAnswer) {
        practiceScore++;
        feedbackText.textContent = '🎉 ถูกต้อง! เก่งมาก!';
        feedbackText.className = 'text-lg font-medium text-emerald-600';
        questionEl.classList.add('correct-answer');
        setTimeout(() => questionEl.classList.remove('correct-answer'), 500);
      } else {
        feedbackText.textContent = `❌ ไม่ถูกต้อง คำตอบคือ ${currentAnswer} บาท`;
        feedbackText.className = 'text-lg font-medium text-red-500';
        questionEl.classList.add('wrong-answer');
        setTimeout(() => questionEl.classList.remove('wrong-answer'), 500);
      }

      practiceQuestion++;
      updateScore();

      if (practiceQuestion >= 10) {
        setTimeout(() => {
          feedbackText.textContent = `🏆 จบแบบฝึกหัด! คะแนนของคุณ: ${practiceScore}/10`;
          feedbackText.className = 'text-lg font-medium text-emerald-600';
        }, 1500);
      } else {
        setTimeout(generateQuestion, 1500);
      }
    }

    function updateScore() {
      document.getElementById('practice-score').innerHTML = `คะแนน: <span class="font-bold text-emerald-600">${practiceScore}</span>/10`;
    }

    // Game functions
    function buyItem(name, price) {
      if (myMoney >= price) {
        myMoney -= price;
        cart.push({ name, price });
        updateGame();
        showGameMessage(`✅ ซื้อ${name}แล้ว! จ่าย ${price} บาท`, 'success');
      } else {
        showGameMessage(`❌ เงินไม่พอ! ต้องการ ${price} บาท แต่มีเพียง ${myMoney} บาท`, 'error');
      }
    }

    function updateGame() {
      document.getElementById('my-money').textContent = `${myMoney} บาท`;
      
      const cartEl = document.getElementById('cart-items');
      const total = cart.reduce((sum, item) => sum + item.price, 0);
      
      if (cart.length === 0) {
        cartEl.innerHTML = '<p class="text-gray-400 text-center py-4">ยังไม่มีสินค้าในตะกร้า</p>';
      } else {
        cartEl.innerHTML = cart.map((item, index) => `
          <div class="flex justify-between items-center bg-white rounded-lg px-3 py-2">
            <span>${item.name}</span>
            <div class="flex items-center gap-2">
              <span class="text-emerald-600">${item.price} บาท</span>
              <button onclick="removeItem(${index})" class="text-red-400 hover:text-red-600 text-sm">✕</button>
            </div>
          </div>
        `).join('');
      }
      
      document.getElementById('cart-total').textContent = `${total} บาท`;
    }

    function removeItem(index) {
      const item = cart[index];
      myMoney += item.price;
      cart.splice(index, 1);
      updateGame();
      showGameMessage(`🔄 คืน${item.name}แล้ว ได้เงินคืน ${item.price} บาท`, 'info');
    }

    function resetGame() {
      myMoney = 100;
      cart = [];
      updateGame();
      showGameMessage('🔄 เริ่มเกมใหม่! มีเงิน 100 บาท', 'info');
    }

    function showGameMessage(message, type) {
      const msgEl = document.getElementById('game-message');
      const msgText = document.getElementById('game-message-text');
      
      msgEl.classList.remove('hidden');
      msgText.textContent = message;
      
      const colors = {
        success: 'bg-emerald-100 text-emerald-700',
        error: 'bg-red-100 text-red-700',
        info: 'bg-blue-100 text-blue-700'
      };
      
      msgText.className = `text-lg font-medium py-4 rounded-xl ${colors[type]}`;
      
      setTimeout(() => msgEl.classList.add('hidden'), 3000);
    }

    // Config change handler
    async function onConfigChange(newConfig) {
      config = { ...defaultConfig, ...newConfig };
      
      // Update title
      const titleEl = document.getElementById('main-title');
      if (titleEl) titleEl.textContent = config.app_title || defaultConfig.app_title;
      
      // Update welcome message
      const welcomeEl = document.getElementById('welcome-text');
      if (welcomeEl) welcomeEl.textContent = config.welcome_message || defaultConfig.welcome_message;
      
      // Apply colors
      document.body.style.background = `linear-gradient(to bottom right, ${config.background_color}, ${adjustColor(config.background_color, -10)})`;
      
      document.querySelectorAll('.tab-active').forEach(el => {
        el.style.background = `linear-gradient(135deg, ${config.primary_color}, ${config.accent_color})`;
      });
    }

    function adjustColor(color, amount) {
      const hex = color.replace('#', '');
      const r = Math.max(0, Math.min(255, parseInt(hex.substr(0, 2), 16) + amount));
      const g = Math.max(0, Math.min(255, parseInt(hex.substr(2, 2), 16) + amount));
      const b = Math.max(0, Math.min(255, parseInt(hex.substr(4, 2), 16) + amount));
      return `#${r.toString(16).padStart(2, '0')}${g.toString(16).padStart(2, '0')}${b.toString(16).padStart(2, '0')}`;
    }

    // Initialize SDK
    if (window.elementSdk) {
      window.elementSdk.init({
        defaultConfig,
        onConfigChange,
        mapToCapabilities: (cfg) => ({
          recolorables: [
            {
              get: () => cfg.background_color || defaultConfig.background_color,
              set: (v) => { cfg.background_color = v; window.elementSdk.setConfig({ background_color: v }); }
            },
            {
              get: () => cfg.secondary_surface_color || defaultConfig.secondary_surface_color,
              set: (v) => { cfg.secondary_surface_color = v; window.elementSdk.setConfig({ secondary_surface_color: v }); }
            },
            {
              get: () => cfg.text_color || defaultConfig.text_color,
              set: (v) => { cfg.text_color = v; window.elementSdk.setConfig({ text_color: v }); }
            },
            {
              get: () => cfg.primary_color || defaultConfig.primary_color,
              set: (v) => { cfg.primary_color = v; window.elementSdk.setConfig({ primary_color: v }); }
            },
            {
              get: () => cfg.accent_color || defaultConfig.accent_color,
              set: (v) => { cfg.accent_color = v; window.elementSdk.setConfig({ accent_color: v }); }
            }
          ],
          borderables: [],
          fontEditable: undefined,
          fontSizeable: undefined
        }),
        mapToEditPanelValues: (cfg) => new Map([
          ['app_title', cfg.app_title || defaultConfig.app_title],
          ['welcome_message', cfg.welcome_message || defaultConfig.welcome_message]
        ])
      });
    }
  </script>
 <script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'9c031fe7f7d774f2',t:'MTc2ODc5MjA3Ni4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script></body>
</html>
