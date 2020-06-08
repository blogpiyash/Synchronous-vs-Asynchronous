# Synchronous-vs-Asynchronous
Synchronous and Asynchronous Tutorial
## Synchronous Programming :
```
- এখানে একই সময়ে Program execute হবে line by line.
- যখন কোন Function কে কল করা হবে,
  তখন ঐ ফাংশনটি Return  না করা পর্যন্ত কিনবা ফাংশনটির কাজ শেষ না হওয়া পর্যন্ত পরবর্তী  statement execute  হব না। 
```
উদাহরণ -

statement 1... execute

Function (); // 1s 2s 3s 4s.... execute Done

then,

Statement 2 ... execute

statement 3 ... execute

## Asynchronous Programming:
```
- এখানে প্রোগ্রাম line by line execute হবে না।
- যখন কোন Function  call করা হয়, 
  তখন ফাংশন সম্পূর্ণ  হতে যে সময় লাগবে তার জন্য অপেক্ষা  না করে পরবর্তী  statement execute  করবে।
```

উদাহরণি-

statement 1...  // execute

function  () // waiting

statement 2 ...  // done

statement 3 ... // done

## asynchronous কেন এত গুরুত্বপূর্ণ ?
> async প্রোগ্রামিংয়ের খুবই গুরুত্বপূর্ণ ফিচার,  কারন - এটা আমাদের Future টাইপের data গুলোকে সংগ্রেহের প্রেসেস  এ  রেখে  অন্য কাজ  সমাপ্ত  করতে সাহায্যে  করে।  ফলে প্রোগ্রাম execution  time সেইভ হয় এবং   সফটওয়্যারের কার্যকারিতা বৃদ্ধি পায়। কিছু সাধারন async operation যেমন -
-নেটওয়ার্কের মাধ্যমে  ডাটা আনা ।
-ডাটাবেইজ লিখা ।
-একটি ফাইল থেকে ডাটা পড়া ।

> ধরুন, আমরা api server থেকে ডাটা রিকুয়েষ্ট  পাঠাব। এবং এই রিকুয়েষ্ট সার্ভার থেকে ডাটা নিয়ে response  করবে।  আর request এবং  response  এর মাঝে কিছু সময়ের দরকার পড়ে,  এখন আমরা চাচ্ছি না ঐ  সময়টুকু অপেক্ষা  না করতে।  আমরা চাচ্ছি সার্ভার যে সময়ে  ডাটা  প্রসেস করবে সেই সমযে আমাদের প্রোগ্রামের অনান্য  statement  গুলো execute করবে।
