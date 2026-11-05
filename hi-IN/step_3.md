## सेल के लिए आइटम्स

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
आपकी दुकान को बिक्री के लिए वस्तुओं की आवश्यकता है। प्रत्येक आइटम का मूल्य होगा जो एक 'कुल'{:class="block3variables"} वेरिएबल में जोड़ा जाएगा।
</div>
<div>
![](images/step3-image.png){:width="300px"}
</div>
</div>

आपको यह ट्रैक रखना होगा कि आपका ग्राहक कितना खर्च कर रहा है।

--- task ---

Add a new variable called `total`{:class="block3variables"} for all sprites.

अपने **सेलर** स्प्राइट पर क्लिक करें और `set`{:class="block3variables"} में एक स्क्रिप्ट जोड़ें `total`{:class="block3variables"} से `0` जब प्रोजेक्ट शुरू होता है।

[[[scratch3-create-set-variable]]]

--- /task ---

What **items** will your customer(s) be buying?
+ कुछ तरह का खाना या पीना
+ खेल उपकरण, खिलौने, या गैजेट्स
+ मैजिक वैंड्स, लोशन, या स्पैल बुक्स
+ वस्त्र या अन्य फैशन आइटम्स
+ Your own idea

--- task ---

पहले **आइटम** के लिए स्प्राइट जोड़ें जिसे आप अपनी दुकान में बेचने जा रहे हैं।

यदि आप चाहें, तो आप पेंट संपादक में टेक्स्ट टूल का उपयोग करके पोशाक में मूल्य जोड़ सकते हैं। या पृष्ठभूमि में एक मूल्य जोड़ें और उसके आगे के आइटम को स्थित करें।

![उनके आगे लिखी गई मात्रा के साथ आइटम्स के उदाहरण।](images/item-amounts.png)

--- /task ---

--- task ---

जब ग्राहक स्प्राइट पर क्लिक करता है, तो `change`{:class="block3variables"} को `total`{:class="block3variables"} में एक स्क्रिप्ट जोड़ें।

--- collapse ---
---
title: Click to add an item
---

```blocks3
जब इस स्प्राइट ने
शुरू ध्वनि पर क्लिक किया (Coin v)
[total v] by [10]
```

--- /collapse ---

यह `play a sound`{:class="block3sound"} का भी एक अच्छा विचार है जो उन्होंने एक आइटम जोड़ा है।

![एक ध्वनि चिह्न जोड़ें](images/add-sound.png)

[[[scratch3-add-sound]]]

--- /task ---

--- task ---

**Test:** Click on your item and check that the value of the `total`{:class="block3variables"} variable increases by the price of the item, and you hear the sound effect. कुल वृद्धि देखने के लिए अधिक बार क्लिक करें।

अपना प्रोजेक्ट शुरू करने के लिए हरे झंडे पर क्लिक करें और सुनिश्चित करें कि `total`{:class="block3variables"} `0` से शुरू होता है।

--- /task ---

--- task ---

अपनी दुकान में और मदें जोड़ें।

आप या तो:
+ पहले आइटम को डुप्लिकेट करें और फिर पेंट एडिटर में एक नया कॉस्ट्यूम जोड़ें
+ एक स्प्राइट जोड़ें और फिर `when flag clicked`{:class="block3events"} स्क्रिप्ट को पहले आइटम से अपने नए आइटम में खींचें

यदि आप इनका उपयोग कर रहे हैं, तो पोशाक या पृष्ठभूमि में एक मूल्य लेबल जोड़ें।

--- /task ---

--- task ---

Click on your new **Item** sprite in the Sprite list then click on the **Code** tab.

`total`{:class="block3variables"} बदलने की मात्रा को अपने नए आइटम के मूल्य में बदलें।

--- /task ---

--- task ---

**Test:** Click the green flag to start your project and click on items to add them. जाँच करें कि जब भी आप किसी आइटम पर क्लिक करते हैं, तो कुल राशि सही मात्रा से बढ़ जाती है।

यदि आपने मूल्य लेबल जोड़े हैं, तो सुनिश्चित करें कि वे `total`{:class="block3variables"} में जोड़ी जाने वाली राशि से मेल खाते हैं, या आपके ग्राहक भ्रमित होंगे!

--- /task ---

--- task ---

**डीबग करें:** आपको अपने प्रोजेक्ट में कुछ बग मिल सकते हैं जिन्हें आपको ठीक करने की आवश्यकता है। यहाँ कुछ सामान्य बग हैं।

--- collapse ---
---
title: The total doesn't go to 0 when I click the green flag
---

जांचें कि आपने **विक्रेता** स्प्राइट पर `when flag clicked`{:class="block3events"} स्क्रिप्ट में `when flag clicked`{:class="block3events"} वेरिएबल का प्रारंभ मान सेट किया है।

--- /collapse ---

--- collapse ---
---
title: The total doesn't increase by the correct amount when I click on an item
---

जांचें कि प्रत्येक आइटम में एक `when this sprite clicked`{:class="block3events"} स्क्रिप्ट है जो `total`{:class="block3variables"} को उस आइटम के लिए सही मात्रा में बदल देती है — हो सकता है कि आपने गलत स्प्राइट के लिए कीमत बदल दी हो।

जांचें कि आपने `change`{:class="block3variables"} ब्लॉक का उपयोग किया है और `set`{:class="block3variables"} ब्लॉक को `total`{:class="block3variables"} बदलने के लिए नहीं किया है। आपको कुल मूल्य जोड़ने के लिए `change`{:class="block3variables"} का उपयोग करने की आवश्यकता है, आप अभी जोड़े गए आइटम के मूल्य के लिए कुल योग को सेट नहीं करना चाहते हैं।

--- /collapse ---

--- /task ---

--- save ---
