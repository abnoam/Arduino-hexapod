# 🤖 Arduino Hexapod Robot

## Overview

פרוייקט כיתה יב של נועם ויוסי - הקספוד המונע על ידי Arduino Mega ונשלט באפליקציה ◄◄◄ <a href="https://github.com/abnoam/Arduino-hexapod/releases/download/app/richard.apk"><img src="https://img.shields.io/badge/Download-APK-green?style=for-the-badge&logo=android" alt="Download APK" align="middle"></a>

---
##  How We Built it

<p align="center">
  <a href="https://www.youtube.com/watch?v=qhv6EdeWh7k">
    <img src="https://img.youtube.com/vi/qhv6EdeWh7k/maxresdefault.jpg" width="800">
  </a>
</p>

<p align="center">
  <a href="https://www.youtube.com/watch?v=qhv6EdeWh7k">
    <img src="https://img.shields.io/badge/YouTube-Watch%20Video-red?style=for-the-badge&logo=youtube">
  </a>
</p>

---

##יכולות הרובוט

### תנועה בסיסית
-  הליכה קדימה (`walk.forward.ino`) - תנועה רגילה קדימה 
-  הליכה לאחור (`walk.backward.ino`) - תנועה אחורה
<img width="800" height="450" alt="ezgif com-video-to-webp-converter (1)" src="https://github.com/user-attachments/assets/012068f3-894b-4b2a-b1a5-72ae1f17e9bf" />



-  פנייה ימינה (`right.ino`) - סיבוב מבוקר לימין
-  פנייה שמאלה (`left.ino`) - סיבוב מבוקר לשמאל
-  ישיבה/עמידה  (`still.ino`) - הרובוט עומד או יושב בהתאם למצבו הקודם
<img width="800" height="450" alt="ezgif com-video-to-webp-converter" src="https://github.com/user-attachments/assets/3c337a94-29a3-4591-aa7c-6e22065a94db" />


 
### פעולות מיוחדות
-  ריקוד 1 (`dance1.ino`) - רצף תנועה ראשון עם מוזיקה
-  ריקוד 2 (`dance2.ino`) - רצף תנועה שני עם מוזיקה
<img width="800" height="450" alt="ezgif com-video-to-webp-converter (2)" src="https://github.com/user-attachments/assets/18fcfab0-bd16-4e3a-a888-c2a860615530" />



---

## 🏗️ חומרה (Hardware)
<div align="right" dir="rtl">

| רכיב | תיאור |
|---|---|
| Arduino Mega 2560 | Main controller |
| 18 Servo Motors | 3 servos per leg |
| PIR Sensors | Motion detection |
| MP3 Module | Audio playback |
| RF Module | Wireless control |
</div>

---

## 🎮 פקודות בקרה

הרובוט מקבל פקודות דרך `Serial3` בפורמט של תו בודד:
<div align="right" dir="rtl">

| פקודה | פעולה | פרטים |
| ---: | ---: | ---: |
| `1` | ישיבה | הרובוט יושב למצב נמוך |
| `2` | עמידה | הרובוט עומד ברגליים מיושרות |
| `3` | הליכה קדימה | תנועה קדימה |
| `4` | הליכה לאחור | תנועה לאחור |
| `5` | פנייה ימינה | סיבוב לימין |
| `6` | פנייה שמאלה | סיבוב לשמאל |
| `7` | עצירה | עצירת תנועה וביטול מוזיקה |
| `8` | ריקוד 1 | ריקוד ראשון עם מוזיקה |
| `9` | ריקוד 2 | ריקוד שני עם מוזיקה |
| `a` | עצירה חכמה | הרובוט עוצר עד שאין בדרכו משהו |

</div>
---

## 📂 מבנה הקבצים

```
Arduino-hexapod/
├── working_everything.ino    # קוד ראשי משולב עם כל הפונקציות
├── stand.ino                 # סקריפט עמידה
├── sit.ino                   # סקריפט ישיבה
├── still.ino                 # סקריפט עצירה
├── walk.forward.ino          # סקריפט הליכה קדימה
├── walk.backward.ino         # סקריפט הליכה לאחור
├── right.ino                 # סקריפט פנייה ימינה
├── left.ino                  # סקריפט פנייה שמאלה
├── dance1.ino                # סקריפט ריקוד ראשון
├── dance2.ino                # סקריפט ריקוד שני
└── pircheck.ino              # סקריפט בדיקת חיישן PIR
```

---

## 🤝 תודות

תודה רבה לענת אלבלינג על הליווי וההדרכה במהלך היצירה של הפרוייקט
