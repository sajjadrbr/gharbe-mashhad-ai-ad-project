# بررسی LoRAهای SDXL برای ظاهر سه‌بعدی کارتونی سینمایی — ۲۰۲۶-۱۰-۲۱

**وضعیت:** تحقیق مقایسه‌ای، بدون تست تصویری روی سیستم کاربر. هیچ ادعای «بهترین» یا «قطعی» نداریم.

## مسئله
بخش داخلی فست‌فودِ تیزر «غرب مشهد» باید از نظر **آشپزخانه، سوسیس‌های شخصیت‌دار، پتی برگر، سرآشپز، میز آماده‌سازی و تیم پشت‌صحنه** همگی حس انیمیشن سه‌بعدی سینمایی یکپارچه داشته باشند. صرف پرتره کارتونی کافی نیست. کاربر علاقه‌مند به زیبایی‌شناسی فیلم‌های پیکسار است و از دانلودهای بزرگ غیرضروری پرهیز می‌کند.

## گزینه‌های بررسی‌شده

| مدل | فایل اصلی | نوع/حجم | سازگاری | ابهام و نکات |
|---|---|---|---|---|
| thejagstudio/3d-animation-style-sdxl | 3D_Animation_Style-000009.safetensors | LoRA ~228.68 MB | SDXL Base 1.0 | گالری موجود ولی کارت مدل شرح آموزش و مثال پرامپت معتبر ندارد؛ اثر بر محیط فست‌فود آزمایش نشده؛ مجوز bespoke با allowCommercialUse=Image و allowNoCredit=False، کاربرد در ویدئوی تجاری نیازمند بررسی |
| ntc-ai/SDXL-LoRA-slider.pixar-style | pixar-style.safetensors | Style slider LoRA **8.79 MB** | SDXL Base 1.0 | هدف صریحاً «pixar-style»، با trigger pixar-style و نمونه‌مقایسه‌های شدت. مجوز MIT ثبت‌شده؛ روی آشپزخانه و food characters هنوز تست نشده. Slider کنترل شدت سبک است و به‌تنهایی کیفیت نهایی را تضمین نمی‌کند. |
| yyw666/pixar-sdxl-lora | pixar-sdxl-lora.safetensors + embedding | LoRA ~46.7 MB به‌علاوه embedding کوچک | SDXL Base 1.0 | کارت مدل صریحاً نیاز به embedding جداگانه برای نتایج مرتبط را می‌گوید؛ نمونه‌ها عمدتاً کاراکتر/کودکان هستند. مجوز openrail++. اولویت پایین‌تر برای کل صحنهٔ فست‌فود. |
| animte/pixar-sdxl-lora | PixarXL.safetensors | LoRA ~228 MB | SDXL Base 1.0 | خود سازنده استفادهٔ اصلی را تبدیل پرتره‌های عکس به کاراکتر کارتونی ذکر کرده؛ برای محیط/food scene کمتر مرتبط است. |

## منابع اصلی
- https://huggingface.co/thejagstudio/3d-animation-style-sdxl
- https://huggingface.co/ntc-ai/SDXL-LoRA-slider.pixar-style
- https://huggingface.co/ntc-ai/SDXL-LoRA-slider.pixar-style/tree/main
- https://huggingface.co/yyw666/pixar-sdxl-lora
- https://huggingface.co/animte/pixar-sdxl-lora

## پیشنهاد مرحله بعد (مشروط)
- اگر LoRA 3D Animation Style SDXL قبلاً دانلود شده است: **ابتدا بدون دانلود تازه** یک فریم تست همان Shot A با DreamShaper XL و LoRA موجود بسازیم؛ خروجی را در کنار مرجع سبک بررسی کنیم.
- اگر هنوز دانلود نشده: از لحاظ هزینه دانلود و مجوز، گزینهٔ **NTC Pixar-style Slider حدود 8.79 MB** برای یک تست اولیه مناسب‌تر است؛ نه لزوماً بهتر از لحاظ کیفیت. ابتدا گالری را ببینیم.
- از دانلود هر دو یا چند LoRA همزمان پرهیز شود.
- برای داوری منصفانه: یک پرامپت فست‌فود یکسان، رزولوشن یکسان، seed یکسان و فقط LoRA/weight متفاوت.
- صرف SDXL بودن دلیل تأیید کیفیت یا امنیت حقوقی نیست. مجوز checkpoint پایه و محدودیت‌های برند/IP هم باید رعایت شوند.
- **در این تحقیق هیچ مدل جدید دانلود نشده و هیچ رندری اجرا نشده است.** وضعیت دانلود قبلی LoRA باید از کاربر پرسیده/تأیید شود.

## جمع‌بندی
3D Animation Style SDXL **اثباتاً نزدیک‌ترین به Pixar نیست**؛ مدل NTC Slider با هدف صریح Pixar، سبک‌تر و از نظر مجوز اعلام‌شده روشن‌تر است، اما برای محیط‌های پیچیده هنوز ارزیابی عملی لازم دارد. فعلاً تعویض checkpoint توجیهی ندارد.
