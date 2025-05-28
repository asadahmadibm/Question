# Question

12 Bad Practices to Avoid in ASP.NET Core API Controllers | by Andy | Jul, 2023 | Level Up Coding
https://levelup.gitconnected.com/12-bad-practices-to-avoid-in-asp-net-core-api-controllers-3ba52a10954e

درباره Clean Code توضیح دهید
------------------
قواعد برنامه نویسی :

1- طول نام توابع و متغیرها بیشتر از 25 کاراکتر نشود

2- نامگذاری با معنی داشته باشیم و طوری کد بنویسیم که به کامنت کمتری نیاز باشد

3- از کمل کیس برای نامگذاری استفاده کنیم

4- اصول solid و dry را رعایت شود

5- پارامترهای ورودی نباید از 4 تا بیشتر شود

6- اصول encapsolation  رعایت شود

7- کلاسها نباید بزرگ باشند

8- از design pattern  ها استفاده کنیم

9- از interface و Abstraction استفاده شود

10- اصل تک مسوولیتی رعایت شود

11- چوری کد بنویسیم که نفر بعدی را در نظر بگیریم

12- تست نویسی


انواع نامگذاری متغیرها یا فانکشن ها
----------------------
فقط مت۶یر محلی camel case باشد بقیه pascal case

kebab case : all words are lowercase, and each word gets separated by a dash                                                   : number-of-donuts = 34

pascal case : every word starts with an uppercase letter                                                                       : NumberOfDonuts = 34

camel case : you start by making the first word lowercase. Then, you capitalize the first letter of each word that follows     : numberOfDonuts = 34

snake case : When using snake case, all letters need to be lowercase  and separates each word with an underscore character     : number_of_donuts = 34


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

الگوهای طراحیGOF (Gang of Four)

پرکاربردترین Singleton, Factory Method, Abstract Factory, Builder, Adapter, Observer, Strategy, Decorator, Facade هستند.

الگوی factory
استفاده از Factory Pattern باعث می‌شود کدنویس دیگر به صورت مستقیم با دستور new اشیا را نسازد و ساخت آن‌ها را به یک کارخانه بسپارد. در مقابل، Abstract Factory یک سطح انتزاعی بیشتر اضافه می‌کند تا حتی بدون نیاز به دانستن جزئیات سازندگان و پارامترها، مجموعه‌ای از اشیای مرتبط و سازگار را بتوان به طور یکجا و خودکار تولید کرد

الگوی observe
برای پیاده‌سازی Observer، شیء (موضوع یا Subject) را میسازی و سپس ناظرها را به آن اضافه کنی؛ پس از آن، وقتی تغییر یا خبری در موضوع اتفاق بیفتد، موضوع می‌تواند به همه ناظرهایش خبر دهد.

الگوی طراحی Builder
---------------------------
جهت طراحی کلاسهای پیچیده استفاده میشه که یک راه ان استفاده از پارامتر در سازنده کلاس است که اگر حالتهای مختلف رو در نظر بگیریم ارسال پارامترهای فراوان که در بعضی حالات نال هم میباشند کار نامعقولی است در این حالت با تعریف یک اینترفیس اجزای ساخت رو بصورت متد تعریف میکنیم بعد برای هر نوع مشخص کلاسی تعریف میکنیم که از اینترفیس تبعیت کند 

الگوی استراتژی به ما اجازه می‌دهد چند روش یا الگوریتم مختلف برای انجام یک کار داشته باشیم و هنگام اجرا به‌راحتی، بدون تغییر کد اصلی، هر کدام را که خواستیم انتخاب کنیم.

الگوی decorator  این الگو با تعریف virtual  متدها باعث میشود هنگام پیاده سازی روشها را تغییر دهیم و به شی اولیه مرحله به مرحله رفتار جدید بدیم

الگوی facad
چند متد یا کار را در یک متد ساده به کاربر نشان دهی یعنی پشت صحنه، Facade کار را بین کلاس‌های مختلف تقسیم می‌کند اما همه چیز را در قالب یک متد ساده به کاربر ارائه می‌دهد


درباره CQRS توضیح دهید
------------
الگوی یا Command and Query Responsibility Segregation جداسازی عملیات خواندن و نوشتن داده را میگوید

When to use CQRS
-------------------
We can use Command Query Responsibility Segregation when the application is huge and access the same data in parallel. CQRS helps reduce merge conflicts while performing multiple operations with data.
In DDD terminology, if the domain data model is complex and needs to perform many operations on priority like validations and executing some business logic so in that case, we need the consistency that we will by using CQRS.

کتابخانه MediatR
----------------------------
در الگوی Mediator دیگر کلاس ها و سرویس ها با یکدیگر مستقیم در ارتباط نیستند بلکه درخواست خود را از طریق یک واسط می فرستند و از طریق همان واسط، پاسخ مربوطه را دریافت میکنند. این کار باعث می شود که وابستگی شدید بین دو سرویس به حداقل برسد و Loose Coupling داشته باشیم که به توسعه و نگهداری یک پروژه کمک شایانی میکند.

MediatR pattern helps to reduce direct dependency between multiple objects and make them collaborative through MediatR.

در این الگو هر گونه ارتباط مستقیم بین دو شیء را محدود کرده و برای ارتباط پیدا کردن با هم آن ها را مجبور به استفاده از یک شیء رابط به نام Mediator می کنیم الگوی Mediator به ما این توانایی را می دهد که یک شبکه ی منظمی از ارتباط بین اجزای مختلف فرم ها ایجاد کنیم و شلختگی یا پیچیدگی را تا حد قابل ملاحظه ای کاهش دهیم

نقش واسط رو عمل میکند بجای اینکه در هر کنترلر سرویسهای متعدد و کانتکس رو اینجکت کنیم به این واسط میگیم چیکار کنه

در راستای معماری تمیز میباشد و با دیکاپلینک یا کوچکتر و سبک تر کردن و مستقل کردن اجزا حرکت میکند

کتابخانه ای که میتوان عملیات ارسال و دریافت داده رو متمرکز کرد

Include command , handler , response ,INotification ,INotificationHandler ,Behavior, call by send or Publish 

اینترفیس IMediator علاوه بر متد Send ، دارای متد دیگری بنام Publish نیز هست که وظیفه Raise کردن Event‌ها را برعهده دارد 

هر Request نیاز به یک Handler دارد تا آن را پردازش کند

bevavour : قبل و بعد هر درخواست این کار انجام شود

#توضیحات در پروژه CleanArtchitecture آمده است

کلمه Value Objects چیست
--------------------------
بسیاری از اشیا هویت مفهومی ندارند. این اشیا ویژگی های یک چیز را توصیف می کنند. خود مرجعیتی ندارند و در توصیف مرجعی بکار میروند و به تنهایی وجود ندارند  توجه اینکه ممکن است در جایی یک شی مرجع باشد ولی در جای دیگر فقط value object مثلا 1 دلار میتواند value object  باشد ولی در جایی که اسکناس ها را ردیابی کنیم ان موجودیت میشود






