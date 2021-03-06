---
layout: post_page
title: האקינג למתחילים - מהי מתקפת מניעת שירות (DOS) ומתקפת מניעת שירות מבוזרת (DDOS)
description: 
---

בלעם הסתבך. מפקד הכלא שלח אותו לצינוק אחרי שסרב לעמוד על רגל אחת ולדקלם את "אנה קרנינה" כפי שצווה, והודיע לו שלמחרת הוא מתכוון לכתוב מכתב להעברתו למתקן אחר, סימפטי אפילו פחות. לודה, מפקדת המחתרת בה חבר בלעם, החליטה לסכל את תכניתו המרושעת של מפקד הכלא.

היא יצרה קשר עם פעיל מחתרת ושכנעה אותו לכתוב המון מכתבים למפקד הכלא. הפעיל כתב כל הלילה, ובבוקר שלח מאה מכתבים המוחים על היחס לכלואי המחתרת. מפקד הכלא ישב כל היום וקרא את המכתבים, וכך לא היה לו זמן לכתוב את מכתב ההעברה של בלעם. "נהדר", אמרה לודה לפעיל המחתרת, "תמשיך ככה". מפקד הכלא הפדנט לא יכול שלא לטפל בדואר הנכנס, ולכן כל עוד יהיו המון מכתבים כך הוא לא יתפנה לטפל בעניינו של בלעם.


{:refdef: style="text-align: center;"}
![the warden](/img/2018-03-03-01.jpg)
{: refdef}


> המתקפה הזו נקראת "מתקפת מניעת שירות" (Denial of Service, או בקיצור DOS). מחשב אחד שולח המון המון בקשות לשרת המחובר לרשת, וככה מונע ממנו לטפל בבקשות אחרות.

אחרי מספר ימים כאלה מפקד הכלא התעשת, ופקד על חדר הדואר להשליך את כל המכתבים המגיעים מפעיל המחתרת הספציפי הזה, ישירות לפח. ככה הוא לא יצטרך לבזבז זמן בטיפול בפניות האלה, שנועדו רק להעסיק אותו ולא היתה בהן תועלת אמיתית.

לודה לא אמרה נואש. היא פרסמה קריאה לכל תומכי המחתרת לשבת ולכתוב מכתבים למפקד הכלא. ככה הוא לא יוכל להורות לחדר הדואר להיפטר מהם, כי לא היתה לו דרך לדעת מהו מכתב חשוב ומהו מכתב מיותר. למחרת בבוקר הוצף שולחנו של מפקד הכלא באלפי מכתבים, והוא ישב כל היום, רוטן, ועבר עליהם אחד אחד, משליך אותם לפח שעד מהרה גם הוא עלה על גדותיו.

> הסוג הזה של מתקפה נקרא "מתקפת מניעת שירות מבוזרת" (Distributed Denial of Service, או בקיצור DDOS), והיא האחות הגדולה של מתקפת מניעת השירות. טיפול במתקפה כזו הוא מורכב הרבה יותר, כי אי אפשר פשוט "לחסום" מקור אחד בלבד כמו אצל אחותה הקטנה.

אחרי מספר ימים כאלה התחנן מפקד הכלא להפסקת אש. הוא לא ישלח את בלעם לכלא אחר, ובתמורה המחתרת תפסיק לשתק את מערכת הדואר של הכלא. לודה הרהרה בכך מספר שניות, ולבסוף הסכימה בחיוך. היא הורתה לחברים להפסיק את מבצע שליחת הדואר, ובית הכלא חזר לשגרתו המנומנמת.

> בסופו של דבר, מטרת ההתקפה היא חבלה ביכולת של המטרה המותקפת לבצע את תפקידה, וזה נעשה לא על ידי חדירה, אלא על ידי פגיעה בחיבור מ/אל המטרה. 

עד כאן הבסיס. עכשיו ניכנס קצת יותר לעומק הדברים, אבל זה באמת לא נחוץ לרוב רובכם, אז תרגישו חופשיים לעצור כאן. 

---

מתקפת מניעת שירות יכולה לפעול בשבע שכבות. נעבור בקצרה על כל אחת מהן עם דוגמה מחיי הכלא:

__שכבה 7__: שכבת האפליקציה (Application layer). אלה המכתבים שנשלחו לכלא במעטפות חוקיות, עם בול, שם השולח, והכל. ברשת זה יכול להיות קריאה לטעינה של דפים, מילוי טפסים אוטומטי, העלאה או הורדה של קבצים גדולים, שליחת מיילים (תלוי בסוג המערכת אותה רוצים לשתק), וכו'.

__שכבה 6__: שכבת התצוגה (Presentation layer). מתקפה כזו תשלח מכתבים מוצפנים בהצפנה לא נכונה, או מכתבים בהונגרית לקוראי עברית בלבד. ברשת היא תשחית את המידע של ה-SSL/TLS או תשנה את הקידוד של התווים הנשלחים מ/אל השרת.

__שכבה 5__: שכבת השיחה (תרגום קלוקל ל-Session Layer). במתקפה כזו יוצרים הרבה "שיחות" (סשנים) עם השרת עד שהוא מגיע למגבלות שלו ולא יכול לפתוח שיחות חדשות.

__שכבה 4__: שכבת ההעברה (Transport Layer). במתקפה כזו משחיתים את חבילות ה-TCP או מחבלים בפרוטוקול (SYN בלי ACK ולהפך). בכלא זה יכול להיות שליחת  מעטפות מעוותות, או הכנסה של נעצים למעטפות כדי שיפגעו במי שמוביל אותן.

__שכבה 3__: שכבת הרשת (Network Layer) - תקיפה של נתבים ברשת כך שלא יוכלו לנתב את המידע. בכלא זו יכולה להיות סתימה של חדר הדואר שמנתב את המכתבים שמגיעים מחוץ לכלא לכתובות השונות בתוכו.

__שכבה 2__: שכבת החיבור (Link Layer) - זיוף של כתובת MAC ואחרות כך שהנתבים יתבלבלו בניתוב המידע, יצרו חיבורים לא הגיוניים, וימנעו חיבור אחרים. בכלא אפשר להסביר את זה על ידי שליחה של בקבוק קוניאק טוב לחדר הדואר, כדי שהעובדים שם יעשו שטויות.

__שכבה 1__: שכבה פיזית (Physical Layer) - פגיעה בחיבור הרשת עצמו, בחיבור החשמל, או בתשתית אחרת שבלעדיה לא תיתכן העברה של מידע.

> מתקפות מניעת שירות מבוזרות הופכות נפוצות יותר ויותר, לפעמים עומדים מאחוריהם אנשים אמיתיים (כמו מתקפות של ארגון אנונימוס נגד ישראל, למשל), ולפעמים רשתות בוטים המותקנים על מחשבים או מכשירים של אנשים תמימים ברשת (כמו רשת Mirai הידועה לשמצה). ככל שההתנהגות של הרשת דומה יותר להתנהגות אנושית, כך קשה יותר למנוע אותה בלי לפגוע גם בגולשים לגיטימיים. כאשר רשות הסייבר הישראלית מזהה שתשתיות בישראל שתחת אחריותה נתונות למתקפה כזו, פעמים רבות היא תבחר לסגור את כל התעבורה שמקורה מחוץ לישראל ולמנוע גישה מחו"ל לחווה הממשלתית. להרוג זבוב עם תותחי נברון, אבל לפחות לא צריך להודות בתבוסה כשאתרי הממשל לא יעלו גם לאזרחי ישראל הממוקמים בגבולות המדינה.

> ברשת האפלה מוצעות להשכרה רשתות בוטים גדולות במחיר שווה לכל נפש המאפשרות לכל מי שרוצה להפעיל מתקפת מניעת שירות מבוזרת ולהשבית את המטרה שהוא מבקש להשבית. מקרה בולט ששווה להזכיר הוא מתקפה שהונחתה על רשת הימורים בריטית בדיוק בזמן משחק חשוב, מה שגרם לה להפסדים גדולים. לקראת המשחק הגדול הבא פנו אליה כמה חברים מנומסים וביקשו סכום כסף לא קטן כדי שלא יתפתו לעשות את זה שוב. רשת ההימורים שילמה להם בעין יפה, והם, מצידם, לא הפילו לה את המערכות.

---

אם יש נושאים שהייתם רוצים שלודה ובלעם יעסקו בהם, כמו למשל חוזים חכמים, סוגי מטבעות, צורות שונות של הצפנה, פרוטוקולים של תקשורת ברשת, וכל סוג של ירק שתרצו, תרגישו חופשיים להשאיר תגובות כאן למטה, והם ישקלו את העניין בחיוב.


