## आव्हान: अधिक अडथळे

आपला गेम अद्यापही खूप सोपा आहे असे आपल्याला वाटत असल्यास आपण त्यात आणखी अडथळे जोडू शकता. अडथळे आपल्या आवडीचे पण असू शकतात! काही कल्पना:

+ एक धोकादायक फुलपाखरू
+ दृश्य आणि अदृश्य होणारे फलाट
+ पडणारे टेनिस चेंडू जे टाळणं आवश्यक असेल

![screenshot](images/dodge-obstacles.png)

आपण पुढील स्तरावर जाण्यासाठी आणखी एक पार्श्वभूमी देखील डिझाइन करू शकता. तुम्ही कोड जोडू शकता जेणेकरून, आपले पात्र जेव्हा हिरव्या दाराजवळ पोहोचेल तेव्हा खेळची पार्श्वभूमी बदलली जाईल:

![pico walking sprite](images/pico_walking_sprite.png)

```blocks3
    if <touching color [#00FF00]?> then
        switch backdrop to (next backdrop v)
        go to x: (-210) y: (-120)
        wait (1) seconds
    end
```