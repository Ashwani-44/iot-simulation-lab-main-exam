# ⚡ IoT Simulation Lab — Setup Guide
# Ek baar setup karein, permanent link milega!

## ════════════════════════════════════════
## STEP 1 — FIREBASE SETUP (FREE — 5 min)
## ════════════════════════════════════════

### 1.1 Firebase Account Banayein
1. https://console.firebase.google.com par jaayein
2. "Create a project" click karein
3. Project naam: "iot-simulation-lab" (kuch bhi)
4. Google Analytics: "Disable" karein → Continue

### 1.2 Realtime Database Banayein
1. Left sidebar → "Realtime Database" click karein
2. "Create Database" click karein
3. Region: "Asia Southeast (Singapore)" select karein
4. "Start in TEST MODE" select karein → Enable

### 1.3 Firebase Config Copy Karein
1. Project Settings (gear icon) → General tab
2. Scroll down → "Your apps" section
3. "</>" (Web app) icon click karein
4. App nickname: "iot-lab" → Register App
5. Ye config copy karein:

```javascript
const firebaseConfig = {
  apiKey: "AIzaSy...",
  authDomain: "iot-lab-xxxxx.firebaseapp.com",
  databaseURL: "https://iot-lab-xxxxx-default-rtdb.asia-southeast1.firebasedatabase.app",
  projectId: "iot-lab-xxxxx",
  storageBucket: "iot-lab-xxxxx.appspot.com",
  messagingSenderId: "123456789",
  appId: "1:123456789:web:abcdef"
};
```

### 1.4 Config File Mein Paste Karein
- index.html aur faculty.html dono mein
- "YOUR_API_KEY" etc. ki jagah apni values daalen
- Dono files mein SAME config daalen

## ════════════════════════════════════════
## STEP 2 — PASSWORDS SET KAREIN
## ════════════════════════════════════════

index.html aur faculty.html dono mein top par:

```javascript
const EXAM_PASSWORD    = "iot2024";    // ← Students ko yeh batayein
const LAB_NAME         = "IoT Lab — CS3A";  // ← Apna lab naam
const TEACHER_NAME     = "Prof. Sharma";     // ← Apna naam
const FACULTY_PASSWORD = "faculty@123"; // ← Sirf aapke liye (faculty dashboard)
```

## ════════════════════════════════════════
## STEP 3 — HOSTING (FREE PERMANENT LINK)
## ════════════════════════════════════════

### Option A: Netlify Drop (SABSE AASAAN — 2 min)
1. https://netlify.com/drop par jaayein
2. "iot-lab-website" folder drag karke drop karein
3. Instant link milega jaise: https://amazing-tesla-123456.netlify.app
4. Yahi link students ko share karein!

### Option B: GitHub Pages (Permanent)
1. https://github.com par free account banayein
2. New repository banayein: "iot-simulation-lab"
3. Upload karein: index.html, faculty.html
4. Settings → Pages → Source: main branch
5. Link milega: https://yourusername.github.io/iot-simulation-lab

### Option C: School Network (LAN — No Internet)
1. Ek PC par XAMPP install karein (free)
2. "htdocs" folder mein files copy karein
3. Students is PC ki IP address se access karein
   Example: http://192.168.1.5/index.html

## ════════════════════════════════════════
## STUDENT USAGE
## ════════════════════════════════════════

1. Link kholen (browser mein)
2. Naam, Roll No, aur Exam Password daalen
3. Lab start hoti hai — fullscreen mode automatic
4. Components drag & drop karein palette se
5. Code editor mein Arduino code likhein
6. ▶ Start Simulation dabayein
7. 📤 Submit button se practical submit karein

## ════════════════════════════════════════
## FACULTY USAGE
## ════════════════════════════════════════

1. Link/faculty.html kholen (same link + /faculty.html)
2. Faculty password se login karein
3. Dashboard mein sab students real-time dikhte hain:
   - Active / Blocked / Submitted status
   - Violation log (kab, kahan, kya kar raha tha)
   - Circuit components aur code dekhein
   - 🔓 Re-login allow karein blocked students ko
   - 🚫 Manually block karein
   - 📥 Student ka submitted work download karein
   - 📊 Export CSV (sab students ka record)

## ════════════════════════════════════════
## VIOLATION TRACKING — FACULTY KO KYA MILTA HAI
## ════════════════════════════════════════

Jab student tab change karta hai, faculty ko pata chalta hai:
- ⏰ Exact time (HH:MM:SS)
- 📝 Violation reason (Tab switch / Minimize / Right-click etc.)
- 🔌 Kaun kaun se components the circuit mein
- 💻 Kitni lines ka code tha
- ▶ Simulation chal raha tha ya nahi
- 📄 Last 5 lines of code (what they were doing)

## ════════════════════════════════════════
## DEFAULT PASSWORDS
## ════════════════════════════════════════

Students Exam Password : iot2024
Faculty Dashboard Password : faculty@123

(index.html aur faculty.html mein change karein)

## ════════════════════════════════════════
## FILE STRUCTURE
## ════════════════════════════════════════

iot-lab-website/
├── index.html      ← Student lab (main file)
├── faculty.html    ← Faculty dashboard
└── SETUP_GUIDE.md  ← Yeh file

Support: Dono files mein firebaseConfig aur passwords
         update karein, phir Netlify par upload karein.
