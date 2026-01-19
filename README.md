<html lang="th" class="h-full">
 <head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>คณิตศาสตร์การเงิน ป.5</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <script src="/_sdk/element_sdk.js"></script>
  <link href="https://fonts.googleapis.com/css2?family=Prompt:wght@300;400;500;600;700&amp;display=swap" rel="stylesheet">
  <style>
    body {
      box-sizing: border-box;
      font-family: 'Prompt', sans-serif;
    }
    
    .coin-bounce {
      animation: bounce 0.5s ease-in-out;
    }
    
    @keyframes bounce {
      0%, 100% { transform: scale(1); }
      50% { transform: scale(1.2); }
    }
    
    .correct-flash {
      animation: correctFlash 0.6s ease-out;
    }
    
    @keyframes correctFlash {
      0% { background-color: #10b981; }
      100% { background-color: transparent; }
    }
    
    .wrong-shake {
      animation: shake 0.5s ease-in-out;
    }
    
    @keyframes shake {
      0%, 100% { transform: translateX(0); }
      25% { transform: translateX(-10px); }
      75% { transform: translateX(10px); }
    }
    
    .star-spin {
      animation: spin 1s linear;
    }
    
    @keyframes spin {
      from { transform: rotate(0deg); }
      to { transform: rotate(360deg); }
    }
    
    .gradient-bg {
      background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    }
    
    .card-shadow {
      box-shadow: 0 10px 40px rgba(102, 126, 234, 0.3);
    }
  </style>
  <style>@view-transition { navigation: auto; }</style>
  <script src="/_sdk/data_sdk.js" type="text/javascript"></script>
 </head>
 <body class="h-full bg-gradient-to-br from-indigo-100 via-purple-50 to-pink-100">
  <div id="app" class="h-full overflow-auto"><!-- Header -->
   <header class="gradient-bg text-white py-4 px-6 shadow-lg">
    <div class="max-w-4xl mx-auto flex items-center justify-between">
     <div class="flex items-center gap-3">
      <div class="text-4xl">
       💰
      </div>
      <div>
       <h1 id="app-title" class="text-2xl font-bold">คณิตศาสตร์การเงิน ป.5</h1>
       <p id="welcome-msg" class="text-purple-200 text-sm">เรียนรู้เรื่องเงินอย่างสนุกสนาน!</p>
      </div>
     </div>
     <div class="flex items-center gap-2 bg-white/20 rounded-full px-4 py-2"><span class="text-yellow-300 text-xl">⭐</span> <span id="total-score" class="font-bold text-lg">0</span> <span class="text-sm">คะแนน</span>
     </div>
    </div>
   </header><!-- Main Content -->
   <main class="max-w-4xl mx-auto p-6"><!-- Menu -->
    <div id="menu-section" class="grid grid-cols-1 md:grid-cols-2 gap-6 mb-8"><!-- บทเรียนที่ 1 -->
     <div onclick="selectLesson(1)" class="bg-white rounded-2xl p-6 card-shadow cursor-pointer hover:scale-105 transition-transform duration-300">
      <div class="flex items-center gap-4 mb-4">
       <div class="w-16 h-16 bg-gradient-to-br from-yellow-400 to-orange-500 rounded-xl flex items-center justify-center text-3xl shadow-lg">
        🪙
       </div>
       <div>
        <h3 class="font-bold text-lg text-gray-800">บทที่ 1: รู้จักเหรียญ</h3>
        <p class="text-gray-500 text-sm">เรียนรู้ค่าของเหรียญต่างๆ</p>
       </div>
      </div>
      <div class="flex items-center justify-between">
       <div class="flex gap-1"><span id="lesson1-star1" class="text-gray-300 text-xl">⭐</span> <span id="lesson1-star2" class="text-gray-300 text-xl">⭐</span> <span id="lesson1-star3" class="text-gray-300 text-xl">⭐</span>
       </div><span class="text-purple-600 font-medium">เริ่มเรียน →</span>
      </div>
     </div><!-- บทเรียนที่ 2 -->
     <div onclick="selectLesson(2)" class="bg-white rounded-2xl p-6 card-shadow cursor-pointer hover:scale-105 transition-transform duration-300">
      <div class="flex items-center gap-4 mb-4">
       <div class="w-16 h-16 bg-gradient-to-br from-green-400 to-emerald-500 rounded-xl flex items-center justify-center text-3xl shadow-lg">
        💵
       </div>
       <div>
        <h3 class="font-bold text-lg text-gray-800">บทที่ 2: รู้จักธนบัตร</h3>
        <p class="text-gray-500 text-sm">เรียนรู้ค่าของธนบัตร</p>
       </div>
      </div>
      <div class="flex items-center justify-between">
       <div class="flex gap-1"><span id="lesson2-star1" class="text-gray-300 text-xl">⭐</span> <span id="lesson2-star2" class="text-gray-300 text-xl">⭐</span> <span id="lesson2-star3" class="text-gray-300 text-xl">⭐</span>
       </div><span class="text-purple-600 font-medium">เริ่มเรียน →</span>
      </div>
     </div><!-- บทเรียนที่ 3 -->
     <div onclick="selectLesson(3)" class="bg-white rounded-2xl p-6 card-shadow cursor-pointer hover:scale-105 transition-transform duration-300">
      <div class="flex items-center gap-4 mb-4">
       <div class="w-16 h-16 bg-gradient-to-br from-blue-400 to-cyan-500 rounded-xl flex items-center justify-center text-3xl shadow-lg">
        🛒
       </div>
       <div>
        <h3 class="font-bold text-lg text-gray-800">บทที่ 3: ซื้อของคิดเงิน</h3>
        <p class="text-gray-500 text-sm">ฝึกคำนวณราคาสินค้���</p>
       </div>
      </div>
      <div class="flex items-center justify-between">
       <div class="flex gap-1"><span id="lesson3-star1" class="text-gray-300 text-xl">⭐</span> <span id="lesson3-star2" class="text-gray-300 text-xl">⭐</span> <span id="lesson3-star3" class="text-gray-300 text-xl">⭐</span>
       </div><span class="text-purple-600 font-medium">เริ่มเรียน →</span>
      </div>
     </div><!-- บทเรียนที่ 4 -->
     <div onclick="selectLesson(4)" class="bg-white rounded-2xl p-6 card-shadow cursor-pointer hover:scale-105 transition-transform duration-300">
      <div class="flex items-center gap-4 mb-4">
       <div class="w-16 h-16 bg-gradient-to-br from-pink-400 to-rose-500 rounded-xl flex items-center justify-center text-3xl shadow-lg">
        💱
       </div>
       <div>
        <h3 class="font-bold text-lg text-gray-800">บทที่ 4: ทอนเงิน</h3>
        <p class="text-gray-500 text-sm">ฝึกคิดเงินทอน</p>
       </div>
      </div>
      <div class="flex items-center justify-between">
       <div class="flex gap-1"><span id="lesson4-star1" class="text-gray-300 text-xl">⭐</span> <span id="lesson4-star2" class="text-gray-300 text-xl">⭐</span> <span id="lesson4-star3" class="text-gray-300 text-xl">⭐</span>
       </div><span class="text-purple-600 font-medium">เริ่มเรียน →</span>
      </div>
     </div>
    </div><!-- Quiz Section (Hidden by default) -->
    <div id="quiz-section" class="hidden">
     <div class="bg-white rounded-2xl p-6 card-shadow"><!-- Quiz Header -->
      <div class="flex items-center justify-between mb-6"><button onclick="backToMenu()" class="flex items-center gap-2 text-purple-600 hover:text-purple-800 transition-colors"> <span>��</span> <span>กลับหน้าหลัก</span> </button>
       <div class="flex items-center gap-4">
        <div class="text-sm text-gray-500">
         ข้อ <span id="current-question" class="font-bold text-purple-600">1</span> / <span id="total-questions">5</span>
        </div>
        <div class="flex items-center gap-1 bg-yellow-100 rounded-full px-3 py-1"><span class="text-yellow-500">⭐</span> <span id="quiz-score" class="font-bold text-yellow-600">0</span>
        </div>
       </div>
      </div><!-- Progress Bar -->
      <div class="w-full bg-gray-200 rounded-full h-3 mb-6">
       <div id="progress-bar" class="bg-gradient-to-r from-purple-500 to-pink-500 h-3 rounded-full transition-all duration-500" style="width: 20%"></div>
      </div><!-- Question Display -->
      <div id="question-container" class="text-center mb-8">
       <div id="question-icon" class="text-6xl mb-4">
        🪙
       </div>
       <h2 id="question-text" class="text-xl font-bold text-gray-800 mb-2">คำถาม</h2>
       <p id="question-hint" class="text-gray-500">คำใบ้</p>
      </div><!-- Visual Display -->
      <div id="visual-display" class="flex justify-center flex-wrap gap-3 mb-8 min-h-[80px]"><!-- Dynamic content -->
      </div><!-- Answer Options -->
      <div id="answer-options" class="grid grid-cols-2 gap-4 mb-6"><!-- Dynamic options -->
      </div><!-- Feedback -->
      <div id="feedback" class="hidden text-center p-4 rounded-xl mb-4"><span id="feedback-icon" class="text-4xl"></span>
       <p id="feedback-text" class="font-bold mt-2"></p>
      </div><!-- Next Button --> <button id="next-btn" onclick="nextQuestion()" class="hidden w-full py-4 bg-gradient-to-r from-purple-500 to-pink-500 text-white font-bold rounded-xl hover:opacity-90 transition-opacity"> ข้อถัดไป → </button>
     </div>
    </div><!-- Result Section (Hidden by default) -->
    <div id="result-section" class="hidden">
     <div class="bg-white rounded-2xl p-8 card-shadow text-center">
      <div id="result-stars" class="text-6xl mb-4">
       ⭐⭐⭐
      </div>
      <h2 id="result-title" class="text-2xl font-bold text-gray-800 mb-2">ยอดเยี่ยม!</h2>
      <p id="result-message" class="text-gray-600 mb-6">คุณทำได้ดีมาก!</p>
      <div class="bg-purple-50 rounded-xl p-6 mb-6">
       <p class="text-gray-600">คะแนนที่ได้</p>
       <p class="text-4xl font-bold text-purple-600"><span id="final-score">0</span> / <span id="max-score">50</span></p>
      </div>
      <div class="flex gap-4"><button onclick="retryLesson()" class="flex-1 py-3 bg-gray-100 text-gray-700 font-bold rounded-xl hover:bg-gray-200 transition-colors"> 🔄 ทำอีกครั้ง </button> <button onclick="backToMenu()" class="flex-1 py-3 bg-gradient-to-r from-purple-500 to-pink-500 text-white font-bold rounded-xl hover:opacity-90 transition-opacity"> 🏠 กลับหน้าหลัก </button>
      </div>
     </div>
    </div>
   </main><!-- Footer -->
   <footer class="bg-white/80 backdrop-blur-sm border-t border-purple-200 py-6 mt-8">
    <div class="max-w-4xl mx-auto px-6 text-center">
     <div class="flex items-center justify-center gap-3 mb-2"><span class="text-2xl">👨‍💻</span>
      <div class="text-left">
       <p class="text-sm text-gray-500">ผู้สร้างเกม</p>
       <p class="font-bold text-purple-700">เด็กชาย ธีทัต เพ็ชรหิน</p>
      </div>
     </div>
     <div class="flex items-center justify-center gap-2 text-sm text-gray-600"><span class="inline-flex items-center gap-1 bg-gradient-to-r from-blue-50 to-purple-50 px-3 py-1 rounded-full border border-purple-200"> <span>🎓</span> <span>ชั้นประถมศึกษาปีที่ 5</span> </span> <span class="inline-flex items-center gap-1 bg-gradient-to-r from-purple-50 to-pink-50 px-3 py-1 rounded-full border border-purple-200"> <span>🌟</span> <span>สายชั้น MEP</span> </span>
     </div>
    </div>
   </footer>
  </div>
  <script>
    // Default configuration
    const defaultConfig = {
      app_title: 'คณิตศาสตร์การเงิน ป.5',
      welcome_message: 'เรียนรู้เรื่องเงินอย่างสนุกสนาน!',
      primary_color: '#667eea',
      secondary_color: '#764ba2',
      background_color: '#f3e8ff',
      text_color: '#1f2937',
      accent_color: '#10b981'
    };

    let config = { ...defaultConfig };

    // Game State
    let currentLesson = 1;
    let currentQuestionIndex = 0;
    let quizScore = 0;
    let totalScore = 0;
    let lessonScores = { 1: 0, 2: 0, 3: 0, 4: 0 };
    let questions = [];

    // Coin values for reference
    const coins = [
      { value: 0.25, name: '25 สตางค���', emoji: '🟤' },
      { value: 0.50, name: '50 สตางค์', emoji: '🟡' },
      { value: 1, name: '1 บาท', emoji: '⚪' },
      { value: 2, name: '2 บาท', emoji: '🥈' },
      { value: 5, name: '5 บาท', emoji: '🥉' },
      { value: 10, name: '10 บาท', emoji: '🥇' }
    ];

    const bills = [
      { value: 20, name: '20 บาท', emoji: '💵', color: 'bg-green-500' },
      { value: 50, name: '50 บาท', emoji: '💶', color: 'bg-blue-500' },
      { value: 100, name: '100 บาท', emoji: '💴', color: 'bg-red-500' },
      { value: 500, name: '500 บาท', emoji: '💷', color: 'bg-purple-500' },
      { value: 1000, name: '1,000 บาท', emoji: '💰', color: 'bg-yellow-600' }
    ];

    const products = [
      { name: 'ขนมปัง', price: 15, emoji: '🍞' },
      { name: 'นม', price: 12, emoji: '🥛' },
      { name: 'ไข่', price: 8, emoji: '🥚' },
      { name: 'แอปเปิ้ล', price: 20, emoji: '🍎' },
      { name: 'น้ำผลไม้', price: 25, emoji: '🧃' },
      { name: 'คุกกี้', price: 35, emoji: '🍪' },
      { name: 'ช็อกโกแลต', price: 45, emoji: '🍫' },
      { name: 'ไอศกรีม', price: 30, emoji: '🍦' },
      { name: 'พิซซ่า', price: 89, emoji: '🍕' },
      { name: 'แฮมเบอร์เกอร์', price: 59, emoji: '🍔' }
    ];

    // Generate questions based on lesson
    function generateQuestions(lesson) {
      questions = [];
      
      switch(lesson) {
        case 1: // Coin recognition
          for (let i = 0; i < 5; i++) {
            const coin = coins[Math.floor(Math.random() * coins.length)];
            const wrongAnswers = coins.filter(c => c.value !== coin.value)
              .sort(() => Math.random() - 0.5)
              .slice(0, 3)
              .map(c => c.value);
            
            questions.push({
              type: 'coin',
              icon: '🪙',
              text: `เหรียญนี้มีค่าเท่าไร?`,
              hint: coin.name,
              visual: [coin],
              answer: coin.value,
              options: shuffleArray([coin.value, ...wrongAnswers]),
              displayValue: (v) => v < 1 ? `${v * 100} สตางค์` : `${v} บาท`
            });
          }
          break;
          
        case 2: // Bill recognition
          for (let i = 0; i < 5; i++) {
            const bill = bills[Math.floor(Math.random() * bills.length)];
            const wrongAnswers = bills.filter(b => b.value !== bill.value)
              .sort(() => Math.random() - 0.5)
              .slice(0, 3)
              .map(b => b.value);
            
            questions.push({
              type: 'bill',
              icon: '💵',
              text: `ธนบัตรนี้มีค่าเท่าไร?`,
              hint: bill.name,
              visual: [bill],
              answer: bill.value,
              options: shuffleArray([bill.value, ...wrongAnswers]),
              displayValue: (v) => `${v.toLocaleString()} บาท`
            });
          }
          break;
          
        case 3: // Shopping calculation
          for (let i = 0; i < 5; i++) {
            const numProducts = Math.floor(Math.random() * 2) + 2; // 2-3 products
            const selectedProducts = shuffleArray([...products]).slice(0, numProducts);
            const total = selectedProducts.reduce((sum, p) => sum + p.price, 0);
            
            const wrongAnswers = [
              total + Math.floor(Math.random() * 20) + 5,
              total - Math.floor(Math.random() * 10) - 3,
              total + Math.floor(Math.random() * 30) + 10
            ].filter(v => v > 0 && v !== total);
            
            questions.push({
              type: 'shopping',
              icon: '🛒',
              text: `ซื้อของเหล่านี้��้องจ่ายเงินเท่าไร?`,
              hint: selectedProducts.map(p => `${p.emoji} ${p.name} ${p.price} บาท`).join(' • '),
              visual: selectedProducts,
              answer: total,
              options: shuffleArray([total, ...wrongAnswers.slice(0, 3)]),
              displayValue: (v) => `${v} บาท`
            });
          }
          break;
          
        case 4: // Change calculation
          for (let i = 0; i < 5; i++) {
            const product = products[Math.floor(Math.random() * products.length)];
            const possiblePay = [50, 100, 200, 500].filter(p => p > product.price);
            const paid = possiblePay[Math.floor(Math.random() * possiblePay.length)] || 100;
            const change = paid - product.price;
            
            const wrongAnswers = [
              change + Math.floor(Math.random() * 15) + 5,
              change - Math.floor(Math.random() * 10) - 2,
              paid - change
            ].filter(v => v > 0 && v !== change);
            
            questions.push({
              type: 'change',
              icon: '💱',
              text: `ซื้อ${product.name} ${product.emoji} ราคา ${product.price} บาท จ่าย ${paid} บาท ได้เงินทอนเท่าไร?`,
              hint: `คิดจาก ${paid} - ${product.price} = ?`,
              visual: [{ ...product, paid }],
              answer: change,
              options: shuffleArray([change, ...wrongAnswers.slice(0, 3)]),
              displayValue: (v) => `${v} บาท`
            });
          }
          break;
      }
      
      return questions;
    }

    function shuffleArray(array) {
      const newArray = [...array];
      for (let i = newArray.length - 1; i > 0; i--) {
        const j = Math.floor(Math.random() * (i + 1));
        [newArray[i], newArray[j]] = [newArray[j], newArray[i]];
      }
      return newArray;
    }

    function selectLesson(lesson) {
      currentLesson = lesson;
      currentQuestionIndex = 0;
      quizScore = 0;
      generateQuestions(lesson);
      
      document.getElementById('menu-section').classList.add('hidden');
      document.getElementById('quiz-section').classList.remove('hidden');
      document.getElementById('result-section').classList.add('hidden');
      
      updateQuizScore();
      showQuestion();
    }

    function showQuestion() {
      const q = questions[currentQuestionIndex];
      
      document.getElementById('current-question').textContent = currentQuestionIndex + 1;
      document.getElementById('total-questions').textContent = questions.length;
      document.getElementById('progress-bar').style.width = `${((currentQuestionIndex + 1) / questions.length) * 100}%`;
      
      document.getElementById('question-icon').textContent = q.icon;
      document.getElementById('question-text').textContent = q.text;
      document.getElementById('question-hint').textContent = q.hint;
      
      // Visual display
      const visualContainer = document.getElementById('visual-display');
      visualContainer.innerHTML = '';
      
      if (q.type === 'coin') {
        q.visual.forEach(coin => {
          const coinEl = document.createElement('div');
          coinEl.className = 'w-20 h-20 rounded-full bg-gradient-to-br from-yellow-300 to-yellow-600 flex items-center justify-center text-3xl shadow-lg coin-bounce';
          coinEl.innerHTML = `<span>${coin.emoji}</span>`;
          visualContainer.appendChild(coinEl);
        });
      } else if (q.type === 'bill') {
        q.visual.forEach(bill => {
          const billEl = document.createElement('div');
          billEl.className = `w-32 h-16 ${bill.color} rounded-lg flex items-center justify-center text-white font-bold shadow-lg`;
          billEl.innerHTML = `<span class="text-2xl mr-2">${bill.emoji}</span>`;
          visualContainer.appendChild(billEl);
        });
      } else if (q.type === 'shopping') {
        q.visual.forEach(product => {
          const productEl = document.createElement('div');
          productEl.className = 'flex flex-col items-center bg-white rounded-xl p-3 shadow-md';
          productEl.innerHTML = `
            <span class="text-4xl mb-1">${product.emoji}</span>
            <span class="text-sm font-medium text-gray-700">${product.name}</span>
            <span class="text-purple-600 font-bold">${product.price} ��</span>
          `;
          visualContainer.appendChild(productEl);
        });
      } else if (q.type === 'change') {
        const item = q.visual[0];
        visualContainer.innerHTML = `
          <div class="flex items-center gap-4">
            <div class="flex flex-col items-center bg-white rounded-xl p-4 shadow-md">
              <span class="text-5xl mb-2">${item.emoji}</span>
              <span class="font-medium text-gray-700">${item.name}</span>
              <span class="text-red-500 font-bold">${item.price} บาท</span>
            </div>
            <span class="text-3xl">➡️</span>
            <div class="flex flex-col items-center bg-green-100 rounded-xl p-4 shadow-md">
              <span class="text-4xl mb-2">💵</span>
              <span class="font-medium text-gray-700">จ่าย</span>
              <span class="text-green-600 font-bold">${item.paid} บาท</span>
            </div>
          </div>
        `;
      }
      
      // Answer options
      const optionsContainer = document.getElementById('answer-options');
      optionsContainer.innerHTML = '';
      
      q.options.forEach((option, index) => {
        const btn = document.createElement('button');
        btn.className = 'py-4 px-6 bg-gray-100 hover:bg-purple-100 text-gray-800 font-bold rounded-xl transition-all duration-300 hover:scale-105';
        btn.textContent = q.displayValue(option);
        btn.onclick = () => checkAnswer(option, btn);
        optionsContainer.appendChild(btn);
      });
      
      document.getElementById('feedback').classList.add('hidden');
      document.getElementById('next-btn').classList.add('hidden');
    }

    function checkAnswer(selected, btnElement) {
      const q = questions[currentQuestionIndex];
      const isCorrect = selected === q.answer;
      const feedback = document.getElementById('feedback');
      const feedbackIcon = document.getElementById('feedback-icon');
      const feedbackText = document.getElementById('feedback-text');
      
      // Disable all buttons
      document.querySelectorAll('#answer-options button').forEach(btn => {
        btn.disabled = true;
        if (parseFloat(btn.textContent) === q.answer || btn.textContent.includes(q.answer)) {
          btn.classList.add('bg-green-500', 'text-white');
        }
      });
      
      if (isCorrect) {
        btnElement.classList.add('correct-flash', 'bg-green-500', 'text-white');
        feedbackIcon.textContent = '🎉';
        feedbackText.textContent = 'ถูกต้อง! เก่งมาก!';
        feedback.className = 'text-center p-4 rounded-xl mb-4 bg-green-100 text-green-800';
        quizScore += 10;
        updateQuizScore();
      } else {
        btnElement.classList.add('wrong-shake', 'bg-red-500', 'text-white');
        feedbackIcon.textContent = '😅';
        feedbackText.textContent = `ไม่ถูกต้อง คำตอบที่ถูกคือ ${q.displayValue(q.answer)}`;
        feedback.className = 'text-center p-4 rounded-xl mb-4 bg-red-100 text-red-800';
      }
      
      feedback.classList.remove('hidden');
      document.getElementById('next-btn').classList.remove('hidden');
    }

    function nextQuestion() {
      currentQuestionIndex++;
      
      if (currentQuestionIndex >= questions.length) {
        showResult();
      } else {
        showQuestion();
      }
    }

    function showResult() {
      document.getElementById('quiz-section').classList.add('hidden');
      document.getElementById('result-section').classList.remove('hidden');
      
      const maxScore = questions.length * 10;
      const percentage = (quizScore / maxScore) * 100;
      
      document.getElementById('final-score').textContent = quizScore;
      document.getElementById('max-score').textContent = maxScore;
      
      let stars = 0;
      let title = '';
      let message = '';
      
      if (percentage >= 80) {
        stars = 3;
        title = '🌟 ยอดเยี่ยม! 🌟';
        message = 'คุณเข้าใจเรื่องเงินได้ดีมาก!';
      } else if (percentage >= 60) {
        stars = 2;
        title = '👏 ดีมาก!';
        message = 'ลองทำอีกครั้งเพื่อให้ได้คะแนนเต็ม!';
      } else if (percentage >= 40) {
        stars = 1;
        title = '💪 พยายามอีกนิด!';
        message = 'ฝึกฝนเพิ่มเติมจะทำได้ดีขึ้น!';
      } else {
        stars = 0;
        title = '📚 มาเรียนรู้กันใหม่!';
        message = 'อย่าท้อ ลองทำอีกครั้งนะ!';
      }
      
      document.getElementById('result-stars').textContent = '⭐'.repeat(stars) + '☆'.repeat(3 - stars);
      document.getElementById('result-title').textContent = title;
      document.getElementById('result-message').textContent = message;
      
      // Update lesson stars
      if (quizScore > lessonScores[currentLesson]) {
        lessonScores[currentLesson] = quizScore;
        updateLessonStars(currentLesson, stars);
      }
      
      // Update total score
      totalScore = Object.values(lessonScores).reduce((a, b) => a + b, 0);
      document.getElementById('total-score').textContent = totalScore;
    }

    function updateLessonStars(lesson, stars) {
      for (let i = 1; i <= 3; i++) {
        const starEl = document.getElementById(`lesson${lesson}-star${i}`);
        if (starEl) {
          starEl.textContent = i <= stars ? '⭐' : '☆';
          if (i <= stars) {
            starEl.classList.add('star-spin');
            setTimeout(() => starEl.classList.remove('star-spin'), 1000);
          }
        }
      }
    }

    function updateQuizScore() {
      document.getElementById('quiz-score').textContent = quizScore;
    }

    function retryLesson() {
      selectLesson(currentLesson);
    }

    function backToMenu() {
      document.getElementById('menu-section').classList.remove('hidden');
      document.getElementById('quiz-section').classList.add('hidden');
      document.getElementById('result-section').classList.add('hidden');
    }

    // Element SDK Integration
    async function onConfigChange(newConfig) {
      const title = newConfig.app_title || defaultConfig.app_title;
      const welcome = newConfig.welcome_message || defaultConfig.welcome_message;
      
      document.getElementById('app-title').textContent = title;
      document.getElementById('welcome-msg').textContent = welcome;
    }

    function mapToCapabilities(config) {
      return {
        recolorables: [],
        borderables: [],
        fontEditable: undefined,
        fontSizeable: undefined
      };
    }

    function mapToEditPanelValues(config) {
      return new Map([
        ['app_title', config.app_title || defaultConfig.app_title],
        ['welcome_message', config.welcome_message || defaultConfig.welcome_message]
      ]);
    }

    // Initialize
    if (window.elementSdk) {
      window.elementSdk.init({
        defaultConfig,
        onConfigChange,
        mapToCapabilities,
        mapToEditPanelValues
      });
    }
  </script>
 <script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'9c03218020377322',t:'MTc2ODc5MjE0MS4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script></body>
</html>
