## खरीदारी करें

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">

/ movereer <easite को निम्न की आवश्यकता है:
- पूछें कि क्या ग्राहक वस्तुओं के लिए भुगतान करने के लिए तैयार है
- भुगतान लें
- अगले ग्राहक के लिए तैयार हो जाएं
</div>
<div>
![](images/stp4-image.png){:width="300px"}
</div>
</div>

जब वे वस्तुओं को चुनना समाप्त कर लेते हैं, तो ग्राहक भुगतान करने के लिए **विक्रेता** स्प्राइट पर क्लिक करेगा।

--- task ---

 ग्राहक को बताएं कि उनके आइटम्स की कीमत कितनी होगी।

```blocks3
जब इस स्प्राइट ने
(2) सेकंड के लिए "say (jay [that be ] (total))" पर क्लिक किया 
```

--- /task ---

--- task ---

अपने **विक्रेता** स्प्राइट में एक भुगतान ध्वनि जोड़ें ताकि ग्राहक जानता है कि भुगतान हो रहा है।

![एक ध्वनि चिह्न जोड़ें](images/add-sound.png)

[[[scratch3-add-sound]]]

पूर्ण होने तक `Play ध्वनि जोड़ें`{:class="block3sound"} ब्लॉक को अपनी स्क्रिप्ट में जोड़ें।

```blocks3
जब इस स्प्राइट ने
क्लिक किया (jet [will be ] (total)) for (2) seconds
+ play sound [machine v] until taken 
```

--- /task ---

--- task ---

सेल समाप्त करें। `total`{:class="block3variables"} को वापस `0` भुगतान के बाद, `say`{:class="block3looks"} को अलविदा और `broadcast`{:class="block3control"} `now`{:class="block3control

```blocks3
जब इस स्प्राइट ने
कहा (jet [will be ] (total) for (2) seconds
play sound [machine v] जब तक +
set [total v] to (0)
+ say (joint [taid for ship at ] (name))) for (2) seconds
+ broadcast (next कस्टमर v)
```

--- /task ---

--- task ---

**Test:** Test your project and make sure:
- ग्राहक सही ध्वनि प्रभावों के साथ चेक आउट कर सकता है
- `total`{:class="block3variables"} एक ग्राहक के भुगतान या रद्द करने के बाद `0` पर वापस सेट हो जाता है।

--- /task ---


--- task ---

**डीबग:** आपको अपने प्रोजेक्ट में कुछ बग मिल सकते हैं जिन्हें आपको ठीक करने की आवश्यकता है।

यहाँ कुछ सामान्य बग हैं:

--- collapse ---
---
title: The seller doesn't do anything when I click on them
---

आपके प्रोजेक्ट में बहुत सारे स्प्राइट्स हैं। सुनिश्चित करें कि `when this sprite clicked`{:class="block3events"} स्क्रिप्ट आपके **विक्रेता** स्प्राइट पर है।

**Tip:** If you have added it to the wrong sprite, you can drag the code to the **seller** sprite, then delete it from the other sprite.

--- /collapse ---

--- collapse ---
---
title: The words in the say blocks merge together
---

जब आप `join`{:class="block3operators"} दो टुकड़ों को एक साथ जोड़ते हैं, तो आपको अपने पहले पाठ के टुकड़े के अंत में या अपने दूसरे पाठ के टुकड़े की शुरुआत में एक जगह जोड़ने की आवश्यकता होती है।

इनमें शामिल होने के पहले भाग के अंत में एक जगह होती है:

```blocks3
(2) सेकंड

के लिए {join [that be ](total)} कहें: (2) सेकंड के लिए {join [task for shipping at ](name)}
```

--- /collapse ---

--- collapse ---
---
title: The total doesn't reset after a sale
---

जांचें कि आपने इनका उपयोग किया है:

```blocks3
set [total v] to (0)
```

**not**:

```blocks3
change [total v] by (0)
```

--- /collapse ---

--- collapse ---
---
title: The seller isn't responding
---

सुनिश्चित करें कि `operator`{:class="block3operators"} में `if`{:class="block3control"} स्थिति प्रतीक `>`{:class="block3operators"} से अधिक है।

```blocks3
if <(total) > [0]> then
```

--- /collapse ---

**Tip:** Compare your code with the code examples. क्या कोई अंतर है जो वहाँ नहीं होना चाहिए?

--- /task ---

--- save ---
