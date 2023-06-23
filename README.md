# Question

اصل SOLID چیست
-------------------
در نوشتن کد باید از 5 اصل پیروی کرد

Single Responsibility Principle یا اصل تک وظیفگی (SRP)

Open/Closed Principle یا اصل باز و بسته بودن (OCP)

Liskov Substitution Principle یا اصل جانشینی لیسکف (LSP)

Interface Segregation Principle یا اصل تفکیک Interface (ISP)

Dependency Inversion Principle یا اصل وارونه کردن وابستگی (DIP)

اصل  تفکیک Interface
-----------------
بر اساس اصل تفکیک Interface ما نباید از Interface هایی استفاده کنیم که بیش از حد چاق هستند یا مجبور به استفاده از Interface هایی شوند که متدهای بلا استفاهده داشته باشند


اصل dependency inversion یا اصل وارونگی وابستگی یا DIP چیست
-----------------
ماژول‌های سطح بالای برنامه نباید به ماژول‌های سطح پایین آن وابسته باشند هر دو باید به Abstraction‌ها وابسته باشند منظور این است همیشه از Interface‌ها و Abstract‌ها در برنامه نویسی استفاده کنیم

تزریق وابستگی یا Dependency injection  چیست؟
--------------------


یک الگوی طراحی است که با هدف حذف وابستگی های موجود بین دو کلاس با استفاده از یک Interface یا همان رابط ایجاد شده است. به عبارت دیگر تزریق وابستگی به معنی تزریق وابستگی های یک کلاس به جای استفاده مستقیم از آن ها درون کلاس است

روشها

تزریق سازنده (Constructor Injection)

تزریق پراپرتی (Property Injection)

تزریق متد (Method Injection)

الگوی طراحی Builder
---------------------------
جهت طراحی کلاسهای پیچیده استفاده میشه که یک راه ان استفاده از پارامتر در سازنده کلاس است که اگر حالتهای مختلف رو در نظر بگیریم ارسال پارامترهای فراوان که در بعضی حالات نال هم میباشند کار نامعقولی است در این حالت با تعریف یک اینترفیس اجزای ساخت رو بصورت متد تعریف میکنیم بعد برای هر نوع مشخص کلاسی تعریف میکنیم که از اینترفیس تبعیت کند 

کتابخانه MediatR
----------------------------

نقش واسط رو عمل میکند بجای اینکه در هر کنترلر سرویسهای متعدد و کانتکس رو اینجکت کنیم به این واسط میگیم چیکار کنه

در راستای معماری تمیز میباشد و با دیکاپلینک یا کوچکتر و سبک تر کردن و مستقل کردن اجزا حرکت میکند

کتابخانه ای که میتوان عملیات ارسال و دریافت داده رو متمرکز کرد

Include command , handler , response ,INotification ,INotificationHandler ,Behavior, call by send or Publish 

اینترفیس IMediator علاوه بر متد Send ، دارای متد دیگری بنام Publish نیز هست که وظیفه Raise کردن Event‌ها را برعهده دارد 

هر Request نیاز به یک Handler دارد تا آن را پردازش کند

bevavour : قبل و بعد هر درخواست این کار انجام شود







