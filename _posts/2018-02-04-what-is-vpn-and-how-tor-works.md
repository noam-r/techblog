---
layout: post_page
title: מה זה VPN ואיך עובדת רשת TOR
description: 
---

בפרק הקודם הכרנו את לודה ובלעם, חברים במחתרת המוחזקים בכלא של המשטר, ואת הדרכים המחוכמות בהן בחרו לתקשר כדי שמפקד הכלא החלקלק לא יחשף לתוכן דבריהם. אם החמצתם אותו, מומלץ לעצור [ולקרוא אותו קודם](http://tech.b48.club/2018/01/27/how-https-works.html). אנחנו נחכה כאן.

אחרי שהצליחו לודה ובלעם לפתור, בצורה סבירה, את בעיית התוכן ההודעות שלהם, החליט מנהל הכלא שאם הוא לא יודע מה הם אומרים, הוא פשוט יחסום את התקשורת ביניהם. אמר, ועשה. יעקב, מחלק המזון של הכלא, שעד היום העביר את המסרים בין לודה לבלעם, לא הורשה יותר לעבור בין שני התאים. שוד ושבר.

{:refdef: style="text-align: center;"}
![blocked connection](/img/2018-02-04-01.jpg)
{: refdef}

> חסימות כאלה מתבצעות לעתים תכופות במשטרים מדכאים. [אירן](https://www.nytimes.com/2018/01/02/technology/iran-protests-social-media.html), למשל, חסמה גישה של משתמשים לרשתות החברתיות בינואר 2018, וחסימות דומות התרחשו [בסין](https://www.nytimes.com/2017/09/25/business/china-whatsapp-blocked.html), [בטורקיה](https://techcrunch.com/2016/11/04/turkey-blocks-social-media-again-to-stall-protests-heres-how-to-access-them/), [במצריים](https://www.theguardian.com/world/2011/jan/26/egypt-blocks-social-media-websites), ואפילו לזמן קצר גם [בישראל](https://internet-israel.com/%D7%97%D7%93%D7%A9%D7%95%D7%AA-%D7%90%D7%99%D7%A0%D7%98%D7%A8%D7%A0%D7%98/%D7%90%D7%99%D7%A8%D7%90%D7%9F-%D7%96%D7%94-%D7%9B%D7%90%D7%9F-%D7%A0%D7%98%D7%95%D7%95%D7%99%D7%96%D7%9F-%D7%97%D7%A1%D7%9E%D7%94-%D7%90%D7%AA-%D7%98%D7%9C%D7%92%D7%A8%D7%9D-%D7%90%D7%97%D7%A8/).

בהתחלה, ניסה בלעם ליצור קשר עם לודה באמצעות צד שלישי. הוא יצר ערוץ מוצפן (בדומה לשיטת הקופסאות עליה דיברנו בפרק הקודם) עם פיני, אפסנאי הכלא, ופיני יצר ערוץ מוצפן עם לודה, וכך יכלו לודה ובלעם לתקשר. 

> שיטת תקשורת כזו נקראת תקשורת באמצעות פרוקסי (Proxy), שמימוש קצת יותר מתוחכם שלה הוא VPN, "רשת וירטואלית פרטית" (Virtual private network), באמצעותה יוצרים ערוץ תקשורת מנקודה א' לנקודה ב' דרך צד ג'.

הבעיה החלה כשמפקד הכלא שם לב לתעבורה מוגברת בין בלעם לפיני האפסנאי, ובין לודה לפיני האפסנאי, עשה אחד ועוד אחד, וחסם גם את הגישה של בלעם לפיני. 

> שימוש ב-VPN הוא כלי פשוט לעקיפת חסימות, אך יש לו גם צדדים אפלים. חברות המפעילות את השירות [מוכרות](https://www.cyberscoop.com/hotspot-shield-accused-of-snooping-on-vpn-users-and-selling-data-to-advertisers/) את המידע על המשתמשים, וגרוע מכך אפילו מזריקות רושעות לתוך התעבורה. [מחקר מ-2016](https://research.csiro.au/ng/wp-content/uploads/sites/106/2016/08/paper-1.pdf) בדק 283 אפליקציות VPN ומצא ש-75% מהן מפעילות שירותי ניטור חיצוניים, 82% מבקשות גישה למידע הפרטי של המשתמש, ו-38% מהן מכילות רושעות מסוגים שונים. בשורה התחתונה, אם אתם לא משלמים על השירות, ו/או בודקים היטב את המוניטין של החברה - סביר להניח שפרטיותכם בסכנה.

ישבו וחשבו, שעתיים בערך, ובזמן שלעסה לודה את הבצל של ארוחת הערב עלה לה רעיון מבריק: הם זיהו כמה אסירים אחראיים בכלא, והחלו לשחק איתם משחק של "חבילה עוברת". בלעם שלח קופסה עליה כתב "מאת: בלעם, אל: אסיר א'". בתוך הקופסה היתה עוד קופסה בה נכתב "מאת: אסיר א', אל: אסיר ב'", בתוכה היתה עוד קופסה מאסיר ב' לאסיר ג', ובתוכה עוד קופסה מאת "אסיר ג', אל: לודה", ובתוך הקופסה של לודה היתה הודעה של בלעם. ככה אף אחד בדרך לא היה יכול לדעת שהשולח הוא בלעם והמקבלת היא לודה. מפקד הכלא החלקלק רק ידע שבלעם שלח חבילה לאסיר א', ושלודה קיבלה חבילה מאסיר ג'. אפילו בין אסיר א' לג' לא היה קשר ישיר, והם לא ידעו זה על קיומו של זה.

{:refdef: style="text-align: center;"}
![onion packages](/img/2018-02-04-02.jpg)
{: refdef}

בכל פעם שבלעם רצה לשלוח הודעה ללודה הוא היה בוחר אסירים אחראיים אחרים להעביר דרכם את החבילה שלו, כך שהדרך היחידה של מנהל הכלא החלקלק למנוע ממנו לתקשר עם לודה היתה למנוע ממנו לשלוח חבילות לכל האסירים בכלא, צעד קיצוני אפילו בשביל משטר מדכא כמו שלו.

> התיאור הכללי הזה הוא פחות או יותר איך שעובדת רשת TOR, "הרשת האפלה", "רשת הבצל" (בעבר ראשי התיבות של TOR היו The Onion Router, בגלל השכבות מהן היא בנויה, אבל הם החליטו לרדת מזה). האסירים האחראיים הם "צמתים" (Nodes) ברשת, אשר מעבירים את החבילות המגיעות אליהם בינם לבין עצמם, ובכך מנתקים את אפשרות זיהוי הקשר בין השולח למקבל.

שימוש נוסף בשיטה הזו יכול להגן גם על זהות המקבל. נניח שבכלא יש חנות סודית שמוכרת פצירות, שחשיפת מיקומה יאפשר למנהל הכלא החלקלק לסגור אותה ולהעניש את מפעיליה. איך אפשר לתקשר עם חנות שלא יודעים את מיקומה? לצורך כך החנות יכולה ליצור "רשת" משלה של אסירים אחראיים, והלקוחות הפוטנציאלים שלה ידברו רק עם הרשת ויעבירו את ה"חבילה עוברת" באמצעות הרשת שלהם לרשת של החנות. כך החנות לא תדע מי הקונה, והקונה לא ידע איפה החנות.

> שימוש כזה ברשת תור נקרא "שירותים נסתרים", ובאמצעותו יכולים לפעול כל השווקים האפלים שמוכרים סחורה בעייתית, או אתרים אחרים שמנגישים מידע אסור, או פלטפורמות להדלפת חומרים מעניינים במיוחד, כמו [תיבת ההדלפות של הבלוג](https://www.b48.club/2017/12/02/leakbox.html), למשל. לאנשים הטכניים שביניכם, אני מרחיב על הנושא הזה בהמשך, תחת הכותרת "הסבר טכני משעמם".

באמצעות שימוש ברשת הזו, גם אם ישכנע מנהל הכלא החלקלק כמה מהאסירים המשמשים כ"צמתים" לשתף איתו פעולה ולחלוק איתו את המידע שלהם, זה עדיין לא יספיק כדי לפצח אותה. כיום, שימוש ברשת הזו נחשב "בטוח מספיק" לרוב הפעולות הדורשות אנונימיות. כדי להתחיל להשתמש בה כל מה שאתם, הקוראים, צריכים לעשות זה להוריד דפדפן יעודי, להפעיל אותו, וזהו. תוכלו לעשות את זה [כאן](https://www.torproject.org/download/download-easy.html.en).

אם הגעתם עד הנה, יש לכם כבר מושג כללי על איך עובדת רשת TOR. ההסבר מכאן והלאה הוא טכני לעייפה ומיועד לאנשים משועממים במיוחד. זה בסדר גמור להפסיק לקרוא ולשוב בפרק הבא של הרפתקאות לודה ובלעם בכלא.

---

### הסבר טכני משעמם

ברשת הבצל ישנם "שירותים נסתרים" (Hidden services) שמאפשרים לא רק למשתמש לשמור על האנונימיות שלו, אלא גם למפעיל השירות לשמור על פרטיותם. ככה, למשל, יכולים מפעילי השווקים האפלים, בהם נמכרים מיני טובין שמידת חוקיותם מפוקפקת, להמשיך בפעולתם מבלי שרשויות החוק ידעו איפה נמצאים השרתים שלהם, ולבוא לסגור אותם. 

השירותים הנסתרים מזוהים על ידי "כתובת בצל" (Onion Address) שהיא מחרוזת של 16 תווים ואחריה הסיומת .onion. המחרוזת הזו היא בעצם האש (hash) על המפתח הפרטי/ציבורי שנועד למנוע התחזות.

מכיוון שברשת תור אין שרתי DNS שמתרגמים שם לכתובת IP (שהרי חלק מהרעיון הוא להסתיר את הכתובת), זה עובד בצורה מעט שונה: מפעיל השירות מייצר זוג מפתחות פרטי/ציבורי (1024 bit), ומריץ עליו את סדרת הפעולות הבאה: SHA-1, חיתוך לשניים, ואז הפעלה של Base32 על התוצאה, והוספת הסיומת onion. קל ופשוט, נכון? אגב, בגלל שמשתמשים בפונקציה המקוללת base32 אין כתובות בצל עם הספרות 0,1,8 ו-9. חדי העין מביניכם ודאי הבחינו שמדובר באלגוריתמים חלשים להחריד, לכן בעתיד הקרוב תהפוך הכתובת מ-16 תווים ל-54 תווים כדי לספק אבטחה טובה משמעותית מול כח חישוב עולה.

לאחר שהכין מפעיל השירות את הכתובת, הוא יוצר קשר עם כמה שרתי Relay ומספר להם על המפתח הציבורי היפה והחדש שלו. השרתים האלה נקראים "נקודות ההיכרות" (Introduction points) שלו מכאן והלאה. השילוב בין המפתח הציבורי ונקודות ההיכרות נקרא Hidden service descriptor, או בקיצור HSD, אותו חותם מפעיל השירות הנסתר בעזרת המפתח הפרטי שלו. את ה-HSD מפרסם מפעיל השירות ב"טבלת ההאשים המופצים" (Distributed Hash Table - ראשי תיבות DHT), ואז כל מי שמחפש אותו יודע מה המפתח הציבורי שלו ועם מי צריך לדבר כדי להגיע אליו. המקבילה האפלה של "דויד שלח אותי".

כאשר משתמש מבקש להתחבר לשירות הנסתר, הדפדפן שלו פונה ל-DHT עם כתובת הבצל שברשותו (בדומה לשימוש רגיל ב-DNS), ומקבל בתגובה את ההאש (שכזכור מורכב מהמפתח הציבורי ומנקודות ההיכרות של השירות). 

אז המשתמש בוחר באקראי את אחד ה"צמתים" ברשת שישמש כ"נקודת מפגש" (Rendezvous Point) ויוצר מה שנקרא "מעגל" (Circuit) ובו 3 "קפיצות". המשתמש מצפין הודעה עם המפתח הציבורי של השירות הנסתר והודעה המכילה "סוד" (One-time-secret) ומבקש מנקודת המפגש שלו להעביר את ההודעה לשירות הנסתר. ההודעה מגיעה לשירות הנסתר, שמפענח אותה בעזרת המפתח הפרטי שלו, ויוצר הודעה חדשה, אותה הוא שולח בחזרה לנקודת המפגש, שבתורה מעבירה אותה למשתמש. עכשיו, באמצעות ה"סוד" שחלקו המשתמש והשירות, כל התקשורת שלהם מוצפנת לכל אורך השרשרת, כך שגם אם קיים צומת רשע אחד או יותר - הם לא יוכלו לפענח את התשדורות. מה שנוצר לנו הוא "מעגל" ובו 6 קפיצות בין המשתמש לשירות הנסתר, שזה מספר גדול מספיק לשמירה על אנונימיות, וקטן מספיק כדי לאפשר זרימת נתונים סבירה.

זהו, ככה, בגדול, פועלת התקשורת ברשת הבצל. בעתיד הקרוב מתוכננת סדנה בה ניכנס קצת יותר לעומק הדברים, ואפילו נרים כמה שירותים נסתרים בכל מיני צבעים.
