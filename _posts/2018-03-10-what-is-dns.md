---
layout: post_page
title: מה זה DNS
description: 
---

באגף ההפרדה בכלא של המשטר מוחזק כל אסיר בתא קטן משלו במשך כל שעות היממה. התאים מסודרים אחד ליד השני במסדרון ארוך כאשר בדלתותיהם הכחולות יש פתח דרכו מוכנסים מגשי האוכל שלהם ומדי פעם ספרים ומגזינים של בישול אזרי, המטבח החביב על מפקד הכלא.

על מנת לתקשר זה עם זה משתמשים האסירים בשירותיו של יעקב, מחלק המזון בכלא. הם נותנים לו מכתב, אומרים לו למי יש להעביר אותו, ויעקב מעביר. מכיוון שיעקב לא מכיר את האסירים בשמותיהם, על האסיר השולח לציין את מספר התא בו נמצא היעד שלו ולא את שמו. ברם, ומדי פעם מחליפים הסוהרים בכלא את מיקום האסירים בתאים, כך שמי שביום ראשון היה בתא מספר 4, למשל, ביום שלישי כבר נמצא בתא מספר 6. בעיה.

על מנת להתגבר על הבעיה הזו, לפני כל מתן של מעטפה ליעקב, צריכים האסירים לשאול את הסוהר היושב בקצה המסדרון מה מספר התא הנוכחי של אסיר מסוים. כך למשל כשבלעם מבקש להעביר מכתב ללודה הוא צועק מתאו: "סוהר סוהר בקצה המסדרון! מה מספר התא של לודה?", והסוהר עונה לו "לודה נמצאת בתא מספר 7". עכשיו כותב בלעם בגדול את הספרה "7" על המעטפה ונותן אותה ליעקב, שבתורו מעביר אותה לתא בו מוחזקת לודה.

{:refdef: style="text-align: center;"}
![dns server](/img/2018-03-10-01.jpg)
{: refdef}

> ברשת האינטרנט, מספרי התאים הם כתובות IP, והאסירים שיושבים בהם הם כתובות המתחם שלהם (שמות הדומיינים, Domain names). למשל, שם המתחם tech.b48.club שזה הבלוג שאתם קוראים כעת הוא בעצם 104.28.1.9. התקשורת ברשת לא עובדת בשמות אלא במספרים. כל מספר כזה, שנקרא כתובת IP, מורכב מ-4 חלקים המופרדים בנקודות, שבכל חלק יש מספר בין 0 ל-255. (יש גם גרסה חדשה יותר שנקראת IPv6, עליה נדבר בהזדמנות אחרת)

> אבל אי אפשר לצפות מהמשתמשים לזכור כל כך הרבה מספרים, לכן יש מה שנקרא כתובות מתחם, או בשמם הפופולרי יותר - דומיינים. במקום לזכור ארבעה מספרים, לבני אדם קל הרבה יותר לזכור שם. "גוגל" למשל, או "טוויטר". המערכת שמתרגמת בין שמות הדומיינים לאותם מספרים, או כתובות IP, נקראת DNS - שזה קיצור של Domain Name System. כל מה שהיא עושה זה לקבל את השאלה "מערכת מערכת, מה הכתובת במספרים של הדומיין כך וכך?" ולהשיב עם המספר המבוקש. 

> הזקנים יותר מאיתנו ודאי זוכרים את שירות 144 של בזק. כשרצינו לדעת מהו מספר הטלפון של פלוני, התקשרנו אליהם, ציינו את שם האדם המבוקש, וקיבלנו מספר טלפון. מערכת ה-DNS דומה מאוד מאוד לשירות הזה. הרי אי אפשר להרים את השפופרת, לצעוק "דני דנון", ולצפות שהטלפון יקשר אותנו לשגריר ישראל באו"ם. על מנת להתקשר למר דנון, עלינו להקליד שורה של ספרות שיעברו דרך מרכזיית הטלפונים  ויקשרו אותנו עם כבוד השגריר.

המערכת הזו עבדה יופי, עד שיום אחד החליט מפקד הכלא שהאסירים לא יוכלו יותר לשלוח מכתבים ללודה. הוא ציווה על הסוהר שישב בקצה המסדרון שכשאסיר מבקש לדעת מהו מספר תאה של לודה הוא יענה לו "אין כאן לודה", מה שחשב שימנע מהאסירים לדעת איזה מספר תא לכתוב על המעטפה שלהם ובכך לבלבל את יעקב שלא ידע לאן להעביר אותו.

> החסימה הזו נקראת "חסימה ברמת DNS". בית משפט מוציא צו לספקיות האינטרנט, שמחזיקות אצלן שרתי DNS לטובת לקוחותיהן, לא לענות כששואלים אותן לגבי דומיין מסויים, או לתת תשובה שגויה שתעביר את הגולשים לעמוד אחר. בארץ ארגון "זירה" הצליח [לתחמן](https://internet-israel.com/%D7%97%D7%93%D7%A9%D7%95%D7%AA-%D7%90%D7%99%D7%A0%D7%98%D7%A8%D7%A0%D7%98/%D7%96%D7%99%D7%A8%D7%94-%D7%9E%D7%A6%D7%A0%D7%96%D7%A8%D7%AA-%D7%9C%D7%9B%D7%9D-%D7%90%D7%AA-%D7%94%D7%90%D7%99%D7%A0%D7%98%D7%A8%D7%A0%D7%98-%D7%9B%D7%9A-%D7%AA%D7%AA%D7%92%D7%91%D7%A8%D7%95/) את בתי המשפט על מנת שיחסמו אתרי תוכן, ואפילו לזמן קצר את [טלגרם](https://internet-israel.com/%D7%97%D7%93%D7%A9%D7%95%D7%AA-%D7%90%D7%99%D7%A0%D7%98%D7%A8%D7%A0%D7%98/%D7%90%D7%99%D7%A8%D7%90%D7%9F-%D7%96%D7%94-%D7%9B%D7%90%D7%9F-%D7%A0%D7%98%D7%95%D7%95%D7%99%D7%96%D7%9F-%D7%97%D7%A1%D7%9E%D7%94-%D7%90%D7%AA-%D7%98%D7%9C%D7%92%D7%A8%D7%9D-%D7%90%D7%97%D7%A8/).

על מנת לעקוף את החסימה הזו, כל מה שעשו האסירים זה פשוט לא לשאול את הסוהר בקצה המסדרון, אלא אסיר ניקיון שישב לא רחוק משם, ומכיוון שאסיר הניקיון לא קיבל פקודה ממפקד הכלא לא לענות, הוא פשוט ענה על כל שאלותיהם של האסירים במדויק.

> גם ברשת זה עד כדי כך פשוט. אם לא הגדרתם שום דבר, שירות ה-DNS שלכם ככל הנראה יושב בספק האינטרנט. כל מה שצריך לעשות כדי לשנות את זה זה להכניס כתובת DNS בהגדרות הרשת שלכם. יש כמה גופים שמפעילים שירותי DNS טובים וחינמיים שיעקפו את הצנזורה שמטילות ספקיות הרשת שלכם.

> שירות פופולרי אחד כזה, למרות שאינו מומלץ על ידי הבלוג שמקפיד לעודד אך ורק פרוייקטים פתוחים, הוא השירות של חברת "גוגל". הוא מספק תשובות במהירות אבל אוגר עליכם המון מידע (ועל כך באחד הפרקים הקרובים). אם בכל זאת תבחרו להשתמש בו, תוכלו למצוא הוראות איך לעשות זאת [בלינק הזה](https://developers.google.com/speed/public-dns/docs/using).

> שירות אחר, חופשי ופתוח, הוא זה של [אופן-ניק](https://www.opennic.org/) (openNIC). לא יודע אם הייתי ממליץ עליו למתחילים, אבל הוא בהחלט מספק אלטרנטיבה לא רעה בכלל. אופציה נוספת היא השירות שמציע [quad9](https://www.globalcyberalliance.org/initiatives/quad9.html) שלא מסתפק במענה בלבד אלא גם מחזיק רשימה של כתובות פושעות [ומזהיר](https://www.themarker.com/techblogs/cybernation/1.4609692) את המשתמשים בו אם הם מבקשים להיכנס לאחת מהן. רשימה מלאה יותר של אלטרנטיבות אפשר למצוא [בלינק הזה](https://www.lifewire.com/free-and-public-dns-servers-2626062), והבלוג מאיץ בכם להשתמש באחת מהן ולא לסמוך על ספקיות הרשת הישראליות.

--- 

אם יש נושאים שהייתם רוצים שלודה ובלעם יעסקו בהם, כמו למשל חוזים חכמים, סוגי מטבעות, צורות שונות של הצפנה, פרוטוקולים של תקשורת ברשת, וכל סוג של ירק שתרצו, תרגישו חופשיים להשאיר תגובות כאן למטה, והם ישקלו את העניין בחיוב.
