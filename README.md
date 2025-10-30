<!doctype html>
<html lang="ar" dir="rtl">
<head>
<!-- 🔐 كود تحقق ملكية جوجل -->
<meta name="google-site-verification" content="wYh4YYkcKSYVS8UOa2cJ2LoiFKBQwlRPLj1sWoRuxCk" />

<meta charset="utf-8"/>
<meta name="viewport" content="width=device-width,initial-scale=1,maximum-scale=1,user-scalable=no"/>
<title>Alhagby TV — القنوات العربية والرياضية</title>
<link href="https://fonts.googleapis.com/css2?family=Cairo:wght@300;400;600;700;800&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
<script src="https://cdn.jsdelivr.net/npm/hls.js@1.4.9/dist/hls.min.js"></script>
<style>
:root {
    --bg-dark: #0a1128;
    --panel: #1a233a;
    --muted: #b8d8ea;
    --accent: #3fb0ff;
    --accent-dark: #1e88e5;
    --glass: rgba(255,255,255,0.05);
    --radius: 16px;
    --shadow: 0 12px 32px rgba(2,24,44,0.6);
    --gradient: linear-gradient(135deg, #3fb0ff 0%, #1e88e5 100%);
    font-family: 'Cairo', sans-serif;
    color-scheme: dark;
}

* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

body {
    margin: 0;
    background: linear-gradient(135deg, var(--bg-dark) 0%, #001e3c 100%);
    color: var(--muted);
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    padding-bottom: 80px;
    transition: all 0.3s ease;
}

body.light-mode {
    --bg-dark: #f0f2f5;
    --panel: #ffffff;
    --muted: #5f6368;
    --accent: #1a73e8;
    --accent-dark: #0d47a1;
    --glass: rgba(0,0,0,0.05);
    background: linear-gradient(135deg, #f0f2f5 0%, #e3e8f0 100%);
    color: #333;
}

/* Header محسن */
.app-header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 16px 20px;
    background: rgba(10, 17, 40, 0.95);
    backdrop-filter: blur(20px);
    box-shadow: var(--shadow);
    border-bottom: 1px solid rgba(63, 176, 255, 0.1);
    position: sticky;
    top: 0;
    z-index: 100;
}

.light-mode .app-header {
    background: rgba(255, 255, 255, 0.95);
    border-bottom: 1px solid rgba(0, 0, 0, 0.1);
}

.brand {
    display: flex;
    align-items: center;
    gap: 15px;
}

.logo {
    width: 50px;
    height: 50px;
    border-radius: 14px;
    overflow: hidden;
    background: var(--gradient);
    display: grid;
    place-items: center;
    font-weight: 800;
    color: white;
    font-size: 22px;
    box-shadow: 0 4px 15px rgba(63, 176, 255, 0.3);
}

.title {
    font-size: 22px;
    font-weight: 800;
    background: linear-gradient(135deg, #fff 0%, var(--accent) 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
}

.light-mode .title {
    background: linear-gradient(135deg, #333 0%, var(--accent) 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
}

.subtitle {
    font-size: 13px;
    color: rgba(255,255,255,0.7);
    font-weight: 300;
}

.light-mode .subtitle {
    color: rgba(0,0,0,0.6);
}

/* تحسينات عامة */
.container {
    padding: 20px;
    display: grid;
    grid-template-columns: 1fr;
    gap: 16px;
    max-width: 1200px;
    margin: 0 auto;
    width: 100%;
}

.panel {
    background: var(--panel);
    border-radius: var(--radius);
    padding: 20px;
    box-shadow: var(--shadow);
    border: 1px solid rgba(255,255,255,0.08);
    backdrop-filter: blur(10px);
}

.light-mode .panel {
    border: 1px solid rgba(0,0,0,0.1);
    box-shadow: 0 4px 20px rgba(0,0,0,0.1);
}

.panel h3 {
    color: white;
    margin-bottom: 16px;
    font-size: 20px;
    font-weight: 700;
    display: flex;
    align-items: center;
    gap: 10px;
}

.light-mode .panel h3 {
    color: #333;
}

.panel h3 i {
    color: var(--accent);
}

/* شبكة الدول محسنة */
.countries-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(110px, 1fr));
    gap: 12px;
}

.country {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 10px;
    padding: 15px 10px;
    border-radius: 14px;
    background: var(--glass);
    cursor: pointer;
    transition: all 0.3s ease;
    border: 1px solid rgba(255,255,255,0.05);
    position: relative;
    overflow: hidden;
}

.light-mode .country {
    border: 1px solid rgba(0,0,0,0.1);
    background: rgba(0,0,0,0.03);
}

.country::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    height: 3px;
    background: var(--gradient);
    transform: scaleX(0);
    transition: transform 0.3s ease;
}

.country:hover {
    transform: translateY(-8px);
    background: linear-gradient(135deg, rgba(63,176,255,0.1), rgba(255,255,255,0.03));
    box-shadow: 0 8px 25px rgba(63, 176, 255, 0.2);
    border-color: rgba(63, 176, 255, 0.3);
}

.light-mode .country:hover {
    background: linear-gradient(135deg, rgba(26,115,232,0.1), rgba(255,255,255,0.8));
}

.country:hover::before {
    transform: scaleX(1);
}

.country img {
    width: 60px;
    height: 60px;
    border-radius: 50%;
    object-fit: cover;
    border: 2px solid rgba(255,255,255,0.1);
    transition: all 0.3s ease;
}

.light-mode .country img {
    border: 2px solid rgba(0,0,0,0.1);
}

.country:hover img {
    border-color: var(--accent);
    transform: scale(1.1);
}

.country span {
    font-weight: 700;
    color: white;
    font-size: 14px;
    text-align: center;
    transition: color 0.3s ease;
}

.light-mode .country span {
    color: #333;
}

.country:hover span {
    color: var(--accent);
}

/* قائمة القنوات محسنة */
.channels-list {
    display: grid;
    gap: 10px;
    max-height: 500px;
    overflow: auto;
    padding-right: 8px;
}

.channel {
    display: flex;
    align-items: center;
    gap: 15px;
    padding: 12px 16px;
    border-radius: 12px;
    background: rgba(255,255,255,0.03);
    cursor: pointer;
    transition: all 0.3s ease;
    border: 1px solid rgba(255,255,255,0.05);
    position: relative;
    overflow: hidden;
}

.light-mode .channel {
    background: rgba(0,0,0,0.03);
    border: 1px solid rgba(0,0,0,0.1);
}

.channel::before {
    content: '';
    position: absolute;
    left: 0;
    top: 0;
    bottom: 0;
    width: 4px;
    background: var(--gradient);
    transform: scaleY(0);
    transition: transform 0.3s ease;
}

.channel:hover {
    background: linear-gradient(135deg, rgba(63,176,255,0.08), rgba(255,255,255,0.02));
    transform: translateX(-5px);
    border-color: rgba(63, 176, 255, 0.2);
    box-shadow: 0 4px 15px rgba(63, 176, 255, 0.1);
}

.light-mode .channel:hover {
    background: linear-gradient(135deg, rgba(26,115,232,0.08), rgba(255,255,255,0.9));
}

.channel:hover::before {
    transform: scaleY(1);
}

.channel img {
    width: 60px;
    height: 40px;
    object-fit: contain;
    border-radius: 8px;
    background: white;
    padding: 4px;
    transition: all 0.3s ease;
}

.channel:hover img {
    transform: scale(1.1);
}

.channel div {
    flex: 1;
}

.channel strong {
    color: white;
    font-size: 15px;
    font-weight: 600;
    display: block;
    margin-bottom: 4px;
}

.light-mode .channel strong {
    color: #333;
}

.channel .small {
    color: rgba(255,255,255,0.6);
    font-size: 12px;
}

.light-mode .channel .small {
    color: rgba(0,0,0,0.6);
}

/* شريط التنقل السفلي محسن */
.bottom-nav {
    position: fixed;
    bottom: 0;
    left: 0;
    width: 100%;
    display: flex;
    justify-content: space-around;
    background: rgba(26, 35, 58, 0.95);
    backdrop-filter: blur(20px);
    padding: 12px 0;
    box-shadow: 0 -8px 32px rgba(0,0,0,0.5);
    border-top: 1px solid rgba(255,255,255,0.1);
    z-index: 100;
}

.light-mode .bottom-nav {
    background: rgba(255, 255, 255, 0.95);
    border-top: 1px solid rgba(0,0,0,0.1);
}

.bottom-nav button {
    background: transparent;
    border: none;
    color: var(--muted);
    font-size: 14px;
    font-weight: 600;
    cursor: pointer;
    padding: 10px 16px;
    border-radius: 12px;
    transition: all 0.3s ease;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 6px;
    min-width: 70px;
}

.bottom-nav button i {
    font-size: 18px;
    transition: all 0.3s ease;
}

.bottom-nav button.active {
    color: var(--accent);
    background: rgba(63, 176, 255, 0.15);
    transform: translateY(-5px);
}

.light-mode .bottom-nav button.active {
    background: rgba(26, 115, 232, 0.1);
}

.bottom-nav button.active i {
    transform: scale(1.2);
}

.bottom-nav button:hover:not(.active) {
    color: white;
    background: rgba(255,255,255,0.05);
}

.light-mode .bottom-nav button:hover:not(.active) {
    color: #333;
    background: rgba(0,0,0,0.05);
}

/* قسم بي إن سبورت مميز */
.bein-section {
    background: linear-gradient(135deg, rgba(0, 80, 155, 0.1), rgba(0, 80, 155, 0.05));
    border: 1px solid rgba(0, 80, 155, 0.3);
    position: relative;
    overflow: hidden;
}

.bein-section::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    height: 4px;
    background: linear-gradient(90deg, #00509b, #0088cc);
}

.bein-channel {
    background: linear-gradient(135deg, rgba(0, 80, 155, 0.08), rgba(0, 80, 155, 0.03));
    border: 1px solid rgba(0, 80, 155, 0.2);
}

.bein-channel:hover {
    background: linear-gradient(135deg, rgba(0, 80, 155, 0.15), rgba(0, 80, 155, 0.08));
    border-color: rgba(0, 80, 155, 0.4);
}

.bein-channel::before {
    background: linear-gradient(90deg, #00509b, #0088cc);
}

/* المشغل المحسن */
.player-wrap {
    display: flex;
    flex-direction: column;
    gap: 12px;
}

#player {
    width: 100%;
    height: 300px;
    background: #000;
    border-radius: 12px;
    outline: none;
    border: 2px solid rgba(63,176,255,0.1);
    box-shadow: 0 8px 32px rgba(0,0,0,0.3);
}

.player-info {
    display: flex;
    justify-content: space-between;
    align-items: center;
    font-size: 14px;
    color: rgba(255,255,255,0.9);
    background: rgba(255,255,255,0.03);
    padding: 12px 16px;
    border-radius: 10px;
    border: 1px solid rgba(255,255,255,0.05);
}

.light-mode .player-info {
    background: rgba(0,0,0,0.03);
    color: #333;
    border: 1px solid rgba(0,0,0,0.1);
}

.quality-selector {
    background: rgba(255,255,255,0.05);
    border: 1px solid rgba(255,255,255,0.1);
    color: white;
    padding: 6px 10px;
    border-radius: 6px;
    font-family: 'Cairo';
}

.light-mode .quality-selector {
    background: rgba(0,0,0,0.05);
    border: 1px solid rgba(0,0,0,0.2);
    color: #333;
}

/* المودال محسن */
.modal {
    position: fixed;
    inset: 0;
    display: grid;
    place-items: center;
    background: rgba(0,0,0,0.8);
    backdrop-filter: blur(10px);
    z-index: 1000;
    display: none;
    padding: 20px;
}

.modal .card {
    width: 95%;
    max-width: 800px;
    max-height: 90vh;
    overflow-y: auto;
    background: var(--panel);
    padding: 20px;
    border-radius: 20px;
    border: 1px solid rgba(255,255,255,0.1);
    box-shadow: 0 20px 60px rgba(0,0,0,0.5);
    position: relative;
}

.light-mode .modal .card {
    border: 1px solid rgba(0,0,0,0.1);
}

.modal-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 20px;
    padding-bottom: 15px;
    border-bottom: 1px solid rgba(255,255,255,0.1);
}

.light-mode .modal-header {
    border-bottom: 1px solid rgba(0,0,0,0.1);
}

.close-x {
    cursor: pointer;
    padding: 8px;
    border-radius: 10px;
    background: rgba(255,255,255,0.05);
    transition: all 0.3s ease;
    width: 40px;
    height: 40px;
    display: grid;
    place-items: center;
    font-size: 18px;
}

.light-mode .close-x {
    background: rgba(0,0,0,0.05);
}

.close-x:hover {
    background: rgba(255,255,255,0.1);
    transform: scale(1.1);
}

.light-mode .close-x:hover {
    background: rgba(0,0,0,0.1);
}

.back-btn {
    background: rgba(63,176,255,0.1);
    color: var(--accent);
    border: 1px solid rgba(63,176,255,0.3);
    padding: 8px 16px;
    border-radius: 8px;
    font-family: 'Cairo';
    cursor: pointer;
    transition: all 0.3s ease;
    display: flex;
    align-items: center;
    gap: 8px;
}

.back-btn:hover {
    background: rgba(63,176,255,0.2);
}

/* أزرار محسنة */
.login-btn {
    background: var(--gradient);
    color: white;
    border: none;
    padding: 12px 24px;
    border-radius: 12px;
    font-weight: 700;
    cursor: pointer;
    transition: all 0.3s ease;
    box-shadow: 0 4px 15px rgba(63, 176, 255, 0.3);
}

.login-btn:hover {
    transform: translateY(-2px);
    box-shadow: 0 6px 20px rgba(63, 176, 255, 0.4);
}

.contact-btn {
    background: rgba(63,176,255,0.1);
    color: var(--accent);
    border: 1px solid rgba(63,176,255,0.3);
    padding: 12px 24px;
    border-radius: 12px;
    font-weight: 700;
    cursor: pointer;
    transition: all 0.3s ease;
}

.light-mode .contact-btn {
    background: rgba(26,115,232,0.1);
    color: var(--accent);
}

.contact-btn:hover {
    background: rgba(63,176,255,0.2);
    transform: translateY(-2px);
}

.light-mode .contact-btn:hover {
    background: rgba(26,115,232,0.2);
}

/* تحسينات إضافية */
.small {
    font-size: 12px;
    color: rgba(255,255,255,0.7);
}

.light-mode .small {
    color: rgba(0,0,0,0.6);
}

.note {
    font-size: 13px;
    color: #9fcff8;
    margin-top: 8px;
    line-height: 1.5;
}

.light-mode .note {
    color: #5f6368;
}

.loading {
    text-align: center;
    padding: 40px;
    color: var(--accent);
    font-size: 16px;
}

.loading i {
    animation: spin 1s linear infinite;
    margin-left: 10px;
}

@keyframes spin {
    0% { transform: rotate(0deg); }
    100% { transform: rotate(360deg); }
}

/* تبويبات */
.tabs {
    display: flex;
    gap: 10px;
    margin-bottom: 20px;
    border-bottom: 1px solid rgba(255,255,255,0.1);
    padding-bottom: 10px;
}

.tab {
    padding: 10px 20px;
    background: rgba(255,255,255,0.05);
    border-radius: 8px;
    cursor: pointer;
    transition: all 0.3s ease;
}

.tab.active {
    background: var(--accent);
    color: white;
}

.tab:hover:not(.active) {
    background: rgba(255,255,255,0.1);
}

/* إعدادات التبديل */
.settings-option {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 15px 0;
    border-bottom: 1px solid rgba(255,255,255,0.05);
}

.light-mode .settings-option {
    border-bottom: 1px solid rgba(0,0,0,0.1);
}

.toggle-switch {
    position: relative;
    display: inline-block;
    width: 50px;
    height: 24px;
}

.toggle-switch input {
    opacity: 0;
    width: 0;
    height: 0;
}

.slider {
    position: absolute;
    cursor: pointer;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background-color: rgba(255,255,255,0.1);
    transition: .4s;
    border-radius: 24px;
}

.light-mode .slider {
    background-color: rgba(0,0,0,0.1);
}

.slider:before {
    position: absolute;
    content: "";
    height: 16px;
    width: 16px;
    left: 4px;
    bottom: 4px;
    background-color: white;
    transition: .4s;
    border-radius: 50%;
}

input:checked + .slider {
    background-color: var(--accent);
}

input:checked + .slider:before {
    transform: translateX(26px);
}

/* أنماط جديدة لنظام التسجيل */

.welcome-screen {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: linear-gradient(135deg, var(--bg-dark) 0%, #001e3c 100%);
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    z-index: 10000;
    padding: 20px;
    text-align: center;
}

.welcome-content {
    background: var(--panel);
    padding: 40px 30px;
    border-radius: 24px;
    box-shadow: var(--shadow);
    max-width: 500px;
    width: 100%;
    border: 1px solid rgba(255,255,255,0.1);
}

.welcome-logo {
    width: 100px;
    height: 100px;
    border-radius: 20px;
    background: var(--gradient);
    display: grid;
    place-items: center;
    margin: 0 auto 20px;
    font-size: 40px;
    color: white;
    font-weight: 800;
}

.welcome-title {
    font-size: 28px;
    font-weight: 800;
    background: linear-gradient(135deg, #fff 0%, var(--accent) 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    margin-bottom: 10px;
}

.welcome-subtitle {
    color: rgba(255,255,255,0.7);
    margin-bottom: 30px;
    line-height: 1.6;
}

.welcome-buttons {
    display: flex;
    flex-direction: column;
    gap: 15px;
    margin-top: 30px;
}

.welcome-btn {
    padding: 16px 24px;
    border-radius: 12px;
    font-weight: 700;
    cursor: pointer;
    transition: all 0.3s ease;
    border: none;
    font-family: 'Cairo';
    font-size: 16px;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 10px;
}

.welcome-btn.primary {
    background: var(--gradient);
    color: white;
    box-shadow: 0 4px 15px rgba(63, 176, 255, 0.3);
}

.welcome-btn.secondary {
    background: rgba(255,255,255,0.05);
    color: var(--muted);
    border: 1px solid rgba(255,255,255,0.1);
}

.welcome-btn:hover {
    transform: translateY(-2px);
    box-shadow: 0 6px 20px rgba(63, 176, 255, 0.4);
}

.welcome-btn.secondary:hover {
    background: rgba(255,255,255,0.1);
}

.welcome-features {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 15px;
    margin: 25px 0;
}

.feature-item {
    display: flex;
    align-items: center;
    gap: 10px;
    font-size: 14px;
    color: rgba(255,255,255,0.8);
}

.feature-item i {
    color: var(--accent);
    width: 20px;
}

.light-mode .welcome-screen {
    background: linear-gradient(135deg, #f0f2f5 0%, #e3e8f0 100%);
}

.light-mode .welcome-content {
    background: white;
    border: 1px solid rgba(0,0,0,0.1);
}

.light-mode .welcome-title {
    background: linear-gradient(135deg, #333 0%, var(--accent) 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
}

.light-mode .welcome-subtitle {
    color: rgba(0,0,0,0.7);
}

.light-mode .welcome-btn.secondary {
    background: rgba(0,0,0,0.05);
    color: #333;
    border: 1px solid rgba(0,0,0,0.1);
}

.light-mode .feature-item {
    color: rgba(0,0,0,0.8);
}

/* تحسينات نموذج التسجيل */
.auth-form {
    display: flex;
    flex-direction: column;
    gap: 15px;
}

.form-group {
    display: flex;
    flex-direction: column;
    gap: 8px;
}

.form-label {
    font-weight: 600;
    color: white;
    font-size: 14px;
}

.light-mode .form-label {
    color: #333;
}

.form-input {
    padding: 14px 16px;
    background: rgba(255,255,255,0.05);
    border: 1px solid rgba(255,255,255,0.1);
    border-radius: 10px;
    color: white;
    font-family: 'Cairo';
    font-size: 15px;
    transition: all 0.3s ease;
}

.light-mode .form-input {
    background: rgba(0,0,0,0.05);
    border: 1px solid rgba(0,0,0,0.1);
    color: #333;
}

.form-input:focus {
    outline: none;
    border-color: var(--accent);
    background: rgba(255,255,255,0.08);
}

.light-mode .form-input:focus {
    background: rgba(0,0,0,0.08);
}

.form-options {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin: 10px 0;
}

.remember-me {
    display: flex;
    align-items: center;
    gap: 8px;
    font-size: 14px;
}

.forgot-password {
    color: var(--accent);
    text-decoration: none;
    font-size: 14px;
}

.forgot-password:hover {
    text-decoration: underline;
}

.auth-divider {
    display: flex;
    align-items: center;
    margin: 20px 0;
    color: rgba(255,255,255,0.5);
}

.light-mode .auth-divider {
    color: rgba(0,0,0,0.5);
}

.auth-divider::before,
.auth-divider::after {
    content: '';
    flex: 1;
    height: 1px;
    background: rgba(255,255,255,0.2);
}

.light-mode .auth-divider::before,
.light-mode .auth-divider::after {
    background: rgba(0,0,0,0.2);
}

.auth-divider span {
    padding: 0 15px;
    font-size: 14px;
}

.social-login {
    display: flex;
    gap: 12px;
}

.social-btn {
    flex: 1;
    padding: 12px;
    border-radius: 10px;
    border: 1px solid rgba(255,255,255,0.1);
    background: rgba(255,255,255,0.05);
    color: white;
    cursor: pointer;
    transition: all 0.3s ease;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 8px;
}

.light-mode .social-btn {
    border: 1px solid rgba(0,0,0,0.1);
    background: rgba(0,0,0,0.05);
    color: #333;
}

.social-btn:hover {
    background: rgba(255,255,255,0.1);
    transform: translateY(-1px);
}

.social-btn.google {
    border-color: #DB4437;
    color: #DB4437;
}

.social-btn.facebook {
    border-color: #4267B2;
    color: #4267B2;
}

.auth-switch {
    text-align: center;
    margin-top: 20px;
    font-size: 14px;
}

.auth-link {
    color: var(--accent);
    text-decoration: none;
    font-weight: 600;
    margin-right: 5px;
}

.auth-link:hover {
    text-decoration: underline;
}

/* تحسينات الرفع التلقائي */
.auto-login {
    position: fixed;
    top: 20px;
    left: 20px;
    background: rgba(255,255,255,0.1);
    padding: 10px 15px;
    border-radius: 8px;
    font-size: 12px;
    backdrop-filter: blur(10px);
    border: 1px solid rgba(255,255,255,0.2);
    animation: slideIn 0.5s ease;
}

@keyframes slideIn {
    from { transform: translateX(-100%); opacity: 0; }
    to { transform: translateX(0); opacity: 1; }
}

/* إشعارات */
.notification {
    position: fixed;
    top: 20px;
    left: 50%;
    transform: translateX(-50%);
    background: #4CAF50;
    color: white;
    padding: 12px 24px;
    border-radius: 8px;
    box-shadow: 0 4px 12px rgba(0,0,0,0.3);
    z-index: 10001;
    font-weight: 600;
    animation: slideDown 0.3s ease;
}

.notification.error {
    background: #f44336;
}

.notification.info {
    background: #2196F3;
}

@keyframes slideDown {
    from { transform: translateX(-50%) translateY(-100%); opacity: 0; }
    to { transform: translateX(-50%) translateY(0); opacity: 1; }
}

@keyframes slideUp {
    from { transform: translateX(-50%) translateY(0); opacity: 1; }
    to { transform: translateX(-50%) translateY(-100%); opacity: 0; }
}

/* أنماط واجهة المباريات الجديدة */
.matches-container {
    height: calc(100vh - 140px);
    position: relative;
}

.matches-frame {
    width: 100%;
    height: 100%;
    border: none;
    border-radius: 12px;
}

.matches-loading {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    text-align: center;
    color: white;
    background: rgba(0,0,0,0.8);
    padding: 20px;
    border-radius: 10px;
    z-index: 100;
}

/* responsive */
@media (max-width: 768px) {
    .container {
        padding: 15px;
    }
    
    .countries-grid {
        grid-template-columns: repeat(auto-fill, minmax(90px, 1fr));
        gap: 10px;
    }
    
    .country {
        padding: 12px 8px;
    }
    
    .country img {
        width: 50px;
        height: 50px;
    }
    
    .bottom-nav button {
        min-width: 60px;
        padding: 8px 12px;
        font-size: 12px;
    }
    
    .bottom-nav button i {
        font-size: 16px;
    }
    
    .welcome-content {
        padding: 30px 20px;
    }
    
    .welcome-features {
        grid-template-columns: 1fr;
    }
    
    .matches-container {
        height: calc(100vh - 120px);
    }
}

/* تأثيرات scrollbar */
.channels-list::-webkit-scrollbar {
    width: 6px;
}

.channels-list::-webkit-scrollbar-track {
    background: rgba(255,255,255,0.05);
    border-radius: 3px;
}

.light-mode .channels-list::-webkit-scrollbar-track {
    background: rgba(0,0,0,0.05);
}

.channels-list::-webkit-scrollbar-thumb {
    background: var(--accent);
    border-radius: 3px;
}

.channels-list::-webkit-scrollbar-thumb:hover {
    background: var(--accent-dark);
}
</style>
</head>
<body>
<!-- شاشة الترحيب والتسجيل -->
<div class="welcome-screen" id="welcomeScreen">
    <div class="welcome-content">
        <div class="welcome-logo">A</div>
        <h1 class="welcome-title">Alhagby TV</h1>
        <p class="welcome-subtitle">البث المباشر للقنوات العربية والرياضية<br>استمتع بأفضل المحتوى الرياضي والعربي</p>
        
        <div class="welcome-features">
            <div class="feature-item">
                <i class="fas fa-tv"></i>
                <span>قنوات رياضية مباشرة</span>
            </div>
            <div class="feature-item">
                <i class="fas fa-futbol"></i>
                <span>مباريات حية</span>
            </div>
            <div class="feature-item">
                <i class="fas fa-satellite-dish"></i>
                <span>بي إن سبورت كاملة</span>
            </div>
            <div class="feature-item">
                <i class="fas fa-mobile-alt"></i>
                <span>متوافق مع جميع الأجهزة</span>
            </div>
        </div>
        
        <div class="welcome-buttons">
            <button class="welcome-btn primary" onclick="showLoginForm()">
                <i class="fas fa-sign-in-alt"></i>
                تسجيل الدخول
            </button>
            <button class="welcome-btn secondary" onclick="showRegisterForm()">
                <i class="fas fa-user-plus"></i>
                إنشاء حساب جديد
            </button>
            <button class="welcome-btn secondary" onclick="skipLogin()">
                <i class="fas fa-play"></i>
                متابعة كزائر
            </button>
        </div>
    </div>
</div>

<!-- نموذج التسجيل -->
<div class="modal" id="registerModal" style="display:none">
    <div class="card">
        <div class="modal-header">
            <h3 style="margin:0">إنشاء حساب جديد</h3>
            <div class="close-x" onclick="closeRegister()">✖</div>
        </div>
        <div class="auth-form">
            <div class="form-group">
                <label class="form-label">الاسم الكامل</label>
                <input type="text" class="form-input" id="registerName" placeholder="أدخل اسمك الكامل">
            </div>
            <div class="form-group">
                <label class="form-label">البريد الإلكتروني</label>
                <input type="email" class="form-input" id="registerEmail" placeholder="example@email.com">
            </div>
            <div class="form-group">
                <label class="form-label">كلمة المرور</label>
                <input type="password" class="form-input" id="registerPassword" placeholder="أدخل كلمة المرور">
            </div>
            <div class="form-group">
                <label class="form-label">تأكيد كلمة المرور</label>
                <input type="password" class="form-input" id="registerConfirmPassword" placeholder="أعد إدخال كلمة المرور">
            </div>
            
            <div class="form-options">
                <label class="remember-me">
                    <input type="checkbox" id="registerAgreement">
                    <span>أوافق على الشروط والأحكام</span>
                </label>
            </div>
            
            <button class="login-btn" style="width:100%;margin:10px 0;padding:14px" onclick="register()">
                <i class="fas fa-user-plus"></i> إنشاء حساب
            </button>
            
            <div class="auth-divider">
                <span>أو</span>
            </div>
            
            <div class="social-login">
                <button class="social-btn google" onclick="loginWithGoogle()">
                    <i class="fab fa-google"></i>
                    Google
                </button>
                <button class="social-btn facebook" onclick="loginWithFacebook()">
                    <i class="fab fa-facebook"></i>
                    Facebook
                </button>
            </div>
            
            <div class="auth-switch">
                <span>لديك حساب بالفعل؟</span>
                <a href="#" class="auth-link" onclick="showLoginForm()">تسجيل الدخول</a>
            </div>
        </div>
    </div>
</div>

<!-- الهيدر الرئيسي -->
<header class="app-header" style="display:none" id="mainHeader">
    <div class="brand">
        <div class="logo">A</div>
        <div>
            <div class="title">Alhagby TV</div>
            <div class="subtitle small">البث المباشر للقنوات العربية والرياضية</div>
        </div>
    </div>
    <div style="display:flex;gap:10px;align-items:center">
        <button class="contact-btn" onclick="toggleDarkMode()" id="themeToggle">
            <i class="fas fa-moon"></i>
        </button>
        <button class="login-btn" onclick="showLoginFromApp()" id="loginBtn">
            <i class="fas fa-user"></i> تسجيل الدخول
        </button>
    </div>
</header>

<!-- المحتوى الرئيسي -->
<div class="container" id="mainContent" style="display:none">
    <div class="panel">
        <h3><i class="fas fa-home"></i>مرحباً بك في Alhagby TV</h3>
        <p class="note">اختر من القائمة أدناه لاستعراض القنوات والمباريات والترتيبات</p>
    </div>
</div>

<!-- شريط التنقل السفلي -->
<div class="bottom-nav" style="display:none" id="bottomNav">
    <button id="btnCountries" class="active">
        <i class="fas fa-globe-asia"></i>
        <span>الدول</span>
    </button>
    <button id="btnSports">
        <i class="fas fa-tv"></i>
        <span>القنوات</span>
    </button>
    <button id="btnBein">
        <i class="fas fa-satellite-dish"></i>
        <span>بي إن سبورت</span>
    </button>
    <button id="btnMatches">
        <i class="fas fa-futbol"></i>
        <span>المباريات</span>
    </button>
    <button id="btnSettings">
        <i class="fas fa-cog"></i>
        <span>الإعدادات</span>
    </button>
</div>

<!-- المودالات الأخرى -->
<div class="modal" id="channelModal">
    <div class="card">
        <div class="modal-header">
            <h3 style="margin:0" id="channelName">اسم القناة</h3>
            <div class="close-x" onclick="closeModal()">✖</div>
        </div>
        <div class="player-wrap">
            <video id="player" controls playsinline webkit-playsinline></video>
            <div class="player-info">
                <div id="nowLabel">جارٍ التحميل...</div>
                <select class="quality-selector" id="qualitySelector">
                    <option value="auto">جودة تلقائية</option>
                    <option value="360">360p</option>
                    <option value="480">480p</option>
                    <option value="720">720p</option>
                    <option value="1080">1080p</option>
                </select>
                <div id="playerStatus" class="small">مستعد</div>
            </div>
        </div>
    </div>
</div>

<div class="modal" id="loginModal">
    <div class="card">
        <div class="modal-header">
            <h3 style="margin:0">تسجيل الدخول</h3>
            <div class="close-x" onclick="closeLogin()">✖</div>
        </div>
        <div class="auth-form">
            <div class="form-group">
                <label class="form-label">البريد الإلكتروني</label>
                <input type="email" class="form-input" id="loginEmail" placeholder="example@email.com">
            </div>
            <div class="form-group">
                <label class="form-label">كلمة المرور</label>
                <input type="password" class="form-input" id="loginPassword" placeholder="أدخل كلمة المرور">
            </div>
            
            <div class="form-options">
                <label class="remember-me">
                    <input type="checkbox" id="rememberMe">
                    <span>تذكرني</span>
                </label>
                <a href="#" class="forgot-password">نسيت كلمة المرور؟</a>
            </div>
            
            <button class="login-btn" style="width:100%;margin:10px 0;padding:14px" onclick="login()">
                <i class="fas fa-sign-in-alt"></i> تسجيل الدخول
            </button>
            
            <div class="auth-divider">
                <span>أو</span>
            </div>
            
            <div class="social-login">
                <button class="social-btn google" onclick="loginWithGoogle()">
                    <i class="fab fa-google"></i>
                    Google
                </button>
                <button class="social-btn facebook" onclick="loginWithFacebook()">
                    <i class="fab fa-facebook"></i>
                    Facebook
                </button>
            </div>
            
            <div class="auth-switch">
                <span>ليس لديك حساب؟</span>
                <a href="#" class="auth-link" onclick="showRegisterForm()">إنشاء حساب جديد</a>
            </div>
        </div>
    </div>
</div>

<script>
// جميع البيانات والمتغيرات
const countries = {
    "اليمن":"https://iptv-org.github.io/iptv/countries/ye.m3u",
    "السعودية":"https://iptv-org.github.io/iptv/countries/sa.m3u",
    "قطر":"https://iptv-org.github.io/iptv/countries/qa.m3u",
    "الإمارات":"https://iptv-org.github.io/iptv/countries/ae.m3u",
    "مصر":"https://iptv-org.github.io/iptv/countries/eg.m3u",
    "العراق":"https://iptv-org.github.io/iptv/countries/iq.m3u",
    "الجزائر":"https://iptv-org.github.io/iptv/countries/dz.m3u",
    "تونس":"https://iptv-org.github.io/iptv/countries/tn.m3u",
    "المغرب":"https://iptv-org.github.io/iptv/countries/ma.m3u",
    "لبنان":"https://iptv-org.github.io/iptv/countries/lb.m3u",
    "سوريا":"https://iptv-org.github.io/iptv/countries/sy.m3u",
    "ليبيا":"https://iptv-org.github.io/iptv/countries/ly.m3u",
    "الأردن":"https://iptv-org.github.io/iptv/countries/jo.m3u",
    "فلسطين":"https://iptv-org.github.io/iptv/countries/ps.m3u",
    "الكويت":"https://iptv-org.github.io/iptv/countries/kw.m3u",
    "البحرين":"https://iptv-org.github.io/iptv/countries/bh.m3u",
    "سلطنة عمان":"https://iptv-org.github.io/iptv/countries/om.m3u",
    "جزر القمر":"https://iptv-org.github.io/iptv/countries/km.m3u",
    "موريتانيا":"https://iptv-org.github.io/iptv/countries/mr.m3u",
    "السودان":"https://iptv-org.github.io/iptv/countries/sd.m3u",
    "جيبوتي":"https://iptv-org.github.io/iptv/countries/dj.m3u",
    "الصومال":"https://iptv-org.github.io/iptv/countries/so.m3u"
};

const countryFlags = {
    'اليمن':'ye','السعودية':'sa','قطر':'qa','الإمارات':'ae','مصر':'eg','العراق':'iq','الجزائر':'dz','تونس':'tn','المغرب':'ma','لبنان':'lb','سوريا':'sy','ليبيا':'ly','الأردن':'jo','فلسطين':'ps','الكويت':'kw','البحرين':'bh','سلطنة عمان':'om','جزر القمر':'km','موريتانيا':'mr','السودان':'sd','جيبوتي':'dj','الصومال':'so'
};

// قنوات بي إن سبورت - معدلة للربط مع الموقع الخارجي
const beinSportsChannels = [
    { title: "بي إن سبورت HD 1", logo: "https://i.ibb.co/0Q8L8wZ/beinsports1.png", external: true },
    { title: "بي إن سبورت HD 2", logo: "https://i.ibb.co/0Q8L8wZ/beinsports2.png", external: true },
    { title: "بي إن سبورت HD 3", logo: "https://i.ibb.co/0Q8L8wZ/beinsports3.png", external: true },
    { title: "بي إن سبورت HD 4", logo: "https://i.ibb.co/0Q8L8wZ/beinsports4.png", external: true },
    { title: "بي إن سبورت HD 5", logo: "https://i.ibb.co/0Q8L8wZ/beinsports5.png", external: true },
    { title: "بي إن سبورت HD 6", logo: "https://i.ibb.co/0Q8L8wZ/beinsports6.png", external: true },
    { title: "بي إن سبورت HD 7", logo: "https://i.ibb.co/0Q8L8wZ/beinsports7.png", external: true },
    { title: "بي إن سبورت HD 8", logo: "https://i.ibb.co/0Q8L8wZ/beinsports8.png", external: true },
    { title: "بي إن سبورت HD 9", logo: "https://i.ibb.co/0Q8L8wZ/beinsports9.png", external: true },
    { title: "بي إن سبورت HD 10", logo: "https://i.ibb.co/0Q8L8wZ/beinsports10.png", external: true },
    { title: "بي إن سبورت NBA", logo: "https://i.ibb.co/0Q8L8wZ/beinnba.png", external: true },
    { title: "بي إن سبورت PREMIUM 1", logo: "https://i.ibb.co/0Q8L8wZ/beinpremium1.png", external: true },
    { title: "بي إن سبورت PREMIUM 2", logo: "https://i.ibb.co/0Q8L8wZ/beinpremium2.png", external: true },
    { title: "بي إن سبورت NEWS", logo: "https://i.ibb.co/0Q8L8wZ/beinnews.png", external: true },
    { title: "بي إن سبورت English 1", logo: "https://i.ibb.co/0Q8L8wZ/beinen1.png", external: true },
    { title: "بي إن سبورت English 2", logo: "https://i.ibb.co/0Q8L8wZ/beinen2.png", external: true }
];

// مصادر القنوات الرياضية
const sportsSources = [
    "https://iptv-org.github.io/iptv/categories/sports.m3u",
    "https://raw.githubusercontent.com/Free-IPTV/Countries/master/SA/sport.m3u",
    "https://raw.githubusercontent.com/iloveiptv/iptv/main/sports.m3u"
];

// المتغيرات العامة
let hlsInstance = null;
let currentUser = null;
let isDarkMode = true;
let currentView = 'leagues';

// بيانات المستخدمين
const users = JSON.parse(localStorage.getItem('alhagby_users')) || [];
let currentUserData = JSON.parse(localStorage.getItem('alhagby_current_user')) || null;
const isGuest = localStorage.getItem('alhagby_guest') === 'true';

// دوال نظام التسجيل
function showLoginForm() {
    document.getElementById('welcomeScreen').style.display = 'none';
    document.getElementById('loginModal').style.display = 'grid';
}

function showRegisterForm() {
    document.getElementById('welcomeScreen').style.display = 'none';
    document.getElementById('registerModal').style.display = 'grid';
}

function closeRegister() {
    document.getElementById('registerModal').style.display = 'none';
    document.getElementById('welcomeScreen').style.display = 'flex';
}

function closeLogin() {
    document.getElementById('loginModal').style.display = 'none';
    if (!currentUserData && !isGuest) {
        document.getElementById('welcomeScreen').style.display = 'flex';
    }
}

function skipLogin() {
    localStorage.setItem('alhagby_guest', 'true');
    showMainApp();
    showNotification('مرحباً بك كزائر! يمكنك التسجيل لاحقاً من الإعدادات');
}

function showMainApp() {
    document.getElementById('welcomeScreen').style.display = 'none';
    document.getElementById('mainHeader').style.display = 'flex';
    document.getElementById('mainContent').style.display = 'grid';
    document.getElementById('bottomNav').style.display = 'flex';
    updateUserInterface();
    loadDefaultContent();
}

function register() {
    const name = document.getElementById('registerName').value;
    const email = document.getElementById('registerEmail').value;
    const password = document.getElementById('registerPassword').value;
    const confirmPassword = document.getElementById('registerConfirmPassword').value;
    const agreement = document.getElementById('registerAgreement').checked;

    if (!name || !email || !password || !confirmPassword) {
        showNotification('يرجى ملء جميع الحقول', 'error');
        return;
    }

    if (password !== confirmPassword) {
        showNotification('كلمات المرور غير متطابقة', 'error');
        return;
    }

    if (password.length < 6) {
        showNotification('كلمة المرور يجب أن تكون 6 أحرف على الأقل', 'error');
        return;
    }

    if (!agreement) {
        showNotification('يرجى الموافقة على الشروط والأحكام', 'error');
        return;
    }

    if (users.find(user => user.email === email)) {
        showNotification('هذا البريد الإلكتروني مسجل بالفعل', 'error');
        return;
    }

    const newUser = {
        id: Date.now().toString(),
        name: name,
        email: email,
        password: password,
        createdAt: new Date().toISOString(),
        favorites: [],
        preferences: {
            darkMode: true,
            videoQuality: 'auto',
            notifications: true
        }
    };

    users.push(newUser);
    localStorage.setItem('alhagby_users', JSON.stringify(users));
    loginUser(newUser);
    showNotification('تم إنشاء الحساب بنجاح!', 'success');
}

function login() {
    const email = document.getElementById('loginEmail').value;
    const password = document.getElementById('loginPassword').value;
    const rememberMe = document.getElementById('rememberMe')?.checked || false;

    if (!email || !password) {
        showNotification('يرجى إدخال البريد الإلكتروني وكلمة المرور', 'error');
        return;
    }

    const user = users.find(u => u.email === email && u.password === password);
    
    if (user) {
        loginUser(user, rememberMe);
        showNotification('تم تسجيل الدخول بنجاح!', 'success');
    } else {
        showNotification('البريد الإلكتروني أو كلمة المرور غير صحيحة', 'error');
    }
}

function loginUser(user, rememberMe = true) {
    currentUserData = {
        id: user.id,
        name: user.name,
        email: user.email,
        preferences: user.preferences
    };

    if (rememberMe) {
        localStorage.setItem('alhagby_current_user', JSON.stringify(currentUserData));
    } else {
        sessionStorage.setItem('alhagby_current_user', JSON.stringify(currentUserData));
    }

    closeLogin();
    closeRegister();
    showMainApp();
    
    if (user.preferences) {
        applyUserPreferences(user.preferences);
    }
}

function applyUserPreferences(preferences) {
    if (preferences.darkMode !== undefined) {
        isDarkMode = preferences.darkMode;
        document.body.classList.toggle('light-mode', !isDarkMode);
        const themeIcon = document.querySelector('#themeToggle i');
        if (themeIcon) {
            themeIcon.className = isDarkMode ? 'fas fa-moon' : 'fas fa-sun';
        }
    }
    
    if (preferences.videoQuality) {
        document.getElementById('qualitySelector').value = preferences.videoQuality;
    }
}

function logout() {
    currentUserData = null;
    localStorage.removeItem('alhagby_current_user');
    sessionStorage.removeItem('alhagby_current_user');
    localStorage.removeItem('alhagby_guest');
    
    document.getElementById('mainHeader').style.display = 'none';
    document.getElementById('mainContent').style.display = 'none';
    document.getElementById('bottomNav').style.display = 'none';
    document.getElementById('welcomeScreen').style.display = 'flex';
    
    showNotification('تم تسجيل الخروج بنجاح');
}

function loginWithGoogle() {
    const googleUser = {
        id: 'google_' + Date.now(),
        name: "مستخدم Google",
        email: "user@gmail.com",
        provider: 'google',
        createdAt: new Date().toISOString(),
        preferences: {
            darkMode: true,
            videoQuality: 'auto',
            notifications: true
        }
    };
    
    if (!users.find(u => u.email === googleUser.email)) {
        users.push(googleUser);
        localStorage.setItem('alhagby_users', JSON.stringify(users));
    }
    
    loginUser(googleUser);
    showNotification('تم التسجيل بحساب Google بنجاح!', 'success');
}

function loginWithFacebook() {
    const facebookUser = {
        id: 'facebook_' + Date.now(),
        name: "مستخدم Facebook",
        email: "user@facebook.com",
        provider: 'facebook',
        createdAt: new Date().toISOString(),
        preferences: {
            darkMode: true,
            videoQuality: 'auto',
            notifications: true
        }
    };
    
    if (!users.find(u => u.email === facebookUser.email)) {
        users.push(facebookUser);
        localStorage.setItem('alhagby_users', JSON.stringify(users));
    }
    
    loginUser(facebookUser);
    showNotification('تم التسجيل بحساب Facebook بنجاح!', 'success');
}

function showNotification(message, type = 'info') {
    const notification = document.createElement('div');
    notification.className = `notification ${type}`;
    notification.style.cssText = `
        position: fixed;
        top: 20px;
        left: 50%;
        transform: translateX(-50%);
        background: ${type === 'error' ? '#f44336' : type === 'success' ? '#4CAF50' : '#2196F3'};
        color: white;
        padding: 12px 24px;
        border-radius: 8px;
        box-shadow: 0 4px 12px rgba(0,0,0,0.3);
        z-index: 10001;
        font-weight: 600;
        animation: slideDown 0.3s ease;
    `;
    
    notification.textContent = message;
    document.body.appendChild(notification);
    
    setTimeout(() => {
        notification.style.animation = 'slideUp 0.3s ease';
        setTimeout(() => {
            if (notification.parentNode) {
                notification.parentNode.removeChild(notification);
            }
        }, 300);
    }, 3000);
}

function updateUserInterface() {
    const loginBtn = document.getElementById('loginBtn');
    if (currentUserData) {
        loginBtn.innerHTML = '<i class="fas fa-user"></i> ' + currentUserData.name;
    } else if (isGuest) {
        loginBtn.innerHTML = '<i class="fas fa-user"></i> زائر';
    } else {
        loginBtn.innerHTML = '<i class="fas fa-user"></i> تسجيل الدخول';
    }
}

function showLoginFromApp() {
    if (currentUserData || isGuest) {
        // إذا كان مسجل دخول أو زائر، عرض خيار تسجيل الخروج
        if (confirm('هل تريد تسجيل الخروج؟')) {
            logout();
        }
    } else {
        // إذا لم يكن مسجل دخول، عرض نموذج التسجيل
        showLoginForm();
    }
}

// دوال المشغل
function loadStream(url) {
    if (hlsInstance) {
        try {
            hlsInstance.destroy();
        } catch (e) {}
        hlsInstance = null;
    }
    
    const player = document.getElementById('player');
    player.pause();
    player.removeAttribute('src');
    player.load();
    
    document.getElementById('nowLabel').textContent = 'جارٍ التحميل…';
    document.getElementById('playerStatus').textContent = 'جاري الاتصال';

    if (player.canPlayType('application/vnd.apple.mpegurl')) {
        player.src = url;
        player.play().then(() => {
            document.getElementById('playerStatus').textContent = 'يعمل الآن';
        }).catch(e => {
            document.getElementById('playerStatus').textContent = 'خطأ في التشغيل';
            console.warn(e);
        });
    } else if (Hls.isSupported()) {
        hlsInstance = new Hls();
        hlsInstance.loadSource(url);
        hlsInstance.attachMedia(player);
        hlsInstance.on(Hls.Events.MANIFEST_PARSED, function() {
            player.play().then(() => {
                document.getElementById('playerStatus').textContent = 'يعمل الآن';
            }).catch(() => {
                document.getElementById('playerStatus').textContent = 'خطأ في التشغيل';
            });
        });
        hlsInstance.on(Hls.Events.ERROR, function(event, data) {
            console.warn('hls error', data);
            document.getElementById('playerStatus').textContent = 'خطأ في البث: ' + data.type;
        });
    } else {
        player.src = url;
        player.play().catch(e => {
            document.getElementById('playerStatus').textContent = 'التشغيل غير مدعوم';
        });
    }
}

// ⭐⭐ التعديل الجديد: ربط قنوات بي إن سبورت بالموقع الخارجي ⭐⭐
function openChannel(name, url, isExternal = false) {
    if (isExternal) {
        // توجيه إلى الموقع الخارجي
        window.open('https://www.goalyallashoot.com/', '_blank');
        showNotification('جاري التوجيه إلى قنوات بي إن سبورت...');
    } else {
        // فتح القناة بشكل طبيعي
        document.getElementById('channelName').textContent = name;
        document.getElementById('channelModal').style.display = 'grid';
        loadStream(url);
    }
}

function closeModal() {
    document.getElementById('channelModal').style.display = 'none';
    if (hlsInstance) {
        try {
            hlsInstance.destroy();
        } catch (e) {}
        hlsInstance = null;
    }
    const player = document.getElementById('player');
    player.pause();
    player.removeAttribute('src');
    player.load();
}

// دوال تحميل القنوات
function parseM3U(text) {
    const lines = text.split(/\r?\n/).map(l => l.trim()).filter(Boolean);
    const items = [];
    for (let i = 0; i < lines.length; i++) {
        const l = lines[i];
        if (l.startsWith('#EXTINF:')) {
            const info = l;
            const name = info.split(',').slice(1).join(',').trim();
            let logo = null, group = null;
            const tvgMatch = info.match(/tvg-logo="([^"]+)"/i);
            if (tvgMatch) logo = tvgMatch[1];
            const grpMatch = info.match(/group-title="([^"]+)"/i);
            if (grpMatch) group = grpMatch[1];
            const urlLine = lines[i + 1] || '';
            items.push({ title: name, logo, group, url: urlLine });
        }
    }
    return items;
}

function loadCountryChannels(country) {
    const main = document.getElementById('mainContent');
    main.innerHTML = '<div class="panel loading"><i class="fas fa-spinner"></i> جاري تحميل قنوات ' + country + '…</div>';
    
    fetch(countries[country])
        .then(r => r.text())
        .then(text => {
            const items = parseM3U(text);
            let html = '<div class="panel"><h3><i class="fas fa-flag"></i>قنوات ' + country + '</h3>';
            html += '<div class="channels-list">';
            items.forEach(it => {
                html += '<div class="channel" onclick="openChannel(\'' + it.title.replace(/'/g, "\\'") + '\',\'' + it.url + '\')">';
                html += '<img src="' + (it.logo || '') + '" onerror="this.src=\'https://via.placeholder.com/60x40/333/white?text=TV\'" class="channel-logo">';
                html += '<div><strong>' + it.title + '</strong><span class="small">' + (it.group || '') + '</span></div>';
                html += '</div>';
            });
            html += '</div></div>';
            main.innerHTML = html;
        })
        .catch(e => {
            main.innerHTML = '<div class="panel">فشل تحميل القنوات: ' + e.message + '</div>';
            console.warn(e);
        });
}

function loadAllSportsChannels() {
    const main = document.getElementById('mainContent');
    main.innerHTML = '<div class="panel loading"><i class="fas fa-spinner"></i> جاري تحميل جميع القنوات الرياضية…</div>';
    
    let allSportsChannels = [];
    let loadedSources = 0;
    
    sportsSources.forEach(source => {
        fetch(source)
            .then(r => r.text())
            .then(text => {
                const items = parseM3U(text);
                allSportsChannels = allSportsChannels.concat(items);
                loadedSources++;
                
                if (loadedSources === sportsSources.length) {
                    displaySportsChannels(allSportsChannels);
                }
            })
            .catch(e => {
                console.warn('Failed to load sports source:', source, e);
                loadedSources++;
                if (loadedSources === sportsSources.length) {
                    displaySportsChannels(allSportsChannels);
                }
            });
    });
}

function displaySportsChannels(channels) {
    let html = '<div class="panel"><h3><i class="fas fa-tv"></i>القنوات الرياضية العالمية</h3>';
    html += '<div class="channels-list">';
    
    const uniqueChannels = channels.filter((channel, index, self) =>
        index === self.findIndex(c => c.title === channel.title && c.url === channel.url)
    );
    
    uniqueChannels.forEach(it => {
        html += '<div class="channel" onclick="openChannel(\'' + it.title.replace(/'/g, "\\'") + '\',\'' + it.url + '\')">';
        html += '<img src="' + (it.logo || '') + '" onerror="this.src=\'https://via.placeholder.com/60x40/333/white?text=SPORT\'" class="channel-logo">';
        html += '<div><strong>' + it.title + '</strong><span class="small">' + (it.group || '') + '</span></div>';
        html += '</div>';
    });
    
    html += '</div></div>';
    document.getElementById('mainContent').innerHTML = html;
}

// ⭐⭐ التعديل الجديد: تحميل قنوات بي إن سبورت مع الربط الخارجي ⭐⭐
function loadBeinSports() {
    let html = '<div class="panel bein-section">';
    html += '<h3><i class="fas fa-satellite-dish"></i>قنوات بي إن سبورت</h3>';
    html += '<p class="note" style="margin-bottom:20px;color:#9fcff8">جميع قنوات بي إن سبورت متاحة عبر الموقع الرسمي</p>';
    html += '<div class="channels-list">';
    
    beinSportsChannels.forEach(channel => {
        html += '<div class="channel bein-channel" onclick="openChannel(\'' + channel.title + '\', \'\', true)">';
        html += '<img src="' + channel.logo + '" onerror="this.src=\'https://via.placeholder.com/60x40/00509b/white?text=BEIN\'" class="channel-logo">';
        html += '<div><strong>' + channel.title + '</strong><span class="small">انقر للمشاهدة عبر الموقع الرسمي</span></div>';
        html += '<i class="fas fa-external-link-alt" style="color:var(--accent);font-size:14px"></i>';
        html += '</div>';
    });
    
    html += '</div></div>';
    document.getElementById('mainContent').innerHTML = html;
}

// ⭐⭐ واجهة المباريات الجديدة ⭐⭐
function loadMatches() {
    let html = '<div class="panel">';
    html += '<h3><i class="fas fa-futbol"></i>المباريات الحية والنتائج</h3>';
    html += '<p class="note">متابعة حية لجميع المباريات والبطولات العالمية</p>';
    html += '</div>';
    
    html += '<div class="matches-container">';
    html += '<div class="matches-loading" id="matchesLoading">';
    html += '<i class="fas fa-spinner fa-spin"></i><br>';
    html += 'جاري تحميل Alhagby TV...';
    html += '</div>';
    html += '<iframe class="matches-frame" id="matchesFrame" src="about:blank"></iframe>';
    html += '</div>';
    
    document.getElementById('mainContent').innerHTML = html;
    
    // تحميل واجهة المباريات
    loadMatchesInterface();
}

function loadMatchesInterface() {
    const frame = document.getElementById('matchesFrame');
    const loading = document.getElementById('matchesLoading');
    const currentURL = 'https://www.ysscores.com/ar/index';
    
    class AdvancedProxyModifier {
        constructor() {
            this.frame = frame;
            this.loading = loading;
            this.currentURL = currentURL;
            this.init();
        }

        async init() {
            await this.loadAndInject(this.currentURL);
            this.setupNavigationHandler();
        }

        setupNavigationHandler() {
            // مراقبة جميع النقرات على الروابط في الإطار
            this.frame.addEventListener('load', () => {
                try {
                    const frameDoc = this.frame.contentDocument || this.frame.contentWindow.document;
                    
                    // استبدال النصوص فور تحميل الصفحة
                    this.replaceTextInDocument(frameDoc);
                    
                    // اعتراض جميع النقرات على الروابط
                    const links = frameDoc.querySelectorAll('a');
                    links.forEach(link => {
                        link.addEventListener('click', (e) => {
                            e.preventDefault();
                            const href = link.getAttribute('href');
                            if (href) {
                                const fullUrl = href.startsWith('http') ? href : 
                                               href.startsWith('/') ? 'https://www.ysscores.com' + href : 
                                               this.currentURL + href;
                                this.loadAndInject(fullUrl);
                            }
                        });
                    });

                    // اعتراض forms
                    const forms = frameDoc.querySelectorAll('form');
                    forms.forEach(form => {
                        form.addEventListener('submit', (e) => {
                            e.preventDefault();
                            // يمكن معالجة الفورمز هنا إذا لزم الأمر
                        });
                    });

                } catch (error) {
                    console.log('لا يمكن الوصول للمحتوى بسبب CORS');
                }
            });
        }

        async loadAndInject(url) {
            try {
                this.showLoading();
                this.currentURL = url;
                
                const proxyURL = `https://api.allorigins.win/raw?url=${encodeURIComponent(url)}`;
                const response = await fetch(proxyURL);
                
                if (!response.ok) throw new Error('فشل التحميل');
                
                let html = await response.text();
                
                // استبدال شامل لجميع النصوص
                html = this.comprehensiveTextReplacement(html);
                
                // إضافة CSS لتغطية أي أسماء متبقية
                html = this.injectCustomCSS(html);
                
                // إضافة script للاستبدال الديناميكي
                html = this.injectReplacementScript(html);
                
                this.frame.srcdoc = html;
                this.hideLoading();
                
            } catch (error) {
                this.showError();
            }
        }

        comprehensiveTextReplacement(html) {
            // قائمة شاملة لجميع الأشكال الممكنة
            const patterns = [
                // يلا شوت بالعربي
                /يَلاَّ?\s*شُوتَ?/gi,
                /يَلاَّ?\s*شوتَ?/gi, 
                /يلا\s*شوت/gi,
                /يلاشوت/gi,
                /يَلا\s*شُوت/gi,
                
                // Yalla Shot بالإنجليزي
                /Yalla\s*Shot/gi,
                /YALLA\s*SHOT/gi,
                /yalla\s*shot/gi,
                /YallaShot/gi,
                /yallashot/gi,
                
                // اختصارات
                /Yalla/gi,
                /yalla/gi,
                /شوت/gi,
                /Shot/gi,
                
                // في attributes
                /"([^"]*يلا[^"]*)"/gi,
                /'([^']*يلا[^']*)'/gi,
                /"([^"]*Yalla[^"]*)"/gi,
                /'([^']*Yalla[^']*)'/gi
            ];

            patterns.forEach(pattern => {
                html = html.replace(pattern, (match) => {
                    if (match.includes('يلا') || match.includes('Yalla') || match.includes('yalla') || 
                        match.includes('شوت') || match.includes('Shot') || match.includes('shot')) {
                        return match.replace(/يلا|Yalla|yalla|شوت|Shot|shot/gi, 'Alhagby TV')
                                   .replace(/\s+/g, ' ')
                                   .trim();
                    }
                    return match;
                });
            });

            return html;
        }

        injectCustomCSS(html) {
            const css = `
                <style>
                    /* إخفاء جميع العناصر التي قد تحتوي على الاسم القديم */
                    [class*="yalla"],
                    [class*="Yalla"],
                    [id*="yalla"],
                    [id*="Yalla"],
                    [class*="shot"],
                    [class*="Shot"],
                    [class*="شوت"],
                    .logo,
                    .header-logo,
                    .site-logo,
                    .navbar-brand,
                    .brand,
                    footer *,
                    header * {
                        position: relative !important;
                    }

                    /* استبدال بالنص الجديد */
                    [class*="yalla"]::before,
                    [class*="Yalla"]::before,
                    [class*="shot"]::before,
                    [class*="Shot"]::before,
                    [class*="شوت"]::before,
                    .logo::before,
                    .header-logo::before,
                    .site-logo::before {
                        content: "Alhagby TV" !important;
                        position: absolute !important;
                        top: 50% !important;
                        left: 50% !important;
                        transform: translate(-50%, -50%) !important;
                        background: linear-gradient(135deg, #1a237e 0%, #283593 100%) !important;
                        color: white !important;
                        padding: 8px 16px !important;
                        border-radius: 20px !important;
                        font-weight: bold !important;
                        font-size: 16px !important;
                        z-index: 9999 !important;
                        white-space: nowrap !important;
                    }

                    /* إخفاء المحتوى الأصلي */
                    [class*="yalla"] > *,
                    [class*="Yalla"] > *,
                    [class*="shot"] > *,
                    [class*="Shot"] > *,
                    [class*="شوت"] > *,
                    .logo > *,
                    .header-logo > *,
                    .site-logo > * {
                        visibility: hidden !important;
                    }

                    /* تغطية النصوص في الفوتر */
                    footer:contains("يلا"),
                    footer:contains("Yalla"),
                    footer:contains("yalla") {
                        background: #1a237e !important;
                    }
                </style>
            `;

            return html.replace('</head>', css + '</head>');
        }

        injectReplacementScript(html) {
            const script = `
                <script>
                    // استبدال ديناميكي بعد تحميل الصفحة
                    function replaceAllText() {
                        // استبدال في النصوص
                        document.body.innerHTML = document.body.innerHTML.replace(/يلا\\\\s*شوت/gi, 'Alhagby TV');
                        document.body.innerHTML = document.body.innerHTML.replace(/Yalla\\\\s*Shot/gi, 'Alhagby TV');
                        document.body.innerHTML = document.body.innerHTML.replace(/yalla\\\\s*shot/gi, 'Alhagby TV');
                        
                        // استبدال في attributes
                        const elements = document.querySelectorAll('*');
                        elements.forEach(el => {
                            for (let attr of ['alt', 'title', 'placeholder', 'value']) {
                                if (el[attr] && (el[attr].includes('يلا') || el[attr].includes('Yalla'))) {
                                    el[attr] = el[attr].replace(/يلا\\\\s*شوت|Yalla\\\\s*Shot/gi, 'Alhagby TV');
                                }
                            }
                        });
                    }

                    // تنفيذ فوري وتكرار كل ثانية
                    replaceAllText();
                    setInterval(replaceAllText, 1000);

                    // اعتراض الروابط
                    document.addEventListener('click', function(e) {
                        const link = e.target.closest('a');
                        if (link && link.href) {
                            e.preventDefault();
                            window.parent.postMessage({ 
                                type: 'NAVIGATE', 
                                url: link.href 
                            }, '*');
                        }
                    });
                <\/script>
            `;

            return html.replace('</body>', script + '</body>');
        }

        replaceTextInDocument(doc) {
            try {
                // استبدال النصوص في document
                const walker = document.createTreeWalker(
                    doc.body,
                    NodeFilter.SHOW_TEXT,
                    null,
                    false
                );

                let node;
                while (node = walker.nextNode()) {
                    if (node.textContent.includes('يلا') || node.textContent.includes('Yalla')) {
                        node.textContent = node.textContent.replace(/يلا\s*شوت|Yalla\s*Shot/gi, 'Alhagby TV');
                    }
                }
            } catch (error) {
                console.log('لا يمكن تعديل النصوص مباشرة');
            }
        }

        showLoading() {
            this.loading.style.display = 'block';
        }

        hideLoading() {
            this.loading.style.display = 'none';
        }

        showError() {
            this.frame.srcdoc = `
                <div style="background: #1a237e; color: white; height: 100vh; display: flex; justify-content: center; align-items: center; flex-direction: column;">
                    <h1>Alhagby TV</h1>
                    <p>تعذر تحميل المحتوى</p>
                    <button onclick="window.location.reload()" style="padding: 10px 20px; background: white; color: #1a237e; border: none; border-radius: 5px; margin-top: 10px;">
                        إعادة المحاولة
                    </button>
                </div>
            `;
        }
    }

    // التعامل مع التنقل
    window.addEventListener('message', (event) => {
        if (event.data.type === 'NAVIGATE') {
            proxyModifier.loadAndInject(event.data.url);
        }
    });

    const proxyModifier = new AdvancedProxyModifier();
}

function loadSettings() {
    let html = '<div class="panel"><h3><i class="fas fa-cog"></i>الإعدادات</h3>';
    
    if (currentUserData) {
        html += '<div class="settings-option">';
        html += '<span><i class="fas fa-user"></i> المستخدم: ' + currentUserData.name + '</span>';
        html += '<span class="small">' + currentUserData.email + '</span>';
        html += '</div>';
        html += '<button class="login-btn" onclick="logout()" style="width:100%;margin:10px 0">';
        html += '<i class="fas fa-sign-out-alt"></i> تسجيل الخروج';
        html += '</button>';
    } else if (isGuest) {
        html += '<div class="settings-option">';
        html += '<span><i class="fas fa-user"></i> الحالة: زائر</span>';
        html += '<span class="small">يمكنك التسجيل لحفظ التفضيلات</span>';
        html += '</div>';
        html += '<button class="login-btn" onclick="showLoginForm()" style="width:100%;margin:10px 0">';
        html += '<i class="fas fa-sign-in-alt"></i> تسجيل الدخول / إنشاء حساب';
        html += '</button>';
    } else {
        html += '<div class="settings-option">';
        html += '<span><i class="fas fa-user"></i> الحالة: غير مسجل</span>';
        html += '<span class="small">سجل الدخول للاستفادة من جميع الميزات</span>';
        html += '</div>';
        html += '<button class="login-btn" onclick="showLoginForm()" style="width:100%;margin:10px 0">';
        html += '<i class="fas fa-sign-in-alt"></i> تسجيل الدخول / إنشاء حساب';
        html += '</button>';
    }
    
    html += '<div class="settings-option">';
    html += '<span><i class="fas fa-moon"></i> الوضع المظلم</span>';
    html += '<label class="toggle-switch">';
    html += '<input type="checkbox" ' + (isDarkMode ? 'checked' : '') + ' onchange="toggleDarkMode()">';
    html += '<span class="slider"></span>';
    html += '</label>';
    html += '</div>';
    
    html += '<div class="settings-option">';
    html += '<span><i class="fas fa-bell"></i> الإشعارات</span>';
    html += '<label class="toggle-switch">';
    html += '<input type="checkbox" checked>';
    html += '<span class="slider"></span>';
    html += '</label>';
    html += '</div>';
    
    html += '<div class="settings-option">';
    html += '<span><i class="fas fa-video"></i> جودة الفيديو الافتراضية</span>';
    html += '<select class="quality-selector" onchange="setDefaultQuality(this.value)">';
    html += '<option value="auto">تلقائي</option>';
    html += '<option value="360">360p</option>';
    html += '<option value="480">480p</option>';
    html += '<option value="720">720p</option>';
    html += '<option value="1080">1080p</option>';
    html += '</select>';
    html += '</div>';
    
    html += '<div style="text-align:center;margin-top:20px">';
    html += '<button class="contact-btn" onclick="contactUs()" style="margin:5px">';
    html += '<i class="fas fa-envelope"></i> تواصل معنا';
    html += '</button>';
    html += '</div>';
    
    html += '<div class="note" style="text-align:center;margin-top:20px">';
    html += 'تطبيق Alhagby TV - جميع الحقوق محفوظة 2025';
    html += '</div>';
    
    html += '</div>';
    document.getElementById('mainContent').innerHTML = html;
}

function toggleDarkMode() {
    isDarkMode = !isDarkMode;
    document.body.classList.toggle('light-mode', !isDarkMode);
    const themeIcon = document.querySelector('#themeToggle i');
    if (themeIcon) {
        themeIcon.className = isDarkMode ? 'fas fa-moon' : 'fas fa-sun';
    }
    localStorage.setItem('darkMode', isDarkMode);
    
    if (currentUserData) {
        // تحديث تفضيلات المستخدم
        const userIndex = users.findIndex(u => u.id === currentUserData.id);
        if (userIndex !== -1) {
            users[userIndex].preferences.darkMode = isDarkMode;
            localStorage.setItem('alhagby_users', JSON.stringify(users));
        }
    }
}

function setDefaultQuality(quality) {
    localStorage.setItem('defaultQuality', quality);
    showNotification('تم حفظ إعدادات الجودة: ' + quality);
    
    if (currentUserData) {
        const userIndex = users.findIndex(u => u.id === currentUserData.id);
        if (userIndex !== -1) {
            users[userIndex].preferences.videoQuality = quality;
            localStorage.setItem('alhagby_users', JSON.stringify(users));
        }
    }
}

function contactUs() {
    window.location.href = 'mailto:zidanalhagby@gmail.com?subject=تواصل مع Alhagby TV';
}

// التنقل بين الأقسام
const btnCountries = document.getElementById('btnCountries');
const btnSports = document.getElementById('btnSports');
const btnBein = document.getElementById('btnBein');
const btnMatches = document.getElementById('btnMatches');
const btnSettings = document.getElementById('btnSettings');

function clearActive() {
    [btnCountries, btnSports, btnBein, btnMatches, btnSettings].forEach(b => b.classList.remove('active'));
}

btnCountries.onclick = function() {
    clearActive();
    this.classList.add('active');
    let html = '<div class="panel"><h3><i class="fas fa-globe-asia"></i>الدول العربية</h3><div class="countries-grid">';
    for (const c in countries) {
        html += '<div class="country" onclick="loadCountryChannels(\'' + c + '\')">';
        html += '<img src="https://flagcdn.com/w80/' + countryFlags[c] + '.png" onerror="this.style.display=\'none\'">';
        html += '<span>' + c + '</span>';
        html += '</div>';
    }
    html += '</div></div>';
    document.getElementById('mainContent').innerHTML = html;
};

btnSports.onclick = function() {
    clearActive();
    this.classList.add('active');
    loadAllSportsChannels();
};

btnBein.onclick = function() {
    clearActive();
    this.classList.add('active');
    loadBeinSports();
};

btnMatches.onclick = function() {
    clearActive();
    this.classList.add('active');
    loadMatches();
};

btnSettings.onclick = function() {
    clearActive();
    this.classList.add('active');
    loadSettings();
};

function loadDefaultContent() {
    let html = '<div class="panel"><h3><i class="fas fa-globe-asia"></i>الدول العربية</h3><div class="countries-grid">';
    for (const c in countries) {
        html += '<div class="country" onclick="loadCountryChannels(\'' + c + '\')">';
        html += '<img src="https://flagcdn.com/w80/' + countryFlags[c] + '.png" onerror="this.style.display=\'none\'">';
        html += '<span>' + c + '</span>';
        html += '</div>';
    }
    html += '</div></div>';
    document.getElementById('mainContent').innerHTML = html;
}

// تهيئة التطبيق
function initApp() {
    // التحقق من وجود مستخدم مسجل الدخول
    const savedUser = localStorage.getItem('alhagby_current_user') || sessionStorage.getItem('alhagby_current_user');
    const guestStatus = localStorage.getItem('alhagby_guest') === 'true';
    
    if (savedUser) {
        currentUserData = JSON.parse(savedUser);
        showMainApp();
        applyUserPreferences(currentUserData.preferences || {});
    } else if (guestStatus) {
        showMainApp();
    } else {
        document.getElementById('welcomeScreen').style.display = 'flex';
    }
    
    // تحميل الإعدادات الأخرى
    isDarkMode = localStorage.getItem('darkMode') !== 'false';
    document.body.classList.toggle('light-mode', !isDarkMode);
    
    const themeIcon = document.querySelector('#themeToggle i');
    if (themeIcon) {
        themeIcon.className = isDarkMode ? 'fas fa-moon' : 'fas fa-sun';
    }
    
    const defaultQuality = localStorage.getItem('defaultQuality') || 'auto';
    const qualitySelector = document.getElementById('qualitySelector');
    if (qualitySelector) {
        qualitySelector.value = defaultQuality;
    }
}

// بدء التطبيق
document.addEventListener('DOMContentLoaded', initApp);
</script>
</body>
</html>
