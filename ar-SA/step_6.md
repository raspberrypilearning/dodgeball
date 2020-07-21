## تفادي الكرات

يمكن لشخصيتك التحرك والقفز الآن، لذا حان الوقت لإضافة بعض الكرات التي يجب على الشخصية تجنبها.

--- task ---

أنشئ كائن كرة جديد. يمكنك اختيار نوع الكرة الذي يعجبك.

![لقطة الشاشة](images/dodge-balls.png)

---/task--

--- task ---

غير حجم كائن الكرة بحيث يمكن للشخصية أن تقفز فوقه. حاول جعل الشخصية تقفز فوق الكرة لاختبار ما إذا كانت الكرة بالحجم الصحيح.

![لقطة الشاشة](images/dodge-ball-resize.png)

--- /task ---

--- task ---

أضف هذه التعليمة البرمجية إلى كائن الكرة:

![كائن الكرة](images/ball_sprite.png)

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

هذه التعليمة البرمجية تنشئ نسخة جديدة من كائن الكرة كل ثلاث ثوان. كل نسخة جديدة تتحرك على طول المنصة العليا ثم تسقط.

--- /task ---

--- task ---

انقر فوق العلم لاختبار اللعبة.

![لقطة الشاشة](images/dodge-ball-test.png)

---/task--

--- task ---

أضف المزيد من التعليمات البرمجية إلى كائن الكرة الخاص بك بحيث تتحرك نسخ منه عبر المنصات الثلاث جميعها.

![لقطة الشاشة](images/dodge-ball-more-motion.png)

--- hints ---


--- hint ---

كرر التعليمات البرمجية التي استخدمتها لنقل نسخة كائن الكرة عبر المنصة الأولى. تحتاج إلى تغيير قيم `x`{:class="block3motion"}, `y`{:class="block3motion"}, و`تكرار `{:class="block3control"} الارقام بحيث تتابع النسخ المنصات بشكل صحيح.

--- hint/ ---

--- hint ---

هذه هي الكتل البرمجية التي تحتاجها. تأكد من إضافتها بالترتيب الصحيح.

![كائن الكرة](images/ball_sprite.png)

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

--- hint/ ---

--- hint ---

يجب أن تبدو التعليمات البرمجية لاستنساخ كائن الكرة كما يلي:

![كائن الكرة](images/ball_sprite.png)

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

--- hint/ ---

--- hints/ ---

--- /task ---

--- task ---

الآن أضف بعض الكتل البرمجية لبث (إرسال) رسالة إذا تعرضت شخصيتك للضرب بالكرة!

أضف هذه التعليمة البرمجية إلى كائن الكرة:

![كائن الكرة](images/ball_sprite.png)

```blocks3
    when I start as a clone
    forever
        if < touching (Pico walking v)? > then
            broadcast (ضربة v)
        end
    end
```

--- /task ---

--- task ---

أخيرا، أضف كتل التعليمات البرمجية إلى الكائن الخاص بك لجعله ينتقل إلى موضع البداية عندما يتلقى الرسالة `ضربة`:

![كائن المشي بيكو](images/pico_walking_sprite.png)

```blocks3
    when I receive [ضربة v]
    point in direction (90)
    go to x: (-210) y: (-120)
```

--- /task ---

--- task ---

اختبر التعليمة البرمجية الخاصة بك. تحقق مما إذا كانت الشخصية تتحرك مرة أخرى إلى البداية بعد لمس الكرة.

--- /task ---