# Marathi2India AI Translator — मोबाईल सेटअप

## या आवृत्तीत काय चालते?
- मोबाइल-फ्रेंडली PWA स्क्रीन
- मराठी मजकूर इनपुट
- २२ अनुसूचित भारतीय भाषांसह भाषा निवड
- Chrome मध्ये समर्थित असल्यास १ मिनिट ५० सेकंदांपर्यंत voice-to-text
- कॉपी आणि उपलब्ध असल्यास text-to-speech

## महत्त्वाची मर्यादा
या पहिल्या आवृत्तीत AI भाषांतर API जोडलेली नाही. `index.html` मधील `const API_URL=""` ही जागा तुमच्या स्वतःच्या backend endpoint ने बदलल्याशिवाय भाषांतर होणार नाही. API key कधीही सार्वजनिक HTML/JavaScript मध्ये ठेवू नका.

## Samsung Android वरून प्रकाशित करण्याची सोपी पद्धत
1. ZIP extract करा (Files/My Files अॅप वापरा).
2. GitHub खाते तयार करा किंवा लॉग इन करा: https://github.com
3. नवीन public repository तयार करा, उदा. `marathi2india-pwa`.
4. `index.html`, `manifest.json`, `sw.js` आणि `README_MR.md` या फाइल्स repository मध्ये upload करा.
5. Repository → Settings → Pages → Deploy from a branch → `main` आणि `/(root)` निवडा → Save.
6. काही मिनिटांनी GitHub Pages ने दिलेली HTTPS वेबसाइट Chrome मध्ये उघडा.
7. Chrome ⋮ → Add to Home screen / Install app निवडा.

## पूर्ण AI भाषांतर जोडण्याचा पुढचा टप्पा
IndicTrans2 २२ अनुसूचित भारतीय भाषांसाठी open-source मॉडेल आहे:
https://github.com/AI4Bharat/IndicTrans2

हे मॉडेल चालवण्यासाठी Python/ML सर्व्हर किंवा अधिकृत hosted API आवश्यक आहे. फक्त static GitHub Pages वर मॉडेल चालणार नाही. सर्व्हर endpoint ने खालील स्वरूप स्वीकारावे:

POST JSON:
{"text":"मला इंग्रजी शिकायचे आहे","source":"mar_Deva","target":"eng_Latn"}

Response JSON:
{"translation":"I want to learn English."}

Endpoint URL `index.html` मधील `const API_URL=""` मध्ये द्या. Backend मध्ये CORS फक्त तुमच्या वेबसाइटसाठी उघडा, इनपुटची मर्यादा ठेवा, आणि API credentials server-side environment variables मध्ये ठेवा.

## Professional English सुधारणा
यासाठी backend मध्ये स्वतंत्र सुरक्षित endpoint किंवा language-model API जोडावी लागेल. Translation आणि grammar correction या वेगळ्या प्रक्रिया ठेवा, जेणेकरून अर्थ बदलणार नाही.

## गोपनीयता
माइक वापरताना Chrome permission मागू शकतो. Speech Recognition काही डिव्हाइसवर cloud सेवा वापरू शकते. गोपनीय माहिती/आधार क्रमांक/पासवर्ड बोलू नका.
