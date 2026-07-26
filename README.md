# Top Model Collection — Customer Attribution Platform

מערכת ניהול לקוחות, שיוך סניפים, הזמנות ועמלות. נגישה מכל דפדפן, מכל מחשב או טלפון.

## כתובות

| מה | כתובת |
|---|---|
| דף נחיתה ראשי | https://alalbarservice-svg.github.io/TOP-MODEL/ |
| מרכז שליטה (דשבורד) | https://alalbarservice-svg.github.io/TOP-MODEL/admin.html |
| לינק סניף 1–7 (לביו באינסטגרם) | https://alalbarservice-svg.github.io/TOP-MODEL/1 … /7 |

- כניסת בעלים לדשבורד: עם סיסמת הניהול.
- כניסת שותף/סניף: עם המייל שהוגדר לסניף במפת הדרכים — רואה את הסניף שלו בלבד.
- אפשר להוסיף מקור קמפיין לכל לינק: `/3?c=story_july`

## ארכיטקטורה

- דפים סטטיים (GitHub Pages) — שכבת תצוגה בלבד.
- מקור אמת: Supabase (Postgres) — לקוחות, לידים, הזמנות, פריטים, מוצרים, עמלות, אירועים.
- Edge Functions: `capture-lead` (לכידת ליד+שיוך), `admin-api` (דשבורד), `export-csv` (דוחות).
- שיוך לקוח לסניף המקור קבוע לצמיתות; מניעת כפילויות לפי טלפון; audit מלא.
