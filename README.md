# Question

اصل SOLID چیست
-------------------
در نوشتن کد باید از 5 اصل پیروی کرد

Single Responsibility Principle یا اصل تک وظیفگی (SRP)

Open/Closed Principle یا اصل باز و بسته بودن (OCP)

Liskov Substitution Principle یا اصل جانشینی لیسکف (LSP)

Interface Segregation Principle یا اصل تفکیک Interface (ISP)

Dependency Inversion Principle یا اصل وارونه کردن وابستگی (DIP)

اصل liskov چیست
-------------------
کلاس‌های والد و فرزند، باید بتوانند بدون به وجود آمدن هیچ مشکلی در کدها به جای هم استفاده شوند. پس مربع و مستطیل جایگزین هم نیستند باید کلاس چهار ضلعی ها را بشکل abstract تعریف کرد و مربع و مستطیل از ان مشتق شوند

اصل  تفکیک Interface یا Interface Segregation
-----------------
بر اساس اصل تفکیک Interface ما نباید از Interface هایی استفاده کنیم که بیش از حد چاق هستند یا مجبور به استفاده از Interface هایی شوند که متدهای بلا استفاهده داشته باشند برای این کار اینترفیس ها را تفکیک میکنیم و بعد هر کلاس می‌تواند چندین Interface را پیاده سازی کند


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

الگوی factory
----------------------------
با استفاده از الگوی طراحی Factory برای ساخت اشیا کارخانه ای خواهیم ساخت که وظیفه ساخت اشیا از کلاس‌های مختلف را بر عهده دارد. با این کار دیگر نیازی به ساخت شی‌ها با استفاده از کیورد new به صورت جداگانه نخواهیم داشت و کافی است برای ساخت اشیا از کارخانه ساخت آن کلاس استفاده کنیم این الگوی طراحی برای شرایطی است که چندین کلاس ما از یک کلاس دیگر ارث بری کرده باشند و معمولا از آن کلاس نمونه یا شی ساخته می‌شود

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







