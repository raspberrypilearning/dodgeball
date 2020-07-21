## गेंदों को चकमा देना

अब आपका पात्र चल सकता है और छलांग लगा सकता है, इसलिए यह कुछ गेंदों को जोड़ने का समय है जिनसे पात्र को बचना है।

\--- task \---

एक नया गेंद sprite बनाएं। आप अपनी पसंद के अनुसार किसी भी प्रकार की गेंद चुन सकते हैं।

![स्क्रीनशॉट](images/dodge-balls.png)

\--- /task \---

\--- task \---

गेंद sprite का आकार बदलें ताकि पात्र उसके ऊपर से छलांग लगा सके। गेंद का आकार सही है या नहीं यह जांचने के लिए पात्र को गेंद के ऊपर से छलाँग लगवाने का प्रयास करें।

![स्क्रीनशॉट](images/dodge-ball-resize.png)

\--- /task \---

\--- task \---

इस कोड को अपने गेंद sprite में जोड़ें:

![गेंद sprite](images/ball_sprite.png)

```blocks3
when green flag clicked
hide
forever 
  wait (3) seconds
  create clone of (myself v)
end
```

```blocks3
when I start as a clone
go to x: (160) y: (160)
show
repeat (22) 
  change y by (-4)
end
repeat (170) 
  change x by (-2)
  turn ccw (6) degrees
end
repeat (30) 
  change y by (-4)
end
delete this clone
```

यह कोड हर तीन सेकंड में गेंद sprite का एक नया हूबहू बनाता है। प्रत्येक नया हूबहू शीर्ष प्लेटफार्म पर चलता है और फिर गिरता है।

\--- /task \---

\--- task \---

गेम को जांचने के लिए ध्वज पर क्लिक करें।

![स्क्रीनशॉट](images/dodge-ball-test.png)

\--- /task \---

\--- task \---

अपने गेंद sprite में अधिक कोड जोड़ें ताकि इसके हूबहू सभी तीन प्लेटफार्मों पर चलें।

![स्क्रीनशॉट](images/dodge-ball-more-motion.png)

\--- hints \---

\--- hint \---

पहले प्लेटफ़ॉर्म पर गेंद sprite हूबहू को स्थानांतरित करने के लिए आपके द्वारा उपयोग किए गए कोड खंड को दोहराएं। आपको `x`{:class="block3motion"}, `y`{:class="block3motion"}, और `repeat`{:class="block3control"} मानों को बदलने की आवश्यकता है ताकि हूबहू प्लेटफार्मों का सही ढंग से पालन कर सकें।

\--- /hint \---

\--- hint \---

इन खंडों की आपको आवश्यकता होगी। सुनिश्चित करें कि आप उन्हें सही क्रम में जोड़ते हैं।

![गेंद sprite](images/ball_sprite.png)

```blocks3
repeat (170) 
  change x by (-2)
  turn ccw (6) degrees
end

repeat (180) 
  change x by (2)
  turn cw (6) degrees
end

repeat (30) 
  change y by (-4)
end
```

\--- /hint \---

\--- hint \---

आपकी गेंद sprite हूबहू के लिए कोड इस तरह दिखना चाहिए:

![गेंद sprite](images/ball_sprite.png)

```blocks3
when I start as a clone
go to x: (160) y: (160)
show
repeat (22) 
  change y by (-4)
end
repeat (170) 
  change x by (-2)
  turn ccw (6) degrees
end
repeat (30) 
  change y by (-4)
end
repeat (180) 
  change x by (2)
  turn cw (6) degrees
end
repeat (30) 
  change y by (-4)
end
repeat (170) 
  change x by (-2)
  turn ccw (6) degrees
end
delete this clone
```

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

अब कुछ कोड खंड जोडें एक सन्देश प्रसारित करने (भेजने) के लिए अगर आपका पात्र गेंद से टकरा जाता है!

इस कोड को अपने गेंद sprite में जोड़ें:

![गेंद sprite](images/ball_sprite.png)

```blocks3
    when I start as a clone
    forever
        if < touching (Pico walking v)? > then
            broadcast (hit v)
        end
    end
```

\--- /task \---

\--- task \---

अंत में, अपने पात्र sprite में कोड खंड जोड़ें `hit` संदेश प्राप्त करने पर इसे अपने शुरुआती स्थान पर वापस ले जाने के लिए:

![पिको चलने वाला sprite](images/pico_walking_sprite.png)

```blocks3
    when I receive [hit v]
    point in direction (90)
    go to x: (-210) y: (-120)
```

\--- /task \---

\--- task \---

अपने कोड का परीक्षण करें। जांचें कि क्या गेंद को छूने के बाद पात्र अपने शुरुआती स्थान पर जाता है।

\--- /task \---