# Health Calculator

বাংলা, সবুজ-সাদা, Progressive Web App (PWA) ভিত্তিক স্বাস্থ্য ক্যালকুলেটর। মোবাইল ব্রাউজার থেকে ইনস্টল করা যায়; প্রথমবার WHO ডেটা লোড হলে মূল অ্যাপ ও ডেটা অফলাইনে ক্যাশ হবে।

## Modules
- শিশু ও কিশোরের বৃদ্ধি (০–১৯ বছর): বয়স ও লিঙ্গ অনুযায়ী WHO median height/weight/BMI reference; প্রকৃত মাপ দিলে LMS Z-score screening.
- প্রাপ্তবয়স্ক: বয়স, ওজন ও প্রকৃত উচ্চতা দিয়ে BMI এবং ঐ উচ্চতার জন্য BMI 18.5–24.9 ওজনের গাণিতিক পরিসর।
- গর্ভবতী মা: গর্ভকাল, উচ্চতা, গর্ভধারণ-পূর্ব ও বর্তমান ওজন থেকে BMI ও ওজন পরিবর্তনের হিসাব।

## WHO data and calculation notes
- ০–৫ বছর: WHO Child Growth Standards 2006 LMS tables; height-for-age, weight-for-age, weight-for-length/height. WHO standard অনুযায়ী ২৪ মাসের কম বয়সে recumbent length, ২৪ মাস বা বেশি বয়সে standing height ব্যবহার করতে হবে.
- ৫–১৯ বছর: WHO Growth Reference 2007 LMS tables for height-for-age and BMI-for-age; weight-for-age reference is available only through 10 years.
- Z-score uses the LMS formula. Under-five weight-for-length/height is assessed from the corresponding WHO table when actual weight and length/height are supplied.
- Reference medians are population references, not an individual child's target or a substitute for serial growth-chart review.
- Age and weight alone cannot determine a person's actual or ideal height or BMI. Adult BMI is therefore calculated only when measured height is supplied.
- Pregnancy module reports arithmetic only; it does not classify risk or prescribe a weight-gain target.

## Clinical safety
- MUAC screening cut-offs are not implemented in this version. Use the applicable national protocol and clinical assessment.
- Educational and screening support only; not a diagnostic or treatment tool. Check measurement technique, age accuracy and clinical context before making decisions.

## Sources
- WHO Child Growth Standards: https://www.who.int/tools/child-growth-standards/
- WHO Growth Reference 5–19 years: https://www.who.int/tools/growth-reference-data-for-5to19-years/
- LMS data tables used in this app were sourced from public implementations that identify WHO source tables: RCPCH rcpchgrowth-python and SEHATI WHO LMS extraction. See source metadata in `data/who-growth-data.json`.

## Deployment
The GitHub Actions workflow in `.github/workflows/deploy.yml` publishes the static app to GitHub Pages on pushes to `main`. In repository Settings → Pages, select **GitHub Actions** as the build and deployment source if GitHub Pages has not been enabled yet.

## Offline use
Open the deployed app once while connected so the service worker can cache `index.html`, `manifest.webmanifest`, and `data/who-growth-data.json`. Then use the installed app offline.
