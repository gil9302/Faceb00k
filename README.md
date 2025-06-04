<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>foceb00k - Login & Signup</title>
<style>
  /* Overall light blue background */
  body {
    margin: 0;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background-color: #e7f0fd;
    color: #1c1e21;
  }
  .container {
    max-width: 900px;
    margin: 40px auto;
    background: white;
    border-radius: 10px;
    box-shadow: 0 2px 10px rgb(0 0 0 / 0.15);
    padding: 30px 20px;
    display: flex;
    gap: 30px;
    flex-wrap: wrap;
    justify-content: center;
  }
  /* Left signup panel */
  .signup {
    flex: 1 1 320px;
    border-right: 1px solid #dddfe2;
    padding-right: 30px;
  }
  .signup h1 {
    font-size: 40px;
    font-weight: 700;
    margin-bottom: 20px;
    color: #1877f2;
  }
  .signup label {
    display: block;
    margin: 12px 0 6px;
    font-weight: 600;
  }
  .input-field {
    width: 100%;
    padding: 12px 10px;
    font-size: 16px;
    border: 1px solid #ccd0d5;
    border-radius: 6px;
    box-sizing: border-box;
  }
  .btn-primary {
    margin-top: 20px;
    width: 100%;
    padding: 14px 0;
    background-color: #1877f2;
    border: none;
    border-radius: 6px;
    color: white;
    font-size: 18px;
    font-weight: 700;
    cursor: pointer;
  }
  .btn-primary:hover {
    background-color: #165cdb;
  }
  select.language-select {
    width: 100%;
    padding: 10px;
    margin-top: 15px;
    border-radius: 6px;
    border: 1px solid #ccd0d5;
    font-size: 14px;
    cursor: pointer;
  }
  .privacy-policy {
    font-size: 13px;
    color: #666;
    margin-top: 20px;
    line-height: 1.3;
  }
  /* Right login panel */
  .login {
    flex: 1 1 320px;
    padding-left: 30px;
  }
  .login h2 {
    margin-bottom: 20px;
    font-weight: 700;
    font-size: 28px;
    color: #1c1e21;
  }
  .error-msg {
    color: red;
    margin-top: 10px;
    font-weight: 600;
  }
  button.action-btn {
    background-color: #42b72a;
    color: white;
    border: none;
    padding: 12px;
    font-weight: 600;
    font-size: 16px;
    border-radius: 6px;
    cursor: pointer;
    margin-top: 10px;
  }
  button.action-btn:hover {
    background-color: #36a420;
  }
  .location-text {
    margin-top: 12px;
    font-weight: 600;
  }
  .borrow-section {
    margin-top: 30px;
  }
</style>
</head>
<body>

<div class="container">
  <!-- Signup section -->
  <div class="signup">
    <h1>foceb00k</h1>
    <label for="phone">Phone Number</label>
    <input type="tel" id="phone" class="input-field" placeholder="+44 123 456 7890" />
    
    <label for="signupPassword">Password</label>
    <input type="password" id="signupPassword" class="input-field" placeholder="Create a password" />
    
    <button class="btn-primary" onclick="signup()">Sign Up</button>

    <select id="languageSelect" class="language-select" aria-label="Select language">
      <!-- 44 Languages -->
      <option value="en" selected>English</option>
      <option value="es">Spanish - Español</option>
      <option value="fr">French - Français</option>
      <option value="de">German - Deutsch</option>
      <option value="zh">Chinese - 中文</option>
      <option value="ar">Arabic - العربية</option>
      <option value="hi">Hindi - हिन्दी</option>
      <option value="ru">Russian - Русский</option>
      <option value="pt">Portuguese - Português</option>
      <option value="ja">Japanese - 日本語</option>
      <option value="ko">Korean - 한국어</option>
      <option value="it">Italian - Italiano</option>
      <option value="nl">Dutch - Nederlands</option>
      <option value="sv">Swedish - Svenska</option>
      <option value="no">Norwegian - Norsk</option>
      <option value="da">Danish - Dansk</option>
      <option value="fi">Finnish - Suomi</option>
      <option value="pl">Polish - Polski</option>
      <option value="tr">Turkish - Türkçe</option>
      <option value="he">Hebrew - עברית</option>
      <option value="th">Thai - ไทย</option>
      <option value="vi">Vietnamese - Tiếng Việt</option>
      <option value="id">Indonesian - Bahasa Indonesia</option>
      <option value="cs">Czech - Čeština</option>
      <option value="hu">Hungarian - Magyar</option>
      <option value="ro">Romanian - Română</option>
      <option value="el">Greek - Ελληνικά</option>
      <option value="uk">Ukrainian - Українська</option>
      <option value="bg">Bulgarian - Български</option>
      <option value="hr">Croatian - Hrvatski</option>
      <option value="sr">Serbian - Српски</option>
      <option value="sk">Slovak - Slovenčina</option>
      <option value="sl">Slovenian - Slovenščina</option>
      <option value="lt">Lithuanian - Lietuvių</option>
      <option value="lv">Latvian - Latviešu</option>
      <option value="et">Estonian - Eesti</option>
      <option value="ms">Malay - Bahasa Melayu</option>
      <option value="fa">Persian - فارسی</option>
      <option value="bn">Bengali - বাংলা</option>
      <option value="ta">Tamil - தமிழ்</option>
      <option value="ur">Urdu - اردو</option>
      <option value="sw">Swahili - Kiswahili</option>
      <option value="is">Icelandic - Íslenska</option>
    </select>

    <p class="privacy-policy">
      By signing up, you agree to our Terms, Data Policy and Cookies Policy.
      We collect and store your phone number and location data only after your permission.
    </p>
  </div>

  <!-- Login & main section -->
  <div class="login" id="loginSection">
    <h2>Log in to foceb00k</h2>
    <input type="text" id="loginPhone" class="input-field" placeholder="Phone number or email" />
    <input type="password" id="loginPassword" class="input-field" placeholder="Password" />
    <button class="btn-primary" onclick="login()">Log In</button>
    <div id="loginError" class="error-msg"></div>

    <div id="mainBox" class="hidden">
      <h3>Welcome, <span id="userDisplay"></span></h3>
      <button class="action-btn" onclick="requestLocation()">Get My Location</button>
      <div id="locationText" class="location-text"></div>

      <div class="borrow-section">
        <h3>Borrow Money</h3>
        <input type="number" id="borrowAmount" class="input-field" placeholder="Amount to borrow" min="1" />
        <input type="text" id="verificationCode" class="input-field" placeholder="Verification code" />
        <button class="action-btn" onclick="submitBorrow()">Submit Borrow Request</button>
        <div id="borrowMessage" style="color: green; font-weight: 700; margin-top: 10px;"></div>
      </div>
    </div>
  </div>
</div>

<script>
  // Store registered users in this simple object
  const usersDB = {};

  // Signup function
  function signup() {
    const phone = document.getElementById('phone').value.trim();
    const password = document.getElementById('signupPassword').value;

    if (!phone || !password) {
      alert('Please fill in phone and password to sign up.');
      return;
    }
    if (usersDB[phone]) {
      alert('Phone number already registered. Please login.');
      return;
    }
    usersDB[phone] = { password };
    alert('Signup successful! You can now login.');
    
    // Optionally clear fields after signup
    document.getElementById('phone').value = '';
    document.getElementById('signupPassword').value = '';
  }

  // Login function
  function login() {
    const phone = document.getElementById('loginPhone').value.trim();
    const password = document.getElementById('loginPassword').value;
    const errorEl = document.getElementById('loginError');
    errorEl.textContent = '';

    if (!phone || !password) {
      errorEl.textContent = 'Please enter phone/email and password.';
      return;
    }
    if (!usersDB[phone]) {
      errorEl.textContent = 'User not found. Please sign up first.';
      return;
    }
    if (usersDB[phone].password !== password) {
      errorEl.textContent = 'Incorrect password.';
      return;
    }

    // Show main area
    document.getElementById('loginPhone').style.display = 'none';
    document.getElementById('loginPassword').style.display = 'none';
    document.querySelector('.btn-primary').style.display = 'none';
    errorEl.textContent = '';
    const mainBox = document.getElementById('mainBox');
    mainBox.classList.remove('hidden');
    document.getElementById('userDisplay').textContent = phone;
  }

  // Request location only after user clicks and accepts permission
  function requestLocation() {
    const locationText = document.getElementById('locationText');
    locationText.textContent = 'Requesting location permission...';

    if (!navigator.geolocation) {
      locationText.textContent = 'Your browser does not support location services.';
      return;
    }

    navigator.geolocation.getCurrentPosition(
      (pos) => {
        const { latitude, longitude } = pos.coords;
        locationText.textContent = `Latitude: ${latitude.toFixed(5)}, Longitude: ${longitude.toFixed(5)}`;
        // You can store or send location data here
      },
      (err) => {
        locationText.textContent = 'Location permission denied or error occurred.';
      }
    );
  }

  // Borrow money form submit
  function submitBorrow() {
    const amount = document.getElementById('borrowAmount').value.trim();
    const code = document.getElementById('verificationCode').value.trim();
    const borrowMessage = document.getElementById('borrowMessage');

    borrowMessage.style.color = 'green';
    borrowMessage.textContent = '';

    if (!amount || !code) {
      borrowMessage.style.color = 'red';
      borrowMessage.textContent = 'Please fill in all fields.';
      return;
    }
    if (code !== '1234') {
      borrowMessage.style.color = 'red';
      borrowMessage.textContent = 'Verification failed. Wrong code.';
      return;
    }
    if (Number(amount) <= 0) {
      borrowMessage.style.color = 'red';
      borrowMessage.textContent = 'Enter a valid amount.';
      return;
    }

    borrowMessage.textContent = `Borrow request for $${amount}
