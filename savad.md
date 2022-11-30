<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
  <title>سواد دیجیتال</title>
</head>
<body>

<h1>تولید شعر با شبکه عصبی LSTM و تنسورفلو</h1>
<img src="https://files.virgool.io/upload/users/1223901/posts/rynq4emx1qcx/5bqtxkgjyhop.jpeg">
<p>یادگیری عمیق ابزاری فوق العاده برای ساخت پروژه های مهیج و سرگرم‌کننده است، هر روز خبری در مورد کاربرد های جدید یادگیری عمیق منتشر میشود و همگان را در تعجب فرو میبرد، آموزش این مدل های جذاب هم در نوع خودش سرگرم‌کننده است مخصوصا مدل های مرتبط به پردازش زبان طبیعی(NLP).

در این ویرگول میخواهم نشان بدهم چگونه میتوان از یادگیری عمیق برای تولید شعر استفاده کنیم، مدلی که خواهیم ساخت، ارتباط بین کارکتر ها را متوجه میشود و احتمال وقوع کارکتر بعدی را محاسبه میکند..</p>
<p class="box m-5 has-background-Gray">در این پروژه از شبکه عصبی LSTM استفاده خواهیم کرد. به طور خلاصه، LSTM یک نوع خاص از یک شبکه عصبی RNN است که در پردازش داده هایی که دارای توالی منظم و مرتبط هستند استفاده میشود. مثل متون، موسیقی ها، ویدئو ها و...

تفاوت RNN ها با شبکه های عصبی کلاسیک داشتن وابستگی زمانی یا اثر حافظه است که داده های قبلی را در حافظه به خاطر میسپارد تا در تصمیم گیری های بعدی استفاده کند

<a href="https://l.vrgl.ir/r?l=https%3A%2F%2Fcolah.github.io%2Fposts%2F2015-08-Understanding-LSTMs%2F&st=post&si=rynq4emx1qcx&k=qToANxWsJZcbp30NlTE%2FGPXPRobbWIVbY2orsTBmE0E%3D">
<p>برای مطالعه بیشتر</p></a></p>
<h1>آماده سازی</h1>
<p>برای شروع به تنسورفلو و نامپای نیاز خواهیم داشت که میتوانید با دستور زیر آنها را نصب کنید :</p>
<p class="box m-5 has-background-light">pip install -U tensorflow-gpu***
pip install -U numpy</p>
<p>ما از دیوان حافظ استفاده میکنیم اما میتوانید برای دقت بیشتر از اشعار سعدی یا فردوسی استفاده کنید(یا هرنوع متن بالای 100 هزار کارکتر)، اشعار حافظ را با دستور زیر دریافت میکنیم :</p>
<p class="box m-5 has-background-light">1-wget -O hafez.txt https://raw.githubusercontent.com/amnghd/Persian_poems_corpus/master/normalized/hafez_norm.txt</p>
<p class="box m-5 has-background-light">12345678import tensorflow as tf
import keras
from keras.layers import  Input, LSTM, Dense
import tensorflow.keras.optimizers as optimizers
import numpy as np
import random
text = open(&quothafez.txt&quot, &quotr&quot, encoding=&quotutf-8&quot).read()</p>
</body>
</html>
