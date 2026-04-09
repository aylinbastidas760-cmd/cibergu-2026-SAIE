# MochiGo



<!DOCTYPE html>

<html lang="es">

<head>

<meta charset="UTF-8">

<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0">

<title>PetHabit – Tu compañero saludable</title>

<link href="https://fonts.googleapis.com/css2?family=Nunito:wght@400;600;700;800;900\&family=Baloo+2:wght@700;800\&display=swap" rel="stylesheet">

<style>

&#x20; :root {

&#x20;   --cream: #FFF8F0;

&#x20;   --warm: #FFF3E0;

&#x20;   --gold: #F5A623;

&#x20;   --gold-dark: #E8940F;

&#x20;   --green: #6CC04A;

&#x20;   --green-dark: #4EA832;

&#x20;   --blue: #4A90D9;

&#x20;   --blue-light: #EAF4FF;

&#x20;   --red: #FF6B6B;

&#x20;   --purple: #9B59B6;

&#x20;   --text: #3D2C1E;

&#x20;   --text-light: #7A6255;

&#x20;   --card: #FFFFFF;

&#x20;   --shadow: 0 4px 20px rgba(61,44,30,0.12);

&#x20;   --shadow-lg: 0 8px 40px rgba(61,44,30,0.18);

&#x20;   --radius: 20px;

&#x20;   --radius-sm: 12px;

&#x20; }

&#x20; \* { box-sizing: border-box; margin: 0; padding: 0; }

&#x20; body {

&#x20;   font-family: 'Nunito', sans-serif;

&#x20;   background: var(--cream);

&#x20;   color: var(--text);

&#x20;   min-height: 100vh;

&#x20;   overflow-x: hidden;

&#x20; }



&#x20; /\* ===== PHONE FRAME ===== \*/

&#x20; .phone-wrapper {

&#x20;   display: flex;

&#x20;   justify-content: center;

&#x20;   align-items: center;

&#x20;   min-height: 100vh;

&#x20;   padding: 20px;

&#x20;   background: linear-gradient(135deg, #e8f5e9 0%, #e3f2fd 50%, #fff8e1 100%);

&#x20; }

&#x20; .phone {

&#x20;   width: 390px;

&#x20;   min-height: 844px;

&#x20;   background: var(--cream);

&#x20;   border-radius: 50px;

&#x20;   box-shadow: 0 30px 80px rgba(0,0,0,0.25), inset 0 0 0 2px #e0d8d0;

&#x20;   overflow: hidden;

&#x20;   position: relative;

&#x20;   display: flex;

&#x20;   flex-direction: column;

&#x20; }



&#x20; /\* ===== SCREENS ===== \*/

&#x20; .screen {

&#x20;   display: none;

&#x20;   flex-direction: column;

&#x20;   flex: 1;

&#x20;   min-height: 844px;

&#x20; }

&#x20; .screen.active { display: flex; }



&#x20; /\* ===== SPLASH ===== \*/

&#x20; #screen-splash {

&#x20;   background: linear-gradient(160deg, #fff8f0 0%, #e8f5e9 100%);

&#x20;   align-items: center;

&#x20;   justify-content: center;

&#x20;   gap: 20px;

&#x20; }

&#x20; .splash-logo {

&#x20;   width: 140px;

&#x20;   height: 140px;

&#x20;   background: linear-gradient(135deg, #6CC04A, #4A90D9);

&#x20;   border-radius: 50%;

&#x20;   display: flex;

&#x20;   align-items: center;

&#x20;   justify-content: center;

&#x20;   font-size: 70px;

&#x20;   box-shadow: 0 12px 40px rgba(108,192,74,0.4);

&#x20;   animation: pulse-logo 2s ease-in-out infinite;

&#x20; }

&#x20; @keyframes pulse-logo { 0%,100%{transform:scale(1)} 50%{transform:scale(1.06)} }

&#x20; .splash-title {

&#x20;   font-family: 'Baloo 2', cursive;

&#x20;   font-size: 36px;

&#x20;   color: var(--text);

&#x20;   font-weight: 800;

&#x20; }

&#x20; .splash-sub { color: var(--text-light); font-size: 15px; }



&#x20; /\* ===== LOGIN ===== \*/

&#x20; #screen-login {

&#x20;   background: linear-gradient(160deg, #fff8f0 0%, #e8f5e9 100%);

&#x20;   padding: 50px 30px 30px;

&#x20;   align-items: center;

&#x20;   gap: 16px;

&#x20; }

&#x20; .login-logo {

&#x20;   width: 90px; height: 90px;

&#x20;   background: linear-gradient(135deg, #6CC04A, #4A90D9);

&#x20;   border-radius: 50%;

&#x20;   display: flex; align-items: center; justify-content: center;

&#x20;   font-size: 44px;

&#x20;   box-shadow: 0 8px 24px rgba(108,192,74,0.35);

&#x20;   margin-bottom: 8px;

&#x20; }

&#x20; .login-title { font-family: 'Baloo 2', cursive; font-size: 28px; font-weight: 800; }

&#x20; .login-sub { color: var(--text-light); font-size: 14px; margin-bottom: 8px; }

&#x20; .input-group { width: 100%; position: relative; }

&#x20; .input-group input {

&#x20;   width: 100%; padding: 14px 18px;

&#x20;   border: 2px solid #e8e0d8;

&#x20;   border-radius: var(--radius-sm);

&#x20;   font-family: 'Nunito', sans-serif;

&#x20;   font-size: 15px;

&#x20;   background: white;

&#x20;   outline: none;

&#x20;   transition: border-color 0.2s;

&#x20; }

&#x20; .input-group input:focus { border-color: var(--green); }

&#x20; .btn-primary {

&#x20;   width: 100%; padding: 14px;

&#x20;   background: linear-gradient(135deg, #6CC04A, #4EA832);

&#x20;   color: white; border: none;

&#x20;   border-radius: var(--radius-sm);

&#x20;   font-family: 'Nunito', sans-serif;

&#x20;   font-size: 16px; font-weight: 800;

&#x20;   cursor: pointer;

&#x20;   box-shadow: 0 4px 16px rgba(108,192,74,0.4);

&#x20;   transition: transform 0.15s, box-shadow 0.15s;

&#x20; }

&#x20; .btn-primary:active { transform: scale(0.97); }

&#x20; .btn-google {

&#x20;   width: 100%; padding: 13px;

&#x20;   background: white;

&#x20;   border: 2px solid #e8e0d8;

&#x20;   border-radius: var(--radius-sm);

&#x20;   font-family: 'Nunito', sans-serif;

&#x20;   font-size: 15px; font-weight: 700;

&#x20;   cursor: pointer; display: flex;

&#x20;   align-items: center; justify-content: center; gap: 10px;

&#x20;   color: var(--text);

&#x20;   transition: background 0.2s;

&#x20; }

&#x20; .btn-google:hover { background: #f9f9f9; }

&#x20; .divider { display: flex; align-items: center; gap: 10px; width: 100%; }

&#x20; .divider span { color: var(--text-light); font-size: 13px; white-space: nowrap; }

&#x20; .divider::before, .divider::after { content: ''; flex: 1; height: 1px; background: #e8e0d8; }

&#x20; .link-btn { background: none; border: none; color: var(--blue); font-family: 'Nunito', sans-serif; font-size: 14px; cursor: pointer; text-decoration: underline; }



&#x20; /\* ===== ONBOARDING ===== \*/

&#x20; .onboard-header {

&#x20;   background: linear-gradient(135deg, #6CC04A, #4A90D9);

&#x20;   padding: 60px 30px 30px;

&#x20;   color: white;

&#x20;   text-align: center;

&#x20; }

&#x20; .onboard-header h2 { font-family: 'Baloo 2', cursive; font-size: 24px; font-weight: 800; }

&#x20; .onboard-header p { font-size: 14px; opacity: 0.9; margin-top: 4px; }

&#x20; .progress-dots { display: flex; gap: 8px; justify-content: center; margin-top: 16px; }

&#x20; .dot { width: 8px; height: 8px; border-radius: 50%; background: rgba(255,255,255,0.4); transition: all 0.3s; }

&#x20; .dot.active { background: white; width: 24px; border-radius: 4px; }

&#x20; .onboard-body { padding: 24px 24px; flex: 1; overflow-y: auto; }

&#x20; .option-card {

&#x20;   background: white; border: 2px solid #e8e0d8;

&#x20;   border-radius: var(--radius); padding: 16px 20px;

&#x20;   cursor: pointer; transition: all 0.2s;

&#x20;   display: flex; align-items: center; gap: 14px;

&#x20;   margin-bottom: 12px;

&#x20; }

&#x20; .option-card:hover, .option-card.selected { border-color: var(--green); background: #f0fff4; }

&#x20; .option-card .opt-icon { font-size: 32px; }

&#x20; .option-card .opt-text h4 { font-size: 15px; font-weight: 800; }

&#x20; .option-card .opt-text p { font-size: 12px; color: var(--text-light); }

&#x20; .pet-option-card {

&#x20;   background: white; border: 3px solid #e8e0d8;

&#x20;   border-radius: var(--radius); padding: 20px;

&#x20;   cursor: pointer; transition: all 0.2s;

&#x20;   display: flex; flex-direction: column; align-items: center; gap: 8px;

&#x20;   flex: 1;

&#x20; }

&#x20; .pet-option-card:hover, .pet-option-card.selected { border-color: var(--gold); background: #fffbf0; transform: translateY(-4px); box-shadow: var(--shadow); }

&#x20; .pet-options-row { display: flex; gap: 12px; }

&#x20; .pet-emoji { font-size: 50px; }

&#x20; .pet-name { font-weight: 800; font-size: 14px; }

&#x20; .number-input-row { display: flex; gap: 12px; }

&#x20; .num-group { flex: 1; }

&#x20; .num-group label { font-size: 12px; font-weight: 700; color: var(--text-light); display: block; margin-bottom: 6px; }

&#x20; .num-group input {

&#x20;   width: 100%; padding: 12px 14px;

&#x20;   border: 2px solid #e8e0d8; border-radius: var(--radius-sm);

&#x20;   font-family: 'Nunito', sans-serif; font-size: 16px; font-weight: 700;

&#x20;   text-align: center; outline: none;

&#x20; }

&#x20; .num-group input:focus { border-color: var(--green); }

&#x20; .gender-row { display: flex; gap: 10px; }

&#x20; .gender-btn {

&#x20;   flex: 1; padding: 12px 8px;

&#x20;   background: white; border: 2px solid #e8e0d8;

&#x20;   border-radius: var(--radius-sm);

&#x20;   font-family: 'Nunito', sans-serif; font-size: 14px; font-weight: 700;

&#x20;   cursor: pointer; transition: all 0.2s; text-align: center;

&#x20; }

&#x20; .gender-btn.selected { border-color: var(--blue); background: var(--blue-light); color: var(--blue); }

&#x20; .section-title { font-family: 'Baloo 2', cursive; font-size: 18px; font-weight: 700; margin-bottom: 16px; color: var(--text); }

&#x20; .check-row { display: flex; gap: 10px; flex-wrap: wrap; }

&#x20; .check-tag {

&#x20;   padding: 8px 16px; background: white;

&#x20;   border: 2px solid #e8e0d8; border-radius: 100px;

&#x20;   font-size: 13px; font-weight: 700; cursor: pointer;

&#x20;   transition: all 0.2s;

&#x20; }

&#x20; .check-tag.selected { border-color: var(--green); background: #f0fff4; color: var(--green-dark); }



&#x20; /\* ===== HOME ===== \*/

&#x20; #screen-home {

&#x20;   display: none; flex-direction: column;

&#x20;   background: var(--cream);

&#x20; }

&#x20; #screen-home.active { display: flex; }



&#x20; .home-header {

&#x20;   background: linear-gradient(160deg, #e8f5f0 0%, #ddeeff 100%);

&#x20;   padding: 50px 20px 20px;

&#x20;   position: relative;

&#x20; }

&#x20; .home-top-row { display: flex; justify-content: space-between; align-items: center; }

&#x20; .coins-badge {

&#x20;   background: var(--gold);

&#x20;   border-radius: 100px;

&#x20;   padding: 6px 14px;

&#x20;   display: flex; align-items: center; gap: 6px;

&#x20;   font-weight: 800; font-size: 15px; color: white;

&#x20;   box-shadow: 0 3px 12px rgba(245,166,35,0.4);

&#x20; }

&#x20; .profile-btn {

&#x20;   width: 46px; height: 46px;

&#x20;   border-radius: 50%;

&#x20;   background: linear-gradient(135deg, #6CC04A, #4A90D9);

&#x20;   border: 3px solid white;

&#x20;   display: flex; align-items: center; justify-content: center;

&#x20;   font-size: 22px;

&#x20;   cursor: pointer; box-shadow: var(--shadow);

&#x20;   position: relative;

&#x20; }

&#x20; .progress-label { font-size: 12px; color: var(--text-light); margin-top: 12px; font-weight: 700; }

&#x20; .prog-bar-wrap { background: rgba(0,0,0,0.08); border-radius: 100px; height: 10px; margin-top: 6px; overflow: hidden; }

&#x20; .prog-bar-fill { height: 100%; background: linear-gradient(90deg, #6CC04A, #F5A623); border-radius: 100px; transition: width 0.8s ease; }



&#x20; .pet-stage {

&#x20;   flex: 1;

&#x20;   display: flex; align-items: center; justify-content: center;

&#x20;   position: relative; overflow: hidden;

&#x20;   min-height: 280px;

&#x20; }

&#x20; .pet-display {

&#x20;   font-size: 130px;

&#x20;   animation: pet-idle 3s ease-in-out infinite;

&#x20;   transition: all 0.5s ease;

&#x20;   filter: drop-shadow(0 12px 24px rgba(0,0,0,0.15));

&#x20;   cursor: default;

&#x20;   user-select: none;

&#x20; }

&#x20; @keyframes pet-idle { 0%,100%{transform:translateY(0) rotate(-2deg)} 50%{transform:translateY(-12px) rotate(2deg)} }

&#x20; .pet-display.happy { animation: pet-happy 0.6s ease infinite; }

&#x20; @keyframes pet-happy { 0%,100%{transform:translateY(0) scale(1)} 25%{transform:translateY(-20px) scale(1.1) rotate(-5deg)} 75%{transform:translateY(-10px) scale(1.05) rotate(5deg)} }

&#x20; .pet-display.sad { animation: pet-sad 2s ease infinite; filter: drop-shadow(0 12px 24px rgba(0,0,0,0.1)) grayscale(0.3); }

&#x20; @keyframes pet-sad { 0%,100%{transform:translateY(0)} 50%{transform:translateY(4px)} }

&#x20; .emotion-bubble {

&#x20;   position: absolute; top: 20px; right: 30px;

&#x20;   background: white; border-radius: 16px;

&#x20;   padding: 8px 14px; font-size: 13px; font-weight: 700;

&#x20;   box-shadow: var(--shadow);

&#x20;   animation: bubble-in 0.4s ease;

&#x20; }

&#x20; @keyframes bubble-in { from{opacity:0;transform:scale(0.7)} to{opacity:1;transform:scale(1)} }

&#x20; .emotion-bubble::after {

&#x20;   content: ''; position: absolute; bottom: -8px; left: 20px;

&#x20;   border-left: 8px solid transparent;

&#x20;   border-right: 8px solid transparent;

&#x20;   border-top: 8px solid white;

&#x20; }

&#x20; .rain-effect {

&#x20;   position: absolute; top: 0; left: 0; right: 0; bottom: 0;

&#x20;   pointer-events: none; overflow: hidden;

&#x20; }

&#x20; .raindrop {

&#x20;   position: absolute; width: 2px; height: 12px;

&#x20;   background: linear-gradient(to bottom, transparent, #90caf9);

&#x20;   border-radius: 2px; animation: rain-fall linear infinite;

&#x20; }

&#x20; @keyframes rain-fall { 0%{top:-20px;opacity:0.7} 100%{top:110%;opacity:0} }



&#x20; /\* ===== BOTTOM NAV ===== \*/

&#x20; .bottom-nav {

&#x20;   background: white;

&#x20;   border-top: 1px solid #f0ebe4;

&#x20;   display: flex;

&#x20;   padding: 10px 0 20px;

&#x20; }

&#x20; .nav-item {

&#x20;   flex: 1; display: flex; flex-direction: column;

&#x20;   align-items: center; gap: 4px;

&#x20;   cursor: pointer; padding: 6px;

&#x20;   transition: all 0.2s;

&#x20; }

&#x20; .nav-icon { font-size: 24px; }

&#x20; .nav-label { font-size: 11px; font-weight: 700; color: var(--text-light); }

&#x20; .nav-item.active .nav-label { color: var(--green); }

&#x20; .nav-item.active .nav-icon { transform: scale(1.2); }



&#x20; /\* ===== RETOS SCREEN ===== \*/

&#x20; #screen-retos {

&#x20;   display: none; flex-direction: column;

&#x20;   background: var(--cream);

&#x20; }

&#x20; #screen-retos.active { display: flex; }

&#x20; .retos-header {

&#x20;   background: linear-gradient(135deg, #6CC04A, #4A90D9);

&#x20;   padding: 55px 20px 24px; color: white;

&#x20; }

&#x20; .retos-header h2 { font-family: 'Baloo 2', cursive; font-size: 22px; font-weight: 800; }

&#x20; .streak-row { display: flex; align-items: center; gap: 12px; margin-top: 10px; }

&#x20; .streak-badge {

&#x20;   background: rgba(255,255,255,0.25); border-radius: 100px;

&#x20;   padding: 5px 12px; font-size: 13px; font-weight: 700;

&#x20;   backdrop-filter: blur(4px);

&#x20; }

&#x20; .bonus-badge {

&#x20;   background: var(--gold); border-radius: 100px;

&#x20;   padding: 5px 12px; font-size: 13px; font-weight: 700;

&#x20;   color: white;

&#x20; }

&#x20; .retos-body { flex: 1; overflow-y: auto; padding: 16px; }

&#x20; .reto-card {

&#x20;   background: white; border-radius: var(--radius);

&#x20;   padding: 16px; margin-bottom: 12px;

&#x20;   box-shadow: var(--shadow);

&#x20;   transition: transform 0.2s;

&#x20; }

&#x20; .reto-card:active { transform: scale(0.98); }

&#x20; .reto-top { display: flex; align-items: center; gap: 12px; margin-bottom: 10px; }

&#x20; .reto-icon { font-size: 28px; }

&#x20; .reto-info { flex: 1; }

&#x20; .reto-info h4 { font-size: 15px; font-weight: 800; }

&#x20; .reto-info p { font-size: 12px; color: var(--text-light); }

&#x20; .reto-pts {

&#x20;   background: var(--gold); color: white;

&#x20;   border-radius: 100px; padding: 5px 12px;

&#x20;   font-size: 13px; font-weight: 800;

&#x20; }

&#x20; .reto-pts.done { background: var(--green); }

&#x20; .reto-progress-bar { background: #f0ebe4; border-radius: 100px; height: 8px; overflow: hidden; }

&#x20; .reto-progress-fill { height: 100%; background: linear-gradient(90deg, #6CC04A, #4A90D9); border-radius: 100px; transition: width 0.5s; }

&#x20; .reto-actions { display: flex; gap: 8px; margin-top: 10px; }

&#x20; .btn-complete {

&#x20;   flex: 1; padding: 10px;

&#x20;   background: linear-gradient(135deg, #6CC04A, #4EA832);

&#x20;   color: white; border: none; border-radius: var(--radius-sm);

&#x20;   font-family: 'Nunito', sans-serif; font-size: 13px; font-weight: 700;

&#x20;   cursor: pointer;

&#x20; }

&#x20; .btn-complete:disabled { background: #ccc; cursor: not-allowed; }

&#x20; .btn-photo {

&#x20;   width: 42px; height: 42px;

&#x20;   background: var(--blue-light); border: 2px solid var(--blue);

&#x20;   border-radius: var(--radius-sm); cursor: pointer;

&#x20;   display: flex; align-items: center; justify-content: center;

&#x20;   font-size: 18px;

&#x20; }

&#x20; .btn-star {

&#x20;   width: 42px; height: 42px;

&#x20;   background: #fff8e1; border: 2px solid var(--gold);

&#x20;   border-radius: var(--radius-sm); cursor: pointer;

&#x20;   display: flex; align-items: center; justify-content: center;

&#x20;   font-size: 18px; position: relative;

&#x20; }

&#x20; .soon-badge {

&#x20;   position: absolute; top: -6px; right: -6px;

&#x20;   background: var(--red); color: white;

&#x20;   border-radius: 50%; width: 16px; height: 16px;

&#x20;   font-size: 10px; font-weight: 800;

&#x20;   display: flex; align-items: center; justify-content: center;

&#x20; }

&#x20; .points-today-card {

&#x20;   background: linear-gradient(135deg, #fff8e1, #fff3cd);

&#x20;   border-radius: var(--radius); padding: 16px;

&#x20;   text-align: center; margin-bottom: 12px;

&#x20;   border: 2px solid #f5a62344;

&#x20; }

&#x20; .points-today-card .pts-num { font-family: 'Baloo 2', cursive; font-size: 32px; color: var(--gold-dark); font-weight: 800; }

&#x20; .points-today-card .pts-label { font-size: 13px; color: var(--text-light); }

&#x20; .pts-sub { font-size: 12px; color: var(--text-light); margin-top: 4px; }



&#x20; /\* ===== PROFILE POPUP ===== \*/

&#x20; .overlay {

&#x20;   display: none; position: absolute; top: 0; left: 0; right: 0; bottom: 0;

&#x20;   background: rgba(0,0,0,0.4); z-index: 100;

&#x20;   justify-content: flex-end; align-items: flex-start;

&#x20;   padding: 100px 16px 0;

&#x20; }

&#x20; .overlay.active { display: flex; }

&#x20; .profile-popup {

&#x20;   background: white; border-radius: var(--radius);

&#x20;   padding: 20px; width: 260px;

&#x20;   box-shadow: var(--shadow-lg);

&#x20;   animation: pop-in 0.3s ease;

&#x20; }

&#x20; @keyframes pop-in { from{opacity:0;transform:scale(0.9) translateY(-10px)} to{opacity:1;transform:scale(1) translateY(0)} }

&#x20; .popup-user { display: flex; align-items: center; gap: 12px; margin-bottom: 16px; }

&#x20; .popup-avatar { width: 48px; height: 48px; border-radius: 50%; background: linear-gradient(135deg, #6CC04A, #4A90D9); display: flex; align-items: center; justify-content: center; font-size: 24px; }

&#x20; .popup-name { font-weight: 800; font-size: 15px; }

&#x20; .popup-plan { font-size: 12px; color: var(--text-light); }

&#x20; .popup-divider { height: 1px; background: #f0ebe4; margin: 12px 0; }

&#x20; .popup-item {

&#x20;   display: flex; align-items: center; gap: 10px;

&#x20;   padding: 10px 8px; border-radius: var(--radius-sm);

&#x20;   cursor: pointer; transition: background 0.15s;

&#x20;   font-size: 14px; font-weight: 700;

&#x20; }

&#x20; .popup-item:hover { background: #f9f5f0; }

&#x20; .popup-item span { font-size: 20px; }

&#x20; .vol-row { display: flex; align-items: center; gap: 8px; }

&#x20; .vol-row input\[type=range] { flex: 1; }



&#x20; /\* ===== PLANS SCREEN ===== \*/

&#x20; .plans-overlay {

&#x20;   display: none; position: absolute; top: 0; left: 0; right: 0; bottom: 0;

&#x20;   background: rgba(0,0,0,0.5); z-index: 200;

&#x20;   align-items: flex-end;

&#x20; }

&#x20; .plans-overlay.active { display: flex; }

&#x20; .plans-sheet {

&#x20;   background: white; border-radius: 30px 30px 0 0;

&#x20;   padding: 24px 20px 30px; width: 100%;

&#x20;   max-height: 85vh; overflow-y: auto;

&#x20;   animation: sheet-up 0.35s ease;

&#x20; }

&#x20; @keyframes sheet-up { from{transform:translateY(100%)} to{transform:translateY(0)} }

&#x20; .plans-sheet h3 { font-family: 'Baloo 2', cursive; font-size: 22px; text-align: center; margin-bottom: 20px; }

&#x20; .plan-card {

&#x20;   border: 2px solid #e8e0d8; border-radius: var(--radius);

&#x20;   padding: 18px; margin-bottom: 12px;

&#x20;   cursor: pointer; transition: all 0.2s;

&#x20; }

&#x20; .plan-card.featured { border-color: var(--gold); background: linear-gradient(135deg, #fffbf0, #fff8e1); }

&#x20; .plan-card.premium { border-color: var(--purple); background: linear-gradient(135deg, #fdf8ff, #f5eeff); }

&#x20; .plan-header { display: flex; justify-content: space-between; align-items: center; margin-bottom: 10px; }

&#x20; .plan-name { font-family: 'Baloo 2', cursive; font-size: 18px; font-weight: 700; }

&#x20; .plan-price { font-weight: 800; font-size: 16px; }

&#x20; .plan-price.gold { color: var(--gold-dark); }

&#x20; .plan-price.purple { color: var(--purple); }

&#x20; .plan-features { list-style: none; }

&#x20; .plan-features li { font-size: 13px; color: var(--text-light); padding: 3px 0; }

&#x20; .plan-features li::before { content: '✓ '; color: var(--green); font-weight: 800; }

&#x20; .btn-select-plan {

&#x20;   width: 100%; padding: 13px;

&#x20;   border: none; border-radius: var(--radius-sm);

&#x20;   font-family: 'Nunito', sans-serif; font-size: 15px; font-weight: 800;

&#x20;   cursor: pointer; margin-top: 10px;

&#x20; }

&#x20; .btn-select-plan.gold { background: var(--gold); color: white; }

&#x20; .btn-select-plan.purple { background: var(--purple); color: white; }

&#x20; .btn-close-plans {

&#x20;   width: 100%; padding: 12px;

&#x20;   background: #f5f0ea; border: none; border-radius: var(--radius-sm);

&#x20;   font-family: 'Nunito', sans-serif; font-size: 14px; font-weight: 700;

&#x20;   cursor: pointer; margin-top: 4px;

&#x20; }



&#x20; /\* ===== SUCCESS/FAIL MODAL ===== \*/

&#x20; .result-overlay {

&#x20;   display: none; position: absolute; top: 0; left: 0; right: 0; bottom: 0;

&#x20;   background: rgba(0,0,0,0.5); z-index: 300;

&#x20;   align-items: center; justify-content: center; padding: 20px;

&#x20; }

&#x20; .result-overlay.active { display: flex; }

&#x20; .result-card {

&#x20;   background: white; border-radius: 30px; padding: 30px;

&#x20;   text-align: center; width: 100%;

&#x20;   box-shadow: var(--shadow-lg);

&#x20;   animation: pop-in 0.4s ease;

&#x20; }

&#x20; .result-banner {

&#x20;   background: var(--gold); color: white;

&#x20;   border-radius: 100px; padding: 10px 24px;

&#x20;   font-family: 'Baloo 2', cursive; font-size: 20px; font-weight: 800;

&#x20;   display: inline-block; margin-bottom: 16px;

&#x20; }

&#x20; .result-banner.sad { background: #7f8c8d; }

&#x20; .result-pet { font-size: 80px; margin: 10px 0; animation: pet-happy 0.6s ease infinite; }

&#x20; .result-pet.sad { animation: pet-sad 2s ease infinite; }

&#x20; .result-pts { background: var(--gold); color: white; border-radius: 100px; padding: 10px 28px; font-family: 'Baloo 2', cursive; font-size: 24px; font-weight: 800; display: inline-block; margin: 12px 0; }

&#x20; .result-pts.sad { background: #95a5a6; }

&#x20; .result-msg { font-size: 14px; color: var(--text-light); margin: 8px 0; }

&#x20; .btn-result { background: var(--green); color: white; border: none; border-radius: var(--radius-sm); padding: 13px 32px; font-family: 'Nunito', sans-serif; font-size: 15px; font-weight: 800; cursor: pointer; margin-top: 12px; }



&#x20; /\* ===== PHOTO UPLOAD MODAL ===== \*/

&#x20; .photo-overlay {

&#x20;   display: none; position: absolute; top: 0; left: 0; right: 0; bottom: 0;

&#x20;   background: rgba(0,0,0,0.5); z-index: 400;

&#x20;   align-items: flex-end;

&#x20; }

&#x20; .photo-overlay.active { display: flex; }

&#x20; .photo-sheet {

&#x20;   background: white; border-radius: 30px 30px 0 0;

&#x20;   padding: 24px 20px 30px; width: 100%;

&#x20;   animation: sheet-up 0.3s ease;

&#x20; }

&#x20; .photo-sheet h4 { font-family: 'Baloo 2', cursive; font-size: 18px; margin-bottom: 8px; }

&#x20; .photo-sheet p { font-size: 13px; color: var(--text-light); margin-bottom: 16px; }

&#x20; .photo-preview {

&#x20;   border: 3px dashed #d0c8c0; border-radius: var(--radius);

&#x20;   height: 150px; display: flex; flex-direction: column;

&#x20;   align-items: center; justify-content: center; cursor: pointer;

&#x20;   background: #faf7f4; margin-bottom: 16px;

&#x20;   transition: border-color 0.2s;

&#x20; }

&#x20; .photo-preview:hover { border-color: var(--blue); }

&#x20; .photo-preview img { max-width: 100%; max-height: 140px; border-radius: 10px; display: none; }

&#x20; .photo-preview .upload-icon { font-size: 36px; }

&#x20; .photo-preview .upload-text { font-size: 13px; color: var(--text-light); margin-top: 6px; }

&#x20; .btn-verify { width: 100%; padding: 13px; background: var(--blue); color: white; border: none; border-radius: var(--radius-sm); font-family: 'Nunito', sans-serif; font-size: 15px; font-weight: 800; cursor: pointer; }

&#x20; .btn-cancel { width: 100%; padding: 12px; background: #f5f0ea; border: none; border-radius: var(--radius-sm); font-family: 'Nunito', sans-serif; font-size: 14px; font-weight: 700; cursor: pointer; margin-top: 8px; }



&#x20; /\* ===== TOAST ===== \*/

&#x20; .toast {

&#x20;   position: absolute; bottom: 100px; left: 50%; transform: translateX(-50%) translateY(20px);

&#x20;   background: #2d3436; color: white; border-radius: 100px;

&#x20;   padding: 10px 24px; font-size: 14px; font-weight: 700;

&#x20;   z-index: 500; opacity: 0; transition: all 0.3s;

&#x20;   white-space: nowrap;

&#x20; }

&#x20; .toast.show { opacity: 1; transform: translateX(-50%) translateY(0); }



&#x20; /\* ===== RESPONSIVE ===== \*/

&#x20; @media(max-width:430px) {

&#x20;   .phone-wrapper { padding: 0; background: var(--cream); }

&#x20;   .phone { width: 100vw; border-radius: 0; min-height: 100vh; box-shadow: none; }

&#x20;   .screen { min-height: 100vh; }

&#x20; }



&#x20; /\* Scrollbar \*/

&#x20; ::-webkit-scrollbar { width: 4px; }

&#x20; ::-webkit-scrollbar-track { background: transparent; }

&#x20; ::-webkit-scrollbar-thumb { background: #d0c8c0; border-radius: 2px; }

</style>

</head>

<body>

<div class="phone-wrapper">

<div class="phone" id="app">



&#x20; <!-- SPLASH -->

&#x20; <div class="screen active" id="screen-splash">

&#x20;   <div class="splash-logo">🐾</div>

&#x20;   <div class="splash-title">PetHabit</div>

&#x20;   <div class="splash-sub">Tu compañero de hábitos saludables</div>

&#x20; </div>



&#x20; <!-- LOGIN -->

&#x20; <div class="screen" id="screen-login">

&#x20;   <div class="login-logo">🐾</div>

&#x20;   <div class="login-title">¡Bienvenido/a!</div>

&#x20;   <div class="login-sub">Inicia sesión o crea tu cuenta</div>

&#x20;   <div class="input-group"><input type="text" id="login-user" placeholder="Nombre de usuario" /></div>

&#x20;   <div class="input-group"><input type="email" id="login-email" placeholder="Correo electrónico" /></div>

&#x20;   <div class="input-group"><input type="password" id="login-pass" placeholder="Contraseña" /></div>

&#x20;   <button class="btn-primary" onclick="doLogin()">Iniciar sesión / Registrarse</button>

&#x20;   <div class="divider"><span>o continúa con</span></div>

&#x20;   <button class="btn-google" onclick="doGoogleLogin()">

&#x20;     <svg width="20" height="20" viewBox="0 0 48 48"><path fill="#EA4335" d="M24 9.5c3.54 0 6.71 1.22 9.21 3.6l6.85-6.85C35.9 2.38 30.47 0 24 0 14.62 0 6.51 5.38 2.56 13.22l7.98 6.19C12.43 13.72 17.74 9.5 24 9.5z"/><path fill="#4285F4" d="M46.98 24.55c0-1.57-.15-3.09-.38-4.55H24v9.02h12.94c-.58 2.96-2.26 5.48-4.78 7.18l7.73 6c4.51-4.18 7.09-10.36 7.09-17.65z"/><path fill="#FBBC05" d="M10.53 28.59c-.48-1.45-.76-2.99-.76-4.59s.27-3.14.76-4.59l-7.98-6.19C.92 16.46 0 20.12 0 24c0 3.88.92 7.54 2.56 10.78l7.97-6.19z"/><path fill="#34A853" d="M24 48c6.48 0 11.93-2.13 15.89-5.81l-7.73-6c-2.18 1.48-4.97 2.35-8.16 2.35-6.26 0-11.57-4.22-13.47-9.91l-7.98 6.19C6.51 42.62 14.62 48 24 48z"/></svg>

&#x20;     Continuar con Google

&#x20;   </button>

&#x20;   <button class="link-btn" onclick="showToast('Usa el mismo formulario para registrarte 😊')">¿No tienes cuenta? Regístrate</button>

&#x20; </div>



&#x20; <!-- ONBOARD 1: Mascota -->

&#x20; <div class="screen" id="screen-onboard1">

&#x20;   <div class="onboard-header">

&#x20;     <h2>Elige tu mascota 🐾</h2>

&#x20;     <p>Será tu compañero de hábitos diarios</p>

&#x20;     <div class="progress-dots">

&#x20;       <div class="dot active"></div><div class="dot"></div><div class="dot"></div><div class="dot"></div>

&#x20;     </div>

&#x20;   </div>

&#x20;   <div class="onboard-body">

&#x20;     <div class="pet-options-row">

&#x20;       <div class="pet-option-card" onclick="selectPet('🐶','Perro')" id="pet-dog">

&#x20;         <div class="pet-emoji">🐶</div>

&#x20;         <div class="pet-name">Perro</div>

&#x20;         <div style="font-size:11px;color:var(--text-light)">Fiel y activo</div>

&#x20;       </div>

&#x20;       <div class="pet-option-card" onclick="selectPet('🐱','Gato')" id="pet-cat">

&#x20;         <div class="pet-emoji">🐱</div>

&#x20;         <div class="pet-name">Gato</div>

&#x20;         <div style="font-size:11px;color:var(--text-light)">Elegante y listo</div>

&#x20;       </div>

&#x20;       <div class="pet-option-card" onclick="selectPet('🦦','Nutria')" id="pet-otter">

&#x20;         <div class="pet-emoji">🦦</div>

&#x20;         <div class="pet-name">Nutria</div>

&#x20;         <div style="font-size:11px;color:var(--text-light)">Juguetona y lista</div>

&#x20;       </div>

&#x20;     </div>

&#x20;     <div style="margin-top:20px">

&#x20;       <div class="section-title">¿Cuántos años tienes?</div>

&#x20;       <div class="number-input-row">

&#x20;         <div class="num-group"><label>Edad</label><input type="number" id="age" placeholder="25" min="5" max="100"></div>

&#x20;         <div class="num-group"><label>Altura (cm)</label><input type="number" id="height" placeholder="170" min="100" max="250"></div>

&#x20;         <div class="num-group"><label>Peso (kg)</label><input type="number" id="weight" placeholder="70" min="20" max="300"></div>

&#x20;       </div>

&#x20;       <div class="section-title" style="margin-top:16px">Género</div>

&#x20;       <div class="gender-row">

&#x20;         <button class="gender-btn" onclick="selectGender(this,'Masculino')">♂ Masculino</button>

&#x20;         <button class="gender-btn" onclick="selectGender(this,'Femenino')">♀ Femenino</button>

&#x20;         <button class="gender-btn" onclick="selectGender(this,'Otro')">⚧ Otro</button>

&#x20;       </div>

&#x20;     </div>

&#x20;     <button class="btn-primary" style="margin-top:20px" onclick="goOnboard2()">Continuar →</button>

&#x20;   </div>

&#x20; </div>



&#x20; <!-- ONBOARD 2: Objetivo -->

&#x20; <div class="screen" id="screen-onboard2">

&#x20;   <div class="onboard-header">

&#x20;     <h2>¿Cuál es tu objetivo? 🎯</h2>

&#x20;     <p>Personalizaremos tus retos diarios</p>

&#x20;     <div class="progress-dots">

&#x20;       <div class="dot"></div><div class="dot active"></div><div class="dot"></div><div class="dot"></div>

&#x20;     </div>

&#x20;   </div>

&#x20;   <div class="onboard-body">

&#x20;     <div class="option-card" onclick="toggleGoal(this,'salud')" data-goal="salud">

&#x20;       <div class="opt-icon">⚖️</div>

&#x20;       <div class="opt-text"><h4>Adelgazar</h4><p>Perder peso de forma saludable</p></div>

&#x20;     </div>

&#x20;     <div class="option-card" onclick="toggleGoal(this,'musculo')" data-goal="musculo">

&#x20;       <div class="opt-icon">💪</div>

&#x20;       <div class="opt-text"><h4>Ganar músculo</h4><p>Aumentar masa muscular</p></div>

&#x20;     </div>

&#x20;     <div class="option-card" onclick="toggleGoal(this,'tonificar')" data-goal="tonificar">

&#x20;       <div class="opt-icon">🏃</div>

&#x20;       <div class="opt-text"><h4>Tonificar</h4><p>Definir y tonificar el cuerpo</p></div>

&#x20;     </div>

&#x20;     <div class="option-card" onclick="toggleGoal(this,'estudios')" data-goal="estudios">

&#x20;       <div class="opt-icon">📚</div>

&#x20;       <div class="opt-text"><h4>Mejorar estudios</h4><p>Hábitos académicos y concentración</p></div>

&#x20;     </div>

&#x20;     <div class="option-card" onclick="toggleGoal(this,'bienestar')" data-goal="bienestar">

&#x20;       <div class="opt-icon">🧘</div>

&#x20;       <div class="opt-text"><h4>Bienestar general</h4><p>Hábitos de vida saludable</p></div>

&#x20;     </div>

&#x20;     <button class="btn-primary" style="margin-top:8px" onclick="goOnboard3()">Continuar →</button>

&#x20;   </div>

&#x20; </div>



&#x20; <!-- ONBOARD 3: Asignaturas (si estudios) / Actividad -->

&#x20; <div class="screen" id="screen-onboard3">

&#x20;   <div class="onboard-header">

&#x20;     <h2>Cuéntanos más 📋</h2>

&#x20;     <p>Para personalizar mejor tus retos</p>

&#x20;     <div class="progress-dots">

&#x20;       <div class="dot"></div><div class="dot"></div><div class="dot active"></div><div class="dot"></div>

&#x20;     </div>

&#x20;   </div>

&#x20;   <div class="onboard-body" id="onboard3-body">

&#x20;   </div>

&#x20; </div>



&#x20; <!-- ONBOARD 4: Listo -->

&#x20; <div class="screen" id="screen-onboard4">

&#x20;   <div class="onboard-header" style="text-align:center">

&#x20;     <h2>¡Todo listo! 🎉</h2>

&#x20;     <p>Tu compañero está esperándote</p>

&#x20;     <div class="progress-dots">

&#x20;       <div class="dot"></div><div class="dot"></div><div class="dot"></div><div class="dot active"></div>

&#x20;     </div>

&#x20;   </div>

&#x20;   <div class="onboard-body" style="display:flex;flex-direction:column;align-items:center;justify-content:center;gap:16px;text-align:center;">

&#x20;     <div style="font-size:90px" id="onboard-pet-preview">🐶</div>

&#x20;     <div style="font-family:'Baloo 2',cursive;font-size:20px;font-weight:800" id="onboard-pet-msg">¡Tu perro te está esperando!</div>

&#x20;     <div style="font-size:14px;color:var(--text-light)">Completa tus retos diarios para mantenerlo feliz y ganar puntos ⭐</div>

&#x20;     <button class="btn-primary" style="width:100%;margin-top:8px" onclick="startApp()">¡Empezar! 🚀</button>

&#x20;   </div>

&#x20; </div>



&#x20; <!-- HOME -->

&#x20; <div class="screen" id="screen-home">

&#x20;   <div class="home-header">

&#x20;     <div class="home-top-row">

&#x20;       <div class="coins-badge">🪙 <span id="coins-display">0</span> ⭐</div>

&#x20;       <div class="profile-btn" onclick="toggleProfile()" id="profile-btn">🐾</div>

&#x20;     </div>

&#x20;     <div class="progress-label">Tu progreso hoy: <span id="progress-text">0/100 pts</span></div>

&#x20;     <div class="prog-bar-wrap"><div class="prog-bar-fill" id="home-prog" style="width:0%"></div></div>

&#x20;   </div>



&#x20;   <div class="pet-stage">

&#x20;     <div class="rain-effect" id="rain-effect" style="display:none"></div>

&#x20;     <div class="pet-display" id="pet-display">🐶</div>

&#x20;     <div class="emotion-bubble" id="emotion-bubble">¡Hola! 👋</div>

&#x20;   </div>



&#x20;   <div style="background:white;padding:16px 20px;border-top:1px solid #f0ebe4">

&#x20;     <div style="display:flex;justify-content:space-between;align-items:center">

&#x20;       <div style="font-size:13px;font-weight:700;color:var(--text-light)">🔥 Racha: <span id="streak-display">0</span> días</div>

&#x20;       <div style="font-size:13px;font-weight:700;color:var(--text-light)">⭐ Bonus: <span id="bonus-display">No disponible</span></div>

&#x20;     </div>

&#x20;     <div style="font-size:12px;color:var(--text-light);margin-top:6px" id="bonus-msg">Completa todos los retos para ganar bonus</div>

&#x20;   </div>



&#x20;   <div class="bottom-nav">

&#x20;     <div class="nav-item active" onclick="showTab('home')">

&#x20;       <div class="nav-icon">🏠</div><div class="nav-label">Inicio</div>

&#x20;     </div>

&#x20;     <div class="nav-item" onclick="showTab('retos')">

&#x20;       <div class="nav-icon">⚡</div><div class="nav-label">Retos</div>

&#x20;     </div>

&#x20;     <div class="nav-item" onclick="showTab('stats')">

&#x20;       <div class="nav-icon">📊</div><div class="nav-label">Progreso</div>

&#x20;     </div>

&#x20;   </div>

&#x20; </div>



&#x20; <!-- RETOS -->

&#x20; <div class="screen" id="screen-retos">

&#x20;   <div class="retos-header">

&#x20;     <h2>⚡ Retos diarios</h2>

&#x20;     <div class="streak-row">

&#x20;       <div class="streak-badge">🔥 <span id="streak-retos">0</span> días</div>

&#x20;       <div class="bonus-badge" id="bonus-retos-badge">⭐ Bonus disponible</div>

&#x20;     </div>

&#x20;   </div>



&#x20;   <div class="retos-body">

&#x20;     <div class="points-today-card">

&#x20;       <div class="pts-num"><span id="pts-today">0</span>/100</div>

&#x20;       <div class="pts-label">Puntos hoy</div>

&#x20;       <div class="pts-sub" id="retos-left-msg">Te faltan <strong id="retos-left">3</strong> retos para el bonus</div>

&#x20;     </div>

&#x20;     <div id="retos-list"></div>

&#x20;   </div>



&#x20;   <div class="bottom-nav">

&#x20;     <div class="nav-item" onclick="showTab('home')">

&#x20;       <div class="nav-icon">🏠</div><div class="nav-label">Inicio</div>

&#x20;     </div>

&#x20;     <div class="nav-item active" onclick="showTab('retos')">

&#x20;       <div class="nav-icon">⚡</div><div class="nav-label">Retos</div>

&#x20;     </div>

&#x20;     <div class="nav-item" onclick="showTab('stats')">

&#x20;       <div class="nav-icon">📊</div><div class="nav-label">Progreso</div>

&#x20;     </div>

&#x20;   </div>

&#x20; </div>



&#x20; <!-- STATS -->

&#x20; <div class="screen" id="screen-stats">

&#x20;   <div class="retos-header">

&#x20;     <h2>📊 Tu progreso</h2>

&#x20;     <div class="streak-row">

&#x20;       <div class="streak-badge">🔥 <span id="streak-stats">0</span> días</div>

&#x20;     </div>

&#x20;   </div>

&#x20;   <div class="retos-body">

&#x20;     <div class="points-today-card">

&#x20;       <div style="font-size:14px;font-weight:700;color:var(--text-light);margin-bottom:4px">Total de monedas</div>

&#x20;       <div class="pts-num">🪙 <span id="total-coins-stats">0</span></div>

&#x20;     </div>

&#x20;     <div class="reto-card">

&#x20;       <h4 style="font-size:14px;font-weight:800;margin-bottom:12px">📅 Últimos 7 días</h4>

&#x20;       <div id="week-chart" style="display:flex;align-items:flex-end;gap:6px;height:80px"></div>

&#x20;       <div style="display:flex;gap:6px;margin-top:4px" id="week-labels"></div>

&#x20;     </div>

&#x20;     <div class="reto-card" id="stats-goal-card">

&#x20;       <h4 style="font-size:14px;font-weight:800;margin-bottom:8px">🎯 Tu objetivo</h4>

&#x20;       <div id="stats-goal" style="font-size:13px;color:var(--text-light)">Sin objetivo seleccionado</div>

&#x20;     </div>

&#x20;   </div>

&#x20;   <div class="bottom-nav">

&#x20;     <div class="nav-item" onclick="showTab('home')">

&#x20;       <div class="nav-icon">🏠</div><div class="nav-label">Inicio</div>

&#x20;     </div>

&#x20;     <div class="nav-item" onclick="showTab('retos')">

&#x20;       <div class="nav-icon">⚡</div><div class="nav-label">Retos</div>

&#x20;     </div>

&#x20;     <div class="nav-item active" onclick="showTab('stats')">

&#x20;       <div class="nav-icon">📊</div><div class="nav-label">Progreso</div>

&#x20;     </div>

&#x20;   </div>

&#x20; </div>



&#x20; <!-- PROFILE POPUP -->

&#x20; <div class="overlay" id="profile-overlay" onclick="closeProfile(event)">

&#x20;   <div class="profile-popup">

&#x20;     <div class="popup-user">

&#x20;       <div class="popup-avatar" id="popup-avatar">🐾</div>

&#x20;       <div>

&#x20;         <div class="popup-name" id="popup-username">Usuario</div>

&#x20;         <div class="popup-plan" id="popup-plan">Plan Gratuito</div>

&#x20;       </div>

&#x20;     </div>

&#x20;     <div class="popup-divider"></div>

&#x20;     <div class="popup-item">

&#x20;       <span>🔊</span>

&#x20;       <div style="flex:1">

&#x20;         <div style="font-size:13px;font-weight:800;margin-bottom:4px">Volumen</div>

&#x20;         <div class="vol-row"><input type="range" min="0" max="100" value="70" oninput="updateVol(this.value)"></div>

&#x20;       </div>

&#x20;     </div>

&#x20;     <div class="popup-item" onclick="showPlans()">

&#x20;       <span>⬆️</span>

&#x20;       <div>

&#x20;         <div style="font-size:13px;font-weight:800">Mejorar tu plan</div>

&#x20;         <div style="font-size:11px;color:var(--text-light)">Plus · Premium</div>

&#x20;       </div>

&#x20;     </div>

&#x20;     <div class="popup-item">

&#x20;       <span>🔔</span>

&#x20;       <div style="font-size:13px;font-weight:800">Notificaciones</div>

&#x20;     </div>

&#x20;     <div class="popup-item">

&#x20;       <span>🌙</span>

&#x20;       <div style="font-size:13px;font-weight:800">Modo oscuro</div>

&#x20;     </div>

&#x20;     <div class="popup-divider"></div>

&#x20;     <div class="popup-item" onclick="doLogout()">

&#x20;       <span>🚪</span>

&#x20;       <div style="font-size:13px;font-weight:800;color:var(--red)">Cerrar sesión</div>

&#x20;     </div>

&#x20;   </div>

&#x20; </div>



&#x20; <!-- PLANS OVERLAY -->

&#x20; <div class="plans-overlay" id="plans-overlay" onclick="closePlansIfBg(event)">

&#x20;   <div class="plans-sheet">

&#x20;     <h3>⬆️ Mejorar tu plan</h3>

&#x20;     <div class="plan-card">

&#x20;       <div class="plan-header">

&#x20;         <div class="plan-name">🆓 Plan Gratuito</div>

&#x20;         <div class="plan-price">Gratis</div>

&#x20;       </div>

&#x20;       <ul class="plan-features">

&#x20;         <li>Contiene anuncios</li>

&#x20;         <li>Hasta 3 retos diarios</li>

&#x20;         <li>Retos básicos personalizados</li>

&#x20;         <li>Recompensas limitadas</li>

&#x20;       </ul>

&#x20;     </div>

&#x20;     <div class="plan-card featured">

&#x20;       <div class="plan-header">

&#x20;         <div class="plan-name" style="color:var(--gold-dark)">⭐ Plan Plus</div>

&#x20;         <div class="plan-price gold">4,99 €/mes</div>

&#x20;       </div>

&#x20;       <ul class="plan-features">

&#x20;         <li>Sin anuncios</li>

&#x20;         <li>Hasta 6 retos diarios</li>

&#x20;         <li>Acceso a más mascotas</li>

&#x20;         <li>Más monedas y recompensas</li>

&#x20;         <li>Seguimiento completo del progreso</li>

&#x20;         <li>Plan válido hasta 6 meses</li>

&#x20;         <li>Gimnasios recomendados</li>

&#x20;       </ul>

&#x20;       <button class="btn-select-plan gold" onclick="selectPlan('Plus');closePlans()">Elegir Plan Plus →</button>

&#x20;     </div>

&#x20;     <div class="plan-card premium">

&#x20;       <div class="plan-header">

&#x20;         <div class="plan-name" style="color:var(--purple)">💎 Plan Premium</div>

&#x20;         <div class="plan-price purple">8,99 €/mes</div>

&#x20;       </div>

&#x20;       <ul class="plan-features">

&#x20;         <li>Sin anuncios</li>

&#x20;         <li>Hasta 10 retos diarios</li>

&#x20;         <li>Acceso a más mascotas</li>

&#x20;         <li>Recompensas exclusivas</li>

&#x20;         <li>Seguimiento completo del progreso</li>

&#x20;         <li>Plan válido hasta 1 año y medio</li>

&#x20;         <li>Descuentos en gimnasios</li>

&#x20;         <li>Consejos de nutricionistas</li>

&#x20;       </ul>

&#x20;       <button class="btn-select-plan purple" onclick="selectPlan('Premium');closePlans()">Elegir Plan Premium →</button>

&#x20;     </div>

&#x20;     <button class="btn-close-plans" onclick="closePlans()">Cerrar</button>

&#x20;   </div>

&#x20; </div>



&#x20; <!-- RESULT OVERLAY -->

&#x20; <div class="result-overlay" id="result-overlay">

&#x20;   <div class="result-card" id="result-card">

&#x20;     <div class="result-banner" id="result-banner">¡Retos completos!</div>

&#x20;     <div class="result-pet" id="result-pet">🐶</div>

&#x20;     <div class="result-pts" id="result-pts">100 pts</div>

&#x20;     <div class="result-msg" id="result-msg">Has completado todos los retos de hoy 🎉</div>

&#x20;     <div style="background:#f9f5f0;border-radius:var(--radius-sm);padding:12px;margin-top:8px;font-size:13px;color:var(--text-light)" id="result-check"></div>

&#x20;     <button class="btn-result" onclick="closeResult()">¡Genial!</button>

&#x20;   </div>

&#x20; </div>



&#x20; <!-- PHOTO OVERLAY -->

&#x20; <div class="photo-overlay" id="photo-overlay">

&#x20;   <div class="photo-sheet">

&#x20;     <h4>📸 Verificar reto con foto</h4>

&#x20;     <p id="photo-reto-name">Sube una foto para verificar tu reto</p>

&#x20;     <div class="photo-preview" id="photo-preview-box" onclick="triggerUpload()">

&#x20;       <div class="upload-icon">📷</div>

&#x20;       <div class="upload-text">Toca para subir una foto</div>

&#x20;       <img id="photo-preview-img" />

&#x20;     </div>

&#x20;     <input type="file" id="photo-file-input" accept="image/\*" style="display:none" onchange="handlePhotoUpload(this)">

&#x20;     <button class="btn-verify" onclick="verifyPhoto()">✓ Verificar y completar reto</button>

&#x20;     <button class="btn-cancel" onclick="closePhoto()">Cancelar</button>

&#x20;   </div>

&#x20; </div>



&#x20; <!-- TOAST -->

&#x20; <div class="toast" id="toast"></div>



</div><!-- /phone -->

</div><!-- /wrapper -->



<script>

// ===== STATE =====

let state = {

&#x20; loggedIn: false,

&#x20; username: '',

&#x20; email: '',

&#x20; pet: '🐶',

&#x20; petName: 'Perro',

&#x20; age: 25, height: 170, weight: 70,

&#x20; gender: 'Masculino',

&#x20; goals: \[],

&#x20; subjects: \[],

&#x20; actLevel: 'moderado',

&#x20; coins: 0,

&#x20; streak: 0,

&#x20; dailyPts: 0,

&#x20; plan: 'Gratuito',

&#x20; retos: \[],

&#x20; completedDays: \[],

&#x20; photoTarget: null,

&#x20; currentTab: 'home',

&#x20; weekData: \[0,0,0,0,0,0,0],

};



const RETOS\_BY\_GOAL = {

&#x20; salud: \[

&#x20;   {id:'s1', name:'Comer saludable', desc:'Prepara una comida con verduras', icon:'🥗', pts:10, needPhoto:true},

&#x20;   {id:'s2', name:'Beber agua', desc:'Bebe 2L de agua hoy', icon:'💧', pts:5, needPhoto:false},

&#x20;   {id:'s3', name:'Ejercicio', desc:'30 min de actividad física', icon:'🏋️', pts:20, needPhoto:true},

&#x20;   {id:'s4', name:'Dormir bien', desc:'8 horas de sueño', icon:'😴', pts:10, needPhoto:false},

&#x20;   {id:'s5', name:'Sin azúcar', desc:'Evita azúcar procesada hoy', icon:'🚫🍬', pts:15, needPhoto:false},

&#x20; ],

&#x20; musculo: \[

&#x20;   {id:'m1', name:'Entrenamiento fuerza', desc:'Haz 3 series de ejercicios de fuerza', icon:'💪', pts:20, needPhoto:true},

&#x20;   {id:'m2', name:'Proteína', desc:'Come proteína en cada comida', icon:'🥩', pts:10, needPhoto:true},

&#x20;   {id:'m3', name:'Beber agua', desc:'Bebe 3L de agua hoy', icon:'💧', pts:5, needPhoto:false},

&#x20;   {id:'m4', name:'Descanso activo', desc:'Stretching 15 minutos', icon:'🧘', pts:10, needPhoto:false},

&#x20;   {id:'m5', name:'Sin alcohol', desc:'Evita el alcohol hoy', icon:'🚫🍺', pts:15, needPhoto:false},

&#x20; ],

&#x20; tonificar: \[

&#x20;   {id:'t1', name:'Cardio', desc:'30 min de cardio moderado', icon:'🏃', pts:20, needPhoto:true},

&#x20;   {id:'t2', name:'Hidratación', desc:'Bebe 2L de agua', icon:'💧', pts:5, needPhoto:false},

&#x20;   {id:'t3', name:'Comida ligera', desc:'Come ligero y saludable', icon:'🥙', pts:10, needPhoto:true},

&#x20;   {id:'t4', name:'Abdominales', desc:'3 series de 20 abdominales', icon:'🔥', pts:15, needPhoto:false},

&#x20;   {id:'t5', name:'Pasos diarios', desc:'Camina 8000 pasos', icon:'👟', pts:10, needPhoto:false},

&#x20; ],

&#x20; estudios: \[

&#x20;   {id:'e1', name:'Estudiar 1h', desc:'Estudia durante 1 hora seguida', icon:'📚', pts:15, needPhoto:false},

&#x20;   {id:'e2', name:'Apuntes', desc:'Repasa tus apuntes de hoy', icon:'📝', pts:10, needPhoto:true},

&#x20;   {id:'e3', name:'Sin móvil', desc:'1 hora sin redes sociales', icon:'📵', pts:10, needPhoto:false},

&#x20;   {id:'e4', name:'Ejercicio mental', desc:'Haz un ejercicio de tu asignatura', icon:'🧠', pts:20, needPhoto:true},

&#x20;   {id:'e5', name:'Lectura', desc:'Lee 20 páginas de tu libro de texto', icon:'📖', pts:10, needPhoto:false},

&#x20; ],

&#x20; bienestar: \[

&#x20;   {id:'b1', name:'Meditación', desc:'10 minutos de meditación', icon:'🧘', pts:10, needPhoto:false},

&#x20;   {id:'b2', name:'Hidratación', desc:'Bebe 2L de agua', icon:'💧', pts:5, needPhoto:false},

&#x20;   {id:'b3', name:'Aire libre', desc:'30 min al aire libre', icon:'🌳', pts:15, needPhoto:true},

&#x20;   {id:'b4', name:'Comida sana', desc:'Prepara una comida equilibrada', icon:'🥗', pts:10, needPhoto:true},

&#x20;   {id:'b5', name:'Gratitud', desc:'Escribe 3 cosas por las que estás agradecido', icon:'💛', pts:10, needPhoto:false},

&#x20; ],

};



const PET\_NAMES = { '🐶':'perro', '🐱':'gato', '🦦':'nutria' };



// Load from localStorage

function loadState() {

&#x20; const saved = localStorage.getItem('pethabit\_state');

&#x20; if (saved) {

&#x20;   const parsed = JSON.parse(saved);

&#x20;   Object.assign(state, parsed);

&#x20;   resetDailyIfNeeded();

&#x20; }

}

function saveState() {

&#x20; localStorage.setItem('pethabit\_state', JSON.stringify(state));

}

function resetDailyIfNeeded() {

&#x20; const today = new Date().toDateString();

&#x20; if (state.lastDay !== today) {

&#x20;   // Check if yesterday was completed

&#x20;   const yesterday = new Date();

&#x20;   yesterday.setDate(yesterday.getDate() - 1);

&#x20;   const wasYesterday = state.lastDay === yesterday.toDateString();

&#x20;   const wasCompleted = state.completedDays \&\& state.completedDays.includes(state.lastDay);

&#x20;   if (!wasCompleted \&\& state.lastDay) {

&#x20;     state.streak = 0;

&#x20;   }

&#x20;   // Reset daily

&#x20;   state.lastDay = today;

&#x20;   state.dailyPts = 0;

&#x20;   state.retos = state.retos.map(r => ({...r, done: false, progress: 0}));

&#x20;   // Update week data

&#x20;   if (!state.weekData) state.weekData = \[0,0,0,0,0,0,0];

&#x20;   state.weekData.shift();

&#x20;   state.weekData.push(0);

&#x20;   saveState();

&#x20; }

}



// ===== INIT =====

window.onload = function() {

&#x20; loadState();

&#x20; setTimeout(() => {

&#x20;   if (state.loggedIn) {

&#x20;     generateRetosIfNeeded();

&#x20;     showScreen('screen-home');

&#x20;     updateHomeUI();

&#x20;   } else {

&#x20;     showScreen('screen-login');

&#x20;   }

&#x20; }, 1800);

};



function showScreen(id) {

&#x20; document.querySelectorAll('.screen').forEach(s => s.classList.remove('active'));

&#x20; document.getElementById(id).classList.add('active');

}



// ===== LOGIN =====

function doLogin() {

&#x20; const user = document.getElementById('login-user').value.trim();

&#x20; const email = document.getElementById('login-email').value.trim();

&#x20; const pass = document.getElementById('login-pass').value.trim();

&#x20; if (!user || !email || !pass) { showToast('Por favor rellena todos los campos'); return; }

&#x20; state.username = user;

&#x20; state.email = email;

&#x20; if (state.loggedIn) {

&#x20;   generateRetosIfNeeded();

&#x20;   showScreen('screen-home');

&#x20;   updateHomeUI();

&#x20; } else {

&#x20;   showScreen('screen-onboard1');

&#x20; }

}

function doGoogleLogin() {

&#x20; state.username = 'Usuario Google';

&#x20; state.email = 'google@pethabit.app';

&#x20; if (state.loggedIn) {

&#x20;   generateRetosIfNeeded();

&#x20;   showScreen('screen-home');

&#x20;   updateHomeUI();

&#x20; } else {

&#x20;   showScreen('screen-onboard1');

&#x20; }

}

function doLogout() {

&#x20; state.loggedIn = false;

&#x20; saveState();

&#x20; closeProfile2();

&#x20; showScreen('screen-login');

}



// ===== ONBOARDING =====

function selectPet(emoji, name) {

&#x20; state.pet = emoji;

&#x20; state.petName = name;

&#x20; document.querySelectorAll('.pet-option-card').forEach(c => c.classList.remove('selected'));

&#x20; const map = {'🐶':'pet-dog','🐱':'pet-cat','🦦':'pet-otter'};

&#x20; document.getElementById(map\[emoji]).classList.add('selected');

}

function selectGender(btn, g) {

&#x20; state.gender = g;

&#x20; document.querySelectorAll('.gender-btn').forEach(b => b.classList.remove('selected'));

&#x20; btn.classList.add('selected');

}

function toggleGoal(el, g) {

&#x20; el.classList.toggle('selected');

&#x20; if (state.goals.includes(g)) state.goals = state.goals.filter(x => x !== g);

&#x20; else state.goals.push(g);

}

function goOnboard2() {

&#x20; state.age = parseInt(document.getElementById('age').value) || 25;

&#x20; state.height = parseInt(document.getElementById('height').value) || 170;

&#x20; state.weight = parseInt(document.getElementById('weight').value) || 70;

&#x20; showScreen('screen-onboard2');

}

function goOnboard3() {

&#x20; if (state.goals.length === 0) { showToast('Selecciona al menos un objetivo'); return; }

&#x20; const body = document.getElementById('onboard3-body');

&#x20; if (state.goals.includes('estudios')) {

&#x20;   body.innerHTML = `

&#x20;     <div class="section-title">📚 ¿Qué asignaturas tienes?</div>

&#x20;     <p style="font-size:13px;color:var(--text-light);margin-bottom:12px">Selecciona tus asignaturas actuales</p>

&#x20;     <div class="check-row" id="subjects-row">

&#x20;       ${\['Matemáticas','Física','Química','Historia','Inglés','Literatura','Biología','Filosofía','Arte','Economía'].map(s =>

&#x20;         `<div class="check-tag" onclick="toggleSubject(this,'${s}')">${s}</div>`

&#x20;       ).join('')}

&#x20;     </div>

&#x20;     <div class="section-title" style="margin-top:20px">⚡ Nivel de actividad</div>

&#x20;     <div class="option-card" onclick="selectActivity(this,'sedentario')" data-act="sedentario"><div class="opt-icon">🪑</div><div class="opt-text"><h4>Sedentario</h4><p>Poco o nada de ejercicio</p></div></div>

&#x20;     <div class="option-card" onclick="selectActivity(this,'moderado')" data-act="moderado"><div class="opt-icon">🚶</div><div class="opt-text"><h4>Moderado</h4><p>Ejercicio 2-3 veces/semana</p></div></div>

&#x20;     <div class="option-card" onclick="selectActivity(this,'activo')" data-act="activo"><div class="opt-icon">🏃</div><div class="opt-text"><h4>Activo</h4><p>Ejercicio 4-5 veces/semana</p></div></div>

&#x20;     <button class="btn-primary" style="margin-top:16px" onclick="goOnboard4()">Continuar →</button>`;

&#x20; } else {

&#x20;   body.innerHTML = `

&#x20;     <div class="section-title">⚡ Nivel de actividad física</div>

&#x20;     <div class="option-card" onclick="selectActivity(this,'sedentario')" data-act="sedentario"><div class="opt-icon">🪑</div><div class="opt-text"><h4>Sedentario</h4><p>Poco o nada de ejercicio</p></div></div>

&#x20;     <div class="option-card" onclick="selectActivity(this,'moderado')" data-act="moderado"><div class="opt-icon">🚶</div><div class="opt-text"><h4>Moderado</h4><p>Ejercicio 2-3 veces/semana</p></div></div>

&#x20;     <div class="option-card" onclick="selectActivity(this,'activo')" data-act="activo"><div class="opt-icon">🏃</div><div class="opt-text"><h4>Activo</h4><p>Ejercicio 4-5 veces/semana</p></div></div>

&#x20;     <div class="section-title" style="margin-top:20px">🕐 ¿A qué hora prefieres hacer los retos?</div>

&#x20;     <div class="check-row">

&#x20;       <div class="check-tag" onclick="toggleCheck(this,'Mañana')">🌅 Mañana</div>

&#x20;       <div class="check-tag" onclick="toggleCheck(this,'Tarde')">☀️ Tarde</div>

&#x20;       <div class="check-tag" onclick="toggleCheck(this,'Noche')">🌙 Noche</div>

&#x20;     </div>

&#x20;     <button class="btn-primary" style="margin-top:24px" onclick="goOnboard4()">Continuar →</button>`;

&#x20; }

&#x20; showScreen('screen-onboard3');

}

function toggleSubject(el, s) {

&#x20; el.classList.toggle('selected');

&#x20; if (state.subjects.includes(s)) state.subjects = state.subjects.filter(x=>x!==s);

&#x20; else state.subjects.push(s);

}

function selectActivity(el, a) {

&#x20; state.actLevel = a;

&#x20; document.querySelectorAll('\[data-act]').forEach(c => c.classList.remove('selected'));

&#x20; el.classList.add('selected');

}

function toggleCheck(el, v) { el.classList.toggle('selected'); }

function goOnboard4() {

&#x20; const petMsg = {'🐶':'¡Tu perro te está esperando!','🐱':'¡Tu gato te está esperando!','🦦':'¡Tu nutria te está esperando!'};

&#x20; document.getElementById('onboard-pet-preview').textContent = state.pet;

&#x20; document.getElementById('onboard-pet-msg').textContent = petMsg\[state.pet] || '¡Tu mascota te espera!';

&#x20; showScreen('screen-onboard4');

}

function startApp() {

&#x20; state.loggedIn = true;

&#x20; state.lastDay = new Date().toDateString();

&#x20; state.weekData = \[0,0,0,0,0,0,0];

&#x20; generateRetos();

&#x20; saveState();

&#x20; showScreen('screen-home');

&#x20; updateHomeUI();

}



// ===== RETO GENERATION =====

function generateRetosIfNeeded() {

&#x20; if (!state.retos || state.retos.length === 0) generateRetos();

}

function generateRetos() {

&#x20; const goal = state.goals\[0] || 'bienestar';

&#x20; const pool = RETOS\_BY\_GOAL\[goal] || RETOS\_BY\_GOAL.bienestar;

&#x20; const limit = state.plan === 'Premium' ? 10 : state.plan === 'Plus' ? 6 : 3;

&#x20; const shuffled = \[...pool].sort(() => Math.random() - 0.5);

&#x20; state.retos = shuffled.slice(0, Math.min(limit, pool.length)).map(r => ({...r, done: false, progress: 0}));

}



// ===== HOME UI =====

function updateHomeUI() {

&#x20; const pet = state.pet;

&#x20; document.getElementById('pet-display').textContent = pet;

&#x20; document.getElementById('coins-display').textContent = state.coins;

&#x20; document.getElementById('streak-display').textContent = state.streak;

&#x20; document.getElementById('streak-retos').textContent = state.streak;

&#x20; document.getElementById('streak-stats').textContent = state.streak;



&#x20; const total = state.retos.reduce((s,r) => s + r.pts, 0) || 100;

&#x20; const pct = Math.min(100, (state.dailyPts / total) \* 100);

&#x20; document.getElementById('home-prog').style.width = pct + '%';

&#x20; document.getElementById('progress-text').textContent = state.dailyPts + '/' + total + ' pts';

&#x20; document.getElementById('pts-today').textContent = state.dailyPts;



&#x20; const done = state.retos.filter(r => r.done).length;

&#x20; const left = state.retos.length - done;

&#x20; document.getElementById('retos-left').textContent = left;

&#x20; document.getElementById('retos-left-msg').innerHTML = left > 0

&#x20;   ? `Te faltan <strong>${left}</strong> reto${left!==1?'s':''} para el bonus`

&#x20;   : '🎉 ¡Todos los retos completados!';



&#x20; // Emotion

&#x20; const petEl = document.getElementById('pet-display');

&#x20; const bubbleEl = document.getElementById('emotion-bubble');

&#x20; const rainEl = document.getElementById('rain-effect');

&#x20; const allDone = done === state.retos.length \&\& state.retos.length > 0;

&#x20; const noneDone = done === 0;



&#x20; petEl.className = 'pet-display';

&#x20; if (allDone) {

&#x20;   petEl.classList.add('happy');

&#x20;   bubbleEl.textContent = '¡Soy muy feliz! 🎉';

&#x20;   rainEl.style.display = 'none';

&#x20; } else if (noneDone \&\& state.retos.length > 0) {

&#x20;   petEl.classList.add('sad');

&#x20;   bubbleEl.textContent = '¡Ánimo, puedes hacerlo! 💪';

&#x20;   setupRain();

&#x20;   rainEl.style.display = 'block';

&#x20; } else {

&#x20;   bubbleEl.textContent = '¡Vamos por más! ⚡';

&#x20;   rainEl.style.display = 'none';

&#x20; }



&#x20; const bonusAvail = allDone;

&#x20; document.getElementById('bonus-display').textContent = bonusAvail ? '¡Disponible!' : 'No disponible';

&#x20; document.getElementById('bonus-retos-badge').style.display = bonusAvail ? 'block' : 'none';

&#x20; document.getElementById('bonus-msg').textContent = bonusAvail

&#x20;   ? '🎁 ¡Bonus desbloqueado! +50 monedas extras'

&#x20;   : `Completa todos los retos y gana bonus`;



&#x20; // Profile popup

&#x20; document.getElementById('popup-username').textContent = state.username;

&#x20; document.getElementById('popup-plan').textContent = 'Plan ' + state.plan;

&#x20; document.getElementById('popup-avatar').textContent = state.pet;



&#x20; renderRetosList();

&#x20; renderStatsUI();

}

function setupRain() {

&#x20; const rain = document.getElementById('rain-effect');

&#x20; if (rain.children.length > 0) return;

&#x20; for (let i = 0; i < 20; i++) {

&#x20;   const drop = document.createElement('div');

&#x20;   drop.className = 'raindrop';

&#x20;   drop.style.left = Math.random()\*100+'%';

&#x20;   drop.style.animationDuration = (0.7 + Math.random()\*0.8)+'s';

&#x20;   drop.style.animationDelay = (Math.random()\*1.5)+'s';

&#x20;   rain.appendChild(drop);

&#x20; }

}



// ===== RETOS LIST =====

function renderRetosList() {

&#x20; const list = document.getElementById('retos-list');

&#x20; if (!list) return;

&#x20; list.innerHTML = '';

&#x20; state.retos.forEach((reto, idx) => {

&#x20;   const pct = reto.done ? 100 : 0;

&#x20;   list.innerHTML += `

&#x20;   <div class="reto-card" id="reto-${idx}">

&#x20;     <div class="reto-top">

&#x20;       <div class="reto-icon">${reto.icon}</div>

&#x20;       <div class="reto-info">

&#x20;         <h4>${reto.name}</h4>

&#x20;         <p>${reto.desc}</p>

&#x20;       </div>

&#x20;       <div class="reto-pts ${reto.done?'done':''}">+${reto.pts}pts ${reto.done?'✓':'⏳'}</div>

&#x20;     </div>

&#x20;     <div class="reto-progress-bar"><div class="reto-progress-fill" style="width:${pct}%"></div></div>

&#x20;     <div class="reto-actions">

&#x20;       <button class="btn-complete" ${reto.done?'disabled':''} onclick="completeReto(${idx})">

&#x20;         ${reto.done ? '✓ Completado' : 'Marcar completado'}

&#x20;       </button>

&#x20;       ${reto.needPhoto ? `<div class="btn-photo" onclick="openPhoto(${idx})" title="Verificar con foto">📷</div>` : ''}

&#x20;       <div class="btn-star" title="Próximamente">⭐<div class="soon-badge">?</div></div>

&#x20;     </div>

&#x20;   </div>`;

&#x20; });

}

function completeReto(idx) {

&#x20; if (state.retos\[idx].done) return;

&#x20; state.retos\[idx].done = true;

&#x20; state.dailyPts += state.retos\[idx].pts;

&#x20; state.coins += state.retos\[idx].pts;

&#x20; const allDone = state.retos.every(r => r.done);

&#x20; if (allDone) {

&#x20;   state.streak++;

&#x20;   state.coins += 50;

&#x20;   state.weekData\[6] = state.dailyPts;

&#x20;   if (!state.completedDays) state.completedDays = \[];

&#x20;   state.completedDays.push(new Date().toDateString());

&#x20;   saveState();

&#x20;   updateHomeUI();

&#x20;   setTimeout(() => showResult(true), 400);

&#x20; } else {

&#x20;   saveState();

&#x20;   updateHomeUI();

&#x20;   showToast('+' + state.retos\[idx].pts + ' pts ganados! 🎉');

&#x20; }

}



// ===== PHOTO =====

function openPhoto(idx) {

&#x20; state.photoTarget = idx;

&#x20; document.getElementById('photo-reto-name').textContent = 'Sube una foto para: ' + state.retos\[idx].name;

&#x20; document.getElementById('photo-preview-img').style.display = 'none';

&#x20; document.getElementById('photo-file-input').value = '';

&#x20; document.getElementById('photo-overlay').classList.add('active');

}

function closePhoto() { document.getElementById('photo-overlay').classList.remove('active'); }

function triggerUpload() { document.getElementById('photo-file-input').click(); }

function handlePhotoUpload(input) {

&#x20; if (input.files \&\& input.files\[0]) {

&#x20;   const reader = new FileReader();

&#x20;   reader.onload = e => {

&#x20;     const img = document.getElementById('photo-preview-img');

&#x20;     img.src = e.target.result;

&#x20;     img.style.display = 'block';

&#x20;     document.querySelector('#photo-preview-box .upload-icon').style.display = 'none';

&#x20;     document.querySelector('#photo-preview-box .upload-text').style.display = 'none';

&#x20;   };

&#x20;   reader.readAsDataURL(input.files\[0]);

&#x20; }

}

function verifyPhoto() {

&#x20; const img = document.getElementById('photo-preview-img');

&#x20; if (!img.src || img.src === window.location.href) { showToast('Por favor sube una foto primero'); return; }

&#x20; closePhoto();

&#x20; showToast('📸 Foto verificada correctamente');

&#x20; if (state.photoTarget !== null) {

&#x20;   setTimeout(() => completeReto(state.photoTarget), 600);

&#x20;   state.photoTarget = null;

&#x20; }

}



// ===== RESULT =====

function showResult(success) {

&#x20; const overlay = document.getElementById('result-overlay');

&#x20; document.getElementById('result-banner').textContent = success ? '¡Retos completos! 🎉' : 'Retos incompletos';

&#x20; document.getElementById('result-banner').className = 'result-banner' + (success ? '' : ' sad');

&#x20; document.getElementById('result-pet').textContent = state.pet;

&#x20; document.getElementById('result-pet').className = 'result-pet' + (success ? '' : ' sad');

&#x20; document.getElementById('result-pts').textContent = success ? '100 pts' : state.dailyPts + '/100 puntos';

&#x20; document.getElementById('result-pts').className = 'result-pts' + (success ? '' : ' sad');

&#x20; document.getElementById('result-msg').textContent = success

&#x20;   ? `¡Felicitaciones! Has completado todos los retos 🐾`

&#x20;   : 'No completaste los retos de hoy...';

&#x20; document.getElementById('result-check').innerHTML = success

&#x20;   ? '✅ Todos los retos completados'

&#x20;   : '😞 Hoy no lograste completar todos los retos y perdiste la racha.';

&#x20; overlay.classList.add('active');

}

function closeResult() { document.getElementById('result-overlay').classList.remove('active'); }



// ===== TABS =====

function showTab(tab) {

&#x20; state.currentTab = tab;

&#x20; document.querySelectorAll('.screen').forEach(s => s.classList.remove('active'));

&#x20; const map = {home:'screen-home', retos:'screen-retos', stats:'screen-stats'};

&#x20; document.getElementById(map\[tab]).classList.add('active');

&#x20; if (tab === 'retos') renderRetosList();

&#x20; if (tab === 'stats') renderStatsUI();

}



// ===== STATS =====

function renderStatsUI() {

&#x20; document.getElementById('total-coins-stats').textContent = state.coins;

&#x20; document.getElementById('streak-stats').textContent = state.streak;

&#x20; // Week chart

&#x20; const chart = document.getElementById('week-chart');

&#x20; const labels = document.getElementById('week-labels');

&#x20; if (!chart) return;

&#x20; const days = \['L','M','X','J','V','S','D'];

&#x20; const data = state.weekData || \[0,0,0,0,0,0,0];

&#x20; const max = Math.max(...data, 1);

&#x20; chart.innerHTML = '';

&#x20; labels.innerHTML = '';

&#x20; data.forEach((v, i) => {

&#x20;   const h = Math.max(4, (v/max)\*72);

&#x20;   chart.innerHTML += `<div style="flex:1;display:flex;align-items:flex-end;justify-content:center">

&#x20;     <div style="width:100%;height:${h}px;background:${i===6?'linear-gradient(to top,#6CC04A,#4A90D9)':'#e8e0d8'};border-radius:4px 4px 0 0"></div></div>`;

&#x20;   labels.innerHTML += `<div style="flex:1;text-align:center;font-size:11px;color:var(--text-light);font-weight:700">${days\[i]}</div>`;

&#x20; });

&#x20; // Goal

&#x20; const goalMap = {salud:'⚖️ Adelgazar',musculo:'💪 Ganar músculo',tonificar:'🏃 Tonificar',estudios:'📚 Estudios',bienestar:'🧘 Bienestar'};

&#x20; const goalText = state.goals.map(g => goalMap\[g]).filter(Boolean).join(', ') || 'Sin objetivo';

&#x20; document.getElementById('stats-goal').textContent = goalText;

}



// ===== PROFILE =====

function toggleProfile() { document.getElementById('profile-overlay').classList.toggle('active'); }

function closeProfile(e) { if (e.target === document.getElementById('profile-overlay')) closeProfile2(); }

function closeProfile2() { document.getElementById('profile-overlay').classList.remove('active'); }



// ===== PLANS =====

function showPlans() { closeProfile2(); document.getElementById('plans-overlay').classList.add('active'); }

function closePlans() { document.getElementById('plans-overlay').classList.remove('active'); }

function closePlansIfBg(e) { if (e.target === document.getElementById('plans-overlay')) closePlans(); }

function selectPlan(plan) {

&#x20; state.plan = plan;

&#x20; generateRetos();

&#x20; saveState();

&#x20; showToast('✅ Plan ' + plan + ' activado');

&#x20; updateHomeUI();

}



// ===== VOL =====

function updateVol(v) { showToast('Volumen: ' + v + '%'); }



// ===== TOAST =====

function showToast(msg) {

&#x20; const t = document.getElementById('toast');

&#x20; t.textContent = msg;

&#x20; t.classList.add('show');

&#x20; setTimeout(() => t.classList.remove('show'), 2500);

}

</script>

</body>

</html>

