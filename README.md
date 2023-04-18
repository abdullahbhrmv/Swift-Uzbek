# Swift haqida

**Swift - bu telefonlar, ish stollari, serverlar yoki kod bilan ishlaydigan boshqa narsalar uchun dasturiy ta'minot yozishning ajoyib usuli. Bu xavfsiz, tezkor va interaktiv dasturlash tili boʻlib, u zamonaviy til tafakkuridagi eng yaxshi narsalarni kengroq Apple muhandislik madaniyati donoligi va ochiq manbali hamjamiyatning turli hissalarini birlashtiradi. Kompilyator ishlash uchun optimallashtirilgan va til ikkalasiga ham zarar etkazmasdan ishlab chiqish uchun optimallashtirilgan.**

**Swift barcha asosiy C va Objective-C turlarining o'z versiyalarini taqdim etadi, jumladan butun sonlar uchun Int, suzuvchi nuqta qiymatlari uchun Double va Float, Boolean qiymatlari uchun Bool va matnli ma'lumotlar uchun String. Swift, shuningdek, To'plam turlarida tavsiflanganidek, uchta asosiy to'plam turlarining kuchli versiyalarini taqdim etadi, massiv, to'plam va lug'at.**

**C kabi, Swift o'zgaruvchilardan qiymatlarni saqlash va identifikatsiya qiluvchi nom bilan bog'lash uchun foydalanadi. Swift shuningdek, qiymatlarini o'zgartirib bo'lmaydigan o'zgaruvchilardan keng foydalanadi. Ular konstantalar sifatida tanilgan va C dagi konstantalarga qaraganda ancha kuchliroqdir. Oʻzgartirish kerak boʻlmagan qiymatlar bilan ishlaganda kodni xavfsizroq va aniqroq qilish uchun Swift’da doimiylar qoʻllaniladi.**

**Tanish turlarga qo'shimcha ravishda, Swift Objective-C da topilmagan ilg'or turlarni, masalan, kortejlarni taqdim etadi. Kortejlar sizga qiymatlar guruhlarini yaratish va o'tkazish imkonini beradi. Funktsiyadan bitta birikma qiymat sifatida bir nechta qiymatlarni qaytarish uchun kortejdan foydalanishingiz mumkin.**

**Swift shuningdek, qiymat yo'qligi bilan shug'ullanadigan ixtiyoriy turlarni ham taqdim etadi. Majburiy emas, '*qiymat bor va u x ga teng*' yoki '*umuman qiymat yo'q*' deb aytadi. Opsiyonellardan foydalanish Objective-C da ko'rsatkichlar bilan nil dan foydalanishga o'xshaydi, lekin ular nafaqat sinflar uchun, balki har qanday turdagi uchun ishlaydi. Objective-C-dagi nol ko'rsatkichlarga qaraganda ixtiyoriy imkoniyatlar nafaqat xavfsizroq va ifodaliroq, balki ular Swiftning ko'plab eng kuchli xususiyatlarining markazida joylashgan.**

**Swift - bu *turdagi xavfsiz* til, ya'ni bu til sizning kodingiz bilan ishlashi mumkin bo'lgan qiymatlar turlarini aniq bilishingizga yordam beradi. Agar kodingizning bir qismi Stringni talab qilsa, xavfsizlik turi uni noto'g'ri Int ga o'tkazishdan saqlaydi. Xuddi shunday, xavfsizlik turi ixtiyoriy Stringni ixtiyoriy bo'lmagan Stringni talab qiladigan kod qismiga tasodifan o'tkazishdan saqlaydi. Xavfsizlik turi ishlab chiqish jarayonida xatolarni imkon qadar erta aniqlash va tuzatishga yordam beradi.**

## Konstantalar va o'zgaruvchilar

**Konstantalar va oʻzgaruvchilar nomni (masalan, maximumNumberOfLoginAttempts yoki WelcomeMessage) maʼlum turdagi qiymat (masalan, 10 raqami yoki “Salom” qatori) bilan bogʻlaydi. O'rnatilgandan so'ng doimiy qiymatni o'zgartirib bo'lmaydi, o'zgaruvchi esa kelajakda boshqa qiymatga o'rnatilishi mumkin.**

## Konstantalar va o'zgaruvchilarni e'lon qilish

**Constants and variables must be declared before they’re used. You declare constants with the let keyword and variables with the var keyword. Here’s an example of how constants and variables can be used to track the number of login attempts a user has made:**

```swift
let maximumNumberOfLoginAttempts = 10
var currentLoginAttempt = 0
```

**Ushbu kodni quyidagicha o'qish mumkin:**

**'MaxsimumNumberOfLoginAttempts deb nomlangan yangi konstantani e'lon qiling va unga 10 qiymatini bering. Keyin, currentLoginAttempt deb nomlangan yangi o'zgaruvchini e'lon qiling va unga 0 boshlang'ich qiymatini bering.'**

**Ushbu misolda ruxsat etilgan kirish urinishlarining maksimal soni doimiy deb e'lon qilinadi, chunki maksimal qiymat hech qachon o'zgarmaydi. Joriy kirishga urinish hisoblagichi o'zgaruvchi sifatida e'lon qilinadi, chunki bu qiymat har bir muvaffaqiyatsiz kirish urinishidan keyin oshirilishi kerak.**

**Bitta satrda vergul bilan ajratilgan bir nechta konstantalarni yoki bir nechta o'zgaruvchilarni e'lon qilishingiz mumkin:**

```swift
var x = 0.0, y = 0.0, z = 0.0
```

>Eslatma

>Agar kodingizdagi saqlangan qiymat o'zgarmasa, uni har doim let kalit so'zi bilan doimiy deb e'lon qiling. O'zgaruvchilardan faqat o'zgarishi kerak bo'lgan qiymatlarni saqlash uchun foydalaning.

## Izohlarni yozing

**Doimiy yoki o'zgaruvchini saqlashi mumkin bo'lgan qiymatlar turini aniq bilish uchun siz doimiy yoki o'zgaruvchini e'lon qilganingizda *tur izohini* berishingiz mumkin. Doimiy yoki oʻzgaruvchi nomidan keyin ikki nuqta qoʻyib, undan keyin boʻsh joy va undan keyin foydalaniladigan tur nomini qoʻyib, tur izohini yozing.**

**Ushbu misol o'zgaruvchining String qiymatlarini saqlashi mumkinligini ko'rsatish uchun welcomeMessage deb nomlangan o'zgaruvchining turiga izoh beradi:**

```swift
var welcomeMessage: String
```

**Deklaratsiyadagi ikki nuqta '...turi ...' degan ma'noni anglatadi, shuning uchun yuqoridagi kodni quyidagicha o'qish mumkin:**

**'String tipidagi *welcomeMessage* deb nomlangan o'zgaruvchini e'lon qiling.'**

**'String turi' iborasi 'har qanday String qiymatini saqlashi mumkin' degan ma'noni anglatadi. Bu saqlanishi mumkin bo'lgan 'narsa turi' (yoki 'narsa turi') degan ma'noni anglatadi.**

**WelcomeMessage o'zgaruvchisi endi xatosiz istalgan satr qiymatiga o'rnatilishi mumkin:**

```swift
welcomeMessage = "Hello"
```

**Bitta satrda vergul bilan ajratilgan bir xil turdagi bir nechta bog'liq o'zgaruvchilarni yakuniy o'zgaruvchi nomidan keyin bitta turdagi izoh bilan belgilashingiz mumkin:**

```swift
var red, green, blue: Double
```

>Eslatma

>Amalda turdagi izohlarni yozishingiz kamdan-kam uchraydi. Agar siz doimiy yoki oʻzgaruvchining boshlangʻich qiymatini aniqlangan nuqtada taqdim etsangiz, Swift deyarli har doim oʻsha doimiy yoki oʻzgaruvchi uchun ishlatiladigan tur haqida xulosa chiqarishi mumkin. Yuqoridagi WelcomeMessage misolida hech qanday boshlang‘ich qiymat berilmagan va shuning uchun WelcomeMessage o‘zgaruvchisining turi boshlang‘ich qiymatdan xulosa chiqarishdan ko‘ra, tur izohi bilan ko‘rsatilgan.


## Konstantalar va o'zgaruvchilarni nomlash

**Doimiy va oʻzgaruvchilar nomlari deyarli har qanday belgilarni, shu jumladan Unicode belgilarini oʻz ichiga olishi mumkin:**

```swift
let π = 3.14159
let 你好 = "你好世界"
let 🐶🐮 = "dogcow"
```

**Doimiy va oʻzgaruvchilar nomlarida boʻshliq belgilari, matematik belgilar, oʻqlar, shaxsiy foydalanish uchun Unicode skalyar qiymatlari yoki chiziq va quti chizilgan belgilar boʻlishi mumkin emas. Raqamlar nomning boshqa joylariga kiritilishi mumkin bo'lsa-da, ular raqam bilan boshlana olmaydi.**

**Muayyan turdagi doimiy yoki o'zgaruvchini e'lon qilganingizdan so'ng, uni yana bir xil nom bilan e'lon qila olmaysiz yoki uni boshqa turdagi qiymatlarni saqlash uchun o'zgartira olmaysiz. Shuningdek, siz doimiyni o'zgaruvchiga yoki o'zgaruvchini doimiyga o'zgartira olmaysiz.**

>Eslatma

>Agar siz doimiy yoki oʻzgaruvchiga zaxiralangan Swift kalit soʻzi bilan bir xil nom berishingiz kerak boʻlsa, uni nom sifatida ishlatganda kalit soʻzni teskari belgilar (```) bilan oʻrab oling. Biroq, hech qanday tanlovingiz bo'lmasa, kalit so'zlarni nom sifatida ishlatishdan saqlaning.

Mavjud o'zgaruvchining qiymatini mos keladigan turdagi boshqa qiymatga o'zgartirishingiz mumkin. Bu misolda friendlyWelcome qiymati 'Salom!'dan o'zgartirildi. 'Bonjour!'ga:

```swift
var friendlyWelcome = "Hello!"
friendlyWelcome = "Bonjour!"
// Output: friendlyWelcome is now "Bonjour!"
```

**O'zgaruvchidan farqli o'laroq, doimiy qiymat o'rnatilgandan keyin o'zgartirilmaydi. Kodingiz kompilyatsiya qilinganda shunday qilishga urinish xato deb xabar qilinadi:**

```swift
let languageName = "Swift"
languageName = "Swift++"
// This is a compile-time error: languageName cannot be changed.
// Bu kompilyatsiya vaqtidagi xato: til nomini oʻzgartirib boʻlmaydi.
```

## Konstantalar va o'zgaruvchilarni chop etish

**Siz doimiy yoki o'zgaruvchining joriy qiymatini print(_:separator:terminator:) funksiyasi bilan chop etishingiz mumkin:**

```swift
print(friendlyWelcome)
// Prints "Bonjour!"
// "Bonjour!" qaytaradı bizga
```

**print(_:separator:terminator:) funksiyasi bir yoki bir nechta qiymatlarni tegishli chiqishga chop etadigan global funksiyadir. Masalan, Xcode'da print(_:separator:terminator:) funktsiyasi o'z chiqishini Xcode 'konsol' panelida chop etadi. Ajratuvchi va terminator parametrlari standart qiymatlarga ega, shuning uchun siz ushbu funktsiyani chaqirganingizda ularni o'tkazib yuborishingiz mumkin. Odatiy bo'lib, funksiya satr uzilishini qo'shish orqali chop etadigan qatorni tugatadi. Qiymatni undan keyin qator uzilishisiz chop etish uchun boʻsh qatorni terminator sifatida oʻtkazing — masalan, print(someValue, terminator: ''). Standart qiymatlari bo'lgan parametrlar haqida ma'lumot olish uchun Standart parametr qiymatlari bo'limiga qarang.**

**Swift doimiy yoki oʻzgaruvchining nomini uzunroq satrga oʻrinbosar sifatida kiritish va Swift-dan uni shu doimiy yoki oʻzgaruvchining joriy qiymati bilan almashtirishni soʻrash uchun satr interpolyatsiyasidan foydalanadi. Ismni qavs ichiga o'rang va ochilish qavs oldidan teskari chiziq bilan qoching:**

```swift
print("The current value of friendlyWelcome is \(friendlyWelcome)")
// Printning 'FriendlyWelcome ning hozirgi qiymati - Bonjour!'
```

>Eslatma

>String interpolyatsiyasi bilan foydalanishingiz mumkin bo'lgan barcha variantlar String interpolyatsiyasida tasvirlangan.


## Izohlar

**O'zingizga eslatma yoki eslatma sifatida kodingizga bajarilmaydigan matnni kiritish uchun sharhlardan foydalaning. Kodingiz kompilyatsiya qilinganda, sharhlar Swift kompilyatori tomonidan e'tiborga olinmaydi.**

**Swift-dagi sharhlar C-dagi sharhlarga juda o'xshaydi. Bir qatorli sharhlar ikkita oldinga chiziq (//) bilan boshlanadi:**

```swift
// This is a comment.
// Bu izoh.
```

**Ko‘p satrli izohlar oldinga qiyshiq chiziqdan keyin yulduzcha (/*) bilan boshlanadi va yulduzcha va undan keyin qiyshiq chiziq (*/) bilan tugaydi:**

```swift
/* This is also a comment
but is written over multiple lines. */

/* Bu ham izoh
lekin bir nechta satrlar ustida yozilgan. */
```

C tilidagi ko'p qatorli sharhlardan farqli o'laroq, Swift-dagi ko'p qatorli sharhlar boshqa ko'p qatorli sharhlar ichiga joylashtirilishi mumkin. Siz ko'p qatorli sharhlar blokini boshlash va keyin birinchi blokda ikkinchi ko'p qatorli sharhni boshlash orqali ichki sharhlarni yozasiz. Keyin ikkinchi blok yopiladi, keyin birinchi blok:

```swift
/* This is the start of the first multiline comment.
    /* This is the second, nested multiline comment. */
This is the end of the first multiline comment. */

/* Bu birinchi ko'p qatorli sharhning boshlanishi.
    /* Bu ko'p qatorli ikkinchi sharh. */
Bu birinchi ko'p qatorli sharhning oxiri. */
```

**Ichki ko'p qatorli sharhlar, hatto kodda ko'p qatorli sharhlar mavjud bo'lsa ham, katta kod bloklarini tez va oson izohlash imkonini beradi.**

## Nuqta-vergul

**Ko'pgina boshqa tillardan farqli o'laroq, Swift kodingizdagi har bir bayonotdan keyin nuqta-vergul (;) qo'yishingizni talab qilmaydi, lekin agar xohlasangiz, buni qilishingiz mumkin. Biroq, bitta satrda bir nechta alohida bayonotlarni yozmoqchi bo'lsangiz, nuqta-vergul kerak bo'ladi:**

```swift
let cat = "🐱"; print(cat)
// Prints "🐱"
```

## Butun sonlar

**_Butun sonlar_ kasr komponenti boʻlmagan butun sonlardir, masalan, 42 va -23. Butun sonlar *imzolangan* (musbat, nol yoki manfiy) yoki *belgisiz* (musbat yoki nol) bo'ladi.**

**Swift 8, 16, 32 va 64 bitli shakllarda imzolangan va belgisiz butun sonlarni taqdim etadi. Bu butun sonlar C ga o'xshash nomlash konventsiyasiga amal qiladi, ya'ni 8 bitli belgisiz butun son UInt8 turiga va 32 bitli imzolangan butun son Int32 tipiga ega. Swift-dagi barcha turlar singari, bu butun sonlar ham bosh harf bilan yozilgan nomlarga ega.**

### Butun son chegaralari

**Har bir butun son turining minimal va maksimal qiymatlariga uning min va maksimal xossalari bilan kirishingiz mumkin:**

```swift
let minValue = UInt8.min  // minValue 0 ga teng va UInt8 turiga ega
let maxValue = UInt8.max  // maxValue 255 ga teng va UInt8 turiga ega
```

**Ushbu xususiyatlarning qiymatlari tegishli o'lchamdagi raqamlar turiga ega (masalan, yuqoridagi misolda UInt8) va shuning uchun bir xil turdagi boshqa qiymatlar bilan bir qatorda ifodalarda ishlatilishi mumkin.**

## Int 

**Ko'pgina hollarda, kodingizda foydalanish uchun ma'lum bir butun son hajmini tanlashingiz shart emas. Swift joriy platformaning mahalliy so'z hajmi bilan bir xil o'lchamga ega bo'lgan qo'shimcha Int butun son turini taqdim etadi:**

- 32-bitli platformada Int Int32 bilan bir xil o'lchamga ega.
- 64-bitli platformada Int Int64 bilan bir xil o'lchamga ega.

**Agar ma'lum bir butun son o'lchami bilan ishlashingiz kerak bo'lmasa, kodingizdagi butun son qiymatlari uchun har doim Int dan foydalaning. Bu kodning izchilligi va o'zaro ishlashiga yordam beradi. Hatto 32-bitli platformalarda ham Int har qanday qiymatni -2,147,483,648 va 2,147,483,647 oralig'ida saqlashi mumkin va ko'p sonli diapazonlar uchun etarlicha katta.**

## UInt

**Swift, shuningdek, joriy platformaning mahalliy so'z hajmi bilan bir xil o'lchamga ega bo'lgan UInt belgisisiz butun son turini taqdim etadi:**

- 32-bitli platformada UInt UInt32 bilan bir xil o'lchamda.
- On a 64-bit platform, UInt is the same size as UInt64.

>Eslatma

>UInt-dan faqat platformaning mahalliy so'z o'lchami bilan bir xil o'lchamdagi belgisiz butun son turi kerak bo'lganda foydalaning. Agar bunday bo'lmasa, saqlanadigan qiymatlar manfiy emasligi ma'lum bo'lsa ham, Int afzal ko'riladi. Butun son qiymatlari uchun Int dan doimiy foydalanish kodning o'zaro ishlashiga yordam beradi, turli xil sonlar turlari o'rtasida konvertatsiya qilish zaruratini oldini oladi va 'Tip xavfsizligi va tur xulosasi' bo'limida tavsiflanganidek, butun son turiga mos keladi.

## Floating-Point Numbers / Float sonlar

**_Suzuvchi nuqtali sonlar_ kasr komponentli raqamlardir, masalan, 3,14159, 0,1 va -273,15.**

**Suzuvchi nuqtali tiplar butun sonli turlarga qaraganda ancha kengroq qiymatlar diapazonini ifodalashi mumkin va Int da saqlanadigandan ancha katta yoki kichikroq raqamlarni saqlashi mumkin. Swift ikkita imzolangan suzuvchi nuqtali raqamlar turini taqdim etadi:**

- Double 64-bitli suzuvchi nuqtali raqamni ifodalaydi.
- Float 32 bitli suzuvchi nuqtali raqamni ifodalaydi.

>Eslatma

>Double-ning aniqligi kamida 15 o'nlik raqamga ega, Floatning aniqligi esa 6 o'nlik raqamdan kam bo'lishi mumkin. Foydalanish uchun mos suzuvchi nuqta turi sizning kodingizda ishlashingiz kerak bo'lgan qiymatlar tabiati va diapazoniga bog'liq. Ikkala tur ham mos keladigan holatlarda Double-ga afzallik beriladi.

## Xavfsizlik turi va xulosa chiqarish

**Swift - bu *turdagi xavfsiz* til. Xavfsiz til turi sizni kodingiz bilan ishlashi mumkin bo'lgan qiymat turlari haqida aniq bo'lishga undaydi. Agar kodingizning bir qismi stringni talab qilsa, siz uni Int ni xato bilan o'tkaza olmaysiz.**

**Swift turi xavfsiz bo'lganligi sababli, u kodingizni kompilyatsiya qilishda turdagi tekshiruvlarni amalga oshiradi va har qanday mos kelmaydigan turlarni xato deb belgilaydi. Bu sizga rivojlanish jarayonida xatolarni imkon qadar erta aniqlash va tuzatish imkonini beradi.**

**Turni tekshirish har xil turdagi qiymatlar bilan ishlashda xatolardan qochishga yordam beradi. Biroq, bu siz e'lon qilgan har bir doimiy va o'zgaruvchining turini belgilashingiz kerak degani emas. Agar sizga kerak bo'lgan qiymat turini ko'rsatmasangiz, Swift tegishli turni ishlab chiqish uchun tur xulosasidan foydalanadi. Turi xulosasi kompilyatorga kodingizni kompilyatsiya qilganda ma'lum bir ifoda turini avtomatik ravishda siz taqdim etgan qiymatlarni tekshirish orqali chiqarish imkonini beradi.**

**Turi haqidagi xulosa tufayli Swift C yoki Objective-C kabi tillarga qaraganda kamroq turdagi deklaratsiyalarni talab qiladi. Konstantalar va o'zgaruvchilar hali ham aniq yoziladi, lekin ularning turini belgilash bo'yicha ishning katta qismi siz uchun bajariladi.**

**Turi xulosasi, ayniqsa, siz doimiy yoki o'zgaruvchini boshlang'ich qiymati bilan e'lon qilganingizda foydalidir. Bu ko'pincha siz e'lon qilgan nuqtada doimiy yoki o'zgaruvchiga so'zma-so'z qiymatni (yoki literal) belgilash orqali amalga oshiriladi. (To'g'ridan-to'g'ri qiymat - bu to'g'ridan-to'g'ri manba kodingizda ko'rinadigan qiymat, masalan, quyidagi misollarda 42 va 3,14159.)**

**Misol uchun, agar siz yangi konstantaga uning turini aytmasdan 42 ning so‘zma-so‘z qiymatini belgilasangiz, Swift siz doimiyni Int bo‘lishini xohlaysiz degan xulosaga keladi, chunki siz uni butun songa o‘xshash raqam bilan ishga tushirgansiz:**


```swift
let meaningOfLife = 42
// meaningOfLife Int tipidagi deb taxmin qilinadi
```

**Xuddi shunday, agar siz suzuvchi nuqtali harf uchun turni belgilamasangiz, Swift Double yaratmoqchi ekanligingizni taxmin qiladi:**

```swift
let pi = 3.14159
// pi Double turiga tegishli deb taxmin qilinadi
```

**Swift suzuvchi nuqtali sonlar turini chiqarishda har doim Double (Float o'rniga) ni tanlaydi.**

**Agar ifodada butun son va suzuvchi nuqtali harflarni birlashtirsangiz, kontekstdan Double turi aniqlanadi:**

```swift
let anotherPi = 3 + 0.14159
// anotherPi ham Double turiga tegishli deb taxmin qilinadi
```

**3 ning literal qiymati oʻz-oʻzidan aniq turga ega emas va shuning uchun qoʻshimchaning bir qismi sifatida suzuvchi nuqtali literal mavjudligidan Double ning tegishli chiqish turi aniqlanadi.**

## Raqamli harflar

**Butun sonlar quyidagicha yozilishi mumkin:**

- Prefikssiz (_decimal_) kasrli raqam

- Ikkilik (_binary_) raqam, 0b prefiksi bilan

- Sakkizli (_octal_) raqam, 0o prefiksi bilan

- 0x prefiksi bilan oʻn oltilik raqam (_hexadecimal_)

**Ushbu butun sonli harflarning barchasi o'nlik 17 qiymatiga ega:**

```swift
let decimalInteger = 17
let binaryInteger = 0b10001       // 17 in binary notation (Ikkilik yozuvda 17)
let octalInteger = 0o21           // 17 in octal notation (17 sakkizlik yozuvda)
let hexadecimalInteger = 0x11     // 17 in hexadecimal  notation (17 o'n oltilik tizimda)
```

**Suzuvchi nuqtali harflar o'nli (prefikssiz) yoki o'n oltilik (0x prefiksi bilan) bo'lishi mumkin. Ular har doim kasrning ikkala tomonida raqam (yoki o'n oltilik raqam) bo'lishi kerak. O'nlik suzuvchilar ixtiyoriy ko'rsatkichga ham ega bo'lishi mumkin, ular katta yoki kichik e bilan ko'rsatilgan; o'n oltilik suzuvchilar katta yoki kichik p bilan ko'rsatilgan darajaga ega bo'lishi kerak.**

**Ko'rsatkichi x bo'lgan o'nlik sonlar uchun asosiy raqam 10ˣ ga ko'paytiriladi:**

- 1,25e2 1,25 x 10² yoki 125,0 ni bildiradi.

- 1,25e-2 1,25 x 10⁻² yoki 0,0125 ni bildiradi.

**Ko'rsatkichi x bo'lgan o'n oltilik sonlar uchun asosiy raqam 2ˣ ga ko'paytiriladi:**

- 0xFp2 15 x 2² yoki 60,0 degan ma'noni anglatadi.

- 0xFp-2 15 x 2⁻² yoki 3,75 degan ma'noni anglatadi.

**Ushbu suzuvchi nuqtali harflarning barchasi 12,1875 o'nlik qiymatiga ega:**

```swift
let decimalDouble = 12.1875
let exponentDouble = 1.21875e1
let hexadecimalDouble = 0xC.3p0
```

**Raqamli harflar o'qishni osonlashtirish uchun qo'shimcha formatlashni o'z ichiga olishi mumkin. Butun sonlar ham, suzuvchi raqamlar ham qo‘shimcha nol bilan to‘ldirilishi mumkin va o‘qilishiga yordam berish uchun pastki chiziqdan iborat bo‘lishi mumkin. Hech bir formatlash turi literalning asosiy qiymatiga ta'sir qilmaydi:**

```swift
let paddedDouble = 000123.456
let oneMillion = 1_000_000
let justOverOneMillion = 1_000_000.000_000_1
```

## Raqamli turdagi konvertatsiya

**Kodingizdagi barcha umumiy maqsadli butun son konstantalari va o'zgaruvchilari uchun Int turidan foydalaning, hatto ular manfiy emasligi ma'lum bo'lsa ham. Kundalik vaziyatlarda standart tamsayı turidan foydalanish butun son konstantalari va o'zgaruvchilar kodingizda darhol o'zaro ishlashini va butun son literal qiymatlari uchun taxmin qilingan turga mos kelishini anglatadi.**

**Boshqa butun son turlaridan faqat tashqi manbadan aniq oʻlchamdagi maʼlumotlar yoki unumdorlik, xotiradan foydalanish yoki boshqa zarur optimallashtirish uchun topshiriq uchun zarur boʻlganda foydalaning. Bunday holatlarda aniq o'lchamdagi turlardan foydalanish har qanday tasodifiy qiymatdan oshib ketishini aniqlashga yordam beradi va foydalanilayotgan ma'lumotlarning tabiatini bilvosita hujjatlashtiradi.**

### Butun son konvertatsiyasi

**Butun doimiy yoki o'zgaruvchida saqlanishi mumkin bo'lgan raqamlar diapazoni har bir raqamli tur uchun farq qiladi. Int8 doimiysi yoki o'zgaruvchisi -128 va 127 oralig'idagi raqamlarni saqlashi mumkin, UInt8 doimiysi yoki o'zgaruvchisi esa 0 dan 255 gacha bo'lgan raqamlarni saqlashi mumkin. Konstanta yoki o'lchamli butun son turidagi o'zgaruvchiga sig'maydigan raqam xatolik sifatida xabar qilinadi. kodingiz tuzilganda:**

```swift
let cannotBeNegative: UInt8 = -1
// UInt8 manfiy raqamlarni saqlay olmaydi, shuning uchun bu xato haqida xabar beradi
let tooBig: Int8 = Int8.max + 1
// Int8 maksimal qiymatdan kattaroq raqamni saqlay olmaydi,
// va shuning uchun bu ham xato haqida xabar beradi
```

**Har bir raqamli tur turli qiymatlar diapazonini saqlashi mumkinligi sababli, har bir holatda raqamli turga o'zgartirishni tanlashingiz kerak. Ushbu qo'shilish yondashuvi yashirin konvertatsiya xatolarining oldini oladi va kodingizda turdagi konvertatsiya qilish niyatlarini aniq ko'rsatishga yordam beradi.**

**Bitta ma'lum raqam turini boshqasiga aylantirish uchun siz kerakli turdagi yangi raqamni mavjud qiymat bilan ishga tushirasiz. Quyidagi misolda twoThousand doimiysi UInt16 turiga, doimiysi esa UInt8 turiga tegishli. Ularni to'g'ridan-to'g'ri qo'shib bo'lmaydi, chunki ular bir xil emas. Buning o'rniga, bu misol bir qiymati bilan ishga tushirilgan yangi UInt16 yaratish uchun UInt16(bir) ni chaqiradi va asl qiymati o'rniga ushbu qiymatdan foydalanadi:**

```swift
let twoThousand: UInt16 = 2_000
let one: UInt8 = 1
let twoThousandAndOne = twoThousand + UInt16(one)
```

**Qo'shishning ikkala tomoni endi UInt16 turiga ega bo'lgani uchun qo'shishga ruxsat beriladi. Chiqish konstantasi (ikkiMingOna) UInt16 turiga mos keladi, chunki u ikkita UInt16 qiymatlarining yig'indisidir.**

**SomeType(ofInitialValue) Swift tipidagi initsializatorni chaqirish va boshlang'ich qiymatni o'tkazishning standart usulidir. Sahna ortida UInt16 UInt8 qiymatini qabul qiluvchi ishga tushirgichga ega va shuning uchun bu ishga tushirgich mavjud UInt8 dan yangi UInt16 yaratish uchun ishlatiladi. Biroq, bu erda hech qanday turga o'ta olmaysiz - bu UInt16 ishga tushiruvchini taqdim etadigan tur bo'lishi kerak. Yangi turlarni (jumladan, o'zingizning turdagi ta'riflaringizni) qabul qiluvchi ishga tushirgichlarni taqdim etish uchun mavjud turlarni kengaytirish Kengaytmalar bo'limida yoritilgan.**

### Butun son va suzuvchi nuqta konvertatsiyasi

**Butun va suzuvchi nuqtali sonli turlar orasidagi konvertatsiyalar aniq bo'lishi kerak:**

```swift
let three = 3
let pointOneFourOneFiveNine = 0.14159
let pi = Double(three) + pointOneFourOneFiveNine
// pi 3,14159 ga teng va Double tipidagi deb taxmin qilinadi
```

**Bu yerda doimiy uchlikning qiymati Double tipidagi yangi qiymat yaratish uchun ishlatiladi, shuning uchun qo'shimchaning ikkala tomoni bir xil turdagi bo'ladi. Ushbu konvertatsiya amalga oshirilmasa, qo'shishga ruxsat berilmaydi.**

**Suzuvchi nuqtadan butun songa o'tkazish ham aniq bo'lishi kerak. Butun son turi Double yoki Float qiymati bilan ishga tushirilishi mumkin:**

```swift
let integerPi = Int(pi)
// integerPi 3 ga teng va Int tipidagi deb hisoblanadi
```

**Yangi butun qiymatni shu tarzda ishga tushirish uchun foydalanilganda suzuvchi nuqta qiymatlari har doim kesiladi. Bu 4,75 4 ga, -3,9 esa -3 ga aylanishini anglatadi.**

>Eslatma

>Raqamli konstantalar va o'zgaruvchilarni birlashtirish qoidalari raqamli harflar uchun qoidalardan farq qiladi. Literal qiymat 3 ni to'g'ridan-to'g'ri 0,14159 ga qo'shish mumkin, chunki son harflari o'z-o'zidan aniq turga ega emas. Ularning turi faqat kompilyator tomonidan baholanganda aniqlanadi.

## Taxalluslarni kiriting / Type Aliases

**Turning *taxalluslari* mavjud tur uchun muqobil nomni belgilaydi. Siz turi taxalluslarini typealias kalit so'zi bilan aniqlaysiz.**

**Mavjud turga kontekstga mos keladigan nom bilan murojaat qilmoqchi bo'lsangiz, masalan, tashqi manbadan ma'lum o'lchamdagi ma'lumotlar bilan ishlashda turdagi taxalluslar foydali bo'ladi:**

```swift
typealias AudioSample = UInt16
```

**Taxallus turini aniqlaganingizdan so'ng, taxallusdan asl nomdan foydalanishingiz mumkin bo'lgan har qanday joyda foydalanishingiz mumkin:**

```swift
var maxAmplitudeFound = AudioSample.min
// maxAmplitudeFound endi 0 ga teng
```

**Bu yerda AudioSample UInt16 uchun taxallus sifatida aniqlanadi. Bu taxallus bo‘lgani uchun AudioSample.min ga qo‘ng‘iroq maxAmplitudeFound o‘zgaruvchisi uchun 0 boshlang‘ich qiymatini ta’minlovchi UInt16.min ni chaqiradi.**

## Booleanlar / Booleans

**Swift Bool deb nomlangan asosiy Boolean turiga ega. Mantiqiy qiymatlar mantiqiy deb ataladi, chunki ular faqat haqiqat yoki yolg'on bo'lishi mumkin. Swift ikkita mantiqiy doimiy qiymatlarni beradi, haqiqiy va noto'g'ri:**


```swift
let orangesAreOrange = true
let turnipsAreDelicious = false
```

**apelsinlarAreOrange va sholg'omlarAreDelicious turlari Bool deb nomlandi, chunki ular mantiqiy harfiy qiymatlar bilan ishga tushirilgan. Yuqoridagi Int va Double-da bo'lgani kabi, doimiy yoki o'zgaruvchilarni yaratishingiz bilanoq ularni rost yoki noto'g'ri qilib qo'ysangiz, ularni Bool deb e'lon qilishingiz shart emas. Turi haqida xulosa qilish Swift kodini turi allaqachon ma'lum bo'lgan boshqa qiymatlar bilan doimiy yoki o'zgaruvchilarni ishga tushirganda yanada ixcham va o'qilishi mumkin bo'lishiga yordam beradi.**

**Mantiqiy qiymatlar, ayniqsa, if iborasi kabi shartli iboralar bilan ishlaganingizda foydalidir:**

```swift
if turnipsAreDelicious {
    print("Mmm, tasty turnips!")
} else {
    print("Eww, turnips are horrible.")
}
// Prints "Eww, turnips are horrible."
```

**If iborasi kabi shartli bayonotlar Boshqarish oqimida batafsilroq yoritilgan.**

**Swift turi xavfsizligi mantiqiy bo'lmagan qiymatlarni Bool o'rniga qo'yishdan saqlaydi. Quyidagi misol kompilyatsiya vaqtidagi xato haqida xabar beradi:**

```swift
let i = 1
if i {
    // bu misol kompilyatsiya qilinmaydi va xato haqida xabar beradi
}
```

**Biroq, quyidagi muqobil misol amal qiladi:**

```swift
let i = 1
if i == 1 {
    // bu misol muvaffaqiyatli kompilyatsiya qilinadi
}
```

**i == 1 taqqoslash natijasi Bool turiga tegishli, shuning uchun bu ikkinchi misol tur tekshiruvidan o'tadi. i == 1 kabi taqqoslashlar Asosiy operatorlarda muhokama qilinadi.**

**Swift-dagi boshqa turdagi xavfsizlik misollarida bo'lgani kabi, bu yondashuv tasodifiy xatolardan qochadi va kodning ma'lum bir qismining maqsadi har doim aniq bo'lishini ta'minlaydi.**

## Tuplar / Tuples

**_Kortejlar_ bir nechta qiymatlarni bitta birikma qiymatga guruhlaydi. Kortej ichidagi qiymatlar har qanday turdagi bo'lishi mumkin va bir-biri bilan bir xil turdagi bo'lishi shart emas.**

**Ushbu misolda (404, 'Not Found') HTTP holat kodini tavsiflovchi kortejdir. HTTP holat kodi veb-sahifani so'raganingizda veb-server tomonidan qaytariladigan maxsus qiymatdir. Agar mavjud bo'lmagan veb-sahifani so'rasangiz, 404 'Not Found' holati kodi qaytariladi.**

```swift
let http404Error = (404, "Not Found")
// http404Xato turi (Int, String) va teng (404, "Not Found")
```

**(404, 'Topilmadi') kortej HTTP holat kodiga ikkita alohida qiymat berish uchun Int va Stringni birlashtiradi: raqam va odam o'qiy oladigan tavsif. Uni 'turdagi kortej (Int, String)' deb ta'riflash mumkin.**

**Siz har qanday turdagi almashtirishdan kortejlar yaratishingiz mumkin va ular siz xohlagancha turli xil turlarni o'z ichiga olishi mumkin. Sizni tipdagi kortejga (Int, Int, Int) yoki (String, Bool) yoki sizga kerak bo'lgan boshqa almashtirishga ega bo'lishingizga hech narsa to'sqinlik qilmaydi.**

**Siz kortej tarkibini alohida konstantalar yoki o'zgaruvchilarga ajratishingiz mumkin, keyin odatdagidek kirishingiz mumkin:**

```swift
let (statusCode, statusMessage) = http404Error
print("The status code is \(statusCode)")
// Prints "The status code is 404"
print("The status message is \(statusMessage)")
// Prints "The status message is Not Found"
```

**Agar sizga faqat bir nechta kortej qiymatlari kerak bo'lsa, kortejni parchalashda pastki chiziq (_) bilan uning qismlariga e'tibor bermang:**

```swift
let (justTheStatusCode, _) = http404Error
print("The status code is \(justTheStatusCode)")
// Prints "The status code is 404"
```

**Shu bilan bir qatorda, noldan boshlanadigan indeks raqamlari yordamida kortejdagi alohida element qiymatlariga kiring:**

```swift
print("The status code is \(http404Error.0)")
// Prints "The status code is 404"
print("The status message is \(http404Error.1)")
// Prints "The status message is Not Found"
```

**Kortej aniqlanganda siz kortejdagi alohida elementlarni nomlashingiz mumkin:**

```swift
let http200Status = (statusCode: 200, description: "OK")
```

**Agar siz kortejdagi elementlarga nom bersangiz, ushbu elementlarning qiymatlariga kirish uchun element nomlaridan foydalanishingiz mumkin:**

```swift
print("The status code is \(http200Status.statusCode)")
// Prints "The status code is 200"
print("The status message is \(http200Status.description)")
// Prints "The status message is OK"
```

**Kortejlar, ayniqsa, funksiyalarning qaytish qiymatlari sifatida foydalidir. Veb-sahifani olishga harakat qiladigan funksiya sahifani qidirishning muvaffaqiyatli yoki muvaffaqiyatsizligini tasvirlash uchun (Int, String) kortej turini qaytarishi mumkin. Har biri boshqa turdagi ikkita alohida qiymatga ega kortejni qaytarish orqali funktsiya faqat bitta turdagi bitta qiymatni qaytarishdan ko'ra uning natijasi haqida ko'proq foydali ma'lumot beradi. Qo'shimcha ma'lumot olish uchun Ko'p qaytariladigan qiymatlarga ega funktsiyalarga qarang.**

>Eslatma

>Kortejlar tegishli qiymatlarning oddiy guruhlari uchun foydalidir. Ular murakkab ma'lumotlar tuzilmalarini yaratish uchun mos emas. Agar sizning ma'lumotlar strukturangiz murakkabroq bo'lsa, uni kortej sifatida emas, balki sinf yoki tuzilma sifatida modellashtiring. Qo'shimcha ma'lumot olish uchun 'Tuzilmalar va sinflar' ga qarang.
