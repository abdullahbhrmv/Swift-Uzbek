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

let maximumNumberOfLoginAttempts = 10
var currentLoginAttempt = 0

