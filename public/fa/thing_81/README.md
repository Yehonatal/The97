# تست‌ها علاوه بر صحیح بودن، می‌بایست دقیق هم باشند
در آموزش قبل گفتیم که در حین فرایند تست نرم‌افزار، ضروری است که عملکرد مورد انتظار از نرم‌افزار را تست کرد تا اینکه خصوصیات جانبی و حاشیه‌ای نرم‌افزار که ربطی هم به عملکردش ندارند مورد ارزیابی قرار گیرند اما این در حالی است که این سوء‌تفاهم نمی‌بایست پیش بیاید که تست‌های نرم‌افزاری می‌توانند کلی و دقیق نباشند! به‌ عنوان یک قانون کلی، یک تست خوب می‌بایست دقت و درستی عملکرد کد را بسنجد.

برای روشن‌تر شدن این مسأله، مثالی از دنیای واقعی برنامه‌نویسی می‌زنیم. الگوریتم سورت کردن یکسری داده (مثلاً از بزرگ به کوچک یا به ترتیب حروف الفبا) چیزی است که معمولاً دولوپرها با آن سروکار دارند. وقتی از دولوپری این سؤال پرسیده شود که هدف از تست چنین الگوریتمی چیست، پاسخی که معمولاً با آن مواجه می‌شویم این است که «داده‌ها باید به درستی یا از بزرگ به کوچک و با بالعکس سورت شوند».

گرچه چنین پاسخی کاملاً درست است، اما تمام ماجرا نیست! در واقع، یک تست دقیق برای سنجش چنین الگوریتمی این‌گونه عمل می‌کند که پس از سورت شدن، طول عناصر آرایهٔ مد نظر می‌بایست با طول آرایه قبل از سورت شدن یکسان باشد. گرچه چنین دیدگاهی درست است،‌ اما باز هم کافی نیست! به عنوان نمونه داریم:
```
3 1 4 1 5 9
```
خروجی زیر مجموعه اعدادی را نشان می‌دهد که هم از نظر طول با آرایهٔ اورجینال برابری می‌کند و هم اعداد از کوچک به بزرگ سورت شده‌اند:
```
3 3 3 3 3 3
```
اما می‌بینیم که تک‌تک المان‌های آرایه در خروجی وجود ندارند. این مثال برگرفته از کدی واقعی است که خوشبختانه پیش از ریلیس، باگ آن رفع شد؛ در واقع،‌ مشکل از اینجا ناشی می‌شد که کل خروجی با اولین عضو آرایه (عدد ۳) پر می‌شد.

پس ما می‌بایست تستی می‌نوشتیم که بسنجد کلیهٔ اعضای آرایه سورت شده، طول آن‌ها برابر با آرایهٔ اصلی باشد و از همه مهم‌تر، اعضا دقیقاً همان اعضای اورجینال باشند.

اگر بخواهیم تستی به معنای واقعی کلمه حرفه‌ای بنویسیم، باز هم شرایط توصیف شدهٔ بالا کفایت نمی‌کنند! در حقیقت، یک تست خوب باید خوانا، قابل‌فهم و در عین حال ساده باشد تا یک تستر به سادگی بتواند متوجه شود که آیا نتیجهٔ آن درست است یا غلط به طوری که یک دولوپر صاحب‌نام به اسم Hoare در این باره می‌گوید:

به‌طورکلی ۲ راه برای طراحی معماری یک نرم‌افزار وجود داره؛ راه اول این‌که آن‌قدر آن‌را ساده طراحی کنی که هیچ نقصی در آن وجود نداشته باشه و راه دوم این‌که آن‌قدر آن‌را پیچیده طراحی کنی که هیچ نقصی آشکارا در آن دیده نشه!

با این تفاسیر، به این نتیجه می‌رسیم که تست نرم‌افزاری در صنعت برنامه‌نویسی که روز به روز شاهد اپلیکیشن‌های پیچیده‌‌تری در آن هستیم الزامی است اما این در حالی است که تست‌ها علاوه بر سنجش صحت نرم‌افزار یا اپلیکیشن، می‌بایست دقیق هم باشند.
