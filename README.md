# सार्वजनिक दुर्गादेवी नवरात्र उत्सव मंडळ, मुरुड

नवरात्र उत्सव २०२६ साठी मंडळाची अधिकृत वेबसाइट: कार्यकारिणी समिती, कार्यक्रम पत्रिका (११ ते २१ ऑक्टोबर २०२६), प्रत्येक कार्यक्रमाचे वेगळे पान, संपर्क आणि Instagram लिंक.

## Folder structure

```
.
├── index.html            # संपूर्ण वेबसाइट (HTML + CSS + JavaScript, एकच फाइल)
├── README.md
├── .nojekyll
└── assets/
    ├── images/           # लोगो, २५ वे रौप्य महोत्सव badge, प्रत्येक दिवसाचे फोटो
    └── video/            # २१ तारखेचा मिरवणूक व्हिडिओ
```

कोणतेही build tool किंवा npm package लागत नाही. Fonts Google Fonts वरून load होतात (इंटरनेट लागते).

## Local वर चालवणे

`index.html` थेट browser मध्ये उघडा. किंवा:

```bash
python3 -m http.server 8000
# मग http://localhost:8000 उघडा
```

## GitHub Pages वर publish करणे

1. GitHub वर नवीन repository बनवा (उदा. `murud-navratri`).
2. या folder मधील सर्व फाइल्स (`.nojekyll` सह) repository च्या root मध्ये upload करा.
3. **Settings → Pages → Source:** `Deploy from a branch` निवडा, branch `main` आणि folder `/ (root)` निवडा, मग Save करा.
4. काही मिनिटांत साइट `https://<तुमचे-username>.github.io/murud-navratri/` येथे चालू होईल.

## माहिती बदलणे (नावे, वेळ, कार्यक्रम)

सर्व माहिती `index.html` च्या खालच्या `<script>` मध्ये आहे:

| नाव | काय आहे |
|---|---|
| `COMMITTEE` | पदे आणि नावे (एकापेक्षा जास्त नावे `|` ने वेगळी करा) |
| `PROGRAM` | तारीख → [चिन्ह प्रकार, कार्यक्रम, जबाबदारी, विशेष ओळी] |
| `TIME` | तारीख → वेळ |
| `PHOTO` | तारीख → फोटोचा path (`assets/images/...`) |
| `VIDEO` | तारीख → [व्हिडिओ path, poster path] |

नवीन फोटो हवा असेल तर तो `assets/images/` मध्ये टाका आणि `PHOTO` मध्ये त्याचा path लिहा. व्हिडिओ शक्यतो ५ MB पेक्षा लहान ठेवा, म्हणजे साइट लवकर उघडते.

## प्रत्येक कार्यक्रमाची वेगळी लिंक

`https://<साइट>/#/din/11` ते `#/din/21` अशा लिंक थेट WhatsApp वर share करता येतात.

---
Powered by Shree Pimpale
