<div align="center">
  <img height="60" src="https://img.icons8.com/color/344/javascript.png">
  <h1>বাংলায় জাভাস্ক্রিপ্ট প্রশ্নোত্তর 🇧🇩</h1>
</div>

<p align="center">
<b>বেসিক থেকে এডভ্যান্স:</b> আপনি কতটুকু জাভাস্ক্রিপ্ট জানেন পরীক্ষা করুন, আপনার জ্ঞানকে একটু ঝালাই করে নিন অথবা আপনার ইন্টার্ভিউর জন্য প্রস্তুতি নিন 💪। এই রিপো নিয়িমিত আপডেট করা হয় নতুন প্রশ্নত্তর দিয়ে। উত্তরগুলো কল্যাপ্সড আকারে আছে, দেখার জন্য উত্তর এ ক্লিক করুন। অবসরে আনন্দের জন্য আমি এটাকে বাংলায় অনুবাদ করেছি, ভুল ত্রুটি মার্জনা করবেন। আপনার প্রোগ্রামিং যাত্রার জন্য শুভকামনা 💛। </p>

<p align="center">আমার সাথে যোগাযোগ করতে চাইলে,</p>

<p align="center">
  <a href="https://www.facebook.com/saiefalemon">Facebook</a> || <a href="https://www.linkedin.com/in/saiefalemon">LinkedIn</a> || <a href="https://www.iamsaief.com/">Blog</a>
</p>

---

<details><summary><strong> যে যে ভাষায় অনুবাদগুলো আছে তার লিস্ট - 🇸🇦🇪🇬🇧🇦🇩🇪🇪🇸🇫🇷🇮🇩🇯🇵🇰🇷🇳🇱🇧🇷🇷🇺🇹🇭🇹🇷🇺🇦🇻🇳🇨🇳🇹🇼🇽🇰🇧🇩</strong></summary>
<p>

- [🇸🇦 العربية](./ar-AR/README_AR.md)
- [🇪🇬 اللغة العامية](./ar-EG/README_ar-EG.md)
- [🇧🇦 Bosanski](./bs-BS/README-bs_BS.md)
- [🇩🇪 Deutsch](./de-DE/README.md)
- [🇪🇸 Español](./es-ES/README-ES.md)
- [🇫🇷 Français](./fr-FR/README_fr-FR.md)
- [🇮🇩 Indonesia](./id-ID/README.md)
- [🇮🇹 Italiano](./it-IT/README.md)
- [🇯🇵 日本語](./ja-JA/README-ja_JA.md)
- [🇰🇷 한국어](./ko-KR/README-ko_KR.md)
- [🇳🇱 Nederlands](./nl-NL/README.md)
- [🇵🇱 Polski](./pl-PL/README.md)
- [🇧🇷 Português Brasil](./pt-BR/README_pt_BR.md)
- [🇷o Română](./ro-RO/README.ro.md)
- [🇷🇺 Русский](./ru-RU/README.md)
- [🇽🇰 Shqip](./sq-KS/README_sq_KS.md)
- [🇹🇭 ไทย](./th-TH/README-th_TH.md)
- [🇹🇷 Türkçe](./tr-TR/README-tr_TR.md)
- [🇺🇦 Українська мова](./uk-UA/README.md)
- [🇻🇳 Tiếng Việt](./vi-VI/README-vi.md)
- [🇨🇳 简体中文](./zh-CN/README-zh_CN.md)
- [🇹🇼 繁體中文](./zh-TW/README_zh-TW.md)
- [🇧🇩 বাংলা](./bn-BD/README_bn-BD.md)

</p>
</details>

---

###### 1. এটার আউটপুট কোনটা?

```javascript
function sayHi() {
  console.log(name);
  console.log(age);
  var name = "Lydia";
  let age = 21;
}

sayHi();
```

- A: `Lydia` and `undefined`
- B: `Lydia` and `ReferenceError`
- C: `ReferenceError` and `21`
- D: `undefined` and `ReferenceError`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: D

আমরা ফাংশনের ভেতরে প্রথমে `var` কিওয়ার্ড দিয়ে ভেরিয়েবল ডিক্লেয়ার করেছি। মানে হল ভেরিয়েবলটি হইস্টেড (মেমরিতে জায়গা নিচ্ছে রান করার সময়) হয়ে যাচ্ছে ডিফল্ট ভ্যালু `undefined` দিয়ে যতক্ষন না পর্যন্ত যে লাইনে ডিক্লেয়ার করা হয়েছে সেখানে যাচ্ছে। যে লাইনে আমরা এটাকে লগ করার চেষ্টা করছি তার আগ পর্যন্ত এটাকে ডিফাইন করা হয়নি, তাই এটা এখন পর্যন্ত `undefined` ভ্যালুকেই ধরে রেখেছে।

`let` কিওয়ার্ড (এবং `const`) দিয়ে ভেরিয়েবল নিলে সেটাও হইস্টেড হয় তবে `var` এর মত ইনিশিয়ালাইজ হয় না। যে লাইনে ডিক্লেয়ার (ইনিশিয়ালাইজ) করা হয়েছে তার আগে তাদেরকে এক্সেস (রিড/রাইট) করা যায় না। এটাকে "টেম্পোরাল ডেড জোন বলা হয়"। যখন ভেরিয়েবলকে ডিক্লেয়ার করার আগেই তাকে এক্সেস করার চেষ্টা করা হয় তখন জাভাস্ক্রিপ্ট `ReferenceError` ছুঁঁড়ে দেয়।

</p>
</details>

---

###### 2. এটার আউটপুট কোনটা?

```javascript
for (var i = 0; i < 3; i++) {
  setTimeout(() => console.log(i), 1);
}

for (let i = 0; i < 3; i++) {
  setTimeout(() => console.log(i), 1);
}
```

- A: `0 1 2` and `0 1 2`
- B: `0 1 2` and `3 3 3`
- C: `3 3 3` and `0 1 2`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: C

জাভাস্ক্রিপ্টের ইভেন্ট কিউয়ের জন্য `setTimeout` কলব্যাক ফাংশনটি কল হয়েছে লুপটি রান হওয়ার পরে। যেহেতু ১ম লুপে `var` কিওয়ার্ড ব্যাবহৃত হয়েছে এটার ভ্যালু তাই গ্লোবাল। লুপ চলাকালীন আমরা `i` এর ভ্যালু প্রতিবার `1` করে বাড়িয়েছি উনারি `++` অপারেটর দিয়ে। যতক্ষণে `setTimeout` কলব্যাক ফাংশনটি কল হয়েছে, ১ম উদাহরনের ক্ষেত্রে, `i` এর ভ্যালু ততক্ষণে `3` হয়ে গেছে।

২য় লুপে, `i` ভ্যারিরিয়েবল ডিক্লেয়ার করা হয়েছে `let` কিওয়ার্ড দিয়ে, `let` কিওয়ার্ড (এবং `const`) দিয়ে নেয়া ভেরিয়েবগুলো ব্লক-স্কোপড (ব্লক হচ্ছে `{}` এর মধ্যে থাকা কিছু)। লুপ চলাকালীন প্রতিবারই `i` এর নতুন ভ্যালু হবে এবং প্রতিটি ভ্যালুই লুপের ভেতরে স্কোপড থাকবে।

</p>
</details>

---

###### 3. এটার আউটপুট কোনটা?

```javascript
const shape = {
  radius: 10,
  diameter() {
    return this.radius * 2;
  },
  perimeter: () => 2 * Math.PI * this.radius,
};

console.log(shape.diameter());
console.log(shape.perimeter());
```

- A: `20` and `62.83185307179586`
- B: `20` and `NaN`
- C: `20` and `63`
- D: `NaN` and `63`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: B

> খেয়াল করুন এখানে `diameter` একটি সাধারন ফাংশন অন্যদিকে `perimeter` হচ্ছে একটি অ্যারো ফাংশন।

অ্যারো ফাংশনের `this` কিওয়ার্ড গ্লোবাল স্কোপকে রেফার (পয়েন্ট) করে, কিন্তু সাধারন ফাংশনের নিজের স্কোপেই পয়েন্ট করে। মানে হল, যখন আমরা `perimeter` কে কল করছি এটা shape অব্জেক্ট কে রেফার করছে না বরং গ্লোবাল স্কোপকে করছে (উদাহরনস্বরূপ - window)।

যেহেতু অ্যারো ফাংশনের স্কোপে `radius` এর কোন ভ্যালু নেই `this.radius` রিটার্ন করছে `undefined` একে ২ দিয়ে গুন করার ফলে (`2 * Math.PI`) ফলাফল আসছে `NaN`.

</p>
</details>

---

###### 4. এটার আউটপুট কোনটা?

```javascript
+true;
!"Lydia";
```

- A: `1` and `false`
- B: `false` and `NaN`
- C: `false` and `false`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: A

এখানে ইউনারি (`+`) অপারেটরটি চেষ্টা করেছে তার অপারেন্ডকে নাম্বার এ পরিবর্তন করার। `true` হয় `1`, এবং `false` হয় `0`।

`'Lydia'` স্ট্রিং টি একটি সত্য ভ্যালু। আমরা এখানে আসলে `!` দিয়ে যেটা জিজ্ঞেস করছি "এই সত্য ভ্যালুটি কি মিথ্যা ?"। এটি ফলাফল দিচ্ছে `false`।

</p>
</details>

---

###### 5. এখানে কোনটি সত্য?

```javascript
const bird = {
  size: "small",
};

const mouse = {
  name: "Mickey",
  small: true,
};
```

- A: `mouse.bird.size` is not valid
- B: `mouse[bird.size]` is not valid
- C: `mouse[bird["size"]]` is not valid
- D: All of them are valid

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: A

জাভাস্ক্রিপ্টে অব্জক্টের সকল কি-ই হচ্ছে স্ট্রিং (যদি না এটা কোন সংকেত হয়)। যদিওবা আমরা এদেরকে স্ট্রিং হিসেবে লিখে নাও থাকি, ভেতরে ভেতরে তা সবসময়ই স্ট্রিং এ পরিবর্তন হয়ে যায়।

জাভাস্ক্রিপ্ট স্টেটম্যান্ট কে ভাষান্তর (মেশিনের ভাষা) করে। যখন ব্র্যাকেট নোটেশন ব্যবহৃত হয়, এটা শুরুর ব্র্যাকেট `[` পেলে তা শেষ ব্র্যাকেট পর্যন্ত `]` যেতে থাকে। তারপরই কেবল এটার মান নির্ণয় করা হবে।

অন্যদিকে, ডট নোটেশনের বেলায় এরকমটা ঘটে না। `mouse` এর মধ্যে `bird` নামের কোন কি নেই, তার মানে হচ্ছে `mouse.bird` হয় `undefined`। এরপর ডট নোটেশন ব্যাবহার (`mouse.bird.size`) করে আমরা জানতে চাচ্ছি `size` এর ভ্যালু । যেহেতু `mouse.bird` হয় `undefined`, আমরা আসলে জানতে চাচ্ছি `undefined.size`। এটা বৈধ নয়, এবং `Cannot read property "size" of undefined` -র মত একটা এরর ছুঁড়ে দেয়া হবে।

</p>
</details>

---

###### 6. এটার আউটপুট কোনটা?

```javascript
let c = { greeting: "Hey!" };
let d;

d = c;
c.greeting = "Hello";
console.log(d.greeting);
```

- A: `Hello`
- B: `Hey!`
- C: `undefined`
- D: `ReferenceError`
- E: `TypeError`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: A

জাভাস্ক্রিপ্টে, সব অবজেক্টই কাজ করে রেফারেন্স হিসেবে, যখন আমরা একটিকে অন্যটির সমান ভ্যালু সেট করছি তখন রেফারেন্সই সেট হচ্ছে।

প্রথমে, ভেরিয়েবল `c` একটা অবজেক্টের মান ধরে রাখে। পরবর্তিতে সেই ভ্যালিউই আমরা `d` তে অ্যাসাইন করছি যেটায় আদতে আছে `c` অবজেক্টের রেফারেন্স।

<img src="https://i.imgur.com/ko5k0fs.png" width="200">

যখন আপনি একটি অবজেক্টের মান পরিবর্তন করছেন, আপনি সবগুলোকেই পরিবর্তন করছেন।

</p>
</details>

---

###### 7. এটার আউটপুট কোনটা?

```javascript
let a = 3;
let b = new Number(3);
let c = 3;

console.log(a == b);
console.log(a === b);
console.log(b === c);
```

- A: `true` `false` `true`
- B: `false` `false` `true`
- C: `true` `false` `false`
- D: `false` `true` `true`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: C

`new Number()` হল একটি বিল্ট-ইন ফাংশন কন্সট্রাক্টর। যদিও এটা নাম্বার এর মত দেখতে কিন্তু এটি আসলে নাম্বার নয়ঃ এটাতে আর অনেকগুলো ফিচার আছে এবং এটি একটি অবজেক্ট।

যখন আমরা `==` অপারেটর (সমতুল্য অপারেটর) ব্যাবহার করি, এটা কেবল ভ্যালু সমান কিনা তুলনা করে। `a` ও `b` দুটার ভ্যালুই `3` তাই ফলাফল হয় `true`।

অন্যদিকে, যখন আমরা `===` অপারেটর (কঠোর-সমতুল্য অপারেটর) ব্যাবহার করি, এটা ভ্যালু এবং টাইপ দুটাই সমান কিনা তুলনা করে। এক্ষত্রে `new Number()` যেহেতু নাম্বর নয় অবেজেক্ট। দুটই ফলাফল দেয় `false`।

</p>
</details>

---

###### 8. এটার আউটপুট কোনটা?

```javascript
class Chameleon {
  static colorChange(newColor) {
    this.newColor = newColor;
    return this.newColor;
  }

  constructor({ newColor = "green" } = {}) {
    this.newColor = newColor;
  }
}

const freddie = new Chameleon({ newColor: "purple" });
console.log(freddie.colorChange("orange"));
```

- A: `orange`
- B: `purple`
- C: `green`
- D: `TypeError`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: D

এখানে `colorChange` একটি স্ট্যাটিক ফাংশন। এদের ডিজাইন প্যাটার্ন হল, কেবল যে কন্সট্রাক্টরে এদের তৈরি করা হবে তার বাইরে থেকে এক্সেস করা যাবে না, এবং কোন চিলড্রেনে পাস করা যাবে না বা ক্লাস ইন্সটেন্স দিয়ে কলও করা যাবে না। যেহেতু `freddie` Chameleon ক্লাসের একটি ইন্সটেন্স, তাই সে স্ট্যাটিক ফাংশনকে কল করতে পারবে না। ফলে `TypeError` ছোঁড়া হয়।

</p>
</details>

---

###### 9. এটার আউটপুট কোনটা?

```javascript
let greeting;
greetign = {}; // Typo!
console.log(greetign);
```

- A: `{}`
- B: `ReferenceError: greetign is not defined`
- C: `undefined`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: A

এটা অবজেক্টকে লগ করছে, কারন আমরা খালি অবজেক্টটিকে তৈরি করেছি গ্লোবাল অবজেক্টের মধ্যে! যখন `greeting` কে `greetign` ভুল বানান এ লিখেছি, জেএস ইন্টারপ্রেটার দেখছে এমনঃ

1. নোড জেওএস এ - `global.greetign = {}`।
2. ব্রাউজার এ - `window.greetign = {}`, `frames.greetign = {}` এবং `self.greetign`।
3. ওয়েব ওয়ার্কার্স এ - `self.greetign`।
4. অন্য সকল এনভায়র্ন্মেন্টে - `globalThis.greetign`।

এটাকে এড়ানোর জন্য আমরা `"use strict"` ব্যাবহার করতে পারি । এটা নিশ্চিত করবে যে আপনি ভেরিয়েবলকে কোন কিছু দিয়ে অ্যাসাইন করার আগে তাকে ডিক্লেয়ার করেছেন কিনা ।

</p>
</details>

---

###### 10. আমরা এটা করলে কি ঘটবে?

```javascript
function bark() {
  console.log("Woof!");
}

bark.animal = "dog";
```

- A: Nothing, this is totally fine!
- B: `SyntaxError`. You cannot add properties to a function this way.
- C: `"Woof"` gets logged.
- D: `ReferenceError`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: A

জাভাস্ক্রিপ্টে এটা সম্ভব, কারন ফাংশনগুলো হয় অবজেক্ট! (প্রিমিটিভ টাইপ বাদে সবকিছুই অবজেক্ট)

ফাংশনগুলো হয় বিশেষ ধরনের অবজেক্ট। যে কোডটা আপনি লিখেছেন এটা আসল ফাংশন নয়। ফাংশনটি হচ্ছে একটি অবজেক্ট যার প্রপার্টিস রয়েছে। এই প্রোপার্টিগুলোকে কল করা যায়।

</p>
</details>

---

###### 11. এটার আউটপুট কোনটা?

```javascript
function Person(firstName, lastName) {
  this.firstName = firstName;
  this.lastName = lastName;
}

const member = new Person("Lydia", "Hallie");
Person.getFullName = function () {
  return `${this.firstName} ${this.lastName}`;
};

console.log(member.getFullName());
```

- A: `TypeError`
- B: `SyntaxError`
- C: `Lydia Hallie`
- D: `undefined` `undefined`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: A

জাভাস্ক্রিপ্টে, ফাংশনগুলো হয় অবজেক্ট, অতএব, `getFullName` মেথডটি কন্সট্রাক্টর ফাংশনের অবজেক্টের সাথে যুক্ত হয়। একারনেই, আমরা `Person.getFullName()` কে কল করতে পারছি কিন্তু `member.getFullName` ছুঁড়ে দিচ্ছে `TypeError`।

আপনি যদি একটি মেথডকে অবজেক্টের সকল ইন্সট্যান্সের জন্য ব্যবহারযোগ্য করতে চান তাহলে আপনার এটাকে যুক্ত করতে হবে প্রটোটাইপ প্রোপার্টিতে।

```js
Person.prototype.getFullName = function () {
  return `${this.firstName} ${this.lastName}`;
};
```

</p>
</details>

---

###### 12. এটার আউটপুট কোনটা?

```javascript
function Person(firstName, lastName) {
  this.firstName = firstName;
  this.lastName = lastName;
}

const lydia = new Person("Lydia", "Hallie");
const sarah = Person("Sarah", "Smith");

console.log(lydia);
console.log(sarah);
```

- A: `Person {firstName: "Lydia", lastName: "Hallie"}` and `undefined`
- B: `Person {firstName: "Lydia", lastName: "Hallie"}` and `Person {firstName: "Sarah", lastName: "Smith"}`
- C: `Person {firstName: "Lydia", lastName: "Hallie"}` and `{}`
- D: `Person {firstName: "Lydia", lastName: "Hallie"}` and `ReferenceError`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: A

আমরা `sarah` -র জন্য `new` কিওয়ার্ডটি ব্যবহার করিনি। যখন `new` কিওয়ার্ড ব্যবহার করা হয় `this` রেফার করে আমরা তৈরি করা নতুন খালি অবজেক্টিকে। অন্যদিকে, যদি আপনি `new` যুক্ত না করেন, `this` রেফার করবে **গ্লোবাল অবজেক্টকে** !

আমরা বলছি `this.firstName` সমান হল `"Sarah"` এবং `this.lastName` হল `"Smith"`। আমরা এখানে আসলে যেটা বলছি সেটা হল, ডিফাইন করছি `global.firstName = 'Sarah'` এবং `global.lastName = 'Smith'`। যেহেতু `Person` ফাংশন কোন ফলাফল রিটার্ন করছে না তাই `sarah` নিজেই হয়ে আছে `undefined`।

</p>
</details>

---

###### 13. What are the three phases of event propagation?

- A: Target > Capturing > Bubbling
- B: Bubbling > Target > Capturing
- C: Target > Bubbling > Capturing
- D: Capturing > Target > Bubbling

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: D

**ক্যাপচারিং** অবস্থার সময়, ইভেন্ট ডমের (DOM) পুর্বপুরুষ উপাদান থেকে **লক্ষ্য** -র দিকে যায়। তারপর এটা **লক্ষ্য** উপাদানে পৌঁছালে **বাবলিং** শুরু হয়।

<img src="https://i.imgur.com/N18oRgd.png" width="200">

</p>
</details>

---

###### 14. সকল অবজেক্টের প্রোটোটাইপ আছে?

- A: true
- B: false

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: B

**বেইজ অবজেক্ট** ছাড়া সকল অবজেক্টের প্রোটোটাইপ আছে। বেইজ অবজেক্ট হল সে অবজেক্ট যেটা ইউজার তৈরি করেছে অথবা `new` কিওয়ার্ডটি ব্যবহার করে তৈরি করা হয়েছে। বেইজ অবজেক্টের কিছু বিল্টইন মেথড ব্যবহারের বৈধ অনুমতি আছে, যেমন `.toString`। এই কারনেই আপনি জাভাস্ক্রিপ্টের বিল্টইন মেথড ব্যবহার করতে পারেন! এইরকম মেথডগুলো প্রোটোটাইপের আয়তাধীনে থাকে। যদিও জাভাস্ক্রিপ্ট আপনার অবজেক্টে সরাসরি এগুলোকে খুঁজে পায় না, প্রোটোটাইপ চেইনের ভেতর দিয়ে যেয়ে খুঁজে বের করে, ফলে আপনি এগুলো ব্যবহারের বৈধ অনুমতি পান।

</p>
</details>

---

###### 15. এটার আউটপুট কোনটা?

```javascript
function sum(a, b) {
  return a + b;
}

sum(1, "2");
```

- A: `NaN`
- B: `TypeError`
- C: `"12"`
- D: `3`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: C

জাভাস্ক্রিপ্ট একটি **ডায়নামিক টাইপ ভাষাঃ** আমরা ভেরিয়েবলের টাইপ নির্দিষ্ট করি না। আপনি জানতে পারেন না ভ্যালু স্বয়ংক্রিয়ভাবেই এক টাইপ থেকে অন্য টাইপে পরিবর্তন হয়ে যায়, যেটাকে বলা হয় **কোয়ার্শন [coercion](<(coercion)[https://developer.mozilla.org/en-US/docs/Web/JavaScript/Data_structures#type_coercion]>)**। এটা হল এক টাইপ থেকে অন্য টাইপে পরিবর্তন হওয়া।

এই উদাহরনে, জাভাস্ক্রিপ্ট এই ফাংশনটিকে যুক্তিসঙ্গত ও এর একটি ফলাফল রিটার্ন করার জন্য `1` নাম্বারটিকে স্ট্রিং এ পরিবর্তন করেছে। নাম্বার `1` ও স্ট্রিং `"2"` এর যোগের বেলায় নাম্বারটিকে স্ট্রিং হিসেবে ধরা হয়েছে। আমরা দুটো স্ট্রিং কে যুক্ত করতে পারি এভাবে, `"Hello" + "World"`, তাই এখানে `"1" + "2"` ফলাফল রিটার্ন করছে `"12"`।

</p>
</details>

---

###### 16. এটার আউটপুট কোনটা?

```javascript
let number = 0;
console.log(number++);
console.log(++number);
console.log(number);
```

- A: `1` `1` `2`
- B: `1` `2` `2`
- C: `0` `2` `2`
- D: `0` `1` `2`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: C

**পোস্টফিক্স** ইউনারি অপারেটর `++`:

1. ফলাফল রিটার্ন করে (এক্ষেত্রে রিটার্ন করে `0`)
2. ভ্যালুর মান বৃদ্ধি করে (নাম্বারটি এখন `1`)

**প্রিফিক্স** ইউনারি অপারেটর `++`:

1. ভ্যালুর মান বৃদ্ধি করে (নাম্বারটি এখন `2`)
2. ফলাফল রিটার্ন করে (এক্ষেত্রে রিটার্ন করে `2`)

এজন্যই উত্তরটি হয় `0 2 2`

</p>
</details>

---

###### 17. এটার আউটপুট কোনটা?

```javascript
function getPersonInfo(one, two, three) {
  console.log(one);
  console.log(two);
  console.log(three);
}

const person = "Lydia";
const age = 21;

getPersonInfo`${person} is ${age} years old`;
```

- A: `"Lydia"` `21` `["", " is ", " years old"]`
- B: `["", " is ", " years old"]` `"Lydia"` `21`
- C: `"Lydia"` `["", " is ", " years old"]` `21`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: B

যদি আপনি _ট্যাগড টেম্পলেট লিটারেলস_ ব্যবহার করেন, আর্গুমেন্টের ১ম ভ্যালুটি সবসময় হয় ট্যাগড স্ট্রিং গুলোর একটি অ্যারে। বাকি আর্গুমেন্টের ভ্যালুগুলো হয় যেই এক্সপ্রেশনগুলো পাঠানো হয় তার ভ্যালু।

</p>
</details>

---

###### 18. এটার আউটপুট কোনটা?

```javascript
function checkAge(data) {
  if (data === { age: 18 }) {
    console.log("You are an adult!");
  } else if (data == { age: 18 }) {
    console.log("You are still an adult.");
  } else {
    console.log(`Hmm.. You don't have an age I guess`);
  }
}

checkAge({ age: 18 });
```

- A: `You are an adult!`
- B: `You are still an adult.`
- C: `Hmm.. You don't have an age I guess`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: C

সমতা পরীক্ষা করার ক্ষেত্রে, মৌলিক টাইপগুলো (primitives) _ভ্যালু_ এবং অবজেক্ট টাইপগুলো _রেফেরান্স_ দ্বারা তুলনা করা হয়। জাভাস্ক্রিপ্ট চেক করে অবজেক্টগুলোতে একই মেমরি লোকেশনের রেফারেন্স আছে কিনা।

যেদুটো অবজেক্টকে আমরা তুলনা করছি তাদের সেটা নেইঃ প্যারামিটারে আমরা যে অবজেক্টকে পাঠিয়েছি সেটার মেমরি লোকেশনের রেফারেন্স যেই অবজেক্টটা সমতা চেক করার জন্য ব্যাবহার করেছি তার থেকে আলাদা।

একারনে দুটোই `{ age: 18 } === { age: 18 }` এবং `{ age: 18 } == { age: 18 }` রিটার্ন করে `false`

</p>
</details>

---

###### 19. এটার আউটপুট কোনটা?

```javascript
function getAge(...args) {
  console.log(typeof args);
}

getAge(21);
```

- A: `"number"`
- B: `"array"`
- C: `"object"`
- D: `"NaN"`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: C

এখানে রেস্ট প্যারামিটারটি (`...args`) আমাদেরকে বাকি সব আর্গুমেন্টসকে একটি অ্যারেতে "সংগ্রহ" করতে দেয়। একটি অ্যারে হয় একটি অবজেক্ট, তাই `typeof args` রিটার্ন করে `"object"`।

</p>
</details>

---

###### 20. এটার আউটপুট কোনটা?

```javascript
function getAge() {
  "use strict";
  age = 21;
  console.log(age);
}

getAge();
```

- A: `21`
- B: `undefined`
- C: `ReferenceError`
- D: `TypeError`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: C

`"use strict"` দ্বারা আপনি এটা নিশ্চিত করতে পারেন যে আপনি দুর্ঘটনাবশত গ্লোবাল ভ্যারিয়েবল ডিক্লেয়ার করছেন না। আমরা কোথাও `age` ভ্যারিয়েবলটি ডিক্লেয়ার করিনি এবং যেহেতু আমরা `"use strict"` ব্যাবহার করেছি, এটা _রেফারেন্স এরর_ ছুঁড়ে দেবে। যদি আমরা ব্যাবহার না করতাম `"use strict"`, হয়ত এটা কাজ করত, যেহেতু `age` প্রপার্টিটি গ্লোবাল অবজেক্টে যুক্ত হত।

</p>
</details>

---

###### 21. কোনটি `sum` এর ভ্যালু হবে?

```javascript
const sum = eval("10*10+5");
```

- A: `105`
- B: `"105"`
- C: `TypeError`
- D: `"10*10+5"`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: A

`eval` একটি স্ট্রিং হিসাবে পাস করা কোডকে মূল্যায়ন করে। যদি এটি একটি অভিব্যক্তি (expression) হয়, যেমন এই ক্ষেত্রে, এটি অভিব্যক্তি মূল্যায়ন করেছে। অভিব্যক্তিটি হল `10 * 10 + 5`। এটি ফলাফল রিটার্ন করে `105`।

</p>
</details>

---

###### 22. কতক্ষণ cool_secret এক্সেসযোগ্য?

```javascript
sessionStorage.setItem("cool_secret", 123);
```

- A: Forever, the data doesn't get lost.
- B: When the user closes the tab.
- C: When the user closes the entire browser, not only the tab.
- D: When the user shuts off their computer.

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: B

ট্যাবটি বন্ধ করার পরে `sessionStorage` সংরক্ষিত ডেটা সরানো হয়।

আপনি `localStorage` ব্যবহার করলে, ডেটা চিরকালের জন্য সেখানে থাকবে, যদি না উদাহরণস্বরূপ `localStorage.clear()` কল করা হয়।

</p>
</details>

---

###### 23. এটার আউটপুট কোনটা?

```javascript
var num = 8;
var num = 10;

console.log(num);
```

- A: `8`
- B: `10`
- C: `SyntaxError`
- D: `ReferenceError`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: B

`var` কীওয়ার্ড দিয়ে, আপনি একই নামের একাধিক ভেরিয়েবল ঘোষণা করতে পারেন। তারপর ভেরিয়েবলটি সর্বশেষ মান ধরে রাখবে।

এটি কিন্তু আপনি `let` বা `const` দিয়ে করতে পারবেন না যেহেতু সেগুলি ব্লক-স্কোপড এবং সেইজন্য পুনরায় ডিক্লেয়ার করা যাবে না।

</p>
</details>

---

###### 24. এটার আউটপুট কোনটা?

```javascript
const obj = { 1: "a", 2: "b", 3: "c" };
const set = new Set([1, 2, 3, 4, 5]);

obj.hasOwnProperty("1");
obj.hasOwnProperty(1);
set.has("1");
set.has(1);
```

- A: `false` `true` `false` `true`
- B: `false` `true` `true` `true`
- C: `true` `true` `false` `true`
- D: `true` `true` `true` `true`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: C

সমস্ত অবজেক্ট কী (প্রতীকগুলি ব্যতীত) ভেতরে ভেতরে স্ট্রিং, এমনকি আপনি নিজে স্ট্রিং হিসাবে এটিকে না লিখে থাকলেও৷ `obj.hasOwnProperty('1')` ও এই কারনেই `true` রিটার্ন করে।

একটি সেটের জন্য এটি সেভাবে কাজ করে না। আমাদের সেটে কোন `'1'` নেই: `set.has('1')` রিটার্ন করে `false`। এটির নিউমেরিক টাইপ (সংখ্যাসূচক প্রকার) আছে `1`, `set.has(1)` রিটার্ন করে `true`।

</p>
</details>

---

###### 25. এটার আউটপুট কোনটা?

```javascript
const obj = { a: "one", b: "two", a: "three" };
console.log(obj);
```

- A: `{ a: "one", b: "two" }`
- B: `{ b: "two", a: "three" }`
- C: `{ a: "three", b: "two" }`
- D: `SyntaxError`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: C

আপনার যদি একই নামের দুটি কী থাকে তবে কীটি প্রতিস্থাপন করা হবে। এটি এখনও তার প্রথম অবস্থানে থাকবে, তবে সর্বশেষ নির্দিষ্ট করা ভ্যালুটি সহ।

</p>
</details>

---

###### 26. জাভাস্ক্রিপ্ট গ্লোবাল এক্সিকিউশন কনটেক্সট আপনার জন্য দুটি জিনিস তৈরি করে: গ্লোবাল অবজেক্ট এবং "this" কীওয়ার্ড।

- A: true
- B: false
- C: it depends

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: A

বেস এক্সিকিউশন কনটেক্সট হল গ্লোবাল এক্সিকিউশন কনটেক্সট: এটি আপনার কোডের সর্বত্র অ্যাক্সেসযোগ্য।

</p>
</details>

---

###### 27. এটার আউটপুট কোনটা?

```javascript
for (let i = 1; i < 5; i++) {
  if (i === 3) continue;
  console.log(i);
}
```

- A: `1` `2`
- B: `1` `2` `3`
- C: `1` `2` `4`
- D: `1` `3` `4`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: C

`continue` স্টেটমেন্ট (বিবৃতি) একটি ইটারেশন (ইটারেশন) এড়িয়ে যায় যদি একটি নির্দিষ্ট শর্ত `true` রিটার্ন করে।

</p>
</details>

---

###### 28. এটার আউটপুট কোনটা?

```javascript
String.prototype.giveLydiaPizza = () => {
  return "Just give Lydia pizza already!";
};

const name = "Lydia";

console.log(name.giveLydiaPizza());
```

- A: `"Just give Lydia pizza already!"`
- B: `TypeError: not a function`
- C: `SyntaxError`
- D: `undefined`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: A

`String` হল একটি বিল্ট-ইন কনস্ট্রাক্টর, যেটিতে আমরা প্রপার্টি গুলো যোগ করতে পারি। আমি এর প্রোটোটাইপে একটি মেথড যোগ করেছি। প্রিমিটিভ স্ট্রিংগুলি স্বয়ংক্রিয়ভাবে একটি স্ট্রিং অবজেক্টে রূপান্তরিত হয় স্ট্রিং প্রোটোটাইপ ফাংশন দ্বারা। সুতরাং, সমস্ত স্ট্রিং এর (স্ট্রিং অবজেক্ট) সেই মেথডের অ্যাক্সেস আছে!

জাভাস্ক্রিপ্টে এটাকে **প্রোটোটাইপ ইনহেরিটেন্স** বলা হয়। প্রোটোটাইপ ইনহেরিটেন্স হল একটি নির্দিষ্ট টাইপের (যেমন স্ট্রিং) এর সমস্ত ইন্সট্যান্সগুলির মধ্যে প্রোপার্টিস এবং মেথডগুলি শেয়ার করার একটি উপায় এবং এভাবেই আপনার দেওয়া `giveLydiaPizza` মেথডটি আপনার তৈরি করা প্রতিটি স্ট্রিংয়ের জন্য অ্যাক্সেসেবল হয়ে যায়। এটি একযোগে সমস্ত স্ট্রিংগুলিতে একটি নতুন প্রোপার্টি যুক্ত করার মতো!

</p>
</details>

---

###### 29. এটার আউটপুট কোনটা?

```javascript
const a = {};
const b = { key: "b" };
const c = { key: "c" };

a[b] = 123;
a[c] = 456;

console.log(a[b]);
```

- A: `123`
- B: `456`
- C: `undefined`
- D: `ReferenceError`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: B

অবজেক্টের কিগুলো স্বয়ংক্রিয়ভাবে স্ট্রিং এ পরিবর্তন হয়ে যায়। আমরা `123` ভ্যালুটি দিয়ে `a` অবজেক্টের কি হিসেবে একটি অবজেক্টকেই কে সেট করার চেষ্টা করছি।

যাইহোক, যখন আমরা কোন অবজেক্টকে স্ট্রিংফাই করি তখন সেটি `"[object Object]"` হয়ে যায়। তাহলে এখানে আমরা যা বলছি সেটি হল, `a["[object Object]"] = 123`। তারপর আমরা একি কাজ করার চেষ্টা করেছি। `c` হল অন্য একটি অবজেক্ট যেটাকে আমরা পরোক্ষভাবে স্ট্রিংফাই করছি। তাহলে, `a["[object Object]"] = 456`।

তারপর আমরা `a[b]` লগ করি, যেটা আসলে `a["[object Object]"]`। আমরা কেবলই এটাকে সেট করেছি `456`, তাই এটা ফলাফল রিটার্ন করছে `456`।

</p>
</details>

---

###### 30. এটার আউটপুট কোনটা?

```javascript
const foo = () => console.log("First");
const bar = () => setTimeout(() => console.log("Second"));
const baz = () => console.log("Third");

bar();
foo();
baz();
```

- A: `First` `Second` `Third`
- B: `First` `Third` `Second`
- C: `Second` `First` `Third`
- D: `Second` `Third` `First`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: B

আমাদের একটি `setTimeout` ফাংশন আছে এবং এটিই আগে কল হয়েছে। তবু এটি শেষে লগ হয়েছে।

এর কারন হল ব্রাউজারে কেবল রানটাইম ইঞ্জিনই নেই, আমাদের কাছে `WebAPI` নামেও কিছু একটা জিনিস আছে। এই `WebAPI`-ই আমাদের শুরু করার জন্য `setTimeout` ফাংশন দেয়, এবং উদাহরণস্বরূপ DOM।

_কলব্যাক_ ফাংশনটিকে WebAPI এ পুশ করার পর `setTimeout` ফাংশনটি নিজেই কল স্ট্যাক থেকে পপ হয়ে যায়।

<img src="https://i.imgur.com/X5wsHOg.png" width="200">

এখন `foo` কে কল করা হচ্ছে এবং `"First"` লগ করা হয়েছে।

<img src="https://i.imgur.com/Pvc0dGq.png" width="200">

কল স্ট্যাক থেকে `foo` পপ হয়ে যায়, এবং `baz` কল করা হয়। `"Third"` লগ করা হয়েছে।

<img src="https://i.imgur.com/WhA2bCP.png" width="200">

`WebAPI` প্রস্তুত হলেই সে কল স্ট্যাকে কিছু যুক্ত করতে পারে না। তার পরিবর্তে সে কলব্যাক ফাংশন গুলিকে টাস্ক কিউ নামক কিছুতে পুশ করে দেয়।

<img src="https://i.imgur.com/NSnDZmU.png" width="200">

এখানেই একটি _ইভেন্ট লুপ_ কাজ করতে শুরু করে। একটি _ইভেন্ট লুপ_ কল স্ট্যাক ও টাস্ক কিউর দিকে নজর রাখে। যদি স্ট্যাক খালি থাকে এটা কিউ থেকে ১ম জিনিসটাকে নিয়ে স্ট্যাকে পুশ করে দেয়।

<img src="https://i.imgur.com/uyiScAI.png" width="200">

`bar` কল করা হয়ে, তাই `"Second"` লগ হয়েছে, এবং এটা স্ট্যাক থেকে পপ হয়ে যায়।

</p>
</details>

---

###### 31. বাটনে ক্লিক করলে event.target কোনটি হবে?

```html
<div onclick="console.log('first div')">
  <div onclick="console.log('second div')">
    <button onclick="console.log('button')">Click!</button>
  </div>
</div>
```

- A: Outer `div`
- B: Inner `div`
- C: `button`
- D: An array of all nested elements.

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: C

ইভেন্টের টার্গেট হচ্ছে ডমের গভীরতম নেস্টেড এলিম্যান্ট যে ইনভেনটি ঘটিয়েছে।

</p>
</details>

---

###### 32. যখন প্যারাগ্রাফে ক্লিক করবেন, লগ আউটপুট কোনটি হবে?

```html
<div onclick="console.log('div')">
  <p onclick="console.log('p')">Click here!</p>
</div>
```

- A: `p` `div`
- B: `div` `p`
- C: `p`
- D: `div`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: A

If we click `p`, we see two logs: `p` and `div`. During event propagation, there are 3 phases: capturing, targeting, and bubbling. By default, event handlers are executed in the bubbling phase (unless you set `useCapture` to `true`). It goes from the deepest nested element outwards.

`p` তে ক্লিক করলেই আমরা ২টা লগ দেখতে পাইঃ `p` ও `div`।
ইভেন্ট প্রোপাগেশন এর সময় ৩টা পর্যায় থাকে ক্যাপচারিং, টারগেটিং, ও বাবলিং। স্বাবাবিকভাবেই ইভেন্ট হ্যান্ডলারগুলো কাজ করে বাবলিং পর্যায়ে (যদি না আপনি `capture` কে `true` করে দেন)। এটা গভীরতম নেস্টেড এলিম্যান্ট থেকে বাহিরের (প্যারেন্টের) দিকে যায়।

</p>
</details>

---

###### 33. এটার আউটপুট কোনটা?

```javascript
const person = { name: "Lydia" };

function sayHi(age) {
  return `${this.name} is ${age}`;
}

console.log(sayHi.call(person, 21));
console.log(sayHi.bind(person, 21));
```

- A: `undefined is 21` `Lydia is 21`
- B: `function` `function`
- C: `Lydia is 21` `Lydia is 21`
- D: `Lydia is 21` `function`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: D

`.call` ও `.bind` দুটি দিয়েই আমরা `this` কিওয়ার্ডটি রেফার করা অবজেক্ট পাস করতে পারি। কিন্তু `.call` একই সাথে কলও হয়ে যাচ্ছে।

`.bind.` এর বেলায় সে _ফাংশনের কপি_'র সাথে `this` এর একটি কার্যকর (bound) কনট্যাক্স রিটার্ন করে। কিন্তু একই সাথে কল হয় না।

</p>
</details>

---

###### 34. এটার আউটপুট কোনটা?

```javascript
function sayHi() {
  return (() => 0)();
}

console.log(typeof sayHi());
```

- A: `"object"`
- B: `"number"`
- C: `"function"`
- D: `"undefined"`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: B

`sayHi` ফাংশনটি ইমিডিয়েটলি ইনভোকড ফাংশন এক্সপ্রেশনের (IIFE) রিটার্ন ভ্যালুটিই রিটার্ন করছে। এই ফাংশনটি রিটার্ন করেছে `0` যেটির টাইপ হচ্ছে একটি `"number"`।

> জেনে রাখুনঃ `typeof` লিস্টে উল্লেখিত ভ্যালুগুলো রিটার্ন করতে পারেঃ `undefined`, `boolean`, `number`, `bigint`, `string`, `symbol`, `function` এবং `object`। মনে রাখবেন যে `typeof null` কিন্তু `"object"` রিটার্ন করে।

</p>
</details>

---

###### 35. কোন ভ্যালুগুলো মিথ্যা হয়?

```javascript
0;
new Number(0);
("");
(" ");
new Boolean(false);
undefined;
```

- A: `0`, `''`, `undefined`
- B: `0`, `new Number(0)`, `''`, `new Boolean(false)`, `undefined`
- C: `0`, `''`, `new Boolean(false)`, `undefined`
- D: All of them are falsy

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: A

মোট ৮ রকমের মিথ্যা ভ্যালু হয়ঃ

- `undefined`
- `null`
- `NaN`
- `false`
- `''` (empty string)
- `0`
- `-0`
- `0n` (BigInt(0))

ফাংশন কন্সট্রাক্টরগুলো, যেমন `new Number` ও `new Boolean` সবসময় সত্য হয়। জাভাস্ক্রিপ্টে ফাংশনগুলো হয় অবজেক্ট এবং এরা রেফারেন্স টাইপ। রেফারেন্স টাইপ কখনো মিথ্যা হয় না।

</p>
</details>

---

###### 36. এটার আউটপুট কোনটা?

```javascript
console.log(typeof typeof 1);
```

- A: `"number"`
- B: `"string"`
- C: `"object"`
- D: `"undefined"`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: B

`typeof 1` রিটার্ন করে `"number"`.
আর `typeof "number"` রিটার্ন করে `"string"`

</p>
</details>

---

###### 37. এটার আউটপুট কোনটা?

```javascript
const numbers = [1, 2, 3];
numbers[10] = 11;
console.log(numbers);
```

- A: `[1, 2, 3, null x 7, 11]`
- B: `[1, 2, 3, 11]`
- C: `[1, 2, 3, empty x 7, 11]`
- D: `SyntaxError`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: C

আপনি যখন অ্যারের এমন কোন ইনডেক্সে একটি ভ্যালু সেট করেন যেটা অ্যারের দৈর্ঘ্যকে অতিক্রম করে ফেলে, জাভাস্ক্রিপ্ট তখন "empty slots" নামে কিছু তিরি করে। এটার ভ্যালু আসলে `undefined` কিন্তু আপনি দেখতে পাবেন এমন কিছুঃ

`[1, 2, 3, empty x 7, 11]`

জাভাস্ক্রিপ্ট কোথায় চলছে তার উপর ভিত্তি করে (এটা প্রতিটি ব্রউজার, নোড ইত্যাদির জন্য আলাদা)

</p>
</details>

---

###### 38. এটার আউটপুট কোনটা?

```javascript
(() => {
  let x, y;
  try {
    throw new Error();
  } catch (x) {
    (x = 1), (y = 2);
    console.log(x);
  }
  console.log(x);
  console.log(y);
})();
```

- A: `1` `undefined` `2`
- B: `undefined` `undefined` `undefined`
- C: `1` `1` `2`
- D: `1` `undefined` `undefined`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: A

`catch` ব্লকটি একটি আর্গুমেন্ট `x` রিসিভ করেছে। আমরা যখন আর্গুমেটস পাস করছি এটা আর `x` ভ্যারিয়েবল একই নয়। এই `x` ভ্যারিয়েবলটি হল ব্লক-স্কোপড।

পরবর্তীতে, আমরা ব্লক-স্কোপড ভ্যারিয়েবলটির ভ্যালু সেট করছি `1` এবং `y` ভ্যারিয়েবলটির ভ্যালু সেট করছি `2`। এখন, আমরা লগ করছি ব্লক-স্কোপড `x` ভ্যারিয়েবলটি, যেটা সমান হল `1`।

ক্যাচ-ব্লকের বাইরে `x` ভ্যারিয়েবলটি এখনো `undefined` এবং `y` হল `2`। যখন ক্যাচ-ব্লকের বাইরে `console.log(x)` করতে চাচ্ছি, এটা রিটার্ন করে `undefined`, এবং `y` রিটার্ন করে `2`।

</p>
</details>

---

###### 39. জাভাস্ক্রিপ্টে সবকিছুই হয় একটি ...... ।

- A: primitive or object
- B: function or object
- C: trick question! only objects
- D: number or object

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: A

জাভাস্ক্রিপ্টে আছে কেবল প্রিমিটিভ (মৌলিক) টাইপ ও অবজেক্ট।

প্রিমিটিভ (মৌলিক) টাইপগুলো হল - `boolean`, `null`, `undefined`, `bigint`, `number`, `string`, ও `symbol`।

প্রিমিটিভ টাইপের কোন প্রোপার্টিস/মেথড নেই এটাই একটি প্রিমিটিভ টাইপকে অবজেক্ট থেকে আলাদা করেছে; অন্যদিকে আপনি খেয়াল করবেন যে `'foo'.toUpperCase()` গননা করছে `'FOO'` এবং কোন `TypeError`ও দেয় না। এটার কারন হল, আপনি যখন কোন প্রিমিটিভ টাইপ যেমন স্ট্রিং দিয়ে কোন প্রোপার্টিস/মেথড কে ব্যবহার করতে চাচ্ছেন, জাভাস্ক্রিপ্ট তখন প্রিমিটিভ টাইপকে র‍্যাপার ক্লাসগুলোর একটি যেমন, `String` দিয়ে মুড়ে দেয়, এবং মান গননা হয়ে যাওয়ার সাথে সাথেই সেটি বাতিল হয়ে যায়। `null` ও `undefined` বাদে সকল প্রিমিটিভই একই ব্যবহার প্রদর্শন করে।

</p>
</details>

---

###### 40. এটার আউটপুট কোনটা?

```javascript
[
  [0, 1],
  [2, 3],
].reduce(
  (acc, cur) => {
    return acc.concat(cur);
  },
  [1, 2]
);
```

- A: `[0, 1, 2, 3, 1, 2]`
- B: `[6, 1, 2]`
- C: `[1, 2, 0, 1, 2, 3]`
- D: `[1, 2, 6]`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: C

এখানে `[1, 2]` আমাদের প্রথমিক ভ্যালু। এই ভ্যালুটি দিয়েই আমরা শুরু করব এবং এটাই `acc` এর ১ম ভ্যালু। ১ম রাউন্ডের সময়, `acc` হয় `[1,2]`, এবং `cur` হয় `[0, 1]`। আমরা তাদেরকে যুক্ত করছি, যেটার ফলাফল হল `[1, 2, 0, 1]`।

পরবর্তীতে ২য়/শেষ ধাপে, `acc` হয় `[1, 2, 0, 1]` এবং `cur` হয় `[2, 3]`, আমরা তাদেরকে যুক্ত করে ফলাফল পাচ্ছি `[1, 2, 0, 1, 2, 3]`।

</p>
</details>

---

###### 41. এটার আউটপুট কোনটা?

```javascript
!!null;
!!"";
!!1;
```

- A: `false` `true` `false`
- B: `false` `false` `true`
- C: `false` `true` `true`
- D: `true` `true` `false`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: B

`null` হল মিথ্যা। `!null` রিটার্ন করে `true`। `!true` রিটার্ন করে `false`.

`""` হল মিথ্যা। `!""` রিটার্ন করে `true`। `!true` রিটার্ন করে `false`।

`1` হল সত্য। `!1` রিটার্ন করে `false`। `!false` রিটার্ন করে `true`।

তাই সঠিক হল - `false` `false` `true`।

</p>
</details>

---

###### 42. এই `setInterval` মেথডটি ব্রাউজারে কি রিটার্ন করে?

```javascript
setInterval(() => console.log("Hi"), 1000);
```

- A: a unique id
- B: the amount of milliseconds specified
- C: the passed function
- D: `undefined`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: A

যদিও এটি বাউজারে ১ সেকেন্ড পর পর `'Hi'` লগ করেই যাবে কিন্তু `setInterval` মেথডটি একটি অনন্য আইডি (unique id) রিটার্ন করে। এই পুর্যায়ক্রমিক কাজকে `clearInterval()` দিয়ে মুছে ফেলতে ঐ আইডি ব্যবহার করা হয়।

</p>
</details>

---

###### 43. এটা কি রিটার্ন করে?

```javascript
[..."Lydia"];
```

- A: `["L", "y", "d", "i", "a"]`
- B: `["Lydia"]`
- C: `[[], "Lydia"]`
- D: `[["L", "y", "d", "i", "a"]]`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: A

স্ট্রিং একটি পুনরাবৃত্তিযোগ্য টাইপ। স্প্রেড অপারেটর পুনরাবৃত্তিযোগ্য প্রতিটি অক্ষরকে ম্যাপ করে একটি এলিমেন্টে নিয়ে আসে। তাই ফলাফল হয় `["L", "y", "d", "i", "a"]`।

</p>
</details>

---

###### 44. এটার আউটপুট কোনটা?

```javascript
function* generator(i) {
  yield i;
  yield i * 2;
}

const gen = generator(10);

console.log(gen.next().value);
console.log(gen.next().value);
```

- A: `[0, 10], [10, 20]`
- B: `20, 20`
- C: `10, 20`
- D: `0, 10 and 10, 20`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: C

সাধারন ফাংশনকে কল করার পর মাঝপথে থামিয়ে দেয়া যায় না। অন্যদিকে, জেনারেটর ফাংশনকে মাঝপথে থামিয়ে দেয়া যায়, এবং যেখানে থামানো হয়েছিলো সেখান থেকেই পুনরায় শুরু করা যায়। জেনারেটর ফাংশন প্রতিবার একটি `yield` কীওয়ার্ডের মুখোমুখি হয়, তখন ফাংশনটি তার পরের নির্দিষ্ট করা ভ্যালুটি প্রদান করে। মনে রাখবেন যে সেই ক্ষেত্রে জেনারেটর ফাংশন মানটি _রিটার্ন_ করে না, এটি মানটিকে _ইল্ড_ করে (ফলাফল প্রদান)।

প্রথমে, আমরা জেনারেটর ফাংশনটি শুরু করি `i` এর সমান `10` দিয়ে। আমরা `next()` মেথডটি ব্যবহার করে জেনারেটর ফাংশন চালু করি। প্রথমবার যখন আমরা জেনারেটর ফাংশন চালু করি, `i` সমান `10`। এটি প্রথম `yield` কীওয়ার্ডের মুখোমুখি হয়: এটি `i` এর মান প্রদান করে। জেনারেটরটি এখন "paused" করা হয়েছে এবং `10` লগ হয়ে গেছে।

তারপর, আমরা আবার `next()` মেথডটি ব্যবহার করে ফাংশনটি চালু করি। এখনও `i` এর সমান `10` নিয়ে এটি পূর্বে যেখানে থামে সেখান থেকেই চালিয়ে যেতে শুরু করে। এখন, এটি পরবর্তী `yield` কীওয়ার্ডের মুখোমুখি হয় এবং `i * 2` পায়। `i` হল `10` এর সমান, তাই এটি `10 * 2`, যা প্রদান করে `20`। এর ফলে `10, 20` পাচ্ছি।

</p>
</details>

---

###### 45. What does this return?

```javascript
const firstPromise = new Promise((res, rej) => {
  setTimeout(res, 500, "one");
});

const secondPromise = new Promise((res, rej) => {
  setTimeout(res, 100, "two");
});

Promise.race([firstPromise, secondPromise]).then((res) => console.log(res));
```

- A: `"one"`
- B: `"two"`
- C: `"two" "one"`
- D: `"one" "two"`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: B

যখন `Promise.race` মেথডে আমরা একাধিক প্রোমিস পাস করি, _১ম_ যে প্রমিসটি রিসলভ/রিজেক্ট হয় তাকেই এটা রিসলভ/রিজেক্ট করে। `setTimeout` মেথডে আমরা একটি টাইমার পাস করেছিঃ ১ম প্রমিসে (`firstPromise`) 500ms এবং ২য় প্রমিসে (`secondPromise`) 100ms। এর মানে হল, `secondPromise`টি `'two'` ভ্যালু নিয়ে প্রথমে রিজলভ হয়। তাই `res` এর ভ্যালুটিই (`'two'`) লগ হচ্ছে।

</p>
</details>

---

###### 46. এটার আউটপুট কোনটা?

```javascript
let person = { name: "Lydia" };
const members = [person];
person = null;

console.log(members);
```

- A: `null`
- B: `[null]`
- C: `[{}]`
- D: `[{ name: "Lydia" }]`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: D

১মে, আমরা একটি ভ্যারিয়েবল `person` ডিক্লেয়ার করেছি, এটি একটি অবজেক্ট যার একটি `name` প্রোপার্টি (কি) আছে।

<img src="https://i.imgur.com/TML1MbS.png" width="200">

তারপর আমরা আরও একটি ভ্যারিয়েবল ডিক্লেয়ার করেছি `members` নামে। এটি একটি অ্যারে যার ১ম ইনডেক্সটির ভ্যালু সমান হচ্ছে `person` ভ্যারিয়েলবটি। যখন অবজেক্টকে একে ওপরের সমান সেট করা হয় এরা _রেফারেন্স_ এর মাধ্যমে কাজ করে। যখন আপনি একটি ভ্যারিয়েবলকে অ্যাসাইন করছেন অন্য ভ্যরিয়েবলের রেফারেন্স, আপনি আসলে ঐ রেফারেন্সের একটি _কপি_ করছেন। _মনে রাখবেন তাদের কাছে কিন্তু একই রেফারেন্স নেই_ !

<img src="https://i.imgur.com/FSG5K3F.png" width="300">

পরবর্তিতে `person` ভ্যায়েবলকে আমরা সেট করছি সমান সমান `null`।

<img src="https://i.imgur.com/sYjcsMT.png" width="300">

আমরা কেবল `person` ভ্যায়েবলকে পরিবর্তন করেছি, অ্যারের ১ম এলিমেন্টকে নয়, যেহেতু ঐ এলিমেন্টির কাছে অবজেক্টের ভিন্ন (কপিকৃত) একটি রেফারেন্স আছে। `members` অ্যারের ১ম এলিমেন্টটি এখনো আসল অবজেক্টির রেফারেন্সটি ধরে রেখেছে তাই ১ম এলিমেন্টটি তার ভ্যালুও ধরে রেখেছে আসল অবজেক্টির ভ্যালুকেই। ফলে যখন `members` অ্যারেকে লগ করা হয় সেটাই লগ হয়েছে।

</p>
</details>

---

###### 47. এটার আউটপুট কোনটা?

```javascript
const person = {
  name: "Lydia",
  age: 21,
};

for (const item in person) {
  console.log(item);
}
```

- A: `{ name: "Lydia" }, { age: 21 }`
- B: `"name", "age"`
- C: `"Lydia", 21`
- D: `["name", "Lydia"], ["age", 21]`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: B

`for-in` লুপ ব্যবহার করে আমরা কেবল অবজেক্টের কি-গুলির মধ্যেই পুনরাবৃত্তি করতে পারি, এক্ষেত্রে `name` ও `age`। ভেতরে ভেতরে অবজেক্ট কীগুলি হল স্ট্রিং (যদি তারা কোন একটি প্রতীক (Symbol) না হয়)। প্রতিটি লুপে, আমরা `item` মানটি বর্তমান কী-টির সমান সেট করি যার পুনরাবৃত্তি হচ্ছে। ১মে, `item`-টি `name`-এর সমান, এবং লগ করা হয়। তারপর, `item`-টি `age`-এর সমান, যা লগ হয়।

</p>
</details>

---

###### 48. এটার আউটপুট কোনটা?

```javascript
console.log(3 + 4 + "5");
```

- A: `"345"`
- B: `"75"`
- C: `12`
- D: `"12"`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: B

**অপারেটর অ্যাসোসিয়েটিভিটি** হল সেই ক্রম যেখানে কম্পাইলার বাম-থেকে-ডান বা ডান-থেকে-বামে এক্সপ্রেশনকে মূল্যায়ন করে। এটি শুধুমাত্র তখনই ঘটে যখন সমস্ত অপারেটরের _একই_ অগ্রাধিকার থাকে। আমাদের শুধুমাত্র এক ধরনের অপারেটর আছে: `+`। উপরন্তু, অ্যাসোসিয়েটিভিটি বাম থেকে ডান।

১মে `3 + 4` মূল্যায়ন করা হয়। এর ফলে সংখ্যাটি `7` হয়।

**কোয়ার্শন** এর ফলে `7 + '5'` এর ফলাফল হয় `"75"`। জাভাস্ক্রিপ্ট `7` নম্বরটিকে একটি স্ট্রিংয়ে রূপান্তর করে, [প্রশ্ন 15 দেখুন](#15-এটার-আউটপুট-কোনটা)। আমরা `+` অপারেটর ব্যবহার করে দুটি স্ট্রিংকে সংযুক্ত করতে পারি। `"7" + "5"` ফলাফলে `"75"`।

</p>
</details>

---

###### 49. `num` এর ভ্যালু কোনটি?

```javascript
const num = parseInt("7*6", 10);
```

- A: `42`
- B: `"42"`
- C: `7`
- D: `NaN`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: C

স্ট্রিং এর শুধুমাত্র প্রথম সংখ্যাটি রিটার্ন করা হয়েছে। _radix_ এর উপর ভিত্তি করে স্ট্রিং-এর অক্ষরগুলি বৈধ কিনা তা পরীক্ষা করে (২য় আর্গুমেন্টই নির্দিষ্ট করে আমরা কোন ধরনের সংখ্যাকে পার্স করতে চাই: ডেসিমাল - 10, হেক্সাডেসিমাল - 16, অক্টাল - 8, বাইনারি - 2, ইত্যাদি)। এটি যখন একবার এমন একটি অক্ষরের মুখোমুখি হয় যা রেডিক্সে একটি বৈধ সংখ্যা নয়, তখন পার্সিং বন্ধ করে দেয় এবং পরবর্তি অক্ষরগুলিকে উপেক্ষা করে।

`*` একটি বৈধ সংখ্যা নয়। এটি শুধুমাত্র `"7"` কে ডেসিমাল `7`-এ পার্স করে। `num` মান তাই `7`।

</p>
</details>

---

###### 50. এটার আউটপুট কোনটা?

```javascript
[1, 2, 3].map((num) => {
  if (typeof num === "number") return;
  return num * 2;
});
```

- A: `[]`
- B: `[null, null, null]`
- C: `[undefined, undefined, undefined]`
- D: `[ 3 x empty ]`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: C

অ্যারের উপর ম্যাপিং করার সময়, `num` এর মানটি বর্তমানে লুপ করা হচ্ছে সেই এলিমেন্টের সমান। এই ক্ষেত্রে, এলিমেন্টগুলো সংখ্যা, তাই if স্টেটমেন্টের শর্তটি`typeof num === "number"` - `true` রিটার্ন করে। ম্যাপ ফাংশন একটি নতুন অ্যারে তৈরি করে এবং ফাংশন থেকে রিটার্ন করা ভ্যালুগুলো সেটাতে যুক্ত করে।

অন্যদিকে, আমরা কোন ভ্যালুই রিটার্ন করি নি। যখন ফাংশন থেকে কোন একটি ভ্যালু রিটার্ন করা হয় না, ফাংশন `undefined` রিটার্ন করে। অ্যারের প্রতিটি এলিমেন্টের জন্য, ফাংশন ব্লক কল করা হয়, তাই প্রতিটি এলিমেন্টের জন্য আমরা `undefined` রিটার্ন করছি।

</p>
</details>

---

###### 51. এটার আউটপুট কোনটা?

```javascript
function getInfo(member, year) {
  member.name = "Lydia";
  year = "1998";
}

const person = { name: "Sarah" };
const birthYear = "1997";

getInfo(person, birthYear);

console.log(person, birthYear);
```

- A: `{ name: "Lydia" }, "1997"`
- B: `{ name: "Sarah" }, "1998"`
- C: `{ name: "Lydia" }, "1998"`
- D: `{ name: "Sarah" }, "1997"`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: A

আর্গুমেন্টসগুলো হল পাসড বাই _ভ্যালু_, যদি না তারা অবজেক্ট হয়, তবে তারা পাসড বাই _রেফারেন্স_। যেহেতু `birthYear` একটি স্ট্রিং এটি পাসড বাই ভ্যালু। যখন আমরা আর্গুমেন্টসগুলো পাস করি _ভ্যালু_ হিসেবে, ঐ ভ্যালুর একটি _কপি_ তৈরি হয়। [(প্রশ্ন ৪৬ দেখুন)](#46-এটার-আউটপুট-কোনটা)

`birthYear` ভ্যারিয়েবলটির কাছে `"1997"` ভ্যালুর একটি রেফারেন্স আছে। `year` আর্গুমেন্টের কাছেও `"1997"` ভ্যালুর একটি রেফারেন্স আছে, কিন্তু দুটি রেফারেন্স একি নয়। মানে হল, ফাংশনের ভেতরে আমরা যখন `year` এর ভ্যালুকে আপডেট করছি `"1998"` এর সমান করে, আমরা কেবল `year` এর ভ্যালিটিই পরিবর্তন করছি। `birthYear` এর ভ্যালু এখনো সমান হচ্ছে `"1997"`।

অন্যদিকে, `person` হল একটি অবজেক্ট। এই অবজেক্টের রেফারেন্স পাস হয়েছে `member` আর্গুমেন্টিটির কাছে। যখন আমরা অবজেক্টের কোন প্রপার্টিকে পরিবর্তন করছি যেটার রেফারেন্স আছে `member` এর কাছে, তাই `person` অবজেক্টও পরিবর্তন হচ্ছে যাচ্ছে। যেহেতু তাদের রেফারেন্স একই। ফলে `person`-এর `name` প্রোপার্টিটি এখন সমান হল `"Lydia"`।

</p>
</details>

---

###### 52. এটার আউটপুট কোনটা?

```javascript
function greeting() {
  throw "Hello world!";
}

function sayHi() {
  try {
    const data = greeting();
    console.log("It worked!", data);
  } catch (e) {
    console.log("Oh no an error:", e);
  }
}

sayHi();
```

- A: `It worked! Hello world!`
- B: `Oh no an error: undefined`
- C: `SyntaxError: can only throw Error objects`
- D: `Oh no an error: Hello world!`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: D

`throw` স্টেটমেন্ট ব্যবহার করে আমরা কাস্টম এররস তৈরি করে এক্সসেপশন থ্রো করতে পারি। এক্সসেপশনস হতে পারে **string**, **number**, **boolean**, অথবা একটি **অবজেক্ট** । এক্ষেত্রে, এক্সসেপশন হল একটি স্ট্রিং `'Hello world!'`।

`catch` স্টেটমেন্ট ব্যবহার করে আমরা এটা নির্দিস্ট করতে পারি যে _কি করা হবে_ যখন `try` ব্লক থেকে কোন এক্সসেপশন থ্রো করা হয়। এক্সসেপশন থ্রো করা হয়েছেঃ `'Hello world!'` স্ট্রিংটি। `e` হল এই স্ট্রিংটির সমান, যেটা লগ করা হয়েছে। তাই ফলাফল হয়েছে `'Oh an error: Hello world!'`।

</p>
</details>

---

###### 53. এটার আউটপুট কোনটা?

```javascript
function Car() {
  this.make = "Lamborghini";
  return { make: "Maserati" };
}

const myCar = new Car();
console.log(myCar.make);
```

- A: `"Lamborghini"`
- B: `"Maserati"`
- C: `ReferenceError`
- D: `TypeError`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: B

যখন একটি কনস্ট্রাক্টর ফাংশনকে `new` কীওয়ার্ড দিয়ে কল করা হয়, তখন এটি একটি অবজেক্ট তৈরি করে এবং এটাকে রেফার করার জন্য `this` কীওয়ার্ডটি সেট করে। ডিফল্টরূপে, যদি কনস্ট্রাক্টর ফাংশন সরাসরি কিছু রিটার্ন না করে, তবে এটি নতুন তৈরিকৃত অবজেক্টকেই রিটার্ন করবে।

এই ক্ষেত্রে, কনস্ট্রাক্টর ফাংশন `Car` সরাসরি একটি নতুন অবজেক্ট রিটার্ন করে যার সাথে `make` প্রোপার্টিকে সেট করা হয় `"Maserati"`, যা ডিফল্ট আচরনকে ওভাররাইড করে। তাই, যখন `new Car()` কল করা হয়, তখন _returned_ অবজেক্টটি `myCar`-এ অ্যাসাইন করা হয়, যার ফলে `myCar.make`কে অ্যাক্সেস করা হলে আউটপুট `"Maserati"` হয়।

</p>
</details>

---

###### 54. এটার আউটপুট কোনটা?

```javascript
(() => {
  let x = (y = 10);
})();

console.log(typeof x);
console.log(typeof y);
```

- A: `"undefined", "number"`
- B: `"number", "number"`
- C: `"object", "number"`
- D: `"number", "undefined"`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: A

`let x = (y = 10);` আসলে হচ্ছে নিচের উল্লেখিত অংশের সংক্ষিপ্তরূপ ঃ

```javascript
y = 10;
let x = y;
```

আমরা যখন `y` কে সেট করি `10` এর সমান তখন আমরা আসলে গ্লোবাল অবজেক্টে একটি প্রপার্টি `y` যোগ করি (ব্রাউজারে `উইন্ডো`, নোডে `গ্লোবাল`)। একটি ব্রাউজারে, `window.y` এখন `10` এর সমান।

তারপর, আমরা `y` এর ভ্যালু সহ একটি ভেরিয়েবল `x` ডিক্লেয়ার করি, যা `10`। `let` কীওয়ার্ডের সাথে ডিক্লেয়ার করা ভেরিয়েবলগুলি হল _block scoped_, তারা শুধুমাত্র যে ব্লকে ডিক্লেয়ার করা হয়েছে তার মধ্যেই ডিফাইনকৃত (সংজ্ঞায়িত) থাকবে; এই ক্ষেত্রে ইমিডিয়েটলি ইনভোকড ফাংশন এক্সপ্রেশন (IIFE)। যখন আমরা `typeof` অপারেটর ব্যবহার করছি, সেখানে অপারেন্ড `x` ডিফাইন হয়নি: আমরা যে ব্লকে এটি ঘোষণা করা হয়েছে তার বাইরে `x`-কে অ্যাক্সেস করার চেষ্টা করছি। এখানে `x` ডিফাইন হয়নি। যে মানগুলিকে একটি মান অ্যাসাইন করা হয়নি বা ডিক্লেয়ার করা হয়নি সেগুলি `"undefined"` হয় টাইপের। তাই `console.log(typeof x)` `"undefined"` রিটার্ন করেছে।

অন্যদিকে, আমরা `y` কে `10` এর সমান সেট করে একটি গ্লোবাল ভ্যেরিয়েবল তৈরি করেছি `y`। এই ভ্যালুটি কোডের যেকোন অংশ থেকেই অ্যাক্সেস করা যাবে। `y` যেহেতু একটি `"number"` টাইপ দিয়ে ডিফাইন হয়েছে, `console.log(typeof y)` রিটার্ন করেছে `"number"`।

</p>
</details>

---

###### 55. এটার আউটপুট কোনটা?

```javascript
class Dog {
  constructor(name) {
    this.name = name;
  }
}

Dog.prototype.bark = function () {
  console.log(`Woof I am ${this.name}`);
};

const pet = new Dog("Mara");

pet.bark();

delete Dog.prototype.bark;

pet.bark();
```

- A: `"Woof I am Mara"`, `TypeError`
- B: `"Woof I am Mara"`, `"Woof I am Mara"`
- C: `"Woof I am Mara"`, `undefined`
- D: `TypeError`, `TypeError`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: A

`delete` কিওয়ার্ড ব্যবহার করে অবজেক্টের প্রোপার্টিস মুছে ফেলতে পারি, একইভাবে প্রোটোটাইপ থেকেও মুছে ফেলতে পারি। একটি প্রোপার্টিকে প্রোটোটাইপ থেকে মুছে ফেললে তাকে প্রোটোটাইপ চেইনে আর পাওয়া যায় না। এক্ষেত্রে, `delete Dog.prototype.bark`-এর পরে `bark` ফাংশনটি প্রোটোটাইপ চেইনে আর নেই, তবুও আমরা এটি অ্যাক্সেস করার চেষ্টা করেছি।

যখন আমরা ফাংশন নয় এমন কোনো কিছুকে কল করার চেষ্টা করি, তখন একটি `TypeError` থ্রো করা হয়। এই ক্ষেত্রে `TypeError: pet.bark is not a function`, যেহেতু `pet.bark` `undefined`।

</p>
</details>

---

###### 56. এটার আউটপুট কোনটা?

```javascript
const set = new Set([1, 1, 2, 3, 4]);

console.log(set);
```

- A: `[1, 1, 2, 3, 4]`
- B: `[1, 2, 3, 4]`
- C: `{1, 1, 2, 3, 4}`
- D: `{1, 2, 3, 4}`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: D

`Set` অবজেক্টটি হল _অনন্য_ ভ্যালুসমুহের একটি সংগ্রহ: একটি সেটে একই মান কেবল একবারই থাকতে পারে।

আমরা একটি অ্যারে `[1, 1, 2, 3, 4]` পাস করেছি যেখানে একটি ডুপ্লিকেট মান `1` আছে। যেহেতু আমাদের একটি সেটে একই মান দুটি থাকতে পারে না, তাদের মধ্যে একটি সরানো হয়। তাই ফলাফল হয়ছে `{1, 2, 3, 4}`।

</p>
</details>

---

###### 57. এটার আউটপুট কোনটা?

```javascript
// counter.js
let counter = 10;
export default counter;
```

```javascript
// index.js
import myCounter from "./counter";

myCounter += 1;

console.log(myCounter);
```

- A: `10`
- B: `11`
- C: `Error`
- D: `NaN`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: C

একটি ইম্পোর্ট করা মডিউল হল _শুধুমাত্র পড়া যায়_: আপনি ইম্পোর্ট করা মডিউল পরিবর্তন করতে পারবেন না। শুধুমাত্র যে মডিউল তাদের এক্সপোর্ট করে সেই কেবল মানের পরিবর্তন করতে পারে।

যখন আমরা `myCounter` এর মান বৃদ্ধি করার চেষ্টা করি, এটি একটি এরর ছুড়ে দেয়া হয়: `myCounter` is read-only and cannot be modified.

</p>
</details>

---

###### 58. এটার আউটপুট কোনটা?

```javascript
const name = "Lydia";
age = 21;

console.log(delete name);
console.log(delete age);
```

- A: `false`, `true`
- B: `"Lydia"`, `21`
- C: `true`, `true`
- D: `undefined`, `undefined`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: A

`delete` অপারেটর একটি বুলিয়ান মান রিটার্ন করে: ডিলিট সফল হলে `true`, অন্যথায় এটি `false` প্রদান করবে। অন্যদিকে, `var`, `const`, বা `let` কীওয়ার্ডের দিয়ে ডিক্লেয়ার করা ভেরিয়েবল `delete` অপারেটর ব্যবহার করে মুছে ফেলা যায় না।

`name` ভেরিয়েবলটিকে একটি `const` কীওয়ার্ড দিয়ে ডিক্লেয়ার করা হয়েছিল, তাই এটি মুছে ফেলা সফল হয়নি: `false` রিটার্ন করা হয়েছে। যখন আমরা `age` সমান `21` সেট করি, আমরা আসলে গ্লোবাল অবজেক্টে `age` নামক একটি প্রপার্টি যোগ করি। আপনি সফলভাবে অবজেক্টগুলো থেকে এইভাবে প্রপার্টিগুলি মুছে ফেলতে পারেন, গ্লোবাল অবজেক্ট থেকেও তাই `delete age` `true` রিটার্ন করে।

</p>
</details>

---

###### 59. এটার আউটপুট কোনটা?

```javascript
const numbers = [1, 2, 3, 4, 5];
const [y] = numbers;

console.log(y);
```

- A: `[[1, 2, 3, 4, 5]]`
- B: `[1, 2, 3, 4, 5]`
- C: `1`
- D: `[1]`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: C

আমরা ডিস্ট্রাকচারের মাধ্যমে অ্যারের ভ্যালু বা অবজেক্ট প্রোপার্টিস বের করে আনতে পারি। উদাহরণ স্বরূপ:

```javascript
[a, b] = [1, 2];
```

<img src="https://i.imgur.com/ADFpVop.png" width="200">

`a`-এর ভ্যালুটি এখন `1` এবং `b` -এর ভ্যালু এখন `2`। আমরা আসলে এই প্রশ্নের বেলায় যেটা করেছিঃ

```javascript
[y] = [1, 2, 3, 4, 5];
```

<img src="https://i.imgur.com/NzGkMNk.png" width="200">

এর মানে হল, `y` এর ভ্যালু সমান হয় অ্যারের ১ম এলিমেন্টের ভ্যালু, এই ভ্যালুটিি হল `1` সংখ্যাটি। তাই `y` কে যখন লগ করছি রিটার্ন পাই `1`।

</p>
</details>

---

###### 60. এটার আউটপুট কোনটা?

```javascript
const user = { name: "Lydia", age: 21 };
const admin = { admin: true, ...user };

console.log(admin);
```

- A: `{ admin: true, user: { name: "Lydia", age: 21 } }`
- B: `{ admin: true, name: "Lydia", age: 21 }`
- C: `{ admin: true, user: ["Lydia", 21] }`
- D: `{ admin: true }`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: B

স্প্রেড অপারেটর `...` দিয়ে অবজেক্টগুলোকে একত্রিত করা সম্ভব। এর মাধ্যমে একটি অবজেক্টের কি/ভ্যালু জোড়াদ্বয়ের কপি তৈরি করতে পারবেন এবং অন্য অবজেক্টে তাদের যুক্ত করতে পারবেন। এক্ষেত্রে, আমরা `user` অবজেক্টের কপি তৈরি করেছি এবং `admin` অবজেক্টে যুক্ত করেছি। তাই `admin` অবজেক্টে এখন কি/ভ্যালু জোড়ার কপিও রয়েছে, ফলে লগ করায় `{ admin: true, name: "Lydia", age: 21 }` রিটার্ন পাই।

</p>
</details>

---

###### 61. এটার আউটপুট কোনটা?

```javascript
const person = { name: "Lydia" };

Object.defineProperty(person, "age", { value: 21 });

console.log(person);
console.log(Object.keys(person));
```

- A: `{ name: "Lydia", age: 21 }`, `["name", "age"]`
- B: `{ name: "Lydia", age: 21 }`, `["name"]`
- C: `{ name: "Lydia"}`, `["name", "age"]`
- D: `{ name: "Lydia"}`, `["age"]`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: B

`defineProperty` মেথডের সাহায্যে, আমরা একটি অবজেক্টে নতুন প্রোপার্টিস যোগ করতে পারি বা বিদ্যমানগুলিকে সংশোধন করতে পারি। যখন আমরা `defineProperty` মেথডের ব্যবহার করে কোনো অবজেক্টে একটি প্রোপার্টি যোগ করি, তখন সেগুলি ডিফল্টরূপে _গণনাযোগ্য নয়_ (_not enumerable_)। `Object.keys` মেথড একটি অবজেক্টের সমস্ত _গণনাযোগ্য_ প্রোপার্টিসের নাম রিটার্ন করে, এই ক্ষেত্রে শুধুমাত্র `"name"`।

`defineProperty` মেথড ব্যবহার করে যোগ করা প্রোপার্টিসগুলি ডিফল্টরূপে অপরিবর্তনীয়। এ আচরণটিকে আপনি ওভাররাইড করতে পারেন `writable`, `configurable` ও `enumerable` প্রোপার্টিসগুলি ব্যবহার করে। এইভাবে, `defineProperty` মেথড আপনাকে একটি অবজেক্টে যে প্রোপার্টিসগুলি যোগ করছেন তার উপর অনেক বেশি নিয়ন্ত্রণ দেয়।

</p>
</details>

---

###### 62. এটার আউটপুট কোনটা?

```javascript
const settings = {
  username: "lydiahallie",
  level: 19,
  health: 90,
};

const data = JSON.stringify(settings, ["level", "health"]);
console.log(data);
```

- A: `"{"level":19, "health":90}"`
- B: `"{"username": "lydiahallie"}"`
- C: `"["level", "health"]"`
- D: `"{"username": "lydiahallie", "level":19, "health":90}"`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: A

`JSON.stringify` এর দ্বিতীয় আর্গুমেন্ট হল _replacer_। রিপ্লেসার একটি ফাংশন বা একটি অ্যারে হতে পারে এবং এটি আপনাকে নিয়ন্ত্রণ করতে দেয় ভ্যালুগুলো কি ও কীভাবে তারা স্ট্রিংফাই হবে সেটা।

যদি রিপ্লেসার একটি _array_ হয়, শুধুমাত্র অ্যারেতে অন্তর্ভুক্ত প্রোপার্টিসের নামগুলি JSON স্ট্রিংয়ে যোগ করা হবে। এই ক্ষেত্রে, শুধুমাত্র `"level"` এবং `"health"` নামের প্রোপার্টিসগুলি অন্তর্ভুক্ত করা হয়েছে, `"username"` বাদ দেওয়া হয়েছে। তাই `data` এখন `"{"level":19, "health":90}"` এর সমান।

যদি রিপ্লেসারটি একটি _function_ হয়, তাহলে আপনি যে অবজেক্টকে স্ট্রিংফাই করছেন তার প্রতিটি প্রোপার্টিসের জন্য এই ফাংশনটি কল করা হবে। এই ফাংশন থেকে রিটার্ন করা ভ্যালুই হবে সেই প্রোপার্টিসের ভ্যালু যখন এটি JSON স্ট্রিং-এ যোগ করা হয়। ভ্যালুটি যদি `undefined` হয়, তাহলে এই প্রপার্টিটি JSON স্ট্রিং থেকে বাদ দেওয়া হবে।

</p>
</details>

---

###### 63. এটার আউটপুট কোনটা?

```javascript
let num = 10;

const increaseNumber = () => num++;
const increasePassedNumber = (number) => number++;

const num1 = increaseNumber();
const num2 = increasePassedNumber(num1);

console.log(num1);
console.log(num2);
```

- A: `10`, `10`
- B: `10`, `11`
- C: `11`, `11`
- D: `11`, `12`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: A

ইউনারি অপারেটর `++` _প্রথমে অপারেন্ডের মান রিটার্ন করে_, তারপর অপারেন্ডের মান বৃদ্ধি করে। `num1`-এর ভ্যালু `10`, যেহেতু `increaseNumber` ফাংশনটি প্রথমে ভ্যালুটিকে রিটার্ন করে, যেটা হল `10`, তারপরই কেবল ভ্যালুটিকে বৃদ্ধি করে।

`num2` হল `10`, যেহেতু আমরা `num1` কে `increasePassedNumber`-এ পাস করেছি। `number` সমান হল `10` (`num1` এর মান)। আবার, ইউনারী অপারেটর `++` _প্রথমে অপারেন্ডের মান রিটার্ন করে_, তারপর অপারেন্ডের মান বৃদ্ধি করে। তাই `number` এর ভ্যালু হল `10`, ফলে `num2` সমানও হয় `10`।

</p>
</details>

---

###### 64. এটার আউটপুট কোনটা?

```javascript
const value = { number: 10 };

const multiply = (x = { ...value }) => {
  console.log((x.number *= 2));
};

multiply();
multiply();
multiply(value);
multiply(value);
```

- A: `20`, `40`, `80`, `160`
- B: `20`, `40`, `20`, `40`
- C: `20`, `20`, `20`, `40`
- D: `NaN`, `NaN`, `20`, `40`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: C

ইএস৬ এ, আমরা ফাংশনের প্যারামিটারকে একটি ডিফল্ট ভ্যালু দিয়ে ইনিশিয়ালাইজ করতে পারি। প্যারামিটারের ভ্যালুটিই ডিফল্ট হিসেবে থেকে যায় যদি না ফাংশনে অন্য কোন ভ্যালু পাস করা হয়, অথবা প্যারামিটারের ভ্যালুটি `"undefined"` হয়। এক্ষেত্রে, আমরা `value` অবজেক্টের প্রোপার্টিসগুলোকে নতুন অবজেক্টে স্প্রেড করেছি, তাই `x`-এর কাছে ডিফল্ট ভ্যালু থাকছে `{ number: 10 }`।

ডিফল্ট আর্গুমেন্টটির মান নির্নয় হয়ছে ফাংশন _কলের সময়_ ! আমরা প্রতিবার ফাংশন করছি, একটি _নতুন_ অবজেক্ট তৈরি হচ্ছে। প্রথম দুবার আমরা কোন ভ্যালু পাস না করেই `multiply` ফাংশকে চালিয়েছিঃ তাই `x`-এর কাছে ডিফল্ট ভ্যালুটি থাকছে `{ number: 10 }`। তারপর আমরা গুণফল লগ করেছি, যেটি হয় `20`।

৩য় বার, `multiply` ফাংশকে চালিয়েছি, আর্গুমেন্ট এ `value` অবজেক্টকে পাস করে। `*=` অপারেটরটি আসলে `x.number = x.number * 2` এর সংক্ষিপ্তরূপঃ আমরা `x.number`-এর ভ্যালুকে পরিবর্তন করেছি এবং গুণফল `20`-কে লগ করেছি।

৪র্থ বারে, আমরা আবার `value` অবজেক্টকে পাস করেছি। যেহেতু আগেরবার `x.number`-এর ভ্যালুকে পরিবর্তন করে `20` পেয়েছিলাম, অবজেক্ট যেহেতু রেফারেন্স টাইপ তাই এখন `x.number *= 2` লগ করে `40` পাচ্ছি।

</p>
</details>

---

###### 65. এটার আউটপুট কোনটা?

```javascript
[1, 2, 3, 4].reduce((x, y) => console.log(x, y));
```

- A: `1` `2` and `3` `3` and `6` `4`
- B: `1` `2` and `2` `3` and `3` `4`
- C: `1` `undefined` and `2` `undefined` and `3` `undefined` and `4` `undefined`
- D: `1` `2` and `undefined` `3` and `undefined` `4`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: D

`reduce` মেথড ১ম যে আর্গুমেন্টটি নেয় তাকে বলা হয় _accumulator_, এক্ষেত্রে সেটা `x`। ২য় আর্গুমেন্টটিকে বলা হয় _current value_, `y`। `reduce` মেথডের মাধ্যমে, আমরা অ্যারের প্রতীটি এলিমেন্টের জন্য একটি কলব্যাক ফাংশন চালাই, যা শেষ পর্যন্ত একটি একক মানের ফলাফল প্রদান করে।

এই উদাহরনের বেলায়, আমরা কোন ভ্যালুকেই রিটার্ন করছি না, কেবল দুটি ভ্যালুকে _accumulator_ ও _current value_ লগ করছি

_accumulator_ এর ভ্যালুটি কলব্যাক ফাংশনের আগেরবারের রিটার্ন করা ভ্যালুর সমান হয়। `reduce` মেথডের আর্গুমেন্টে আপনি যদি অপশনাল ভ্যালু `initialValue` পাস না করেন, তবে ১ম কলের সময় _accumulator_ এর ভ্যালু সমান হয় অ্যারের ১ম এলিমেন্টটি।

১ম কলে, _accumulator_ (`x`) হয় `1` এবং _current value_ (`y`) হয় `2`। আমরা কলব্যাক ফাংশন থেকে কোন ভ্যালুকেই রিটার্ন করছি না, কেবল _accumulator_ ও _current value_ ভ্যালু লগ করছিঃ `1` ও `2` লগ হয়েছে।

আপনি যদি ফাংশন থেকে কিছু রিটার্ন না করেন তবে, এটা `undefined` রিটার্ন করে। তাই পরবর্তি কলে, _accumulator_ হয় `undefined` _current value_ হয় `3`। `undefined` ও `3` লগ হয়েছে।

৪র্থ কলে, আমরা আবারও কলব্যাক ফাংশন থেকে রিটার্ন করছি না। তাই _accumulator_ আবারও হয় `undefined`, এবং _current value_ হয় `4`। `undefined` ও `4` লগ হয়েছে।

</p>
</details>
  
---

###### 66. কোন কন্সট্রাক্টরটি দিয়ে আমরা সফলভাবে `Dog` ক্লাসকে এক্সটেন্ড করতে পারি?

```javascript
class Dog {
  constructor(name) {
    this.name = name;
  }
};

class Labrador extends Dog {
  // 1
  constructor(name, size) {
    this.size = size;
  }
  // 2
  constructor(name, size) {
    super(name);
    this.size = size;
  }
  // 3
  constructor(size) {
    super(name);
    this.size = size;
  }
  // 4
  constructor(name, size) {
    this.name = name;
    this.size = size;
  }

};
```

- A: 1
- B: 2
- C: 3
- D: 4

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: B

একটি ডিরাইভড ক্লাসে, আপনি `super` কল করার আগে `this` কীওয়ার্ড অ্যাক্সেস করতে পারবেন না। আপনি যদি এটি করার চেষ্টা করেন তবে এটি একটি রেফারেন্স এরর (ReferenceError) থ্রো করবে: 1 এবং 4 একটি রেফারেন্স এরর থ্রো করবে।

`super` কীওয়ার্ড দিয়ে, আমরা প্রদত্ত আর্গুমেন্ট সহ সেই প্যারেন্ট ক্লাসের কনস্ট্রাক্টরকে কল করি। প্যারেন্টের কন্সট্রাক্টর `name` আর্গুমেন্ট নেয়, তাই `super`-এ আমাদের `name` পাস করতে হবে।

`Labrador` ক্লাস দুটি আর্গুমেন্ট নেয়, `name` যেহেতু এটি `Dog` ক্লাসকে এক্সটেন্ড করে এবং `size` কে `Labrador` ক্লাসে একটি অতিরিক্ত প্রোপার্টি হিসাবে এক্সটেন্ড করে। তাদের উভয়কেই `Labrador`-এর কনস্ট্রাক্টর ফাংশনে পাস করতে হবে, যা কনস্ট্রাক্টর 2 ব্যবহার করে সঠিকভাবে করা হয়েছে।

</p>
</details>

---

###### 67. এটার আউটপুট কোনটা?

```javascript
// index.js
console.log("running index.js");
import { sum } from "./sum.js";
console.log(sum(1, 2));

// sum.js
console.log("running sum.js");
export const sum = (a, b) => a + b;
```

- A: `running index.js`, `running sum.js`, `3`
- B: `running sum.js`, `running index.js`, `3`
- C: `running sum.js`, `3`, `running index.js`
- D: `running index.js`, `undefined`, `running sum.js`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: B

`import` কীওয়ার্ড ব্যবহৃত হলে, `import` করা সমস্ত মডিউল _প্রি-পার্স_ করা হয়। এর মানে হল যে ইম্পোর্ট করা মডিউলগুলি _প্রথমে_ চালানো হয়, এবং যে ফাইলে মডিউলটি ইম্পোর্ট করা হয় তার কোড _পরবর্তীতে_ চলবে।

এটি CommonJS-এ `require()` এবং `import` এর মধ্যে একটি পার্থক্য! `require()` দিয়ে, কোড চালানোর সময় আপনি প্রয়োজন অনুযায়ী ডিপেন্ডেন্সিগুলো লোড করতে পারেন। আমরা যদি `import` এর পরিবর্তে `require` ব্যবহার করতাম, কনসোলে লগ হতোঃ `running index.js`, `running sum.js`, `3`।

</p>
</details>

---

###### 68. এটার আউটপুট কোনটা?

```javascript
console.log(Number(2) === Number(2));
console.log(Boolean(false) === Boolean(false));
console.log(Symbol("foo") === Symbol("foo"));
```

- A: `true`, `true`, `false`
- B: `false`, `true`, `false`
- C: `true`, `false`, `true`
- D: `true`, `true`, `true`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: A

প্রতিটি Symbol সম্পূর্ণ অনন্য। Symbol-এ পাস করা আর্গুমেন্টটির উদ্দেশ্য হল Symbol-টিকে একটি বর্ণনা দেওয়া। Symbol-এর মান পাস করা আর্গুমেন্টের উপর নির্ভর করে না। আমরা সমতা পরীক্ষা করার সময়, আমরা দুটি সম্পূর্ণ নতুন Symbol তৈরি করছি: প্রথম `Symbol('foo')`, এবং দ্বিতীয় `Symbol('foo')`। এই দুটি মান অনন্য এবং একে অপরের সমান নয়, তাই `Symbol('foo') === Symbol('foo')` `false` রিটার্ন করে।

</p>
</details>

---

###### 69. এটার আউটপুট কোনটা?

```javascript
const name = "Lydia Hallie";
console.log(name.padStart(13));
console.log(name.padStart(2));
```

- A: `"Lydia Hallie"`, `"Lydia Hallie"`
- B: `" Lydia Hallie"`, `" Lydia Hallie"` (`"[13x whitespace]Lydia Hallie"`, `"[2x whitespace]Lydia Hallie"`)
- C: `" Lydia Hallie"`, `"Lydia Hallie"` (`"[1x whitespace]Lydia Hallie"`, `"Lydia Hallie"`)
- D: `"Lydia Hallie"`, `"Lyd"`,

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: C

`padStart` পদ্ধতির সাহায্যে, আমরা একটি স্ট্রিংয়ের শুরুতে প্যাডিং (শূন্যস্থান) যোগ করতে পারি। এই পদ্ধতিতে পাস করা মান হল প্যাডিংয়ের সাথে স্ট্রিংয়ের _মোট_ দৈর্ঘ্য। স্ট্রিং `"Lydia Hallie"` এর দৈর্ঘ্য `12`। `name.padStart(13)` স্ট্রিং এর শুরুতে 1টি শূন্যস্থান যুক্ত করার কারনে _মোট_ দৈর্ঘ্য 12 + 1 অর্থাৎ 13 হয়।

যদি `padStart` পদ্ধতিতে পাস করা আর্গুমেন্ট স্ট্রিং-এর দৈর্ঘ্যের চেয়ে ছোট হয়, তাহলে কোনো প্যাডিং যোগ করা হবে না।

</p>
</details>

---

###### 70. এটার আউটপুট কোনটা?

```javascript
console.log("🥑" + "💻");
```

- A: `"🥑💻"`
- B: `257548`
- C: A string containing their code points
- D: Error

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: A

`+` অপারেটর দিয়ে, আপনি স্ট্রিং যুক্ত করতে পারেন। এক্ষেত্রে, আমরা স্ট্রিং `"🥑"` কে স্ট্রিং `"💻"` -এর সাথে যুক্ত করছি, যার ফলাফল `"🥑💻"`।

</p>
</details>

---

###### 71. `console.log` স্ট্যাটম্যান্ট এর পরে কমেন্ট করা ভ্যালুটিকে আমরা কিভাবে লগ করতে পারি?

```javascript
function* startGame() {
  const answer = yield "Do you love JavaScript?";
  if (answer !== "Yes") {
    return "Oh wow... Guess we're done here";
  }
  return "JavaScript loves you back ❤️";
}

const game = startGame();
console.log(/* 1 */); // Do you love JavaScript?
console.log(/* 2 */); // JavaScript loves you back ❤️
```

- A: `game.next("Yes").value` and `game.next().value`
- B: `game.next.value("Yes")` and `game.next.value()`
- C: `game.next().value` and `game.next("Yes").value`
- D: `game.next.value()` and `game.next.value("Yes")`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: C

একটি জেনারেটর ফাংশন যখন `yield` কীওয়ার্ডটি দেখে তখন তার চলমান অবস্থায় "বিরতি দেয়" ("pauses" execution)। প্রথমত, আমাদের ফাংশনটি থেকে "Do you love JavaScript?" স্ট্রিংটি পেতে হবে, যা `game.next().value` কল করে পাওয়া যাবে।

প্রতিটি লাইন চালনা করা হয়, যতক্ষণ না এটি প্রথম `yield` কীওয়ার্ড খুঁজে পায়। ফাংশনের মধ্যে প্রথম লাইনে একটি `yield` কীওয়ার্ড আছে: প্রথম ফলাফলের (yield) সাথেই এক্সিকিউশন বন্ধ হয়ে যায়! _এর মানে হল `answer` ভেরিয়েবল এখনো ডিফাইন করা হয়নি!_

যখন আমরা `game.next("Yes").value` কল করি, তখন আগের `yield`টিকে `next()` ফাংশনে পাস করা প্যারামিটারের মান দিয়ে প্রতিস্থাপিত করা হয়, এই ক্ষেত্রে `"Yes"` দিয়ে। ভেরিয়েবল `answer` এর মান এখন `"Yes"` এর সমান। ইফ-স্ট্যাটম্যান্টের শর্ত `false` রিটার্ন করে এবং `JavaScript loves you back ❤️` লগ হয়ে যায়।

</p>
</details>

---

###### 72. এটার আউটপুট কোনটা?

```javascript
console.log(String.raw`Hello\nworld`);
```

- A: `Hello world!`
- B: `Hello` <br />&nbsp; &nbsp; &nbsp;`world`
- C: `Hello\nworld`
- D: `Hello\n` <br /> &nbsp; &nbsp; &nbsp;`world`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: C

`String.raw` একটি স্ট্রিং রিটার্ন করে যেখানে এস্কেপ ক্যারেক্টার (`\n`, `\v`, `\t` ইত্যাদি) উপেক্ষা করা হয়! ব্যাকস্ল্যাশগুলি একটি সমস্যা হতে পারে যখন আপনি এমন কিছু পাবেন:

`` const path = `C:\Documents\Projects\table.html` ``

যার ফলে আউটপুট হবে:

`"C:DocumentsProjects able.html"`

`String.raw` ব্যবহার করলে, এটি কেবল এস্কেপ ক্যারেক্টার উপেক্ষা করবে এবং প্রিন্ট করবে:

`C:\Documents\Projects\table.html`

এই ক্ষেত্রে, লগ হওয়া স্ট্রিংটি হল `Hello\nworld`।

</p>
</details>

---

###### 73. এটার আউটপুট কোনটা?

```javascript
async function getData() {
  return await Promise.resolve("I made it!");
}

const data = getData();
console.log(data);
```

- A: `"I made it!"`
- B: `Promise {<resolved>: "I made it!"}`
- C: `Promise {<pending>}`
- D: `undefined`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: C

একটি **async** ফাংশন সর্বদা একটি প্রতিশ্রুতি (promise) রিটার্ন করে। প্রমিস সমাধানের (resolve) জন্য `await`কে এখনও অপেক্ষা করতে হচ্ছে: যখন `getData()` কল করে এটির মানকে `data`-র সমান সেট করা হয় তখন আসলে একটি অমীমাংসিত (pending) প্রমিস রিটার্ন ভ্যালু হিসেবে পাওয়া যায়।

যদি আমরা প্রমিস সমাধানের ভ্যালুর - `"I made it"` অ্যাক্সেস পেতে চাইতাম, তাহলে `data`-তে `.then()` মেথড ব্যবহার করতে হত:

`data.then(res => console.log(res))`

তবেই এটি লগ করত `"I made it!"`৷

</p>
</details>

---

###### 74. এটার আউটপুট কোনটা?

```javascript
function addToList(item, list) {
  return list.push(item);
}

const result = addToList("apple", ["banana"]);
console.log(result);
```

- A: `['apple', 'banana']`
- B: `2`
- C: `true`
- D: `undefined`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: B

`.push()` মেথড নতুন অ্যারের _length_ রিটার্ন করে! পূর্বে, অ্যারেতে একটি এলিমেন্ট ছিল (স্ট্রিং `"banana"`) এবং এর দৈর্ঘ্য ছিল `1`। অ্যারেতে স্ট্রিং `"apple"` যোগ করার পর, অ্যারের মোট এলিমেন্ট হয় দুটি এবং এর দৈর্ঘ্য হয় `2`। এটিই 'addToList' ফাংশন থেকে রিটার্ন আসছে।

`push` মেথডটি মূল অ্যারেকে পরিবর্তন করে। আপনি যদি _অ্যারের দৈর্ঘ্যে_-র পরিবর্তে ফাংশন থেকে _array_-টি রিটার্ন চাইতেন, তাহলে `item`-কে পুশ করার পরে আপনার উচিত ছিল `list`-কে রিটার্ন করা।

</p>
</details>

---

###### 75. এটার আউটপুট কোনটা?

```javascript
const box = { x: 10, y: 20 };

Object.freeze(box);

const shape = box;
shape.x = 100;

console.log(shape);
```

- A: `{ x: 100, y: 20 }`
- B: `{ x: 10, y: 20 }`
- C: `{ x: 100 }`
- D: `ReferenceError`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: B

`Object.freeze` অবজেক্টে কোন প্রোপার্টি যোগ, বাদ বা সংশোধন করা অসম্ভব করে তোলে (যদি না প্রোপার্টির মান অন্য কোনো অবজেক্ট হয়)।

যখন আমরা ভেরিয়েবল `shape` তৈরি করি এবং তাকে ফ্রোজেন অবজেক্ট `box` এর সমান সেট করি, `shape`-ও সেই ফ্রোজেন অবজেক্টকে রেফার করে। আপনি `Object.isFrozen` ব্যবহার করে কোনো অবজেক্ট ফ্রোজেন হয়েছে কিনা তা পরীক্ষা করতে পারেন। এই ক্ষেত্রে, `Object.isFrozen(shape)` true রিটার্ন করবে, কারন ভেরিয়েবল `shape`-এর কাছে একটি ফ্রোজেন অবজেক্টের রেফারেন্স আছে।

যেহেতু `shape` ফ্রোজেন হয়েছে, এবং `x` এর মান কোনো অবজেক্ট নয়, তাই আমরা `x` প্রোপার্টিকে পরিবর্তন করতে পারি না। `x` এখনও `10` এর সমান, এবং `{ x: 10, y: 20 }` লগ করা হয়েছে।

</p>
</details>

---

###### 76. এটার আউটপুট কোনটা?

```javascript
const { firstName: myName } = { firstName: "Lydia" };

console.log(firstName);
```

- A: `"Lydia"`
- B: `"myName"`
- C: `undefined`
- D: `ReferenceError`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: D

[ডিস্ট্রাকচারিং অ্যাসাইনমেন্ট](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Destructuring_assignment) সিনট্যাক্স ব্যবহার করে, আমরা অ্যারের ভ্যালু, বা অবজেক্টের প্রোপার্টি বের করে আলাদা ভ্যারিয়েবলে রাখতে পারিঃ

```javascript
const { firstName } = { firstName: "Lydia" };
// ES5 version:
// var firstName = { firstName: 'Lydia' }.firstName;

console.log(firstName); // "Lydia"
```

আবার, অবজেক্ট থেকে প্রোপার্টি বের করে অবজেক্টের ঐ প্রোপার্টির নামে না রেখে অন্য নামের ভ্যারিয়েবলেও রাখতে পারিঃ

```javascript
const { firstName: myName } = { firstName: "Lydia" };
// ES5 version:
// var myName = { firstName: 'Lydia' }.firstName;

console.log(myName); // "Lydia"
console.log(firstName); // Uncaught ReferenceError: firstName is not defined
```

অতএব, `firstName` একটি ভেরিয়েবল হিসেবে আর নেই, এইভাবে এর মান অ্যাক্সেস করার চেষ্টা করলে `ReferenceError` তৈরি হবে।

**দ্রষ্টব্য:** `গ্লোবাল স্কোপ` বৈশিষ্ট্য সম্পর্কে সচেতন থাকুন:

```javascript
const { name: myName } = { name: "Lydia" };

console.log(myName); // "lydia"
console.log(name); // "" ----- Browser e.g. Chrome
console.log(name); // ReferenceError: name is not defined  ----- NodeJS
```

জাভাস্ক্রিপ্ট যখনই একটি ভেরিয়েবলকে তার _বর্তমান স্কোপে_ খুঁজে পায় না, তখন এটিকে খুঁজে পাওয়ার জন্য [স্কোপ চেইন](https://github.com/getify/You-Dont-Know-JS/blob/2nd-ed/scope-closures/ch3.md)-এর উপরে ওঠে এবং যদি এটি শীর্ষ-স্তরের স্কোপে পৌঁছায়, ওরফে **গ্লোবাল স্কোপ**, এবং এখানেও খুঁজে না পায়, তাহলে এটি একটি `ReferenceError` থ্রো করবে।

- **ব্রাউজারে** যেমন _Chrome_, `name` হল একটি _ডেপ্রিকেটেড গ্লোবাল স্কোপ প্রপার্টি_। এই উদাহরনে, কোডটি _global scope_ এর ভিতরে চলছে এবং `name` এর জন্য কোনো ইউজার-ডিফাইন্ড লোকাল ভেরিয়েবল নেই, তাই এটি পূর্বনির্ধারিত _ভেরিয়েবল/প্রোপার্টি_ গ্লোবাল স্কোপে খুঁজে দেখে যা ব্রাউজারের ক্ষেত্রে, `window` অবজেক্টের ভেতরে খুঁজবে এবং এটি [window.name](https://developer.mozilla.org/en-US/docs/Web/API/Window/name) মানটি বের করবে একটি **খালি স্ট্রিং** এর সমান।

- **নোডজেএস**-এ, `গ্লোবাল` অবজেক্টে এমন কোনো প্রপার্টি নেই, এইভাবে অস্তিত্বহীন ভেরিয়েবল অ্যাক্সেস করার চেষ্টা করলে একটি [ReferenceError](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Errors/Not_defined) তৈরি হয়।

</p>
</details>

---

###### 77. এটি কি একটি বিশুদ্ধ ফাংশন?

```javascript
function sum(a, b) {
  return a + b;
}
```

- A: Yes
- B: No

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: A

একটি বিশুদ্ধ ফাংশন হল এমন একটি ফাংশন যা _সবসময়_ একই ফলাফল প্রদান করে, যদি একই আর্গুমেন্ট পাস করা হয়।

`sum` ফাংশন সবসময় একই ফলাফল প্রদান করে। যদি আমরা `1` এবং `2` পাস করি, এটি _সবসময়_ পার্শ্ব প্রতিক্রিয়া ছাড়াই `3` রিটার্ন করে। যদি আমরা `5` এবং `10` পাস করি, তাহলে এটি _সবসময়_ `15` রিটার্ন করে, ইত্যাদি। এটিই হলো একটি বিশুদ্ধ ফাংশনের সংজ্ঞা।

</p>
</details>

---

###### 78. এটার আউটপুট কোনটা?

```javascript
const add = () => {
  const cache = {};
  return (num) => {
    if (num in cache) {
      return `From cache! ${cache[num]}`;
    } else {
      const result = num + 10;
      cache[num] = result;
      return `Calculated! ${result}`;
    }
  };
};

const addFunction = add();
console.log(addFunction(10));
console.log(addFunction(10));
console.log(addFunction(5 * 2));
```

- A: `Calculated! 20` `Calculated! 20` `Calculated! 20`
- B: `Calculated! 20` `From cache! 20` `Calculated! 20`
- C: `Calculated! 20` `From cache! 20` `From cache! 20`
- D: `Calculated! 20` `From cache! 20` `Error`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: C

`add` ফাংশনটি একটি _memoized_ ফাংশন। মেমোাআইজেশনের সাহায্যে, আমরা একটি ফাংশনের ফলাফলগুলি ক্যাশ করতে পারি (ভবিষ্যতে ব্যবহারের জন্য আলাদাভাবে সংরক্ষণ করার পদ্ধতি) যাতে এটি কার্যকর করার (execution) গতি বাড়ানো যায়। এই ক্ষেত্রে, আমরা একটি `cache` অবজেক্ট তৈরি করেছি যা পূর্বের রিটার্ন করা ভ্যালুগুলো সংরক্ষণ করে।

> যেহেতু এখানে `add` ফাংশনটি অন্য একটি ফাংশনকে রিটার্ন করছে যে তার স্কোপের বাহিরের ভ্যালু,`cache` অবজেক্টকে, এক্সেস করছে। ফলে এখানে একটি [ক্লোজার](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Closures) তৈরি হয়েছে।

যদি আমরা একই আর্গুমেন্টের সাথে আবার `addFunction` ফাংশনকে কল করি, এটি প্রথমে পরীক্ষা করে যে সেই ভ্যালুটি ইতিমধ্যে cache-থেকে পেয়েছে কিনা। যদি পায়, cache-থেকেই রিটার্ন করা হবে, যা এক্সিকিউশনের সময় বাঁচায়। অন্যথায়, cache-থেকে না পেলে, এটি গণনা করে প্রাপ্ত ভ্যালুটি সংরক্ষণ করবে।

আমরা একই ভ্যালু দিয়ে `addFunction` ফাংশনকে কল করছি ৩ বারঃ ১ম কলের সময়, ফাংশনের ভ্যালু cache-এ নেই যখন `num` সমান সমান হয় `10`। ইফ-স্টেটম্যান্টের শর্ত `num in cache` রিটার্ন করে `false`, এবং এলস ব্লক এক্সিকিউট হয়েছেঃ `Calculated! 20` লগ হয়, এবং result-এর ভ্যালু cache অবজেক্টে সংরক্ষিত হয়। `cache` এখন হয় - `{ 10: 20 }`।

২য় বারে, `cache` অবজেক্টে `10` এর জন্য যে ভ্যালুটি রিটার্ন করা হয়েছিলো সেটি আছে। ইফ-স্টেটম্যানন্টের শর্ত `num in cache` রিটার্ন করে `true`, এবং লগ হয় `'From cache! 20'`।

৩য় বারে, ফাংশনে আমরা পাস করেছি `5 * 2` যেটা মূল্যায়িত হয় `10`। `cache` অবজেক্টে `10` এর জন্য যে ভ্যালুটি রিটার্ন করা হয়েছিলো সেটি আছে। ইফ-স্টেটম্যানন্টের শর্ত `num in cache` রিটার্ন করে `true`, এবং লগ হয় `'From cache! 20'`।

</p>
</details>

---

###### 79. এটার আউটপুট কোনটা?

```javascript
const myLifeSummedUp = ["☕", "💻", "🍷", "🍫"];

for (let item in myLifeSummedUp) {
  console.log(item);
}

for (let item of myLifeSummedUp) {
  console.log(item);
}
```

- A: `0` `1` `2` `3` and `"☕"` `"💻"` `"🍷"` `"🍫"`
- B: `"☕"` `"💻"` `"🍷"` `"🍫"` and `"☕"` `"💻"` `"🍷"` `"🍫"`
- C: `"☕"` `"💻"` `"🍷"` `"🍫"` and `0` `1` `2` `3`
- D: `0` `1` `2` `3` and `{0: "☕", 1: "💻", 2: "🍷", 3: "🍫"}`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: A

একটি _for-in_ লুপ দিয়ে, আমরা **গণনাযোগ্য (enumerable)** প্রোপার্টির উপর লুপ চালাতে পারি। অ্যারেতে গণনাযোগ্য প্রোপার্টিগুলো হয় অ্যারের এলিমেন্টের "কী", যা আসলে তাদের ইনডেক্স। আপনি অ্যারেটিকে দেখতে পাবেন এমন:

`{0: "☕", 1: "💻", 2: "🍷", 3: "🍫"}`

যেখানে কীগুলি গণনাযোগ্য প্রোপার্টি। তাই `0` `1` `2` `3` লগ হয়েছে।

একটি _for-of_ লুপ দিয়ে, আমরা **পুনরাবৃত্তিযোগ্য (iteables)** এর উপর লুপ চালাতে পারি। অ্যারে পুনরাবৃত্তিযোগ্য। যখন আমরা অ্যারের উপর লুপ চালাই, তখন "item" ভেরিয়েবলটি বর্তমানে পুনরাবৃত্তি হচ্ছে সেই এলিমেন্টের সমান। তাই `"☕"` `"💻"` `"🍷"` `"🍫"` লগ হয়েছে।

</p>
</details>

---

###### 80. এটার আউটপুট কোনটা?

```javascript
const list = [1 + 2, 1 * 2, 1 / 2];
console.log(list);
```

- A: `["1 + 2", "1 * 2", "1 / 2"]`
- B: `["12", 2, 0.5]`
- C: `[3, 2, 0.5]`
- D: `[1, 1, 1]`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: C

অ্যারে এলিমেন্টগুলো যেকোন টাইপের ভ্যালু রাখতে পারে। নাম্বার, স্ট্রিং, অঞ্জেক্ট, অন্য অ্যারে, নাল, বুলিয়ান, আন্ডিফাইন্ড, এবং অন্যান্য এক্সপ্রেশন যেমন, তারিখ, ফাংশন, ও যেগুলো গননা যোগ্য।

এলিমেন্টগুলো সমান হবে তার রিটার্ন ভ্যালু। `1 + 2` রিটার্ন করে `3`, `1 * 2` রিটার্ন করে `2`, এবং `1 / 2` রিটার্ন করে `0.5`।

</p>
</details>

---

###### 81. এটার আউটপুট কোনটা?

```javascript
function sayHi(name) {
  return `Hi there, ${name}`;
}

console.log(sayHi());
```

- A: `Hi there,`
- B: `Hi there, undefined`
- C: `Hi there, null`
- D: `ReferenceError`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: B

ডিফল্টভাবে, আর্গুমেন্টগুলোর ভ্যালু থাকে `undefined`, যদি ফাংশনে কোন একটি ভ্যালু পাস করা না হয়। এক্ষেত্রে, আমরা `name` আর্গুমেন্টের জন্য কোন ভ্যালু পাস করি নি। `name` সমান হয় `undefined`, যেটি লগ হয়েছে।

ইএস৬ এ, আমরা এই ডিফল্ট ভ্যালু `undefined` কে ওভাররাইট করতে পারি ডিফল্ট প্যারামিটার দিয়ে। উদাহরনসরূপঃ

`function sayHi(name = "Lydia") { ... }`

এক্ষেত্রে, আমরা যদি কোন একটি ভ্যালু পাস না করি বা `undefined` পাস করি, `name` এর ভ্যালু সবসময় `Lydia` স্ট্রিংটির সমান হবে।

</p>
</details>

---

###### 82. এটার আউটপুট কোনটা?

```javascript
var status = "😎";

setTimeout(() => {
  const status = "😍";

  const data = {
    status: "🥑",
    getStatus() {
      return this.status;
    },
  };

  console.log(data.getStatus());
  console.log(data.getStatus.call(this));
}, 0);
```

- A: `"🥑"` and `"😍"`
- B: `"🥑"` and `"😎"`
- C: `"😍"` and `"😎"`
- D: `"😎"` and `"😎"`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: B

`this` কীওয়ার্ডের মান নির্ভর করে আপনি এটি কোথায় ব্যবহার করছেন তার উপর। একটি **মেথডে**-এ, যেমন `getStatus` মেথডে, `this` কীওয়ার্ডটি _সেই অবজেক্টকে বোঝায় মেথডটি যার ভেতরে থাকে_। মেথডটি `data` অবজেক্টের অন্তর্গত, `this` তাই `data` অবজেক্টকে রেফার করে। যখন আমরা `this.status` লগ করি, `data` অবজেক্টের `status` প্রোপার্টি লগ হয়, যার ভ্যালু `"🥑"`।

`call` মেথডের মাধ্যমে, আমরা অবজেক্টকে পরিবর্তন করতে পারি `this` কীওয়ার্ডটি যাকে রেফার করে। **ফাংশন**-এ, `this` কীওয়ার্ডটি _সেই অবজেক্টকে বোঝায় যেটি ফাংশনটির অন্তর্গত_। আমরা _গ্লোবাল অবজেক্ট_-এ `setTimeout` ফাংশন ডিক্লেয়ার করেছি, তাই `setTimeout` ফাংশনের মধ্যে, `this` কীওয়ার্ডটি _গ্লোবাল অবজেক্ট_ কে রেফার করে। গ্লোবাল অবজেক্টে, _status_ নামক একটি ভেরিয়েবল আছে যার ভ্যালু `"😎"`। তাই `this.status` লগ করায় `"😎"` লগ হয়।

</p>
</details>

---

###### 83. এটার আউটপুট কোনটা?

```javascript
const person = {
  name: "Lydia",
  age: 21,
};

let city = person.city;
city = "Amsterdam";

console.log(person);
```

- A: `{ name: "Lydia", age: 21 }`
- B: `{ name: "Lydia", age: 21, city: "Amsterdam" }`
- C: `{ name: "Lydia", age: 21, city: undefined }`
- D: `"Amsterdam"`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: A

আমরা `city` ভ্যারিয়েবলের ভ্যালু সমান সেট করছি `person` অবজেক্টের `city` নামক প্রোপার্টির ভ্যালুকে। এই অবজেক্টে `city` নামক কোন প্রোপার্টি নেই, তাই `city` ভ্যারিয়েবলের ভ্যালু থাকছে `undefined`।

খেয়াল করুন আমরা কিন্তু `person` অবজেক্টিকে রেফারেন্স (নির্দেশ) _করছি না_! আমরা সাধারন ভাবেই `city` ভ্যারিয়েবলের ভ্যালু সমান সেট করছি `person` অবজেক্টের `city` নামক প্রোপার্টির বর্তমান ভ্যালুকে।

পরবর্তিতে, `city` সমান সেট করছি একটি স্ট্রিং-`"Amsterdam"`। এটা person অবজেক্টে কোন পরিবর্তন করছে নাঃ এখানে ঐ অবজেক্টের কোন রেফারেন্স নেই।

যখন `person` অবজেক্টিকে লগ করা হয়েছে, অপরিবর্তিত অবজেক্টিই রিটার্ন হয়েছে।

</p>
</details>

---

###### 84. এটার আউটপুট কোনটা?

```javascript
function checkAge(age) {
  if (age < 18) {
    const message = "Sorry, you're too young.";
  } else {
    const message = "Yay! You're old enough!";
  }

  return message;
}

console.log(checkAge(21));
```

- A: `"Sorry, you're too young."`
- B: `"Yay! You're old enough!"`
- C: `ReferenceError`
- D: `undefined`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: C

`const` ও `let` কিওয়ার্ড দিয়ে ভ্যারিয়েবলগুলো হয় _ব্লক-স্কোপড_। একটি ব্লক হলো কার্লি ব্র্যাকেটের (`{ }`) ভেতরের যেকোন কিছুই। এক্ষেত্রে, ইফ-এলস স্টেটমেন্টের কার্লি ব্র্যাকেট। আপনি কোন ভ্যারিয়েবলকে যে ব্লকে তাদের ডিক্লেয়ার করা হয়েছে তার বাইরে থেকে রেফারেন্স করতে পারবেন না, একটি ReferenceError হয়।

</p>
</details>

---

###### 85. এখানে কি ধরনের তথ্য লগ হতে পারে?

```javascript
fetch("https://www.website.com/api/user/1")
  .then((res) => res.json())
  .then((res) => console.log(res));
```

- A: The result of the `fetch` method.
- B: The result of the second invocation of the `fetch` method.
- C: The result of the callback in the previous `.then()`.
- D: It would always be undefined.

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: C

২য় `.then`-এ `res` এর ভ্যালু পূর্ববর্তী `.then`-এর রিটার্ন করা ভ্যালুর সমান। আপনি এভাবে `.then`-গুলোর চেইন করতে পারেন, যেখানে বর্তমান ভ্যালুটি পরবর্তী হ্যান্ডলারের কাছে চলে যায়।

</p>
</details>

---

###### 86. কোন অপশনটি `hasName` কে `true` এর সমান সেট করার একটি উপায়, যদি আপনি `true` কে একটি আর্গুমেন্ট হিসেবে পাস করতে না পারেন?

```javascript
function getName(name) {
  const hasName = //
}
```

- A: `!!name`
- B: `name`
- C: `new Boolean(name)`
- D: `name.length`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: A

A-র ক্ষেত্রে, `!!name` দিয়ে, আমরা নির্ধারণ করি `name` এর ভ্যালু সত্য নাকি মিথ্যা। যদি নামটি সত্য হয়, যার জন্য আমরা পরীক্ষা করতে চাই, `!name` রিটার্ন করে `false`। `!false` (যেটি বাস্তবিকভাবেই `!!name`) রিটার্ন করে `true`।

B-র ক্ষেত্রে, `hasName` সমান `name` সেট করার মাধ্যমে, আপনি `hasName` সমান করছেন `getName` ফাংশনে পাস করা যেকোন ভ্যালু, বুলিয়ান `true` ভ্যালু নয়।

C-র ক্ষেত্রে, `new Boolean(true)` একটি অবজেক্ট র‍্যাপার রিটার্ন করে, তার বুলিয়ান ভ্যালুকে নয়।

D-র ক্ষেত্রে, `name.length` রিটার্ন করে পাস করা আর্গুমেন্টের দৈর্ঘ্য, এটি `true` কিনা তা নয়।

</p>
</details>

---

###### 87. এটার আউটপুট কোনটা?

```javascript
console.log("I want pizza"[0]);
```

- A: `"""`
- B: `"I"`
- C: `SyntaxError`
- D: `undefined`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: B

স্ট্রি-এর কোন নির্দিষ্ট ইনডেক্সের অক্ষরকে পাওয়ার জন্য, আপনি ব্র্যাকেট নোটেশন ব্যবহার করতে পারেন। স্ট্রি-এর ১ম অক্ষরের ইনডেক্স হয় 0, এবং এভাবে পরের ইনডেক্সগুলোতে বাকি অক্ষরগুলো থাকে। এক্ষেত্রে, আমরা 0 ইনডেক্সের এলিমেন্টকে পেতে চাচ্ছি, `"I'` অক্ষরটি, যেটা লগ হয়েছে।

মনে রাখবেন যে এই মেথডটি IE7 এবং নীচে সাপোর্ট করে না। সেক্ষেত্রে `.charAt()` ব্যবহার করুন।

</p>
</details>

---

###### 88. এটার আউটপুট কোনটা?

```javascript
function sum(num1, num2 = num1) {
  console.log(num1 + num2);
}

sum(10);
```

- A: `NaN`
- B: `20`
- C: `ReferenceError`
- D: `undefined`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: B

আপনি ফাংশনের ডিফল্ট প্যারামিটারের ভ্যালুকে সমান অন্য প্যারামিটার করতে পারবেন, যতক্ষণ পর্যন্ত তারা ডিফল্ট প্যারামিটারের _আগে_ ডিফাইন করা থাকে। আমরা `sum` ফাংশনে `10` ভ্যালুকে পাস করছি। যদি `sum` ফাংশন একটি আর্গুমেন্ট রিসিভ করে, এর মানে হলো `num2` এর ভ্যালু পাস করা হয়নি, এবং `num1` এর ভ্যালু সমান হল পাস করা ভ্যালুটি `10` এক্ষেত্রে। `num2` এর ডিফল্ট ভ্যালু হল `num1`, যেটা `10`। `num1 + num2` রিটার্ন করেছে `20`।

যদি আপনি ডিফল্ট প্যারামিটারের ভ্যালুকে সমান অন্য প্যারামিটার করতে চান যেটা _পরে_ ডিফাইন করা হয়েছে (ডান পাশের প্যারামিটার), প্যারামিটারের ভ্যালুটি তখনো ইনিশিয়ালাইজ (ভ্যালু সেট করা) হয় নি, সেটি একটি এরর থ্রো করবে।

</p>
</details>

---

###### 89. এটার আউটপুট কোনটা?

```javascript
// module.js
export default () => "Hello world";
export const name = "Lydia";

// index.js
import * as data from "./module";

console.log(data);
```

- A: `{ default: function default(), name: "Lydia" }`
- B: `{ default: function default() }`
- C: `{ default: "Hello world", name: "Lydia" }`
- D: Global object of `module.js`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: A

`import * as name` সিনট্যাক্স দিয়ে, আমরা `module.js` ফাইল থেকে _সকল এক্সপোর্ট_-গুলোকে `index.js` ফাইলে ইম্পোর্ট করছি `data` নামের একটি নতুন অবজেক্ট হিসেবে। `module.js` ফাইলে, দুটি এক্সপোর্ট আছেঃ ডিফল্ট এক্সপোর্ট ও একটি নেমড এক্সপোর্ট। ডিফল্ট এক্সপোর্টটি একটি অ্যারো ফাংশন যে `"Hello World"` স্ট্রিংটি রিটার্ন করছে, এবং নেমড এক্সপোর্টটি হল `name` নামের এটি ভ্যারিয়েবল যেটির ভ্যালু হল `"Lydia"` স্ট্রিংটি।

`data` অবজেক্টটিতে ডিফল্ট এক্সপোর্টের জন্য একটি প্রোপার্টি আছে `default`, অন্যান্য প্রোপার্টিতে আছে নেমড এক্সপোর্টের নামগুলো ও তাদের সংশ্লিষ্ট ভ্যালু।

</p>
</details>

---

###### 90. এটার আউটপুট কোনটা?

```javascript
class Person {
  constructor(name) {
    this.name = name;
  }
}

const member = new Person("John");
console.log(typeof member);
```

- A: `"class"`
- B: `"function"`
- C: `"object"`
- D: `"string"`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: C

ক্লাসগুলি হলো ফাংশন কনস্ট্রাক্টরদের জন্য _সিনট্যাক্টিক সুগার_। একটি ফাংশন কনস্ট্রাক্টর হিসেবে `Person` ক্লাসের সমতুল্য হবে এমন:

```javascript
function Person(name) {
  this.name = name;
}
```

একটি ফাংশন কনস্ট্রাক্টরকে `new` কীওয়ার্ড দিয়ে কল করার ফলে `Person` এর একটি উদাহরন/নিদর্শন (instance) তৈরি হয়, `typeof` কীওয়ার্ড একটি ইন্সট্যান্সের জন্য `"object"` রিটার্ন করে। `typeof member` রিটার্ন করে `"object"`, যেটা লগ হয়।

</p>
</details>

---

###### 91. এটার আউটপুট কোনটা?

```javascript
let newList = [1, 2, 3].push(4);

console.log(newList.push(5));
```

- A: `[1, 2, 3, 4, 5]`
- B: `[1, 2, 3, 5]`
- C: `[1, 2, 3, 4]`
- D: `Error`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: D

`.push` মেথড অ্যারের নতুন দৈর্ঘ্য ফেরত দেয়, অ্যারেটিকে নয়! `newList` কে `[1, 2, 3].push(4)` এর সমান সেট করার মাধ্যমে আমরা `newList` কে অ্যারের নতুন দৈর্ঘ্য `4` এর সমান করেছি।

তারপর, আমরা `.push` মেথডকে `newList` এ ব্যবহার করার চেষ্টা করি। যেহেতু `newList` হল একটি সংখ্যাগত মান `4`, তাই আমরা `.push` মেথড ব্যবহার করতে পারি না: একটি টাইপ এরর (TypeError) প্রদর্শিত হয়।

</p>
</details>

---

###### 92. এটার আউটপুট কোনটা?

```javascript
function giveLydiaPizza() {
  return "Here is pizza!";
}

const giveLydiaChocolate = () => "Here's chocolate... now go hit the gym already.";

console.log(giveLydiaPizza.prototype);
console.log(giveLydiaChocolate.prototype);
```

- A: `{ constructor: ...}` `{ constructor: ...}`
- B: `{}` `{ constructor: ...}`
- C: `{ constructor: ...}` `{}`
- D: `{ constructor: ...}` `undefined`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: D

সাধারণ ফাংশনগুলির, যেমন `giveLydiaPizza` ফাংশনের, একটি `prototype` প্রপার্টি থাকে, যা একটি অবজেক্ট (প্রোটোটাইপ অবজেক্ট) এবং এতে একটি `constructor` প্রপার্টি থাকে। তবে, অ্যারো ফাংশনগুলির, যেমন `giveLydiaChocolate` ফাংশনের, এই `prototype` প্রপার্টি থাকে না। যখন `giveLydiaChocolate.prototype` প্রপার্টি অ্যাক্সেস করার চেষ্টা করা হয়, তখন `undefined` রিটার্ন করা হয়।

</p>
</details>

---

###### 93. এটার আউটপুট কোনটা?

```javascript
const person = {
  name: "Lydia",
  age: 21,
};

for (const [x, y] of Object.entries(person)) {
  console.log(x, y);
}
```

- A: `name` `Lydia` and `age` `21`
- B: `["name", "Lydia"]` and `["age", 21]`
- C: `["name", "age"]` and `undefined`
- D: `Error`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: A

`Object.entries(person)` একটি নেস্টেড অ্যারের একটি অ্যারে রিটার্ন করে, যার প্রতিটি এলিমেন্টে থাকে কী এবং ভ্যালু:

`[ [ 'name', 'Lydia' ], [ 'age', 21 ] ]`

`for-of` লুপ ব্যবহার করে, আমরা অ্যারের প্রতিটি এলিমেন্টের, এই ক্ষেত্রে সাবঅ্যারেগুলি, তে ইটারেট করতে পারি। আমরা `for-of` লুপে সাবঅ্যারেগুলিকে সাথে সাথে ডিস্ট্রাকচার করতে পারি, `const [x, y]` ব্যবহার করে। `x` সাবঅ্যারের প্রথম এলিমেন্টের সমান হয়, `y` সাবঅ্যারের দ্বিতীয় এলিমেন্টের সমান হয়।

প্রথম সাবঅ্যারে `[ "name", "Lydia" ]`, যেখানে `x` `"name"` এর সমান এবং `y` `"Lydia"` এর সমান, যা লগ করা হয়।

দ্বিতীয় সাবঅ্যারে `[ "age", 21 ]`, যেখানে `x` `"age"` এর সমান এবং `y` `21` এর সমান, যা লগ করা হয়।

</p>
</details>

---

###### 94. এটার আউটপুট কোনটা?

```javascript
function getItems(fruitList, ...args, favoriteFruit) {
  return [...fruitList, ...args, favoriteFruit]
}

getItems(["banana", "apple"], "pear", "orange")
```

- A: `["banana", "apple", "pear", "orange"]`
- B: `[["banana", "apple"], "pear", "orange"]`
- C: `["banana", "apple", ["pear"], "orange"]`
- D: `SyntaxError`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: D

`...args` হল একটি রেস্ট প্যারামিটার। রেস্ট প্যারামিটারের মান একটি অ্যারে হয় যা সমস্ত অবশিষ্ট আর্গুমেন্ট ধারণ করে, **এবং এটি শুধুমাত্র শেষ প্যারামিটার হতে পারে**! এই উদাহরণে, রেস্ট প্যারামিটারটি দ্বিতীয় প্যারামিটার ছিল। এটি সম্ভব নয় এবং একটি সিনট্যাক্স এরর ঘটাবে।

```javascript
function getItems(fruitList, favoriteFruit, ...args) {
  return [...fruitList, ...args, favoriteFruit];
}

getItems(["banana", "apple"], "pear", "orange");
```

উপরের উদাহরণটি সঠিকভাবে কাজ করে। এটি অ্যারে `[ 'banana', 'apple', 'orange', 'pear' ]` রিটার্ন করে দেয়।

</p>
</details>

---

###### 95. এটার আউটপুট কোনটা?

```javascript
function nums(a, b) {
  if (a > b) console.log("a is bigger");
  else console.log("b is bigger");
  return;
  a + b;
}

console.log(nums(4, 2));
console.log(nums(1, 2));
```

- A: `a is bigger`, `6` and `b is bigger`, `3`
- B: `a is bigger`, `undefined` and `b is bigger`, `undefined`
- C: `undefined` and `undefined`
- D: `SyntaxError`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: B

জাভাস্ক্রিপ্টে, আমাদের স্পষ্টভাবে সেমিকোলন (`;`) _না লিখলে হবে_, তবে জাভাস্ক্রিপ্ট ইঞ্জিনই স্টেটম্যান্টের পরে সেগুলি যোগ করে দেয়। এটিকে **স্বয়ংক্রিয় সেমিকোলন সংযোজন** (Automatic Semicolon Insertion) বলা হয়। একটি স্টেটম্যান্ট হতে পারে উদাহরণস্বরূপ ভেরিয়েবলগুলি, বা কীওয়ার্ড যেমন `throw`, `return`, `break`, ইত্যাদি।

এখানে, আমরা একটি `return` স্টেটম্যান্টের লিখেছি, এবং আরেকটি মান `a + b` একটি _নতুন লাইনে_। তবে, যেহেতু এটি একটি নতুন লাইন, ইঞ্জিন জানে না যে এটি আসলে সেই মান যা আমরা ফেরত দিতে চেয়েছিলাম। পরিবর্তে, এটি স্বয়ংক্রিয়ভাবে `return` এর পরে একটি সেমিকোলন যোগ করেছে। আপনি এরকম ভাবতে পারেন:

```javascript
return;
a + b;
```

এর মানে হল যে `a + b`-তে কখনই পৌঁছানো হয় না, কারণ একটি ফাংশন `return` কীওয়ার্ডের পরে চলা বন্ধ করে দেয়। যদি কোনও মান রিটার্ন না করা হয়, যেমন এখানে, ফাংশন `undefined` রিটার্ন করে। লক্ষ্য করবেন যে `if/else` স্টেটম্যান্টের পরে কোনও স্বয়ংক্রিয় সংযোজন নেই!

</p>
</details>

---

###### 96. এটার আউটপুট কোনটা?

```javascript
class Person {
  constructor() {
    this.name = "Lydia";
  }
}

Person = class AnotherPerson {
  constructor() {
    this.name = "Sarah";
  }
};

const member = new Person();
console.log(member.name);
```

- A: `"Lydia"`
- B: `"Sarah"`
- C: `Error: cannot redeclare Person`
- D: `SyntaxError`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: B

আমরা ক্লাসগুলিকে অন্য ক্লাস/ফাংশন কনস্ট্রাক্টরের সমান সেট করতে পারি। এই ক্ষেত্রে, আমরা `Person`-কে `AnotherPerson` এর সমান করেছি। এই কনস্ট্রাক্টরের নাম `Sarah`, তাই নতুন `Person` ইনস্ট্যান্স `member` এর name প্রপার্টি `"Sarah"` হবে।

</p>
</details>

---

###### 97. এটার আউটপুট কোনটা?

```javascript
const info = {
  [Symbol("a")]: "b",
};

console.log(info);
console.log(Object.keys(info));
```

- A: `{Symbol('a'): 'b'}` and `["{Symbol('a')"]`
- B: `{}` and `[]`
- C: `{ a: "b" }` and `["a"]`
- D: `{Symbol('a'): 'b'}` and `[]`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: D

একটি Symbol _enumerable_ নয়। Object.keys মেথড একটি অবজেক্টের সমস্ত _enumerable_ কী প্রপার্টিগুলি রিটার্ন করে। Symbol দৃশ্যমান হবে না, এবং একটি খালি অ্যারে রিটার্ন করে। পুরো অবজেক্টটি লগ করলে, সমস্ত প্রপার্টি দৃশ্যমান হবে, এমনকি non-enumerable প্রপার্টিগুলিও।

এটি একটি Symbol এর অনেক গুণাবলীর মধ্যে একটি: সম্পূর্ণ অনন্য মান উপস্থাপন করার পাশাপাশি (যা অবজেক্টগুলিতে আকস্মিক নাম সংঘর্ষ প্রতিরোধ করে, উদাহরণস্বরূপ যখন দুটি লাইব্রেরি অবজেক্টে একই প্রপার্টি যোগ করতে চায়), আপনি এই উপায়ে অবজেক্টগুলিতে প্রপার্টিগুলি "লুকাতে" পারেন (যদিও সম্পূর্ণরূপে নয়। আপনি এখনও `Object.getOwnPropertySymbols()` মেথড ব্যবহার করে Symbol গুলিতে অ্যাক্সেস করতে পারেন)।

</p>
</details>

---

###### 98. এটার আউটপুট কোনটা?

```javascript
const getList = ([x, ...y]) => [x, y]
const getUser = user => { name: user.name, age: user.age }

const list = [1, 2, 3, 4]
const user = { name: "Lydia", age: 21 }

console.log(getList(list))
console.log(getUser(user))
```

- A: `[1, [2, 3, 4]]` and `SyntaxError`
- B: `[1, [2, 3, 4]]` and `{ name: "Lydia", age: 21 }`
- C: `[1, 2, 3, 4]` and `{ name: "Lydia", age: 21 }`
- D: `Error` and `{ name: "Lydia", age: 21 }`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: A

`getList` ফাংশনটি একটি অ্যারে আর্গুমেন্ট হিসাবে গ্রহণ করে। `getList` ফাংশনের বন্ধনীর মধ্যে, আমরা এই অ্যারেটি সাথে সাথে ডিস্ট্রাকচার করি। আপনি এটি এভাবে দেখতে পারেন:

`[x, ...y] = [1, 2, 3, 4]`

রেস্ট প্যারামিটার `...y` ব্যবহার করে, আমরা সমস্ত "অবশিষ্ট" আর্গুমেন্টগুলিকে একটি অ্যারেতে রাখি। এই ক্ষেত্রে অবশিষ্ট আর্গুমেন্টগুলি হল `2`, `3` এবং `4`। `y` এর মান একটি অ্যারে, যা সমস্ত রেস্ট প্যারামিটার ধারণ করে। `x` এর মান এই ক্ষেত্রে `1`, তাই যখন আমরা `[x, y]` লগ করি, তখন `[1, [2, 3, 4]]` লগ হয়।

`getUser` ফাংশনটি একটি অবজেক্ট গ্রহণ করে। অ্যারো ফাংশনের ক্ষেত্রে, আমরা যদি কেবল একটি মান ফেরত দিতে চাই তবে আমাদের কার্লি ব্র্যাকেট লিখতে _হবে না_। তবে, যদি আপনি অ্যারো ফাংশন থেকে সাথে সাথে একটি _অবজেক্ট_ ফেরত দিতে চান, তবে আপনাকে এটি বন্ধনীর মধ্যে লিখতে হবে, অন্যথায় দুটি ব্রেসের মধ্যে থাকা সবকিছু একটি ব্লক স্টেটমেন্ট হিসাবে গণ্য করা হবে। এই ক্ষেত্রে ব্রেসের মধ্যে থাকা কোডটি একটি বৈধ জাভাস্ক্রিপ্ট কোড নয়, তাই একটি `SyntaxError` প্রদর্শিত হয়।

নিম্নলিখিত ফাংশনটি একটি অবজেক্ট ফেরত দিত:

`const getUser = user => ({ name: user.name, age: user.age })`

</p>
</details>

---

###### 99. এটার আউটপুট কোনটা?

```javascript
const name = "Lydia";

console.log(name());
```

- A: `SyntaxError`
- B: `ReferenceError`
- C: `TypeError`
- D: `undefined`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: C

ভেরিয়েবল `name` একটি স্ট্রিং মান ধারণ করে, যা একটি ফাংশন নয়, এবং তাই এটি ইনভোক (কল) করা সম্ভব নয়।

`TypeErrors` তখন প্রদর্শিত হয় যখন কোনও মান প্রত্যাশিত টাইপের না হয়। জাভাস্ক্রিপ্ট আশা করেছিল যে `name` একটি ফাংশন হবে কারণ আমরা এটি ইনভোক করার চেষ্টা করছি। কিন্তু এটি একটি স্ট্রিং ছিল, তাই একটি TypeError প্রদর্শিত হয়: name is not a function!

`SyntaxErrors` তখন প্রদর্শিত হয় যখন আপনি এমন কিছু লিখেছেন যা বৈধ জাভাস্ক্রিপ্ট নয়, উদাহরণস্বরূপ যখন আপনি `return` শব্দটিকে `retrun` হিসাবে লিখেছেন।

`ReferenceErrors` তখন প্রদর্শিত হয় যখন জাভাস্ক্রিপ্ট সেই মানটির রেফারেন্স খুঁজে পায় না যা আপনি অ্যাক্সেস করার চেষ্টা করছেন।

</p>
</details>

---

###### 100. এটার আউটপুটের ভ্যালু কি?

```javascript
// 🎉✨ This is my 100th question! ✨🎉

const output = `${[] && "Im"}possible!
You should${"" && `n't`} see a therapist after so much JavaScript lol`;
```

- A: `possible! You should see a therapist after so much JavaScript lol`
- B: `Impossible! You should see a therapist after so much JavaScript lol`
- C: `possible! You shouldn't see a therapist after so much JavaScript lol`
- D: `Impossible! You shouldn't see a therapist after so much JavaScript lol`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: B

`[]` একটি truthy মান। `&&` অপারেটরের সাথে, বাম পাশের মান যদি একটি truthy মান হয়, তাহলে ডান পাশের মানটি ফেরত দেওয়া হবে। এই ক্ষেত্রে, বাম পাশের মান `[]` একটি truthy মান, তাই `"I'm"` ফেরত দেওয়া হয়।

`""` একটি falsy মান। যদি বাম পাশের মান falsy হয়, তাহলে কিছুই ফেরত দেওয়া হয় না। `n't` ফেরত দেওয়া হয় না।

</p>
</details>

---

###### 101. এটার আউটপুটের ভ্যালু কি?

```javascript
const one = false || {} || null;
const two = null || false || "";
const three = [] || 0 || true;

console.log(one, two, three);
```

- A: `false` `null` `[]`
- B: `null` `""` `true`
- C: `{}` `""` `[]`
- D: `null` `null` `true`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: C

`||` অপারেটরের সাহায্যে, আমরা **প্রথম সত্য অপারেন্ডটি** রিটার্ন করাতে পারি। যদি সমস্ত মান মিথ্যা হয়, **শেষ অপারেন্ডটি** রিটার্ন করে।

`(false || {} || null)`: খালি অবজেক্ট `{}` একটি সত্য মান। এটি প্রথম (এবং একমাত্র) সত্য মান, যা রিটার্ন হয়। `one` সমান `{}`।

`(null || false || "")`: সমস্ত অপারেন্ড মিথ্যা মান। এর মানে হল শেষ অপারেন্ড, `""` রিটার্ন করা হয়। `two` সমান `""`।

`([] || 0 || "")`: খালি অ্যারে`[]` একটি সত্য মান। এই প্রথম সত্য মান, যা রিটার্ন করা হয়. `three` সমান `[]`।

</p>
</details>

---

###### 102. এটার আউটপুটের ভ্যালু কি?

```javascript
const myPromise = () => Promise.resolve("I have resolved!");

function firstFunction() {
  myPromise().then((res) => console.log(res));
  console.log("second");
}

async function secondFunction() {
  console.log(await myPromise());
  console.log("second");
}

firstFunction();
secondFunction();
```

- A: `I have resolved!`, `second` and `I have resolved!`, `second`
- B: `second`, `I have resolved!` and `second`, `I have resolved!`
- C: `I have resolved!`, `second` and `second`, `I have resolved!`
- D: `second`, `I have resolved!` and `I have resolved!`, `second`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: D

একটি প্রমিসের মাধ্যমে, আমরা মূলত বলি, _আমি এই ফাংশনটি চালাতে চাই, কিন্তু এটি সম্পূর্ণ হতে সময় লাগতে পারে বলে এখন এটিকে একপাশে রেখে দেব। যখন কোন নির্দিষ্ট ভ্যালু রিসল্ভ (বা রিজেক্ট) হয়, এবং যখন কল স্ট্যাক খালি থাকে, ঠিক তখনই আমি এই ভ্যালুটি ব্যবহার করতে চাই।_

একটি `async` ফাংশন থেকে এই ভ্যালুটি আমরা `.then` এবং `await` কিওয়ার্ড দুটি দিয়েই পেতে পারি। যদিও আমরা `.then` এবং `await` দুভাবেই প্রমিসের ভ্যালু পেতে পারি, তবে এরা একটু ভিন্নভাবে কাজ করে।

- `firstFunction` এ, আমরা (যেন) myPromise ফাংশনটিকে একপাশে রেখে দিয়েছিলাম যখন এটি চলমান ছিল, কিন্তু অন্য কোডগুলো চলতে থাকে, এই ক্ষেত্রে `console.log('second')`। তারপর ফাংশনটি "I have resolved" স্ট্রিং নিয়ে রিসল্ভ হয়, এবং এটিই পরবর্তিতে লগ হয়েছে যখন সে কল স্ট্যাক খালি পেয়েছে।

- `secondFunction` এ, `await` কিওয়ার্ডের সাহায্যে আমরা আক্ষরিক অর্থে একটি `async` ফাংশনের কার্যক্রমকে বিরতি দিয়ে ভ্যালুটি নিশ্চিত (রিসল্ভ) না হওয়া পর্যন্ত অপেক্ষা করি, তারপর পরের লাইনে যাই।

  এর মানে হল, এটি `myPromise` ফাংশনটির `I have resolved` স্ট্রিং নিয়ে রিসল্ভ হওয়া পর্যন্ত অপেক্ষা করে, এবং কেবল তা ঘটার পরেই আমরা পরের লাইনে গিয়েছি: `second` লগ হয়েছে।

</p>
</details>

---

###### 103. এটার আউটপুটের ভ্যালু কি?

```javascript
const set = new Set();

set.add(1);
set.add("Lydia");
set.add({ name: "Lydia" });

for (let item of set) {
  console.log(item + 2);
}
```

- A: `3`, `NaN`, `NaN`
- B: `3`, `7`, `NaN`
- C: `3`, `Lydia2`, `[object Object]2`
- D: `"12"`, `Lydia2`, `[object Object]2`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: C

`+` অপারেটরটি শুধুমাত্র সংখ্যাসূচক ভ্যালুই যোগ করার জন্য ব্যবহার করা হয় না, আমরা স্ট্রিং সংযুক্ত (concatenate) করতেও এটি ব্যবহার করতে পারি। যখনই জাভাস্ক্রিপ্ট ইঞ্জিন দেখে যে এক বা একাধিক ভ্যালুগুলো একটি সংখ্যা নয়, এটি সংখ্যাটিকে একটি স্ট্রিংয়ে পরিবর্তন করে, এটাকে বলা হয় কোয়ার্শন ([coercion]([https://developer.mozilla.org/en-US/docs/Web/JavaScript/Data_structures#type_coercion]))।

প্রথমটি হল `1`, যা একটি সংখ্যাসূচক ভ্যালু। `1 + 2` রিটার্ন করে নাম্বার `3`।

অন্যদিকে, দ্বিতীয়টি একটি স্ট্রিং `"Lydia"`। `"Lydia"` একটি স্ট্রিং এবং `2` হল একটি সংখ্যা: তাই `2` একটি স্ট্রিংয়ে পরিবর্তিত হয়। `"Lydia"` এবং `"2"` একত্রিত হয়, যার ফলে `"Lydia2"` স্ট্রিং রিটার্ন করে।

`{ name: "Lydia" }` হল অবজেক্ট। একটি নাম্বার বা অবজেক্ট কোনটাই স্ট্রিং নয়, তাই এ দুটি স্ট্রিংফাই হয়। যখনি আমরা একটি সাধারণ অবজেক্টকে স্ট্রিংফাই করি এটা হয়ে যায় - `"[object Object]"`। `"[object Object]"` `"2"` এর সাথে একত্রিত হয়ে রিটার্ন করে `"[object Object]2"`।

</p>
</details>

---

###### 104. এটার ভ্যালুটি কি হবে?

```javascript
Promise.resolve(5);
```

- A: `5`
- B: `Promise {<pending>: 5}`
- C: `Promise {<fulfilled>: 5}`
- D: `Error`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: C

`Promise.resolve` এ আমরা যেকোন টাইপের ভ্যালু পাস করতে পারি, একটি প্রমিস বা নন-প্রমিস। মেথডটি নিজেই রিসল্ভ হওয়া ভ্যালুটি (`<fulfilled>`) সহ একটি প্রমিস রিটার্ন করে। যদি আপনি একটি একটি রেগুলার ফাংশন পাস করেন, এটা একটি রেগুলার ভ্যালু সহ একটি রিসল্ভ প্রমিস হবে। যদি প্রমিস পাস করেন, এটা পাস করা ঐ প্রমিসের রিসল্ভ ভ্যালু সহ একটি রিসল্ভ প্রমিস হবে।

এক্ষেত্রে, আমরা কেবল পাস করেছি একটি সংখ্যাসূচক ভ্যালু `5`। তাই এটা `5` ভ্যালুটিসহ একটি রিসল্ভ প্রমিস রিটার্ন করেছে।

</p>
</details>

---

###### 105. এটার ভ্যালুটি কি হবে?

```javascript
function compareMembers(person1, person2 = person) {
  if (person1 !== person2) {
    console.log("Not the same!");
  } else {
    console.log("They are the same!");
  }
}

const person = { name: "Lydia" };

compareMembers(person);
```

- A: `Not the same!`
- B: `They are the same!`
- C: `ReferenceError`
- D: `SyntaxError`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: B

অবজেক্ট পাস হয় রেফারেন্স দ্বারা। যখন আমরা কঠোর সমতার (strict equality `===`) জন্য অবজেক্টগুলি পরীক্ষা করি, তখন আমরা আদতে তাদের রেফারেন্সগুলি তুলনা করছি।

আমরা `person2`-এর একটি ডিফল্ট ভ্যালু সমান সেট করেছি `person` অবজেক্টকে এবং `person1`-এর ভ্যালু হিসেবেও একই অবজেক্ট `person`কে পাস করেছি। এর মানে হল যে উভয় ভ্যালুর কাছেই মেমরির একই লোকেশনের রেফারেন্স রয়ছে, এইভাবে তারা সমান হয়।

ফলে, `else` স্টেটম্যান্টের কোড ব্লকটি কার্যকর হয়, এবং `They are the same!` লগ হয়।

</p>
</details>

---

###### 106. এটার ভ্যালুটি কি হবে?

```javascript
const colorConfig = {
  red: true,
  blue: false,
  green: true,
  black: true,
  yellow: false,
};

const colors = ["pink", "red", "blue"];

console.log(colorConfig.colors[1]);
```

- A: `true`
- B: `false`
- C: `undefined`
- D: `TypeError`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: D

জাভাস্ক্রিপ্টে, একটি অবজেক্টের প্রোপার্টির ভ্যালু আমরা দুইভাবে এক্সেস করতে পারিঃ ব্র্যাকেট নোটেশন, অথবা ডট নোটেশন। এই উদাহরনে, আমরা ডট নোটেশন (`colorConfig.colors`) ব্যাবহার করেছি ব্র্যাকেট নোটেশনের (`colorConfig["colors"]`) পরিবর্তে।

ডট নোটেশনের মাধ্যমে, জাভাস্ক্রিপ্ট অবজেক্টে নির্দিষ্ট নাম ধরে প্রোপার্টির ভ্যালু খুঁজে পাওয়ার চেষ্টা করে। এই উদাহরনে, জাভাস্ক্রিপ্ট `colorConfig` অবজেক্টে `colors` প্রোপার্টির ভ্যালু খুঁজে পাওয়ার চেষ্টা করেছে। এখানে `colors` নামে কোন প্রোপার্টি খুঁজে না পাওয়ায় রিটার্ন করছে `undefined`। এরপর আমরা `[1]` ব্যবহার করে ১ম এলিমেন্টকে এক্সেস করার চেষ্টা করছি। কিন্তু আমরা এটা করতে পারি না যার ভ্যালু `undefined`, তাই এটি টাইপ এরর ঘটাবে - `TypeError`: `Cannot read property '1' of undefined`।

জাভাস্ক্রিপ্ট স্টেটম্যান্টগুলোকে ভাষান্তর করে (মেশিনের ভাষায়)। যখন ব্র্যাকেট নোটেশন ব্যবহৃত হয়, এটা শুরুর ব্র্যাকেট `[` পেলে তার শেষ ব্র্যাকেট পর্যন্ত `]` যেতে থাকে। তারপরই কেবল এটার মান নির্ণয় করা হবে। আমরা যদি `colorConfig[colors[1]]` ব্যবহার করতাম, এটা `colorConfig` অবজেক্টের `red` প্রপার্টির ভ্যালু রিটার্ন করত।

</p>
</details>

---

###### 107. এটার ভ্যালুটি কি হবে?

```javascript
console.log("❤️" === "❤️");
```

- A: `true`
- B: `false`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: A

ভেতরে ভেতরে, ইমোজিগুলি হল ইউনিকোড৷ হার্ট ইমোজির ইউনিকোড হল `"U+2764 U+FE0F"`। এই ভ্যালুগুলো একই ইমোজিগুলির জন্য সবসময় একই, তাই আমরা দুটি স্ট্রিংকে একে অপরের সমান কিনা তুলনা করছি, যা সত্য রিটার্ন করে।

</p>
</details>

---

###### 108. এই মেথডগুলির মধ্যে কোনটি মূল অ্যারে পরিবর্তন করে?

```javascript
const emojis = ["✨", "🥑", "😍"];

emojis.map((x) => x + "✨");
emojis.filter((x) => x !== "🥑");
emojis.find((x) => x !== "🥑");
emojis.reduce((acc, cur) => acc + "✨");
emojis.slice(1, 2, "✨");
emojis.splice(1, 2, "✨");
```

- A: `All of them`
- B: `map` `reduce` `slice` `splice`
- C: `map` `slice` `splice`
- D: `splice`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: D

`splice` মেথডের সাহায্যে, আমরা মূল অ্যারে পরিবর্তন করি তার এলিমেন্টগুলি বাদ, প্রতিস্থাপন বা যোগ করার মাধ্যমে। এই ক্ষেত্রে, আমরা ইনডেক্স 1 থেকে 2টি এলিমেন্টকে সরিয়ে (আমরা `'🥑'` এবং `'😍'` সরিয়ে দিয়েছি) নতুন ✨ ইমোজি যোগ করেছি।

`map`, `filter` এবং `slice` একটি নতুন অ্যারে রিটার্ন করে, `find` একটি এলিমেন্ট রিটার্ন করে এবং `reduce` একটি হ্রাসকৃত/একত্রিত ভ্যালু রিটার্ন করে।

</p>
</details>

---

###### 109. এটার আউটপুট কোনটা?

```javascript
const food = ["🍕", "🍫", "🥑", "🍔"];
const info = { favoriteFood: food[0] };

info.favoriteFood = "🍝";

console.log(food);
```

- A: `['🍕', '🍫', '🥑', '🍔']`
- B: `['🍝', '🍫', '🥑', '🍔']`
- C: `['🍝', '🍕', '🍫', '🥑', '🍔']`
- D: `ReferenceError`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: A

আমরা `info` অবজেক্টের `favoriteFood` প্রপার্টির ভ্যালু সমান সেট করেছি পিৎজা ইমোজির স্ট্রিং `'🍕'`কে। স্ট্রিং হচ্ছে একটি প্রিমিটিভ ডেটা টাইপ। জাভাস্ক্রিপ্টে, প্রিমিটিভ ডেটা টাইপগুলো ইন্টারঅ্যাক্ট করে ভ্যালু দ্বারা রেফারেন্স দ্বারা নয়।

জাভাস্ক্রিপ্টে, প্রিমিটিভ ডেটা টাইপ (অবজেক্ট ছাড়া সবকিছুই) তাদের _value_ দ্বারা ইন্টারঅ্যাক্ট করে। এই ক্ষেত্রে, আমরা `info` অবজেক্টের `favoriteFood` প্রপার্টির ভ্যালু সমান সেট করেছি `food` অ্যারের প্রথম এলিমেন্টের ভ্যালু, এই ক্ষেত্রে পিৎজা ইমোজির স্ট্রিং (`'🍕'` )।

তারপর, আমরা `info` অবজেক্টে `favoriteFood` প্রপার্টির ভ্যালু পরিবর্তন করি। `food` অ্যারে পরিবর্তিত হয়নি, যেহেতু `favoriteFood`-এর ভ্যালুটি কেবল অ্যারের প্রথম এলিমেন্টের ভ্যালুর একটি _copy_ ছিল, এবং একই মেমরি লোকেশনের `food[0]` এলিমেন্টের মত কোন রেফারেন্স নয়। যখন food লগ করা হয়, এটা এখনো অরিজিনাল অ্যারেই আছে, `['🍕', '🍫', '🥑', '🍔']`।

</p>
</details>

---

###### 110. এই মেথডটি কি করে?

```javascript
JSON.parse();
```

- A: Parses JSON to a JavaScript value
- B: Parses a JavaScript object to JSON
- C: Parses any JavaScript value to JSON
- D: Parses JSON to a JavaScript object only

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: A

`JSON.parse()` মেথড ব্যাবহার করে, আমারা JSON স্ট্রিংকে একটি জাভাস্ক্রিপ্ট ভ্যালুতে পার্স করতে পারি।

```javascript
// Stringifying a number into valid JSON, then parsing the JSON string to a JavaScript value:
const jsonNumber = JSON.stringify(4); // '4'
JSON.parse(jsonNumber); // 4

// Stringifying an array value into valid JSON, then parsing the JSON string to a JavaScript value:
const jsonArray = JSON.stringify([1, 2, 3]); // '[1, 2, 3]'
JSON.parse(jsonArray); // [1, 2, 3]

// Stringifying an object into valid JSON, then parsing the JSON string to a JavaScript value:
const jsonObject = JSON.stringify({ name: "Lydia" }); // '{"name":"Lydia"}'
JSON.parse(jsonObject); // { name: 'Lydia' }
```

</p>
</details>

---

###### 111. এটার আউটপুট কোনটা?

```javascript
let name = "Lydia";

function getName() {
  console.log(name);
  let name = "Sarah";
}

getName();
```

- A: Lydia
- B: Sarah
- C: `undefined`
- D: `ReferenceError`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: D

প্রতিটি ফাংশনের নিজস্ব _execution context_ (বা _scope_) আছে। `getName` ফাংশনটিতে যে ভ্যারিয়েবলকে এক্সেস করা হচ্ছে যেমন, `name` তাকে প্রথমে তার নিজস্ব _context_ (বা _scope_)-এ খুঁজে দেখছে। এক্ষেত্রে, `getName` ফাংশনে তার নিজস্ব `name` ভ্যারিয়েবল আছেঃ আমরা `name` ভ্যারিয়েবলকে ডিক্লেয়ার করেছি `let` কিওয়ার্ড দিয়ে এবং ইনিশিয়ালাইজ করেছি একটি স্ট্রিং - `'Sarah'`।

`let` কিওয়ার্ড (এবং `const`) দিয়ে ভেরিয়েবল নিলে সেটাও **হইস্টেড হয়** তবে `var` এর মত **ইনিশিয়ালাইজ হয় না**। যে লাইনে ডিক্লেয়ার (ইনিশিয়ালাইজ) করা হয়েছে তার আগে তাদেরকে এক্সেস (রিড/রাইট) করা যায় না। এটাকে **"টেম্পোরাল ডেড জোন"** বলা হয়। যখন ভেরিয়েবলকে ডিক্লেয়ার করার আগেই তাকে এক্সেস করার চেষ্টা করা হয় তখন জাভাস্ক্রিপ্ট `ReferenceError` ছুঁঁড়ে দেয়।

যদি `name` ভ্যারিয়েবলটিকে আমরা `getName` ফাংশনে ডিক্লেয়ার না করতাম, জাভাস্ক্রিপ্ট ইঞ্জিন তাকে _scope chain_ এর ভিতর খুঁজে দেখত। বাইরের স্কোপেও একটি `name` ভ্যারিয়াবল আছে যার ভ্যালু একটি স্ট্রিং - `Lydia`। এক্ষেত্রে, এটা লগ করত `Lydia`।

```javascript
let name = "Lydia";

function getName() {
  console.log(name);
}

getName(); // Lydia
```

</p>
</details>

---

###### 112. এটার আউটপুট কোনটা?

```javascript
function* generatorOne() {
  yield ["a", "b", "c"];
}

function* generatorTwo() {
  yield* ["a", "b", "c"];
}

const one = generatorOne();
const two = generatorTwo();

console.log(one.next().value);
console.log(two.next().value);
```

- A: `a` and `a`
- B: `a` and `undefined`
- C: `['a', 'b', 'c']` and `a`
- D: `a` and `['a', 'b', 'c']`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: C

`yield` কিওয়ার্ড দিয়ে, আমরা জেনারেটর ফাংশন থেকে ভ্যালুগুলো `yield` করতে পারি। `yield*` কিওয়ার্ড দিয়ে, আমরা অন্য জেনারেটর ফাংশন থেকে ভ্যালুগুলো, বা ইটারেবল অবজেক্ট (যেমন একটি অ্যারে) থেকে ভ্যালুগুলো `yield` করতে পারি।

`generatorOne` এ, আমরা `yield` কিওয়ার্ড ব্যবহার করে সম্পুর্ন অ্যারে `['a', 'b', 'c']` -কে `yield` করছি।
`one` এর ক্ষেত্রে, (`one.next().value`) এর `next` মেথডের রিটার্ন করা অবজেক্টে `value` প্রোপার্টির ভ্যালু সমান হলো সম্পুর্ন অ্যারেটি- `['a', 'b', 'c']`।

```javascript
console.log(one.next().value); // ['a', 'b', 'c']
console.log(one.next().value); // undefined
```

`generatorTwo` এ, আমরা `yield*` কিওয়ার্ড ব্যবহার করেছি। এর মানে হলো, `two` এ প্রথম yield হওয়া ভ্যালু সমান হচ্ছে ইটারেটরের (`['a', 'b', 'c']`) প্রথম yield হওয়া ভ্যালু। প্রথম yield হওয়া ভ্যালু হলো `a`, তাই প্রথমবার `two.next().value` কল করলে রিটার্ন করে `a`।

```javascript
console.log(two.next().value); // 'a'
console.log(two.next().value); // 'b'
console.log(two.next().value); // 'c'
console.log(two.next().value); // undefined
```

</p>
</details>

---

###### 113. এটার আউটপুট কোনটা?

```javascript
console.log(`${((x) => x)("I love")} to program`);
```

- A: `I love to program`
- B: `undefined to program`
- C: `${(x => x)('I love') to program`
- D: `TypeError`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: A

টেমপ্লেট লিটারেলের মধ্যে থাকা এক্সপ্রেশনের মান নির্ণয় হয় সর্বপ্রথমে। এর মানে হলো, এক্সপ্রেশন থেকে রিটার্ন করা ভ্যালুটি স্ট্রিং এর মধ্যে থাকবে, এক্ষেত্রে, `(x => x)('I love')` ইমিডিয়েটলি ইনভোকড ফাংশন। আমরা `x => x` অ্যারো ফাংশনের একটি আর্গুমেন্ট হিসেবে `'I love'` স্ট্রিংটি পাস করছি। তাই `x` সমান হয় `'I love'`, যেটা রিটার্ন করা হয়। তাই ফলাফল হিসেবে `I love to program` পাওয়া যাচ্ছে।

</p>
</details>

---

###### 114. এখানে কি ঘটবে?

```javascript
let config = {
  alert: setInterval(() => {
    console.log("Alert!");
  }, 1000),
};

config = null;
```

- A: The `setInterval` callback won't be invoked
- B: The `setInterval` callback gets invoked once
- C: The `setInterval` callback will still be called every second
- D: We never invoked `config.alert()`, config is `null`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: C

সধারনত যখন আমরা অবজেক্ট সমান `null` সেট করি, সেই অবজেক্টগুলো _গারবেজ কালেক্টেড_ হয়ে যায় যেহেতু ঐ অবজেক্টের আর কোন রেফারেন্স থাকে না। অন্যদিকে, যেহেতু `setInterval` এর কলব্যাক ফাংশনটি একটি অ্যারো ফাংশন (এজন্য `config` অবজেক্টের ভেতর আবদ্ধ থাকছে), কলব্যাক ফাংশনটি এখনো `config` অবজেক্টের রেফারেন্স ধরে রেখেছে।

যতক্ষণ পর্যন্ত রেফারেন্স থাকছে, অবজেক্টটি _গারবেজ কালেক্টেড_ হবে না। যেহেতু এটি ইন্টারভাল (টাইমার), `config` অবজেক্টকে `null` সেট করা বা `delete` করলেও ইন্টারভাল _গারবেজ কালেক্টেড_ হবে না, তাই ইন্টারভালটি এখনো কল হবে। এটাকে মেমরি থেকে মুছে ফেলার জন্য একে ক্লিয়ার করা উচিৎ `clearInterval(config.alert)` দিয়ে। যেহেতু এটি ক্লিয়ার হয়নি, `setInterval` এর কলব্যাক ফাংশনটি এখনো কল হতে থাকবে প্রতি ১০০০ মিলিসেকেন্ড (১ সেকেন্ড) পরপর।

</p>
</details>

---

###### 115. কোন মেথড(গুলো) `'Hello world!'` ভ্যালুটি রিটার্ন করবে?

```javascript
const myMap = new Map();
const myFunc = () => "greeting";

myMap.set(myFunc, "Hello world!");

//1
myMap.get("greeting");
//2
myMap.get(myFunc);
//3
myMap.get(() => "greeting");
```

- A: 1
- B: 2
- C: 2 and 3
- D: All of them

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: B

যখন `set` মেথড ব্যবহার করে কি/ভ্যালু জোড় যুক্ত করা হয়, `set` মেথডে পাস করা প্রথম আর্গুমেন্ট হবে _কি_ এবং দ্বিতীয়টি হবে _ভ্যালু_। এক্ষেত্রে _কি_ হলো _function_ `() => 'greeting'` এবং _ভ্যালু_ হলো `'Hello world'`। ফলে `myMap` এখন হয় এমন - `{ () => 'greeting' => 'Hello world!' }`

**1**, `myMap.get('greeting')`টি ভুল, যেহতু কি `'greeting'` নয় বরং `() => 'greeting'`।

**3**, `myMap.get(() => 'greeting')` টিও ভুল, যেহেতু আমরা নতুন একটি ফাংশন তৈরি করছি এটাকে প্যারামিটার হিসেবে `set` মেথডে পাস করার মাধ্যমে। অবজেক্ট _reference_ দ্বারা ইন্টারঅ্যাক্ট করে। ফাংশন হল অবজেক্ট, যে কারণে দুটি ফাংশন কখনোই কঠোরভাবে সমান হয় না, এমনকি তারা যদি হুবহু একই হয়: তাদের কাছে মেমরিতে আলাদা আলাদা রেফারেন্স থাকে।

</details>

---

###### 116. এটার আউটপুট কোনটা?

```javascript
const person = {
  name: "Lydia",
  age: 21,
};

const changeAge = (x = { ...person }) => (x.age += 1);
const changeAgeAndName = (x = { ...person }) => {
  x.age += 1;
  x.name = "Sarah";
};

changeAge(person);
changeAgeAndName();

console.log(person);
```

- A: `{name: "Sarah", age: 22}`
- B: `{name: "Sarah", age: 23}`
- C: `{name: "Lydia", age: 22}`
- D: `{name: "Lydia", age: 23}`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: C

`changeAge` এবং `changeAgeAndName` উভয় ফাংশনেরই একটি ডিফল্ট প্যারামিটার আছে, উল্লেখ্য এরা _নতুন_ তৈরিকৃত অবজেক্ট `{ ...person }`। এই অবজেক্টে `person` অবজেক্টের সমস্ত কী/ভ্যালুগুলির কপি রয়েছে৷

প্রথমত, আমরা `changeAge` ফাংশনকে কল করি এবং `person` অবজেক্টটিকে এর আর্গুমেন্ট হিসেবে পাস করি। এই ফাংশনটি `age` প্রোপার্টির মান 1 দ্বারা বৃদ্ধি করে। `person` এখন `{ name: "Lydia", age: 22 }`।

তারপর, আমরা `changeAgeAndName` ফাংশন কল করি, তবে আমরা কোনো প্যারামিটার পাস করিনি। ফলে, `x` এর ভ্যালু সমান হয় _নতুন_ তৈরিকৃত অবজেক্ট `{ ...person }`। যেহেতু এটি একটি নতুন অবজেক্ট, এটি `person` অবজেক্টের কোন প্রোপার্টির ভ্যালুকে প্রভাবিত করে না। `person` এখনও `{ name: "Lydia", age: 22 }` এর সমান।

</p>
</details>

---

###### 117. উল্লেখ্য কোন অপশনটি রিটার্ন করে `6`?

```javascript
function sumValues(x, y, z) {
  return x + y + z;
}
```

- A: `sumValues([...1, 2, 3])`
- B: `sumValues([...[1, 2, 3]])`
- C: `sumValues(...[1, 2, 3])`
- D: `sumValues([1, 2, 3])`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: C

স্প্রেড অপারেটর দিয়ে `...`, আমরা ইটারেবল গুলোকে আলদা এলিমেন্টে স্প্রেড করতে পারি। `sumValues` ফাংশনটি ৩টি আর্গুমেন্ট রিসিভ করছে `x`, `y` ও `z`। কেবল `...[1, 2, 3]` -এর ফলাফল হয় `1, 2, 3`, যেটা আমরা `sumValues` ফাংশনে পাস করেছি।

</p>
</details>

---

###### 118. এটার আউটপুট কোনটা?

```javascript
let num = 1;
const list = ["🥳", "🤠", "🥰", "🤪"];

console.log(list[(num += 1)]);
```

- A: `🤠`
- B: `🥰`
- C: `SyntaxError`
- D: `ReferenceError`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: B

`+=` অপারেটর দিয়ে, আমরা `num` এর ভ্যালু `1` বৃদ্ধি করছি। `num` এর প্রাথমিক ভ্যালু ছিল `1`, ফলে `1 + 1` হয় `2`। `list` অ্যারের ২ নাম্বার ইনডেক্স আইটেমের ভ্যালু পাওয়া যায় 🥰, `console.log(list[2])` প্রিন্ট করছে 🥰।

</p>
</details>

---

###### 119. এটার আউটপুট কোনটা?

```javascript
const person = {
  firstName: "Lydia",
  lastName: "Hallie",
  pet: {
    name: "Mara",
    breed: "Dutch Tulip Hound",
  },
  getFullName() {
    return `${this.firstName} ${this.lastName}`;
  },
};

console.log(person.pet?.name);
console.log(person.pet?.family?.name);
console.log(person.getFullName?.());
console.log(member.getLastName?.());
```

- A: `undefined` `undefined` `undefined` `undefined`
- B: `Mara` `undefined` `Lydia Hallie` `ReferenceError`
- C: `Mara` `null` `Lydia Hallie` `null`
- D: `null` `ReferenceError` `null` `ReferenceError`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: B

অপশনাল চেইনিং অপারেটর `?.` দিয়ে, কোন ডিপার নেস্টেড ভ্যালুগুলো ভ্যালিড কিনা তা আমাদের সরাসরি চেক করার প্রয়োজন হয় না যে। যদি আমরা কোন `undefined` বা `null` ভ্যালু (_নালিশ_) কে এক্সেস করার চেষ্টা করি, এক্সপ্রেশনটি সেখানেই কাজ করা বন্ধ করে দেয় এবং `undefined` রিটার্ন করে।

- `person.pet?.name` এর ক্ষেত্রে, `person` অবজেক্টে `pet` প্রোপার্টি আছেঃ `person.pet` নালিশ নয়। এটায় `name` নামের একটি প্রোপার্টি আছে, এবং রিটার্ন করছে `Mara`।

- `person.pet?.family?.name` এর ক্ষেত্রে, `person` অবজেক্টে `pet` প্রোপার্টি আছেঃ `person.pet` নালিশ নয়। এটায় `family` নামের কোন প্রোপার্টি নেই, `person.pet.family` হলো নালিশ। এক্সপ্রেশনটি `undefined` রিটার্ন করে।

- `person.getFullName?.()` এর ক্ষত্রে, `person` অবজেক্টে `getFullName` প্রোপার্টি আছেঃ `person.getFullName()` নালিশ নয় এবং কল করতে পেরেছে, যেটা `Lydia Hallie` রিটার্ন করছে।

- `member.getLastName?.()` এর ক্ষেত্রে, `member` ভ্যারিয়েবলটিকেই পাওয়া যাচ্ছে না বলে `ReferenceError` ঘটছে।

</p>
</details>

---

###### 120. এটার আউটপুট কোনটা?

```javascript
const groceries = ["banana", "apple", "peanuts"];

if (groceries.indexOf("banana")) {
  console.log("We have to buy bananas!");
} else {
  console.log(`We don't have to buy bananas!`);
}
```

- A: We have to buy bananas!
- B: We don't have to buy bananas
- C: `undefined`
- D: `1`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: B

আমরা ইফ-এলস স্টেটমেন্টে `groceries.indexOf("banana")` শর্ত দিয়েছি। `groceries.indexOf("banana")` রিটার্ন করে `0`, যেটা ফলসি ভ্যালু। যেতেতু ইফ-এলস স্টেটমেন্টের শর্ত ফলসি, তাই `else` ব্লকের কোডটি চলেছে, এবং `We don't have to buy bananas!` লগ হয়েছে।

</p>
</details>

---

###### 121. এটার আউটপুট কোনটা?

```javascript
const config = {
  languages: [],
  set language(lang) {
    return this.languages.push(lang);
  },
};

console.log(config.language);
```

- A: `function language(lang) { this.languages.push(lang }`
- B: `0`
- C: `[]`
- D: `undefined`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: D

`language` মেথডটি হলো একটি `setter`। Setters কোন ভ্যালুকেই ধরে রাখে না, তাদের উদ্দ্যেশই হলো প্রোপার্টিগুলোকে পরিবর্তন করা। যখন `setter` মেথড কল করা হয়, `undefined` রিটার্ন করে।

</p>
</details>

---

###### 122. এটার আউটপুট কোনটা?

```javascript
const name = "Lydia Hallie";

console.log(!typeof name === "object");
console.log(!typeof name === "string");
```

- A: `false` `true`
- B: `true` `false`
- C: `false` `false`
- D: `true` `true`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: C

`typeof name` রিটার্ন করে `"string"`। স্ট্রিং - `"string"` হলো একটি সত্য ভ্যালু, তাই `!typeof name` রিটার্ন করে বুলিয়ান ভ্যালু `false`। `false === "object"` এবং `false === "string"` উভয়েই রিটার্ন করে `false`।

(যদি আমরা চেক করতে চাইতাম যে কোন একটি টাইপ একটি নির্দিষ্ট টাইপের (অ)সমান কিনা, আমাদের `!typeof` এর পরিবর্তে `!==` লেখা উচিৎ ছিল ।)

</p>
</details>

---

###### 123. এটার আউটপুট কোনটা?

```javascript
const add = (x) => (y) => (z) => {
  console.log(x, y, z);
  return x + y + z;
};

add(4)(5)(6);
```

- A: `4` `5` `6`
- B: `6` `5` `4`
- C: `4` `function` `function`
- D: `undefined` `undefined` `6`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: A

`add` ফাংশনটি একটি অ্যারো ফাংশন রিটার্ন করে (একে বলা হয় curried function), যেটা একটি অ্যারো ফাংশন রিটার্ন করে, যেটা একটি অ্যারো ফাংশন রিটার্ন করে (মাথা খারাপ হচ্ছে নাতো 🤯)। ১ম ফাংশন একটি আর্গুমেন্ট রিসিভ করে `x` যার ভ্যালু হলো `4`। আমরা ২য় ফাংশনটি কল করি, যেটা একটি আর্গুমেন্ট রিসিভ করে `y` যার ভ্যালু হলো `5`। এরপর আমরা ৩য় ফাংশনটি কল করি, যেটা একটি আর্গুমেন্ট রিসিভ করে `z` যার ভ্যালু হলো `6`। আমরা যখন শেষ অ্যারো ফাংশনে `x`, `y` ও `z` ভ্যালুকে এক্সেস করার চেষ্টা করছি, জাভাস্ক্রিপ্ট ইঞ্জিন `x` ও `y` এর ভ্যালুগুলোর জন্য তাদের অবস্থান অনুসারে স্কোপ চেইনের উপরে যাচ্ছে। লগ করছে `4` `5` `6` এবং রিটার্ন করছে `15`।

> - ক্যারি ফাংশন (curried functions) ক্লোজার ([closures](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Closures)) এর মাধ্যমে একাধিক ফাংশন কলের মধ্যে স্টেট মেইন্টেইন করে। প্রতিটি রিটার্ন হওয়া ফাংশন তার স্কোপ ভ্যারিয়েবলের ভ্যালুকে মনে রাখে।
> - যখন আপনি `add(4)(5)(6)` কল করছেন, ইনার ফাংশনগুলোতে `x` ও `y` এর ভ্যালু যথাক্রমে, `4` ও `5` এর এক্সেস এখনো থাকছে, যদিও তারা ভিন্ন কনট্যাক্সে চলে।

</p>
</details>

---

###### 124. এটার আউটপুট কোনটা?

```javascript
async function* range(start, end) {
  for (let i = start; i <= end; i++) {
    yield Promise.resolve(i);
  }
}

(async () => {
  const gen = range(1, 3);
  for await (const item of gen) {
    console.log(item);
  }
})();
```

- A: `Promise {1}` `Promise {2}` `Promise {3}`
- B: `Promise {<pending>}` `Promise {<pending>}` `Promise {<pending>}`
- C: `1` `2` `3`
- D: `undefined` `undefined` `undefined`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: C

আমরা যে রেঞ্জটি পাস করছি তাদের প্রতিটির জন্য জেনারেটর ফাংশন `range` প্রমিসসহ একটি এসিঙ্ক অবজেক্ট রিটার্ন করেঃ `Promise{1}`, `Promise{2}`, `Promise{3}`। `gen` ভ্যারিয়েবল সমান সেট করছি এই এসিঙ্ক অবজেক্টিকে, পরবর্তিতে যেটার উপর আমরা `for await ... of` লুপ চালাচ্ছি। এখানে `item` ভ্যারিয়েবল সমান সেট করছি রিটার্ন করা প্রমিস ভ্যালুগুলোকেঃ ১মে `Promise{1}`, পরবর্তিতে `Promise{2}`, পরবর্তিতে `Promise{3}`। যেহেতু আমরা `item` ভ্যারিয়েবলের জন্য _awaiting_ করছি, তাই প্রমিসের রিসল্ভড _ভ্যালুগুলোই_ রিটার্ন হচ্ছেঃ `1`, `2`, ও `3`।

</p>
</details>

---

###### 125. এটার আউটপুট কোনটা?

```javascript
const myFunc = ({ x, y, z }) => {
  console.log(x, y, z);
};

myFunc(1, 2, 3);
```

- A: `1` `2` `3`
- B: `{1: 1}` `{2: 2}` `{3: 3}`
- C: `{ 1: undefined }` `undefined` `undefined`
- D: `undefined` `undefined` `undefined`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: D

`myFunc` ফাংশনটি আর্গুমেন্টে আশা করছে একটি অবজেক্ট যার `x`, `y` ও `z` প্রোপার্টিগুলো আছে। যেহেতু আমরা একটি `x`, `y` ও `z` প্রোপার্টিসহ একটি অবজেক্টের পরিবর্তে ({x: 1, y: 2, z: 3}) আলাদা আলদা সংখ্যাসুচক ভ্যালু (1, 2, 3) পাস করছি, `x`, `y` ও `z`এর ভ্যালুগুলো তাদের ডিফল্ট ভ্যালু `undefined`-ই থাকছে।q

</p>
</details>

---

###### 126. এটার আউটপুট কোনটা?

```javascript
function getFine(speed, amount) {
  const formattedSpeed = new Intl.NumberFormat("en-US", {
    style: "unit",
    unit: "mile-per-hour",
  }).format(speed);

  const formattedAmount = new Intl.NumberFormat("en-US", {
    style: "currency",
    currency: "USD",
  }).format(amount);

  return `The driver drove ${formattedSpeed} and has to pay ${formattedAmount}`;
}

console.log(getFine(130, 300));
```

- A: The driver drove 130 and has to pay 300
- B: The driver drove 130 mph and has to pay \$300.00
- C: The driver drove undefined and has to pay undefined
- D: The driver drove 130.00 and has to pay 300.00

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: B

`Intl.NumberFormat` মেথড ব্যাবহার করে সংখ্যাসুচক ভ্যালুকে কোন একটি লোকালে ফরম্যাট করতে পারি। আমরা সংখ্যাসুচক ভ্যালু `130` কে `unit` হিসেবে `mile-per-hour` দিয়ে `en-US` লোকালে ফরম্যাট করেছি, যেটা ফলাফল দিয়েছে `130 mph`। একইভাবে সংখ্যাসুচক ভ্যালু `300` কে `currency` হিসেবে `USD` দিয়ে `en-US` লোকালে ফরম্যাট করেছি যেটার ফলাফল হয় `$300.00`।

</p>
</details>

---

###### 127. এটার আউটপুট কোনটা?

```javascript
const spookyItems = ["👻", "🎃", "🕸"];
({ item: spookyItems[3] } = { item: "💀" });

console.log(spookyItems);
```

- A: `["👻", "🎃", "🕸"]`
- B: `["👻", "🎃", "🕸", "💀"]`
- C: `["👻", "🎃", "🕸", { item: "💀" }]`
- D: `["👻", "🎃", "🕸", "[object Object]"]`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: B

অবজেক্ট ডিস্ট্রাকচারিং ([ডিস্ট্রাকচারিং অ্যাসাইনমেন্ট](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Destructuring_assignment)) এর মাধ্যমে, ডানপক্ষের অবজেক্টের ভ্যালুগুলোকে বের করে বামপক্ষের অবজেক্টের একই নামের প্রোপার্টির ভ্যালু দিয়ে অ্যাসাইন করতে পারি। এক্ষেত্রে, আমরা "💀" ভ্যালুটিকে `spookyItems[3]`-তে অ্যাসাইন করছি। এর মানে হলো, "💀" ভ্যালুটিকে যুক্ত করে আমরা `spookyItems` অ্যারেকে পরিবর্তন করেছি। তাই `spookyItems` কে লগ করায় `["👻", "🎃", "🕸", "💀"]` লগ হয়েছে।

</p>
</details>

---

###### 128. এটার আউটপুট কোনটা?

```javascript
const name = "Lydia Hallie";
const age = 21;

console.log(Number.isNaN(name));
console.log(Number.isNaN(age));

console.log(isNaN(name));
console.log(isNaN(age));
```

- A: `true` `false` `true` `false`
- B: `true` `false` `false` `false`
- C: `false` `false` `true` `false`
- D: `false` `true` `false` `true`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: C

`Number.isNaN` মেথডের মাধ্যমে, আপনি চেক করতে পারেন যে ভ্যালুটি আপনি পাস করছেন সেটা _সংখ্যাসুচক ভ্যালু_ এবং _`NaN`_ এর সমান হচ্ছে কিনা। `name` সংখ্যাসুচক ভ্যালু নয়, তাই `Number.isNaN(name)` রিটার্ন করছে `false`। `age` সংখ্যাসুচক ভ্যালু কিন্তু `NaN` এর সমান নয়, তাই `Number.isNaN(age)` রিটার্ন করছে `false`।

অন্যদিকে `isNaN` মেথডের মাধ্যমে, আপনি কেবল চেক করতে পারেন যে ভ্যালুটি আপনি পাস করছেন সেটা কোন _সংখ্যা নয়_ কিনা। `name` কোন সংখ্যা নয়, তাই `isNaN(name)` রিটার্ন করছে `true`। `age` একটি সংখ্যা, তাই `isNaN(age)` রিটার্ন করছে `false`

</p>
</details>

---

###### 129. এটার আউটপুট কোনটা?

```javascript
const randomValue = 21;

function getInfo() {
  console.log(typeof randomValue);
  const randomValue = "Lydia Hallie";
}

getInfo();
```

- A: `"number"`
- B: `"string"`
- C: `undefined`
- D: `ReferenceError`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: D

`const` (ও `let`) কিওয়ার্ড দিয়ে ডিক্লেয়ার করা ভ্যারিয়েবলগুলো যে লাইনে ডিক্লেয়ার (ইনিশিয়ালাইজ) করা হয়েছে তার আগে এদেরকে এক্সেস (রিড/রাইট) বা রেফারেন্স করা যায় না। এটাকে **"টেম্পোরাল ডেড জোন"** বলা হয়। তাই ভেরিয়েবলকে ইনিশিয়ালাইজেশনের আগে এক্সেস করার চেষ্টা করা হলে জাভাস্ক্রিপ্ট `ReferenceError` দেয়।

`getInfo` ফাংশনের `randomValue` ভেরিয়েবলটির স্কোপ হচ্ছে তার ফাংশনাল স্কোপ - `getInfo`। যে লাইনে আমরা `typeof randomValue` এর ভ্যালুকে লগ করছি, তখনো `randomValue` ইনিশিয়ালাইজ হয়নিঃ একটি `ReferenceError` হচ্ছে! জাভাস্ক্রিপ্ট ইঞ্জিন স্কোপ চেইনে খুঁজে দেখছে না যেহেতু আমরা `randomValue` ভেরিয়েবলটিকে `getInfo` ফাংশনেই ডিক্লেয়ার করেছি।

</p>
</details>

---

###### 130. এটার আউটপুট কোনটা?

```javascript
const myPromise = Promise.resolve("Woah some cool data");

(async () => {
  try {
    console.log(await myPromise);
  } catch {
    throw new Error(`Oops didn't work`);
  } finally {
    console.log("Oh finally!");
  }
})();
```

- A: `Woah some cool data`
- B: `Oh finally!`
- C: `Woah some cool data` `Oh finally!`
- D: `Oops didn't work` `Oh finally!`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: C

`try` ব্লকে, আমরা `myPromise` ভেরিয়েবলের অপেক্ষিত ভ্যালুটি লগ করার চেষ্টা করছি: `"Woah some cool data"`। যেহেতু `try` ব্লকে কোনো এরর থ্রো হয়নি, `catch` ব্লকের কোড রান হয় না। `finally` ব্লকের কোড _সবসময়ই_ রান হয়, তাই `"Oh finally!"` লগ হয়।

</p>
</details>

---

###### 131. এটার আউটপুট কোনটা?

```javascript
const emojis = ["🥑", ["✨", "✨", ["🍕", "🍕"]]];

console.log(emojis.flat(1));
```

- A: `['🥑', ['✨', '✨', ['🍕', '🍕']]]`
- B: `['🥑', '✨', '✨', ['🍕', '🍕']]`
- C: `['🥑', ['✨', '✨', '🍕', '🍕']]`
- D: `['🥑', '✨', '✨', '🍕', '🍕']`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: B

`flat` পদ্ধতির সাহায্যে, আমরা একটি নতুন, সমতলকৃত অ্যারে তৈরি করতে পারি। সমতলকৃত অ্যারের গভীরতা নির্ভর করে যে মানটি আমরা পাস করি তার উপর। এই ক্ষেত্রে, আমরা মান `1` পাস করেছি (যা আমাদের পাস না করলেও হত, এটি ডিফল্ট মান), এর অর্থ হল কেবলমাত্র প্রথম স্তরের অ্যারেগুলি সংযুক্ত হবে। এই ক্ষেত্রে `['🥑']` এবং `['✨', '✨', ['🍕', '🍕']]`। এই দুটি অ্যারে সংযুক্ত করার ফলে `['🥑', '✨', '✨', ['🍕', '🍕']]` পাওয়া যায়।

</p>
</details>

---

###### 132. এটার আউটপুট কোনটা?

```javascript
class Counter {
  constructor() {
    this.count = 0;
  }

  increment() {
    this.count++;
  }
}

const counterOne = new Counter();
counterOne.increment();
counterOne.increment();

const counterTwo = counterOne;
counterTwo.increment();

console.log(counterOne.count);
```

- A: `0`
- B: `1`
- C: `2`
- D: `3`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: D

`counterOne` হল `Counter` ক্লাসের একটি ইনস্ট্যান্স। `Counter` ক্লাসের কনস্ট্রাক্টরে একটি `count` প্রপার্টি এবং একটি `increment` মেথড রয়েছে। প্রথমে, আমরা `counterOne.increment()` কল করে `increment` মেথড দু'বার কল করেছি। বর্তমানে, `counterOne.count` হল `2`।

<img src="https://i.imgur.com/KxLlTm9.png" width="400">

তারপর, আমরা একটি নতুন ভেরিয়েবল `counterTwo` তৈরি করি এবং এটিকে `counterOne` এর সমান সেট করি। যেহেতু অবজেক্টগুলি রেফারেন্স দ্বারা ইন্টারঅ্যাক্ট করে, আমরা কেবল `counterOne` যে মেমরির লোকেশনে নির্দেশ করে তার একটি নতুন রেফারেন্স তৈরি করছি। যেহেতু এটি একই মেমরি লোকেশনে নির্দেশ করে, তাই `counterTwo` যেই অবজেক্টটির রেফারেন্স দেয় তাতে করা যেকোনো পরিবর্তন `counterOne` এর ক্ষেত্রেও প্রযোজ্য হবে। বর্তমানে, `counterTwo.count` হল `2`।

আমরা `counterTwo.increment()` কল করি, যা `count` কে সেট করে `3`। তারপর, আমরা `counterOne` এর `count` লগ করি, যা লগ করে `3`।

<img src="https://i.imgur.com/BNBHXmc.png" width="400">

</p>
</details>

---

###### 133. এটার আউটপুট কোনটা?

```javascript
const myPromise = Promise.resolve(Promise.resolve("Promise"));

function funcOne() {
  setTimeout(() => console.log("Timeout 1!"), 0);
  myPromise.then((res) => res).then((res) => console.log(`${res} 1!`));
  console.log("Last line 1!");
}

async function funcTwo() {
  const res = await myPromise;
  console.log(`${res} 2!`);
  setTimeout(() => console.log("Timeout 2!"), 0);
  console.log("Last line 2!");
}

funcOne();
funcTwo();
```

- A: `Promise 1! Last line 1! Promise 2! Last line 2! Timeout 1! Timeout 2!`
- B: `Last line 1! Timeout 1! Promise 1! Last line 2! Promise2! Timeout 2! `
- C: `Last line 1! Promise 2! Last line 2! Promise 1! Timeout 1! Timeout 2!`
- D: `Timeout 1! Promise 1! Last line 1! Promise 2! Timeout 2! Last line 2!`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: C

প্রথমে, আমরা `funcOne` ফাংশন চালিয়েছি। `funcOne` এর ১ম লাইনে আমরা _অ্যাসিঙ্ক্রোনাস_ `setTimeout` ফাংশনটি কল করছি, যেখান থেকে কলব্যাকটি Web API এ পাঠানো হয়েছে। (ইভেন্ট লুপের আর্টিক্যালটি পড়ুন <a href="https://dev.to/lydiahallie/javascript-visualized-event-loop-3dif">এখান থেকে</a>.)

পরবর্তিতে আমরা `myPromise` প্রমিসটি কল করেছি যেটা _অ্যাসিঙ্ক্রোনাস_ অপারেশন। মনোযোগ দিন, এখন কেবল `.then()` চেইনের ১ম অংশটি মাইক্রোটাস্ক কিউতে যুক্ত হয়েছে।

প্রমিস ও টাইম-আউট দুটোই _অ্যাসিঙ্ক্রোনাস_ অপারেশন, ফাংশনটি চলতেই থাকে যখন সে প্রমিস সমাধান এবং টাইম-আউট কলব্যাক হ্যান্ডেল করতে থাকে। এর মানে হলো `Last line 1!` লগ হচ্ছে প্রথমে, যেহেতু এটা কোন _অ্যাসিঙ্ক্রোনাস_ অপারেশন নয়।

যেহেতু কলস্ট্যাক এখনো খালি নয় তাই `funcOne` এর `setTimeout` ফাংশন ও `myPromise` প্রমিস তখনো কলস্ট্যাক এ আসতে পারে না।

`funcTwo` এ, `res` ভয়ারেয়েবলটি একটি `Promise` পাচ্ছে কারন `Promise.resolve(Promise.resolve('Promise'))` এর সমমান হলো `Promise.resolve('Promise')` যেহেতু একটি প্রমিস সমাধান করা মানে হলো এর ভ্যালুটিকেই সমাধান করা। `await` এর জন্য এই লাইনে ফাংশনটির এক্সিকিউশন থেমে থাকবে যতক্ষণ পর্যন্ত না সে প্রমিস সমাধান ভ্যালু পাচ্ছে এবং সিঙ্ক্রনাসভাবে শেষ হওয়া পর্যন্ত চলতে থাকে, তাই `Promise 2!` ও এর পরে `Last line 2!` লগ হয় এবং `setTimeout` Web API কে পাঠানো হয়। যদি `funcOne` ফাংশনে `.then()` এর ১ম অংশ নিজের কোন লগ স্টেটমেন্ট থাকত, সেটা `Promise 2!` এর আগে প্রিন্ট হত। যাই হোক, এটা চুপচাপ এক্সিকিউট হয় এবং `.then()` এর ২য় অংশকে মাইক্রোটাস্ক কিউতে পাঠিয়ে দেয়। তাই, ২য় অংশটি `Promise 2!` এর পরেই প্রিন্ট হবে।

পরের ধাপে, কল স্ট্যাক খালি। প্রমিসগুলো _মাইক্রোটাস্ক_ ফলে তাঁরা প্রথমে রিসলভ হবে যখন কল স্ট্যাক খালি থাকবে তাই `Promise 1!` লগ হয়েছে।

এখন যেহতু `funcTwo` কল স্ট্যাক থেকে রেব হয়ে যায়, কল স্ট্যাক খালি থাকছে। কিউতে যে কলব্যাকগুলি অপেক্ষা করছে (`funcOne` এর - `() => console.log("Timeout 1!")` এবং `funcTwo` এর `() => console.log("Timeout 2!")`) তারা একের পর এক কল স্ট্যাক এ যুক্ত হয়। ১ম কলব্যাক লগ করে `Timeout 1!`, এবং কল স্ট্যাক থেকে রেব হয়ে যায়। এরপর, ২য় কলব্যাক লগ করে `Timeout 2!`, এবং কল স্ট্যাক থেকে রেব হয়ে যায়।

</p>
</details>

---

###### 134. কিভাবে আমরা `sum.js` এর `sum` কে `index.js` থেকে কল করতে পারি?

```javascript
// sum.js
export default function sum(x) {
  return x + x;
}

// index.js
import * as sum from "./sum";
```

- A: `sum(4)`
- B: `sum.sum(4)`
- C: `sum.default(4)`
- D: Default aren't imported with `*`, only named exports

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: C

এখানে এস্টেরিস্ক `*` দিয়ে, আমরা ওই ফাইলের সকল এক্সপোর্ট ভ্যালুগুলোকে ইম্পোর্ট করেছি, _ডিফল্ট_ ও _নেমড_ দুটোই। যদি আমাদের নিচে উল্লেখিত ফাইল থাকতঃ

```javascript
// info.js
export const name = "Lydia";
export const age = 21;
export default "I love JavaScript";

// index.js
import * as info from "./info";
console.log(info);
```

তবে নিচে উল্লেখিতভাবে লগ হতঃ

```javascript
{
  default: "I love JavaScript",
  name: "Lydia",
  age: 21
}
```

`sum` উদাহরণের বেলায়, এটা বোঝায় যে ইম্পোর্ট করা `sum` ভ্যালুটি এরকম দেখাবেঃ

```javascript
{ default: function sum(x) { return x + x } }
```

আমরা এই ফানংশনটিকে চালাতে পারি, `sum.default` কল করার মাধ্যমে।

</p>
</details>

---

###### 135. এটার আউটপুট কোনটা?

```javascript
const handler = {
  set: () => console.log("Added a new property!"),
  get: () => console.log("Accessed a property!"),
};

const person = new Proxy({}, handler);

person.name = "Lydia";
person.name;
```

- A: `Added a new property!`
- B: `Accessed a property!`
- C: `Added a new property!` `Accessed a property!`
- D: Nothing gets logged

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: C

Proxy অবজেক্ট দিয়ে, আমরা কোন একটি অবজেক্টে কাস্টম অচারন যুক্ত করতে পারি যেটাকে ২য় আর্গুমেন্ট হিসেবে পাস করি। এক্ষেত্রে, `handler` অবজেক্ট পাস করেছি যেটায় দুটি প্রোপার্টিস আছেঃ `set` এবং `get`। `set` কল হয় যখনি আমরা কোন প্রোপার্টির ভ্যালু _সেট_ করি, এবং `get` কল হয় যখনি আমরা কোন প্রোপার্টির ভ্যালু _পেতে_ চাই (এক্সেস করি)।

প্রথম আর্গুমেন্টটি হলো একটি ফাঁকা অবজেক্ট `{}`, যেটা `person` অবজেক্টের ভ্যালু। এই অবজেক্টে, `handler` অবজেক্টে বর্নীত কাস্টম আচরণগুলো যুক্ত হয়েছে। যদি আমরা `person` অবজেক্টের কোন প্রোপার্টি যুক্ত করি, `set` কল হবে। যদি আমরা `person` অবজেক্টের কোন প্রোপার্টি এক্সেস করি, `get` কল হবে।

প্রথমে, আমরা প্রক্সি অবজেক্টে নতুন প্রোপার্টি `name` যুক্ত করেছি (`person.name = "Lydia"`)। `set` কল হবে, এবং লগ করে `"Added a new property!"`।

এরপরে, আমরা প্রক্সি অবজেক্টের একটি প্রোপার্টি এক্সেস করছি, এবং হ্যান্ডলার অবজেক্টের `get` প্রোপার্টি কল হয়। `"Accessed a property!"` লগ হয়।

</p>
</details>

---

###### 136. নিচের কোনটি `person` অবজেক্টকে পরিবর্তন করবে?

```javascript
const person = { name: "Lydia Hallie" };

Object.seal(person);
```

- A: `person.name = "Evan Bacon"`
- B: `person.age = 21`
- C: `delete person.name`
- D: `Object.assign(person, { age: 21 })`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: A

`Object.seal` ব্যবহার করে, আমরা অবজেক্টে কোন নতুন প্রোপার্টি _যুক্ত_ করায় বাধা দিতে পারে, অথবা কোন প্রোপার্টি _মুছে_ ফেলায় বাধা দিতে পারি।

কিন্তু, আপনি এখনো বিদ্যমান কোন প্রোপার্টির ভ্যালুকে পরিবর্তন করতে পারবেন। যেমন, `person.name = "Evan Bacon"`।

</p>
</details>

---

###### 137. নিচের কোনটি `person` অবজেক্টকে পরিবর্তন করবে?

```javascript
const person = {
  name: "Lydia Hallie",
  address: {
    street: "100 Main St",
  },
};

Object.freeze(person);
```

- A: `person.name = "Evan Bacon"`
- B: `delete person.address`
- C: `person.address.street = "101 Main St"`
- D: `person.pet = { name: "Mara" }`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: C

`Object.freeze` ব্যবহার করে, একটি অবজেক্টকে _সংরক্ষিত_ বা _ফ্রিজ_ করতে পারেন। অর্থাৎ কোন প্রোপার্টি যুক্ত করা, মুছে ফেলা, বা পরিবর্তন করা যাবে না।

কিন্তু, এটা কেবল _অগভীরভাবে_ অবজেক্টকে ফ্রিজ করে, মানে হলো যে এটি অবজেক্টের কেবল _প্রতক্ষ্য_ প্রোপার্টিস (first level) গুলোকে ফ্রিজ করে, যেমন এক্ষেত্রে `address`, এই অবজেক্টের প্রোপার্টিসগুলো ফ্রিজ হয়নি, এবং েদের প্রইবর্তন করা যাবে। যেমন, `person.address.street = "101 Main St"`।

</p>
</details>

---

###### 138. এটার আউটপুট কোনটা?

```javascript
const add = (x) => x + x;

function myFunc(num = 2, value = add(num)) {
  console.log(num, value);
}

myFunc();
myFunc(3);
```

- A: `2` `4` and `3` `6`
- B: `2` `NaN` and `3` `NaN`
- C: `2` `Error` and `3` `6`
- D: `2` `4` and `3` `Error`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: A

প্রথমে, আমরা কোন আর্গুমেন্ট ছাড়াই `myFunc()` কে কল করেছি। যেহেতু কো নার্গুমেন্ট পাস করিনি, `num` ও `value` তাদের ভ্যালু হিসেবে ডিফল্ট ভ্যালুই পাচ্ছেঃ `num` হল `2`, এবং `value` হল `add` ফাংশনের রিটার্ন ভ্যালু। `add` ফাংশনে আমরা একটি আর্গুমেন্ট পাস করেছি `num`, যেটার ভ্যালু হল `2`। `add` ফাংশন রিটার্ন করে `4`, এটাই হলো `value`-র ভ্যালু।

পরবর্তীতে, আমরা `myFunc(3)` করছি, এখানে `3` কে পাস করছি `num` আর্গুমেন্টের ভ্যালু হিসেবে। আমরা `value` আর্গুমেন্টের কোন ভ্যালু পাস করিনি, এটা ডিফল্ট ভ্যালু পাচ্ছেঃ `add` ফাংশনের রিটার্ন ভ্যালু। `add` ফাংশনে আমরা `num` পাস করেছি, যেটার ভ্যালু `3`। `add` ফাংশনের রিটার্ন করে `6`, এটাই হলো `value`-র ভ্যালু।

</p>
</details>

---

###### 139. এটার আউটপুট কোনটা?

```javascript
class Counter {
  #number = 10;

  increment() {
    this.#number++;
  }

  getNum() {
    return this.#number;
  }
}

const counter = new Counter();
counter.increment();

console.log(counter.#number);
```

- A: `10`
- B: `11`
- C: `undefined`
- D: `SyntaxError`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: D

ইএস২০২০ এ, ক্লাসের ভেতর আমারা প্রাইভেট ভ্যারিয়েবল যুক্ত করতে পারি `#` ব্যাবহার করে। আমরা এই ভ্যারিয়েবলগুলোকে ক্লাসের বাইরে থেকে এক্সেস করতে পারি না। যখন `counter.#number` কে লগ করার চেষ্টা করা হয়, SyntaxError ছোড়া হয়ঃ we cannot access it outside the `Counter` class!

</p>
</details>

---

###### 140. এখানে মিসিং অংশে কি হবে?

```javascript
const teams = [
  { name: "Team 1", members: ["Paul", "Lisa"] },
  { name: "Team 2", members: ["Laura", "Tim"] },
];

function* getMembers(members) {
  for (let i = 0; i < members.length; i++) {
    yield members[i];
  }
}

function* getTeams(teams) {
  for (let i = 0; i < teams.length; i++) {
    // ✨ SOMETHING IS MISSING HERE ✨
  }
}

const obj = getTeams(teams);
obj.next(); // { value: "Paul", done: false }
obj.next(); // { value: "Lisa", done: false }
```

- A: `yield getMembers(teams[i].members)`
- B: `yield* getMembers(teams[i].members)`
- C: `return getMembers(teams[i].members)`
- D: `return yield getMembers(teams[i].members)`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: B

`teams` অ্যারের প্রতিটি এলিমেন্টের জন্য `members` এর উপর লুপ চালাতে হলে, `getMembers` জেনারেটর ফাংশনে `teams[i].members` কে পাস করতে হবে। জেনারেটর ফাংশন রিটার্ন করে একটি জেনারেটর অবজেক্ট। জেনারেটর অবজেক্টের প্রতিটি এলিমেন্টের উপর লুপ চালানোন্র জন্য, আমাদেরকে `yield*` ব্যবহার করতে হবে।

যদি আমরা `yield`, `return yield`, বা `return` লিখতাম, সম্পুর্ন জেনেরাটর ফাংশনটি রিটার্ন পেতাম প্রথমবার `next` মেথড করার পরে।

</p>
</details>

---

###### 141. এটার আউটপুট কোনটা?

```javascript
const person = {
  name: "Lydia Hallie",
  hobbies: ["coding"],
};

function addHobby(hobby, hobbies = person.hobbies) {
  hobbies.push(hobby);
  return hobbies;
}

addHobby("running", []);
addHobby("dancing");
addHobby("baking", person.hobbies);

console.log(person.hobbies);
```

- A: `["coding"]`
- B: `["coding", "dancing"]`
- C: `["coding", "dancing", "baking"]`
- D: `["coding", "running", "dancing", "baking"]`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: C

`addHobby` ফাংশনটি ২টি আর্গুমেন্ট গ্রহণ করে, `hobby` ও `hobbies` - যার ডিফল্ট ভ্যালু হলো `person` অবজেক্টের `hobbies` অ্যারে।

প্রথমে, আমরা `addHobby` ফাংশনটি কল করছি এবং `hobby`-এর ভ্যালু পাস করছি `"running"` এবং `hobbies`-এর ভ্যালু পাস করছি একটি ফাঁকা অ্যারে। যেহেতু একটি ফাঁকা অ্যারে পাস করছি `hobbies`-এর ভ্যালু হিসেবে, `"running"` যুক্ত হচ্ছে এই ফাঁকা অ্যারেতে।

এরপরে, আমরা `addHobby` ফাংশনটি কল করছি এবং `hobby`-এর ভ্যালু পাস করছি `"dancing"`। `hobbies` এর জন্য আমরা কোন ভ্যালু পাস করিনি, তাই এটার ভ্যালু হয় ডিফল্ট ভ্যালুটিই, ভ্যালুটি হলো `person` অবজেক্টের `hobbies` অ্যারে। আমরা `person.hobbies` অ্যারেতে `"dancing"` যুক্ত (পুশ) করছি।

সর্শেষে, আমরা `addHobby` ফাংশনটি কল করছি এবং `hobby`-এর ভ্যালু পাস করছি `"baking"`, এবং `hobbies`-এর ভ্যালু পাস করছি `person.hobbies` অ্যারেটি। আমরা `person.hobbies` অ্যারেতে `"baking"` যুক্ত (পুশ) করছি।

</p>
</details>

---

###### 142. এটার আউটপুট কোনটা?

```javascript
class Bird {
  constructor() {
    console.log("I'm a bird. 🦢");
  }
}

class Flamingo extends Bird {
  constructor() {
    console.log("I'm pink. 🌸");
    super();
  }
}

const pet = new Flamingo();
```

- A: `I'm pink. 🌸`
- B: `I'm pink. 🌸` `I'm a bird. 🦢`
- C: `I'm a bird. 🦢` `I'm pink. 🌸`
- D: Nothing, we didn't call any method

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: B

আমরা `pet` ভ্যারিয়েবলটি তৈরি করেছি যেটা `Flamingo` ক্লাসের একটি ইন্সট্যান্স। যখন আমরা এই ইন্সট্যান্সটিকে ইন্সট্যানশিয়েট (`new Flamingo()`) করি, `Flamingo` ক্লাসের কন্সট্রাক্টর কল হয়। প্রথমে, `"I'm pink. 🌸"` লগ হয়, এরপরে আমরা `super()` কল করি। `super()` প্যারেন্ট ক্লাস `Bird`-এর কন্সট্রাক্টরকে কল করে। `Bird` ক্লাসের কন্সট্রাক্টর কল হয় এবং লগ করে `"I'm a bird. 🦢"`।

</p>
</details>

---

###### 143. কোন অপশনটি এরর রেজাল্ট দেয়?

```javascript
const emojis = ["🎄", "🎅🏼", "🎁", "⭐"];

/* 1 */ emojis.push("🦌");
/* 2 */ emojis.splice(0, 2);
/* 3 */ emojis = [...emojis, "🥂"];
/* 4 */ emojis.length = 0;
```

- A: 1
- B: 1 and 2
- C: 3 and 4
- D: 3

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: D

`const` কিওয়ার্ড দিয়ে নেয়া কোন ভ্যারিয়েবলের ভ্যালুকে আমরা _রিডিক্লেয়ার_ করতে পারব না (`emojis = [...emojis, "🥂"]`), এটা কেবল _রিড-অনলি_। কিন্তু ভ্যারিয়েবলের ভ্যালুগুলো নিজেরা অপরিবর্তনীয় নয়। অর্থাৎ `emojis` অ্যারের এলিমেন্টগুলোকে পরিবর্তন করা যাবে, উদাহরণস্বরূপ, নতুন ভ্যালু পুশ (যুক্ত) করা (`emojis.push("🦌")`), স্প্লাইস করা (নির্দিষ্ট ইনডেক্সে ভ্যালু যুক্ত করা) (`emojis.splice(0, 2)`), বা অ্যারের লেন্থকে জিরো (`emojis.length = 0`) সেট করা।

</p>
</details>

---

###### 144. `[...person]` এর আউটপুট `["Lydia Hallie", 21]` পেতে হলে `person` অবজেক্টে আমাদের কি যুক্ত করতে হবে?

```javascript
const person = {
  name: "Lydia Hallie",
  age: 21
}

[...person] // ["Lydia Hallie", 21]
```

- A: Nothing, object are iterable by default
- B: `*[Symbol.iterator]() { for (let x in this) yield* this[x] }`
- C: `*[Symbol.iterator]() { yield* Object.values(this) }`
- D: `*[Symbol.iterator]() { for (let x in this) yield this }`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: C

অবজেক্ট ডিফল্টভাবে ইটারেবল নয়। একটি ইটারেবল ইটারেবল হয় যদি ইটারেটর প্রোটোকল থাকে। আমরা এটা নিজারা যুক্ত করতে পারি ইটারেটর সিম্বল `[Symbol.iterator]` যুক্ত করার মাধ্যমে, যেটাকে একটি জেনারেটর অবজেক্ট রিটার্ন করতে হবে, উদাহরণস্বরূপ এটাকে একটি জেনারেটর ফাংশন `*[Symbol.iterator]() {}` করার মাধ্যমে। এই জেনারেটর ফাংশন `person` অবজেক্টের `Object.values` কে ইল্ড করতে হবে যদি আমরা চাই এটা অ্যারেটি রিটার্ন করবেঃ `["Lydia Hallie", 21]`: `yield* Object.values(this)`

</p>
</details>

---

###### 145. এটার আউটপুট কোনটা?

```javascript
let count = 0;
const nums = [0, 1, 2, 3];

nums.forEach((num) => {
  if (num) count += 1;
});

console.log(count);
```

- A: 1
- B: 2
- C: 3
- D: 4

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: C

`forEach` লুপের `if` শর্তটি চেক করছে `num` এর ভ্যালু ট্রুথি বা ফলসি কিনা। যেহেতু `num` অ্যারের ১ম নাম্বারটি `0`, একটি ফলসি ভ্যালু, তাই `if` স্টেটমেন্টের কোড ব্লকটি চলবে না। `count` কেবল অন্য ৩টি নাম্বারের জন্য বৃদ্ধি পাবে, `1`, `2` ও `3`। যেহেতু `count` `1` করে ৩বার বৃদ্ধি পায়, `count` এর ভ্যালু এখন হয়েছে `3`।

</p>
</details>

---

###### 146. এটার আউটপুট কোনটা?

```javascript
function getFruit(fruits) {
  console.log(fruits?.[1]?.[1]);
}

getFruit([["🍊", "🍌"], ["🍍"]]);
getFruit();
getFruit([["🍍"], ["🍊", "🍌"]]);
```

- A: `null`, `undefined`, 🍌
- B: `[]`, `null`, 🍌
- C: `[]`, `[]`, 🍌
- D: `undefined`, `undefined`, 🍌

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: D

`?.` ব্যবহার করে আমরা অবজেক্টের ডিপার নেস্টেড কোন প্রোপার্টিকে অপশনালি এক্সেস করতে পারি। আমরা চেষ্টা করছি সাব-অ্যারের ইনডেক্স `1` আইটেমটিকে লগ করার যেটা `fruits` অ্যারের ইনডেক্স `1` এ অবস্থিত। যদি `fruits` অ্যারের ইনডেক্স `1` এ সাব-অ্যারেটিকে পাওয়া না যায়, এটা `undefined` রিটার্ন করবে। যদি `fruits` অ্যারের ইনডেক্স `1` এ সাব-অ্যারেটিকে পাওয়া যায়, কিন্তু সাব-অ্যারেতে ইনডেক্স `1` আইটেমটিকে পাওয়া না যায় তখনও এটা `undefined` রিটার্ন করবে।

প্রথমে, আমরা লগ করার চেষ্টা করছি `[['🍊', '🍌'], ['🍍']]`-অ্যারেটির সাব-অ্যারে `['🍍']` থেকে দ্বিতীয় আইটেমটি। এই সাব-অ্যারেতে কেবল একটি আইটেমই আছে, যার মানে হল এর ইনডেক্স `1`-এ কিছু নেই তাই `undefined` রিটার্ন করছে।

এরপর, `getFruits` ফাংশনটিকে কল করেছি কোন ভ্যালুকে আর্গুমেন্ট হিসেবে পাস না করেই, যার মানে হয় `fruits` এর ডিফল্ট ভ্যালু পাচ্ছে `undefined`। যেহেতু, আমরা `fruits` অ্যারের ইনডেক্স `1` আইটেমকে কন্ডিশনালি চেইনিং করছি, এটা `undefined` রিটার্ন করছে কারন ইনডেক্স `1` এর আইটেম নেই।

সর্বশেষে, আমরা চেষ্টা লগ করার করছি `[["🍍"], ["🍊", "🍌"]]`-অ্যারেটির সাব-অ্যারে `['🍊', '🍌']` থেকে দ্বিতীয় আইটেমটি। সাব-অ্যারের ইনডেক্স `1` এর আইটেমটি হল `🍌`, এটিই লগ হয়েছে।

</p>
</details>

---

###### 147. এটার আউটপুট কোনটা?

```javascript
class Calc {
  constructor() {
    this.count = 0;
  }

  increase() {
    this.count++;
  }
}

const calc = new Calc();
new Calc().increase();

console.log(calc.count);
```

- A: `0`
- B: `1`
- C: `undefined`
- D: `ReferenceError`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: A

আমরা `calc` ভ্যারিয়েবলকে সেট করেছি `Calc` ক্লাসের নতুন ইন্সট্যান্সের সমান। এরপর, আমরা `Calc` ক্লাসের নতুন একটি ইন্সট্যান্সকে ইন্সট্যান্সিয়েট করেছি, এবং এই ইন্সট্যান্স দিয়ে `increase` মেথড কল করেছি। যেহেতু `count` প্রোপার্টিটি `Calc` ক্লাসের কন্সট্রাক্টরের ভেতর আছে, তাই এই প্রোপার্টিটি `Calc` ক্লাসের প্রোটোটাইপে শেয়ার হয়নি। এর মানে হল যে `count` প্রোপার্টির ভ্যালুটির কোন পরিবর্তন হয়নি নতুন ইন্সট্যান্স যে `Calc` ক্লাসকে পয়েন্ট করছে তার জন্য, তাই `count` এখনো `0`।

</p>
</details>

---

###### 148. এটার আউটপুট কোনটা?

```javascript
const user = {
  email: "e@mail.com",
  password: "12345",
};

const updateUser = ({ email, password }) => {
  if (email) {
    Object.assign(user, { email });
  }

  if (password) {
    user.password = password;
  }

  return user;
};

const updatedUser = updateUser({ email: "new@email.com" });

console.log(updatedUser === user);
```

- A: `false`
- B: `true`
- C: `TypeError`
- D: `ReferenceError`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: B

`updateUser` ফাংশনটি `user` অবজেক্টের `email` ও `password` প্রোপার্টির ভ্যালুকে পরিবর্তন করে যদি ফাংশনে তাদের ভ্যালুগুলোকে পাস করা হয়, এরপরে ফাংশনটি `user` অবজেক্টটিকে রিটার্ন করে। `updateUser` ফাংশনটির রিটার্ন ভ্যালুটি হল `user` অবজেক্ট, যার মানে `updateUser` এর ভ্যালুটি হল একই `user` অবজেক্টের রেফারেন্স যেটা `user` পয়েন্ট করছে। ফলে `updatedUser === user` সমান হচ্ছে `true`।

</p>
</details>

---

###### 149. এটার আউটপুট কোনটা?

```javascript
const fruit = ["🍌", "🍊", "🍎"];

fruit.slice(0, 1);
fruit.splice(0, 1);
fruit.unshift("🍇");

console.log(fruit);
```

- A: `['🍌', '🍊', '🍎']`
- B: `['🍊', '🍎']`
- C: `['🍇', '🍊', '🍎']`
- D: `['🍇', '🍌', '🍊', '🍎']`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: C

প্রথমে, আমরা `fruit` অ্যারেতে `slice` মেথড কল করেছি। `slice` মেথড আসল অ্যারেকে পরিবর্তন করে না, কিন্তু অ্যারে থেকে খন্ডিত (স্লাইস) করে আনা আইটেম/গুলো রিটার্ন করেঃ এক্ষেত্রে, কলার ইমজি `'🍌'`।

এরপরে, আমরা `fruit` অ্যারেতে `splice` মেথড কল করেছি। `splice` মেথড আসল অ্যারেকে পরিবর্তন করে, যার মানে হল, এখন `fruit` অ্যারেতে অবশিষ্ট আছে `['🍊', '🍎']`।

সর্বশেষে, আমরা `fruit` অ্যারেতে `unshift` মেথড কল করেছি। `unshift` মেথডে পাস করা ভ্যালু/গুলোকে অ্যারেতে যুক্ত করার মাধ্যমে সে আসল অ্যারেকে পরিবর্তন করে, এক্ষেত্রে অ্যারের প্রথম এলিমেন্ট হিসেবে। তাই এখন `fruit` অ্যারেটিতে থাকছে `['🍇', '🍊', '🍎']`।

</p>
</details>

---

###### 150. এটার আউটপুট কোনটা?

```javascript
const animals = {};
let dog = { emoji: "🐶" };
let cat = { emoji: "🐈" };

animals[dog] = { ...dog, name: "Mara" };
animals[cat] = { ...cat, name: "Sara" };

console.log(animals[dog]);
```

- A: `{ emoji: "🐶", name: "Mara" }`
- B: `{ emoji: "🐈", name: "Sara" }`
- C: `undefined`
- D: `ReferenceError`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: B

অবজেক্টের কি-গুলোকে জাভাস্ক্রিপ্ট ইঞ্জিন স্ট্রিং-এ পরিবর্তন করে।

যেহেতু `dog` এর ভ্যালুটি একটি অবজেক্ট, `animals[dog]` এর মানে আমরা আসলে নতুন একটি অবজেক্ট সমান সেট করছি `"[object Object]"` নামের নতুন একটি প্রোপার্টি। ফলে এখন `animals["[object Object]"]` এর সমান হলো `{ emoji: "🐶", name: "Mara"}`।

`cat`-ও একটি অবজেক্ট, যার মানে হলো `animals[cat]` আসলে `animals["[object Object]"]` এর ভ্যালুকে ওভাররাইড করা হয়েছে নতুন cat প্রোপার্টি দিয়ে অর্থাৎ `animals["[object Object]"]` সমান এখন `{ emoji: "🐈", name: "Sara" }`।

`animals[dog]` কে লগ করা, আসলে `animals["[object Object]"]` কেই লগ করা যেহেতু `dog` অবজেক্টকে স্ট্রিং এ পরিবর্তন করলে পাওয়া যায় `"[object Object]"` যেটা রিটার্ন করে `{ emoji: "🐈", name: "Sara" }`।

</p>
</details>

---

###### 151. এটার আউটপুট কোনটা?

```javascript
const user = {
  email: "my@email.com",
  updateEmail: (email) => {
    this.email = email;
  },
};

user.updateEmail("new@email.com");
console.log(user.email);
```

- A: `my@email.com`
- B: `new@email.com`
- C: `undefined`
- D: `ReferenceError`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: A

The `updateEmail` function is an arrow function, and is not bound to the `user` object. This means that the `this` keyword is not referring to the `user` object, but refers to the global scope in this case. The value of `email` within the `user` object does not get updated. When logging the value of `user.email`, the original value of `my@email.com` gets returned.

</p>
</details>

---

###### 152. এটার আউটপুট কোনটা?

```javascript
const promise1 = Promise.resolve("First");
const promise2 = Promise.resolve("Second");
const promise3 = Promise.reject("Third");
const promise4 = Promise.resolve("Fourth");

const runPromises = async () => {
  const res1 = await Promise.all([promise1, promise2]);
  const res2 = await Promise.all([promise3, promise4]);
  return [res1, res2];
};

runPromises()
  .then((res) => console.log(res))
  .catch((err) => console.log(err));
```

- A: `[['First', 'Second'], ['Fourth']]`
- B: `[['First', 'Second'], ['Third', 'Fourth']]`
- C: `[['First', 'Second']]`
- D: `'Third'`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: D

The `Promise.all` method runs the passed promises in parallel. If one promise fails, the `Promise.all` method _rejects_ with the value of the rejected promise. In this case, `promise3` is rejected with the value `"Third"`. We’re catching the rejected value in the chained `catch` method on the `runPromises` invocation to catch any errors within the `runPromises` function. Only `"Third"` gets logged, since `promise3` is rejected with this value.

</p>
</details>

---

###### 153. What should the value of `method` be to log `{ name: "Lydia", age: 22 }`?

```javascript
const keys = ["name", "age"];
const values = ["Lydia", 22];

const method =
  /* ?? */
  Object[method](
    keys.map((_, i) => {
      return [keys[i], values[i]];
    })
  ); // { name: "Lydia", age: 22 }
```

- A: `entries`
- B: `values`
- C: `fromEntries`
- D: `forEach`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: C

The `fromEntries` method turns a 2d array into an object. The first element in each subarray will be the key, and the second element in each subarray will be the value. In this case, we’re mapping over the `keys` array, which returns an array that the first element is the item on the key array on the current index, and the second element is the item of the values array on the current index.

This creates an array of subarrays containing the correct keys and values, which results in `{ name: "Lydia", age: 22 }`

</p>
</details>

---

###### 154. এটার আউটপুট কোনটা?

```javascript
const createMember = ({ email, address = {} }) => {
  const validEmail = /.+\@.+\..+/.test(email);
  if (!validEmail) throw new Error("Valid email pls");

  return {
    email,
    address: address ? address : null,
  };
};

const member = createMember({ email: "my@email.com" });
console.log(member);
```

- A: `{ email: "my@email.com", address: null }`
- B: `{ email: "my@email.com" }`
- C: `{ email: "my@email.com", address: {} }`
- D: `{ email: "my@email.com", address: undefined }`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: C

The default value of `address` is an empty object `{}`. When we set the variable `member` equal to the object returned by the `createMember` function, we didn't pass a value for the address, which means that the value of the address is the default empty object `{}`. An empty object is a truthy value, which means that the condition of the `address ? address : null` conditional returns `true`. The value of the address is the empty object `{}`.

</p>
</details>

---

###### 155. এটার আউটপুট কোনটা?

```javascript
let randomValue = { name: "Lydia" };
randomValue = 23;

if (!typeof randomValue === "string") {
  console.log("It's not a string!");
} else {
  console.log("Yay it's a string!");
}
```

- A: `It's not a string!`
- B: `Yay it's a string!`
- C: `TypeError`
- D: `undefined`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: B

The condition within the `if` statement checks whether the value of `!typeof randomValue` is equal to `"string"`. The `!` operator converts the value to a boolean value. If the value is truthy, the returned value will be `false`, if the value is falsy, the returned value will be `true`. In this case, the returned value of `typeof randomValue` is the truthy value `"number"`, meaning that the value of `!typeof randomValue` is the boolean value `false`.

`!typeof randomValue === "string"` always returns false, since we're actually checking `false === "string"`. Since the condition returned `false`, the code block of the `else` statement gets run, and `Yay it's a string!` gets logged.

</p>
</details>
