[register.html](https://github.com/user-attachments/files/23605692/register.html)[Uploading <!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>تسجيل حساب جديد</title>
<style>
@import url('https://fonts.googleapis.com/css2?family=Cairo:wght@400;600&display=swap');

body {
  font-family: 'Cairo', sans-serif;
  background: linear-gradient(135deg, #7b2ff7, #4facfe);
  margin: 0;
  padding: 0;
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
}

.register-card {
  background: linear-gradient(145deg, #6a11cb, #2575fc);
  border-radius: 25px;
  width: 600px;
  max-width: 95%;
  padding: 40px;
  color: #fff;
  box-shadow: 0 10px 30px rgba(0,0,0,0.4);
  position: relative;
  overflow: hidden;
  animation: cardFade 0.6s ease forwards;
  text-align: right;
}

.register-card::before,
.register-card::after {
  content: "";
  position: absolute;
  border-radius: 50%;
  opacity: 0.2;
  z-index: 0;
}

.register-card::before {
  width: 140px;
  height: 140px;
  background: #ffffff;
  top: -50px;
  right: -50px;
}

.register-card::after {
  width: 100px;
  height: 100px;
  background: #ffeb3b;
  bottom: -40px;
  left: -40px;
}

@keyframes cardFade {
  from { transform: scale(0.8); opacity: 0; }
  to { transform: scale(1); opacity: 1; }
}

h2 {
  margin-bottom: 25px;
  font-size: 28px;
  text-shadow: 1px 1px 6px rgba(0,0,0,0.4);
  text-align: center;
}

.flag {
  display: block;
  margin: 0 auto 20px auto;
  width: 90px;
  height: 55px;
  border-radius: 6px;
  border: 2px solid #fff;
}

.form-row {
  display: flex;
  gap:50px;
  flex-wrap: wrap;
  margin-bottom: 25px; /* المسافة بين الصفوف */
}

.form-group {
  flex: 1;
  min-width: 45%;
}

label {
  display: block;
  font-weight: 600;
  margin-bottom: 8px;
}

input, select {
  width: 100%;
  padding: 14px;
  border: none;
  border-radius: 12px;
  font-size: 15px;
  background: rgba(0,0,0,0.3);
  color: #fff;
  text-align: right;
  box-shadow: inset 0 2px 6px rgba(0,0,0,0.2);
  transition: 0.3s;
}

input::placeholder {
  color: rgba(255,255,255,0.7);
  font-style: italic;
}

input:focus, select:focus {
  background: rgba(0,0,0,0.4);
  box-shadow: inset 0 2px 8px rgba(0,0,0,0.3);
  outline: none;
  animation: pulse 0.5s;
}

select option {
  background: linear-gradient(145deg, #6a11cb, #2575fc);
  color: #fff;
}

@keyframes pulse {
  0% { transform: scale(1); }
  50% { transform: scale(1.05); }
  100% { transform: scale(1); }
}

button {
  width: 100%;
  padding: 14px;
  border: none;
  border-radius: 12px;
  font-size: 16px;
  font-weight: 600;
  cursor: pointer;
  background: linear-gradient(135deg, #6a11cb, #2575fc);
  color: #fff;
  margin-top: 25px;
  transition: 0.3s;
  box-shadow: 0 5px 15px rgba(0,0,0,0.3);
}

button:hover {
  transform: translateY(-3px);
  box-shadow: 0 10px 25px rgba(0,0,0,0.45);
}

p.error {
  color: #ffeb3b;
  margin: 5px 0;
  display: none;
  text-align: right;
}

.footer {
  margin-top: 25px;
  font-size: 13px;
  color: #d0e6ff;
  text-shadow: 1px 1px 3px rgba(0,0,0,0.3);
  text-align: center;
}
</style>
</head>
<body>

<div class="register-card">
  <img src="https://upload.wikimedia.org/wikipedia/en/b/ba/Flag_of_Germany.svg" alt="علم ألمانيا" class="flag">
  <h2>تسجيل حساب جديد</h2>

  <div class="form-row">
    <div class="form-group">
      <label for="username">اسم المستخدم</label>
      <input type="text" id="username" placeholder="مثال: محمد أحمد">
    </div>
    <div class="form-group">
      <label for="email">البريد الإلكتروني</label>
      <input type="email" id="email" placeholder="مثال: example@mail.com">
    </div>
  </div>

  <div class="form-row">
    <div class="form-group">
      <label for="password">كلمة المرور</label>
      <input type="password" id="password" placeholder="********">
    </div>
    <div class="form-group">
      <label for="confirmPassword">تأكيد كلمة المرور</label>
      <input type="password" id="confirmPassword" placeholder="********">
    </div>
  </div>

  <div class="form-row">
    <div class="form-group">
      <label for="studentPhone">تليفون الطالب</label>
      <input type="tel" id="studentPhone" placeholder="مثال: 01012345678">
    </div>
    <div class="form-group">
      <label for="parentPhone">تليفون ولي الأمر</label>
      <input type="tel" id="parentPhone" placeholder="مثال: 01287654321">
    </div>
  </div>

  <div class="form-row">
    <div class="form-group">
      <label for="grade">المرحلة الدراسية</label>
      <select id="grade" onchange="updateYearOptions()">
        <option value="">اختر المرحلة</option>
        <option value="ابتدائي">ابتدائي</option>
        <option value="إعدادي">إعدادي</option>
        <option value="ثانوي">ثانوي</option>
      </select>
    </div>
    <div class="form-group">
      <label for="year">السنة الدراسية</label>
      <select id="year">
        <option value="">اختر السنة</option>
      </select>
    </div>
  </div>

  <p class="error" id="errorMsg">❌ هناك خطأ في البيانات</p>
  <button onclick="register()">تسجيل الآن</button>

  <div class="footer">© 2025 Frau Mona Platform</div>
</div>

<script>
function updateYearOptions(){
  const grade = document.getElementById('grade').value;
  const yearSelect = document.getElementById('year');
  yearSelect.innerHTML = '<option value="">اختر السنة</option>';

  if(grade === "ابتدائي"){
    yearSelect.innerHTML += `<option value="سادسه">سادسه</option>`;
  } else if(grade === "إعدادي"){
    ["أولى","ثانية","ثالثة"].forEach(y => {
      yearSelect.innerHTML += `<option value="${y}">${y}</option>`;
    });
  } else if(grade === "ثانوي"){
    ["أولى","ثانية"].forEach(y => {
      yearSelect.innerHTML += `<option value="${y}">${y}</option>`;
    });
  }
}

function register(){
  const username = document.getElementById('username').value.trim();
  const email = document.getElementById('email').value.trim();
  const password = document.getElementById('password').value.trim();
  const confirmPassword = document.getElementById('confirmPassword').value.trim();
  const studentPhone = document.getElementById('studentPhone').value.trim();
  const parentPhone = document.getElementById('parentPhone').value.trim();
  const grade = document.getElementById('grade').value;
  const year = document.getElementById('year').value;
  const errorMsg = document.getElementById('errorMsg');

  if(!username || !email || !password || !confirmPassword || !studentPhone || !parentPhone || !grade || !year){
    errorMsg.textContent = "❌ يرجى تعبئة جميع الحقول";
    errorMsg.style.display = "block";
    setTimeout(()=> errorMsg.style.display = "none", 4000);
    return;
  }

  if(password !== confirmPassword){
    errorMsg.textContent = "❌ كلمات المرور غير متطابقة";
    errorMsg.style.display = "block";
    setTimeout(()=> errorMsg.style.display = "none", 4000);
    return;
  }

  if(studentPhone === parentPhone){
    errorMsg.textContent = "❌ رقم الطالب وولي الأمر لا يمكن أن يكونا متشابهين";
    errorMsg.style.display = "block";
    setTimeout(()=> errorMsg.style.display = "none", 4000);
    return;
  }

  alert(`✅ تم تسجيل الحساب بنجاح! مرحبًا ${username}`);
  window.location.href = "home.html";
}
</script>

</body>
</html>
register.html…]()
