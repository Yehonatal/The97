# اعداد اعشاری با خطای محاسباتی در کامپیوتر ذخیره می‌شوند

در این بخش می خواهیم در مورد اعداد اعشاری و نحوه ی ذخیره ی آن ها در کامپیوتر صحبت کنیم، بنابراین بهتر است در ابتدا تعریفی از این نوع اعداد با ذکر مثالی داشته باشیم. 

یک خط کش ۱۰ سانتی متری را در ذهن خود متصور شوید؛ حال عدد ۳/۶ را روی این خط کش فرضی در نظر بگیرید. این عدد از 3 بزرگتر و از 4 کوچکتر است. برای نشان دادن این که این عدد چقدر از 3 بزرگتر و از 4 کوچکتر است از علامت ممیز یا اعشار / استفاده می کنیم که به طور کلی، به این دست اعداد «اعداد اعشاری» می گوییم. بنابراین می توان گفت که یک عدد اعشاری بین دو عدد صحیح قرار دارد.

برای تعریف اعداد صحیح در کامپیوتر از استانداردهای IEEE استفاده می شود. بر اساس این استاندارد برای ذخیره ی هر عدد اعشاری سه فیلد در نظر گرفته می شود:
- اعشار یا مانتیس
- توان
- علامت

برای مثال، بر طبق این استاندارد داریم:

101 × 2.7495 = 27.495

که 2.7495 مانتیس، 1 توان و علامت آن نیز مثبت است (البته اعداد در کامپیوتر در پایه ی 2 ذخیره می شوند نه پایه ی 10).

هر پیاده سازی اعداد اعشاری تعداد مشخصی بیت را برای مانتیس در نظر می گیرد، به عبارت دیگر تعداد اعداد قابل ذخیره سازی در کامپیوتر با محدودیت مواجه است. برای مثال برای ذخیره ی اعداد اعشاری در سیستم های ۳۲ بیتی، برای مانتیس ۲۳ بیت در نظر گرفته شده است. این موضوع باعث می شود که نتوانیم اعداد اعشاری که نمایش آن ها دارای تعداد رقم اعشاری متناهی نیست را به طور دقیق در کامپیوتر ذخیره کنیم.

برای ذخیره سازی هر عدد بسته به فضای اختصاص داده شده به مانتیس، ابتدا عدد مورد نظر گرد می شود و سپس در کامپیوتر ذخیره می شود؛ به همین دلیل ممکن است نمایش یک عدد اعشاری در کامپیوتر 32 بیتی با کامپیوتر 64 بیتی متفاوت باشد، چرا که فضای اختصاص داده شده به مانتیس در آن ها متفاوت است.

بنابراین باید توجه داشته باشیم که امکان ذخیره سازی دقیق تمام اعداد حقیقی که بخش اعشاری آن ها دارای تعداد نامتناهی رقم است در کامپیوترها وجود ندارد و به دلیل این نوع ذخیره سازی در زمان کدنویسی و انجام محاسبات روی اعداد صحیح ممکن است با خطای گرد کردن یا Roundoff Error مواجه شویم و جواب های غیر قابل انتظار از محاسبات کامپیوتری دریافت کنیم. بنابراین می توان گفت که بهتر است در برنامه هایی که نیازمند محاسبات دقیق هستند تا حد امکان از اعداد اعشاری استفاده نکنیم.
