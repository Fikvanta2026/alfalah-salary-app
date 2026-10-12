AL-FALAH SALARY APP  (installable web app - Android + iPhone)
==============================================================

Ye folder aapke maujooda portal ke upar ek "app wrapper" hai. Salary data, login, Google Sheet - sab
pehle jaise Apps Script se hi chalega. Is folder me kuch secret nahi hai (sirf aapka /exec link, jo staff ko
waise bhi dena hota hai).

PART 1 - GITHUB PAR DAALNA (ek baar, ~5 minute)
1. github.com par login karo > top-right "+" > "New repository".
2. Repository name:  alfalah-salary-app     Visibility: PUBLIC (free GitHub Pages ke liye zaroori)
   > "Create repository".
3. Naye repo me "uploading an existing file" link dabao.
   Is folder ki SAARI cheezein drag-drop karo:  index.html, manifest.webmanifest, sw.js  aur  icons  folder.
   (icons folder ke andar ki 5 png files bhi upload honi chahiye.)  > "Commit changes".
4. Repo me  Settings > Pages  >  "Build and deployment":
   Source = "Deploy from a branch",  Branch = main,  Folder = / (root)  > Save.
5. 1-2 minute baad upar ek link aayega:
        https://YOURUSERNAME.github.io/alfalah-salary-app/
   Yahi aapke staff ka APP LINK hai. (Apps Script wala /exec link staff ko mat do.)

PART 2 - STAFF APP INSTALL KAISE KARE
ANDROID (Chrome):
   App link kholo > neeche "Install Al-Falah Salary app" aayega > Install.
   (Na aaye to Chrome menu  ⋮  > "Install app" ya "Add to Home screen".)
IPHONE (Safari):
   App link Safari me kholo > neeche Share button (square + arrow) > "Add to Home Screen" > Add.
   Home screen par logo wala icon aa jayega.

PART 3 - STAFF KO BHEJNE KA MESSAGE (WhatsApp)
   "Al-Falah Salary Slip App install karne ke liye ye link phone me kholo:
    https://YOURUSERNAME.github.io/alfalah-salary-app/
    Android: Install dabao.  iPhone: Safari me Share > Add to Home Screen.
    Pehli baar login: Employee Code + temporary password, phir apna naya password banao."

ZAROORI BAATEN
- Portal me kuch badalna ho (Index.html / Code.gs) to Apps Script me  Deploy > Manage deployments > pencil >
  "New version"  se deploy karo - /exec link same rehta hai, to is wrapper me kuch nahi badalna padta.
  Agar kabhi bilkul NAYA deployment (naya link) banao, to index.html me  EXEC_URL  line me naya link daalo
  aur GitHub par index.html dobara upload karo.
- "Keep me signed in" login har jagah alag save hota hai: browser me kiya login aur installed app ka login
  alag-alag hote hain. App me ek baar login karna hoga, phir 15 din yaad rahega.
- Internet na ho to app "No internet connection" dikhayega aur net aate hi khud khul jayega.
  Salary data kabhi phone me save nahi hota.

JO MAINE ASLI PHONE PAR TEST NAHI KIYA (aap pehle 1-2 staff ke phone par check kar lena)
1. Installed app ke andar "Print / Save PDF" button. Agar kisi phone par na chale to staff slip screen se
   screenshot le sakte hain, ya "Open in browser" se portal browser me khol kar print karein.
2. iPhone me "Keep me signed in" - iOS kabhi kabhi andar wale frame ka storage jaldi saaf kar deta hai.
   Aisa hua to bas dobara login poochega (kuch kharab nahi hota).
3. Google ka "created by a Google Apps Script user" wala grey bar installed app me dikhega ya nahi.

APK (Android file) CHAHIYE TO
   Jab app link chal jaye, https://www.pwabuilder.com par app link daalo > Android > "Download" se APK ban jata hai
   jo WhatsApp/Drive se bheji ja sakti hai. (Play Store par daalna ho to Google ka ek baar $25 fee lagta hai.)
