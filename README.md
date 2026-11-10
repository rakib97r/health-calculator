# Health Calculator

বাংলা, সবুজ-সাদা, অফলাইন-সক্ষম Health Calculator।

স্লোগান: **সুস্থ জীবনের স্মার্ট সহায়ক**

## Modules
- শিশু বৃদ্ধি (০–৫ বছর): জন্মতারিখ, লিঙ্গ এবং ঐচ্ছিক MUAC।
- প্রাপ্তবয়স্ক: বয়স, ওজন এবং উচ্চতা দিলে BMI।
- গর্ভবতী মা: গর্ভকাল, উচ্চতা, গর্ভধারণ-পূর্ব ও বর্তমান ওজন থেকে BMI ও ওজন পরিবর্তন।

## Clinical safety
- বয়স ও ওজন দিয়ে কোনো ব্যক্তির প্রকৃত উচ্চতা বা BMI নির্ণয় করা যায় না। তাই উচ্চতা অনুমান করে দেখানো হয় না।
- শিশুর বয়স থেকে ব্যক্তিগত ওজন/উচ্চতা নির্ধারণ করা যায় না। WHO sex-specific growth reference tables ও সঠিক মাপ ছাড়া কোনো median/classification দেখানো হবে না।
- MUAC cut-offs in children 6–59 months: <115 mm indicates severe acute malnutrition risk; 115 to <125 mm indicates moderate acute malnutrition risk. Clinical assessment and referral are required.
- Pregnancy weight-gain assessment needs pre-pregnancy BMI, gestational age, singleton/multiple pregnancy status and applicable national guidance. Current screen reports arithmetic values only, not risk classification or targets.
- Educational aid only; not a diagnostic or treatment tool.

## Sources for clinical data integration
- WHO Child Growth Standards: https://www.who.int/tools/child-growth-standards/
- WHO 5–19 years Growth Reference: https://www.who.int/tools/growth-reference-data-for-5to19-years/
- Bangladesh National Guidelines for Maternal Nutrition: https://nnsop.gov.bd/storage/files/resource-2025-02-24-67bc0a9551ca0.pdf

## Run locally
Serve this directory with any static web server. Core files are cached for offline use.

## Android
Run `npm install`, then `npx cap add android`, then `npx cap sync android`. Open the Android project in Android Studio and build a debug APK.
