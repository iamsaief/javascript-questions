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
  var name = 'Lydia';
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
!'Lydia';
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
  size: 'small',
};

const mouse = {
  name: 'Mickey',
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
let c = { greeting: 'Hey!' };
let d;

d = c;
c.greeting = 'Hello';
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

  constructor({ newColor = 'green' } = {}) {
    this.newColor = newColor;
  }
}

const freddie = new Chameleon({ newColor: 'purple' });
console.log(freddie.colorChange('orange'));
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
  console.log('Woof!');
}

bark.animal = 'dog';
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

const member = new Person('Lydia', 'Hallie');
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

const lydia = new Person('Lydia', 'Hallie');
const sarah = Person('Sarah', 'Smith');

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

sum(1, '2');
```

- A: `NaN`
- B: `TypeError`
- C: `"12"`
- D: `3`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: C

জাভাস্ক্রিপ্ট একটি **ডায়নামিক টাইপ ভাষাঃ** আমরা ভেরিয়েবলের টাইপ নির্দিষ্ট করি না। আপনি জানতে পারেন না ভ্যালু স্বয়ংক্রিয়ভাবেই এক টাইপ থেকে অন্য টাইপে পরিবর্তন হয়ে যায়, যেটাকে বলা হয় **কোয়ার্শন (coercion)**। এটা হল এক টাইপ থেকে অন্য টাইপে পরিবর্তন হওয়া।

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

const person = 'Lydia';
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
    console.log('You are an adult!');
  } else if (data == { age: 18 }) {
    console.log('You are still an adult.');
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
  'use strict';
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
const sum = eval('10*10+5');
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
sessionStorage.setItem('cool_secret', 123);
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
const obj = { 1: 'a', 2: 'b', 3: 'c' };
const set = new Set([1, 2, 3, 4, 5]);

obj.hasOwnProperty('1');
obj.hasOwnProperty(1);
set.has('1');
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
const obj = { a: 'one', b: 'two', a: 'three' };
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
  return 'Just give Lydia pizza already!';
};

const name = 'Lydia';

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
const b = { key: 'b' };
const c = { key: 'c' };

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
const foo = () => console.log('First');
const bar = () => setTimeout(() => console.log('Second'));
const baz = () => console.log('Third');

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
const person = { name: 'Lydia' };

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
('');
(' ');
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
!!'';
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
setInterval(() => console.log('Hi'), 1000);
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
[...'Lydia'];
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
  setTimeout(res, 500, 'one');
});

const secondPromise = new Promise((res, rej) => {
  setTimeout(res, 100, 'two');
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
let person = { name: 'Lydia' };
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
  name: 'Lydia',
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
console.log(3 + 4 + '5');
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
const num = parseInt('7*6', 10);
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
  if (typeof num === 'number') return;
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
  member.name = 'Lydia';
  year = '1998';
}

const person = { name: 'Sarah' };
const birthYear = '1997';

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

Arguments are passed by _value_, unless their value is an object, then they're passed by _reference_. `birthYear` is passed by value, since it's a string, not an object. When we pass arguments by value, a _copy_ of that value is created (see question 46).

The variable `birthYear` has a reference to the value `"1997"`. The argument `year` also has a reference to the value `"1997"`, but it's not the same value as `birthYear` has a reference to. When we update the value of `year` by setting `year` equal to `"1998"`, we are only updating the value of `year`. `birthYear` is still equal to `"1997"`.

The value of `person` is an object. The argument `member` has a (copied) reference to the _same_ object. When we modify a property of the object `member` has a reference to, the value of `person` will also be modified, since they both have a reference to the same object. `person`'s `name` property is now equal to the value `"Lydia"`

</p>
</details>

---

###### 52. এটার আউটপুট কোনটা?

```javascript
function greeting() {
  throw 'Hello world!';
}

function sayHi() {
  try {
    const data = greeting();
    console.log('It worked!', data);
  } catch (e) {
    console.log('Oh no an error:', e);
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

With the `throw` statement, we can create custom errors. With this statement, you can throw exceptions. An exception can be a <b>string</b>, a <b>number</b>, a <b>boolean</b> or an <b>object</b>. In this case, our exception is the string `'Hello world!'`.

With the `catch` statement, we can specify what to do if an exception is thrown in the `try` block. An exception is thrown: the string `'Hello world!'`. `e` is now equal to that string, which we log. This results in `'Oh an error: Hello world!'`.

</p>
</details>

---

###### 53. এটার আউটপুট কোনটা?

```javascript
function Car() {
  this.make = 'Lamborghini';
  return { make: 'Maserati' };
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

When a constructor function is called with the `new` keyword, it creates an object and sets the `this` keyword to refer to that object. By default, if the constructor function doesn't explicitly return anything, it will return the newly created object.

In this case, the constructor function `Car` explicitly returns a new object with `make` set to `"Maserati"`, which overrides the default behavior. Therefore, when `new Car()` is called, the _returned_ object is assigned to `myCar`, resulting in the output being `"Maserati"` when `myCar.make` is accessed.

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

`let x = (y = 10);` is actually shorthand for:

```javascript
y = 10;
let x = y;
```

When we set `y` equal to `10`, we actually add a property `y` to the global object (`window` in the browser, `global` in Node). In a browser, `window.y` is now equal to `10`.

Then, we declare a variable `x` with the value of `y`, which is `10`. Variables declared with the `let` keyword are _block scoped_, they are only defined within the block they're declared in; the immediately invoked function expression (IIFE) in this case. When we use the `typeof` operator, the operand `x` is not defined: we are trying to access `x` outside of the block it's declared in. This means that `x` is not defined. Values who haven't been assigned a value or declared are of type `"undefined"`. `console.log(typeof x)` returns `"undefined"`.

However, we created a global variable `y` when setting `y` equal to `10`. This value is accessible anywhere in our code. `y` is defined, and holds a value of type `"number"`. `console.log(typeof y)` returns `"number"`.

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

const pet = new Dog('Mara');

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

We can delete properties from objects using the `delete` keyword, also on the prototype. By deleting a property on the prototype, it is not available anymore in the prototype chain. In this case, the `bark` function is not available anymore on the prototype after `delete Dog.prototype.bark`, yet we still try to access it.

When we try to invoke something that is not a function, a `TypeError` is thrown. In this case `TypeError: pet.bark is not a function`, since `pet.bark` is `undefined`.

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

The `Set` object is a collection of _unique_ values: a value can only occur once in a set.

We passed the iterable `[1, 1, 2, 3, 4]` with a duplicate value `1`. Since we cannot have two of the same values in a set, one of them is removed. This results in `{1, 2, 3, 4}`.

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
import myCounter from './counter';

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

An imported module is _read-only_: you cannot modify the imported module. Only the module that exports them can change its value.

When we try to increment the value of `myCounter`, it throws an error: `myCounter` is read-only and cannot be modified.

</p>
</details>

---

###### 58. এটার আউটপুট কোনটা?

```javascript
const name = 'Lydia';
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

The `delete` operator returns a boolean value: `true` on a successful deletion, else it'll return `false`. However, variables declared with the `var`, `const`, or `let` keywords cannot be deleted using the `delete` operator.

The `name` variable was declared with a `const` keyword, so its deletion is not successful: `false` is returned. When we set `age` equal to `21`, we actually added a property called `age` to the global object. You can successfully delete properties from objects this way, also the global object, so `delete age` returns `true`.

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

We can unpack values from arrays or properties from objects through destructuring. For example:

```javascript
[a, b] = [1, 2];
```

<img src="https://i.imgur.com/ADFpVop.png" width="200">

The value of `a` is now `1`, and the value of `b` is now `2`. What we actually did in the question, is:

```javascript
[y] = [1, 2, 3, 4, 5];
```

<img src="https://i.imgur.com/NzGkMNk.png" width="200">

This means that the value of `y` is equal to the first value in the array, which is the number `1`. When we log `y`, `1` is returned.

</p>
</details>

---

###### 60. এটার আউটপুট কোনটা?

```javascript
const user = { name: 'Lydia', age: 21 };
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

It's possible to combine objects using the spread operator `...`. It lets you create copies of the key/value pairs of one object, and add them to another object. In this case, we create copies of the `user` object, and add them to the `admin` object. The `admin` object now contains the copied key/value pairs, which results in `{ admin: true, name: "Lydia", age: 21 }`.

</p>
</details>

---

###### 61. এটার আউটপুট কোনটা?

```javascript
const person = { name: 'Lydia' };

Object.defineProperty(person, 'age', { value: 21 });

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

With the `defineProperty` method, we can add new properties to an object, or modify existing ones. When we add a property to an object using the `defineProperty` method, they are by default _not enumerable_. The `Object.keys` method returns all _enumerable_ property names from an object, in this case only `"name"`.

Properties added using the `defineProperty` method are immutable by default. You can override this behavior using the `writable`, `configurable` and `enumerable` properties. This way, the `defineProperty` method gives you a lot more control over the properties you're adding to an object.

</p>
</details>

---

###### 62. এটার আউটপুট কোনটা?

```javascript
const settings = {
  username: 'lydiahallie',
  level: 19,
  health: 90,
};

const data = JSON.stringify(settings, ['level', 'health']);
console.log(data);
```

- A: `"{"level":19, "health":90}"`
- B: `"{"username": "lydiahallie"}"`
- C: `"["level", "health"]"`
- D: `"{"username": "lydiahallie", "level":19, "health":90}"`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: A

The second argument of `JSON.stringify` is the _replacer_. The replacer can either be a function or an array, and lets you control what and how the values should be stringified.

If the replacer is an _array_, only the property names included in the array will be added to the JSON string. In this case, only the properties with the names `"level"` and `"health"` are included, `"username"` is excluded. `data` is now equal to `"{"level":19, "health":90}"`.

If the replacer is a _function_, this function gets called on every property in the object you're stringifying. The value returned from this function will be the value of the property when it's added to the JSON string. If the value is `undefined`, this property is excluded from the JSON string.

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

The unary operator `++` _first returns_ the value of the operand, _then increments_ the value of the operand. The value of `num1` is `10`, since the `increaseNumber` function first returns the value of `num`, which is `10`, and only increments the value of `num` afterward.

`num2` is `10`, since we passed `num1` to the `increasePassedNumber`. `number` is equal to `10`(the value of `num1`). Again, the unary operator `++` _first returns_ the value of the operand, _then increments_ the value of the operand. The value of `number` is `10`, so `num2` is equal to `10`.

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

In ES6, we can initialize parameters with a default value. The value of the parameter will be the default value, if no other value has been passed to the function, or if the value of the parameter is `"undefined"`. In this case, we spread the properties of the `value` object into a new object, so `x` has the default value of `{ number: 10 }`.

The default argument is evaluated at _call time_! Every time we call the function, a _new_ object is created. We invoke the `multiply` function the first two times without passing a value: `x` has the default value of `{ number: 10 }`. We then log the multiplied value of that number, which is `20`.

The third time we invoke multiply, we do pass an argument: the object called `value`. The `*=` operator is actually shorthand for `x.number = x.number * 2`: we modify the value of `x.number`, and log the multiplied value `20`.

The fourth time, we pass the `value` object again. `x.number` was previously modified to `20`, so `x.number *= 2` logs `40`.

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

The first argument that the `reduce` method receives is the _accumulator_, `x` in this case. The second argument is the _current value_, `y`. With the reduce method, we execute a callback function on every element in the array, which could ultimately result in one single value.

In this example, we are not returning any values, we are simply logging the values of the accumulator and the current value.

The value of the accumulator is equal to the previously returned value of the callback function. If you don't pass the optional `initialValue` argument to the `reduce` method, the accumulator is equal to the first element on the first call.

On the first call, the accumulator (`x`) is `1`, and the current value (`y`) is `2`. We don't return from the callback function, we log the accumulator, and the current values: `1` and `2` get logged.

If you don't return a value from a function, it returns `undefined`. On the next call, the accumulator is `undefined`, and the current value is `3`. `undefined` and `3` get logged.

On the fourth call, we again don't return from the callback function. The accumulator is again `undefined`, and the current value is `4`. `undefined` and `4` get logged.

</p>
</details>
  
---

###### 66. With which constructor can we successfully extend the `Dog` class?

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

In a derived class, you cannot access the `this` keyword before calling `super`. If you try to do that, it will throw a ReferenceError: 1 and 4 would throw a reference error.

With the `super` keyword, we call that parent class's constructor with the given arguments. The parent's constructor receives the `name` argument, so we need to pass `name` to `super`.

The `Labrador` class receives two arguments, `name` since it extends `Dog`, and `size` as an extra property on the `Labrador` class. They both need to be passed to the constructor function on `Labrador`, which is done correctly using constructor 2.

</p>
</details>

---

###### 67. এটার আউটপুট কোনটা?

```javascript
// index.js
console.log('running index.js');
import { sum } from './sum.js';
console.log(sum(1, 2));

// sum.js
console.log('running sum.js');
export const sum = (a, b) => a + b;
```

- A: `running index.js`, `running sum.js`, `3`
- B: `running sum.js`, `running index.js`, `3`
- C: `running sum.js`, `3`, `running index.js`
- D: `running index.js`, `undefined`, `running sum.js`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: B

With the `import` keyword, all imported modules are _pre-parsed_. This means that the imported modules get run _first_, and the code in the file that imports the module gets executed _after_.

This is a difference between `require()` in CommonJS and `import`! With `require()`, you can load dependencies on demand while the code is being run. If we had used `require` instead of `import`, `running index.js`, `running sum.js`, `3` would have been logged to the console.

</p>
</details>

---

###### 68. এটার আউটপুট কোনটা?

```javascript
console.log(Number(2) === Number(2));
console.log(Boolean(false) === Boolean(false));
console.log(Symbol('foo') === Symbol('foo'));
```

- A: `true`, `true`, `false`
- B: `false`, `true`, `false`
- C: `true`, `false`, `true`
- D: `true`, `true`, `true`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: A

Every Symbol is entirely unique. The purpose of the argument passed to the Symbol is to give the Symbol a description. The value of the Symbol is not dependent on the passed argument. As we test equality, we are creating two entirely new symbols: the first `Symbol('foo')`, and the second `Symbol('foo')`. These two values are unique and not equal to each other, `Symbol('foo') === Symbol('foo')` returns `false`.

</p>
</details>

---

###### 69. এটার আউটপুট কোনটা?

```javascript
const name = 'Lydia Hallie';
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

With the `padStart` method, we can add padding to the beginning of a string. The value passed to this method is the _total_ length of the string together with the padding. The string `"Lydia Hallie"` has a length of `12`. `name.padStart(13)` inserts 1 space at the start of the string, because 12 + 1 is 13.

If the argument passed to the `padStart` method is smaller than the length of the array, no padding will be added.

</p>
</details>

---

###### 70. এটার আউটপুট কোনটা?

```javascript
console.log('🥑' + '💻');
```

- A: `"🥑💻"`
- B: `257548`
- C: A string containing their code points
- D: Error

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: A

With the `+` operator, you can concatenate strings. In this case, we are concatenating the string `"🥑"` with the string `"💻"`, resulting in `"🥑💻"`.

</p>
</details>

---

###### 71. How can we log the values that are commented out after the console.log statement?

```javascript
function* startGame() {
  const উত্তর = yield 'Do you love JavaScript?';
  if (উত্তর !== 'Yes') {
    return "Oh wow... Guess we're done here";
  }
  return 'JavaScript loves you back ❤️';
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

A generator function "pauses" its execution when it sees the `yield` keyword. First, we have to let the function yield the string "Do you love JavaScript?", which can be done by calling `game.next().value`.

Every line is executed, until it finds the first `yield` keyword. There is a `yield` keyword on the first line within the function: the execution stops with the first yield! _This means that the variable `উত্তর` is not defined yet!_

When we call `game.next("Yes").value`, the previous `yield` is replaced with the value of the parameters passed to the `next()` function, `"Yes"` in this case. The value of the variable `উত্তর` is now equal to `"Yes"`. The condition of the if-statement returns `false`, and `JavaScript loves you back ❤️` gets logged.

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

`String.raw` returns a string where the escapes (`\n`, `\v`, `\t` etc.) are ignored! Backslashes can be an issue since you could end up with something like:

`` const path = `C:\Documents\Projects\table.html` ``

Which would result in:

`"C:DocumentsProjects able.html"`

With `String.raw`, it would simply ignore the escape and print:

`C:\Documents\Projects\table.html`

In this case, the string is `Hello\nworld`, which gets logged.

</p>
</details>

---

###### 73. এটার আউটপুট কোনটা?

```javascript
async function getData() {
  return await Promise.resolve('I made it!');
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

An async function always returns a promise. The `await` still has to wait for the promise to resolve: a pending promise gets returned when we call `getData()` in order to set `data` equal to it.

If we wanted to get access to the resolved value `"I made it"`, we could have used the `.then()` method on `data`:

`data.then(res => console.log(res))`

This would've logged `"I made it!"`

</p>
</details>

---

###### 74. এটার আউটপুট কোনটা?

```javascript
function addToList(item, list) {
  return list.push(item);
}

const result = addToList('apple', ['banana']);
console.log(result);
```

- A: `['apple', 'banana']`
- B: `2`
- C: `true`
- D: `undefined`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: B

The `.push()` method returns the _length_ of the new array! Previously, the array contained one element (the string `"banana"`) and had a length of `1`. After adding the string `"apple"` to the array, the array contains two elements, and has a length of `2`. This gets returned from the `addToList` function.

The `push` method modifies the original array. If you wanted to return the _array_ from the function rather than the _length of the array_, you should have returned `list` after pushing `item` to it.

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

`Object.freeze` makes it impossible to add, remove, or modify properties of an object (unless the property's value is another object).

When we create the variable `shape` and set it equal to the frozen object `box`, `shape` also refers to a frozen object. You can check whether an object is frozen by using `Object.isFrozen`. In this case, `Object.isFrozen(shape)` would return true, since the variable `shape` has a reference to a frozen object.

Since `shape` is frozen, and since the value of `x` is not an object, we cannot modify the property `x`. `x` is still equal to `10`, and `{ x: 10, y: 20 }` gets logged.

</p>
</details>

---

###### 76. এটার আউটপুট কোনটা?

```javascript
const { firstName: myName } = { firstName: 'Lydia' };

console.log(firstName);
```

- A: `"Lydia"`
- B: `"myName"`
- C: `undefined`
- D: `ReferenceError`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: D

By using [destructuring assignment](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Destructuring_assignment) syntax we can unpack values from arrays, or properties from objects, into distinct variables:

```javascript
const { firstName } = { firstName: 'Lydia' };
// ES5 version:
// var firstName = { firstName: 'Lydia' }.firstName;

console.log(firstName); // "Lydia"
```

Also, a property can be unpacked from an object and assigned to a variable with a different name than the object property:

```javascript
const { firstName: myName } = { firstName: 'Lydia' };
// ES5 version:
// var myName = { firstName: 'Lydia' }.firstName;

console.log(myName); // "Lydia"
console.log(firstName); // Uncaught ReferenceError: firstName is not defined
```

Therefore, `firstName` does not exist as a variable, thus attempting to access its value will raise a `ReferenceError`.

**Note:** Be aware of the `global scope` properties:

```javascript
const { name: myName } = { name: 'Lydia' };

console.log(myName); // "lydia"
console.log(name); // "" ----- Browser e.g. Chrome
console.log(name); // ReferenceError: name is not defined  ----- NodeJS
```

Whenever Javascript is unable to find a variable within the _current scope_, it climbs up the [Scope chain](https://github.com/getify/You-Dont-Know-JS/blob/2nd-ed/scope-closures/ch3.md) and searches for it and if it reaches the top-level scope, aka **Global scope**, and still doesn't find it, it will throw a `ReferenceError`.

- In **Browsers** such as _Chrome_, `name` is a _deprecated global scope property_. In this example, the code is running inside _global scope_ and there is no user-defined local variable for `name`, therefore it searches the predefined _variables/properties_ in the global scope which is in the case of browsers, it searches through `window` object and it will extract the [window.name](https://developer.mozilla.org/en-US/docs/Web/API/Window/name) value which is equal to an **empty string**.

- In **NodeJS**, there is no such property on the `global` object, thus attempting to access a non-existent variable will raise a [ReferenceError](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Errors/Not_defined).

</p>
</details>

---

###### 77. Is this a pure function?

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

A pure function is a function that _always_ returns the same result, if the same arguments are passed.

The `sum` function always returns the same result. If we pass `1` and `2`, it will _always_ return `3` without side effects. If we pass `5` and `10`, it will _always_ return `15`, and so on. This is the definition of a pure function.

</p>
</details>

---

###### 78. What is the output?

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

The `add` function is a _memoized_ function. With memoization, we can cache the results of a function in order to speed up its execution. In this case, we create a `cache` object that stores the previously returned values.

If we call the `addFunction` function again with the same argument, it first checks whether it has already gotten that value in its cache. If that's the case, the cache value will be returned, which saves execution time. Otherwise, if it's not cached, it will calculate the value and store it afterward.

We call the `addFunction` function three times with the same value: on the first invocation, the value of the function when `num` is equal to `10` isn't cached yet. The condition of the if-statement `num in cache` returns `false`, and the else block gets executed: `Calculated! 20` gets logged, and the value of the result gets added to the cache object. `cache` now looks like `{ 10: 20 }`.

The second time, the `cache` object contains the value that gets returned for `10`. The condition of the if-statement `num in cache` returns `true`, and `'From cache! 20'` gets logged.

The third time, we pass `5 * 2` to the function which gets evaluated to `10`. The `cache` object contains the value that gets returned for `10`. The condition of the if-statement `num in cache` returns `true`, and `'From cache! 20'` gets logged.

</p>
</details>

---

###### 79. What is the output?

```javascript
const myLifeSummedUp = ['☕', '💻', '🍷', '🍫'];

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

With a _for-in_ loop, we can iterate over **enumerable** properties. In an array, the enumerable properties are the "keys" of array elements, which are actually their indexes. You could see an array as:

`{0: "☕", 1: "💻", 2: "🍷", 3: "🍫"}`

Where the keys are the enumerable properties. `0` `1` `2` `3` get logged.

With a _for-of_ loop, we can iterate over **iterables**. An array is an iterable. When we iterate over the array, the variable "item" is equal to the element it's currently iterating over, `"☕"` `"💻"` `"🍷"` `"🍫"` get logged.

</p>
</details>

---

###### 80. What is the output?

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

Array elements can hold any value. Numbers, strings, objects, other arrays, null, boolean values, undefined, and other expressions such as dates, functions, and calculations.

The element will be equal to the returned value. `1 + 2` returns `3`, `1 * 2` returns `2`, and `1 / 2` returns `0.5`.

</p>
</details>

---

###### 81. What is the output?

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

By default, arguments have the value of `undefined`, unless a value has been passed to the function. In this case, we didn't pass a value for the `name` argument. `name` is equal to `undefined` which gets logged.

In ES6, we can overwrite this default `undefined` value with default parameters. For example:

`function sayHi(name = "Lydia") { ... }`

In this case, if we didn't pass a value or if we passed `undefined`, `name` would always be equal to the string `Lydia`

</p>
</details>

---

###### 82. What is the output?

```javascript
var status = '😎';

setTimeout(() => {
  const status = '😍';

  const data = {
    status: '🥑',
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

The value of the `this` keyword is dependent on where you use it. In a **method**, like the `getStatus` method, the `this` keyword refers to _the object that the method belongs to_. The method belongs to the `data` object, so `this` refers to the `data` object. When we log `this.status`, the `status` property on the `data` object gets logged, which is `"🥑"`.

With the `call` method, we can change the object to which the `this` keyword refers. In **functions**, the `this` keyword refers to the _the object that the function belongs to_. We declared the `setTimeout` function on the _global object_, so within the `setTimeout` function, the `this` keyword refers to the _global object_. On the global object, there is a variable called _status_ with the value of `"😎"`. When logging `this.status`, `"😎"` gets logged.

</p>
</details>

---

###### 83. What is the output?

```javascript
const person = {
  name: 'Lydia',
  age: 21,
};

let city = person.city;
city = 'Amsterdam';

console.log(person);
```

- A: `{ name: "Lydia", age: 21 }`
- B: `{ name: "Lydia", age: 21, city: "Amsterdam" }`
- C: `{ name: "Lydia", age: 21, city: undefined }`
- D: `"Amsterdam"`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: A

We set the variable `city` equal to the value of the property called `city` on the `person` object. There is no property on this object called `city`, so the variable `city` has the value of `undefined`.

Note that we are _not_ referencing the `person` object itself! We simply set the variable `city` equal to the current value of the `city` property on the `person` object.

Then, we set `city` equal to the string `"Amsterdam"`. This doesn't change the person object: there is no reference to that object.

When logging the `person` object, the unmodified object gets returned.

</p>
</details>

---

###### 84. What is the output?

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

Variables with the `const` and `let` keywords are _block-scoped_. A block is anything between curly brackets (`{ }`). In this case, the curly brackets of the if/else statements. You cannot reference a variable outside of the block it's declared in, a ReferenceError gets thrown.

</p>
</details>

---

###### 85. What kind of information would get logged?

```javascript
fetch('https://www.website.com/api/user/1')
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

The value of `res` in the second `.then` is equal to the returned value of the previous `.then`. You can keep chaining `.then`s like this, where the value is passed to the next handler.

</p>
</details>

---

###### 86. Which option is a way to set `hasName` equal to `true`, provided you cannot pass `true` as an argument?

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

With `!!name`, we determine whether the value of `name` is truthy or falsy. If the name is truthy, which we want to test for, `!name` returns `false`. `!false` (which is what `!!name` practically is) returns `true`.

By setting `hasName` equal to `name`, you set `hasName` equal to whatever value you passed to the `getName` function, not the boolean value `true`.

`new Boolean(true)` returns an object wrapper, not the boolean value itself.

`name.length` returns the length of the passed argument, not whether it's `true`.

</p>
</details>

---

###### 87. এটার আউটপুট কোনটা?

```javascript
console.log('I want pizza'[0]);
```

- A: `"""`
- B: `"I"`
- C: `SyntaxError`
- D: `undefined`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: B

In order to get a character at a specific index of a string, you can use bracket notation. The first character in the string has index 0, and so on. In this case, we want to get the element with index 0, the character `"I'`, which gets logged.

Note that this method is not supported in IE7 and below. In that case, use `.charAt()`.

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

You can set a default parameter's value equal to another parameter of the function, as long as they've been defined _before_ the default parameter. We pass the value `10` to the `sum` function. If the `sum` function only receives 1 argument, it means that the value for `num2` is not passed, and the value of `num1` is equal to the passed value `10` in this case. The default value of `num2` is the value of `num1`, which is `10`. `num1 + num2` returns `20`.

If you're trying to set a default parameter's value equal to a parameter that is defined _after_ (to the right), the parameter's value hasn't been initialized yet, which will throw an error.

</p>
</details>

---

###### 89. এটার আউটপুট কোনটা?

```javascript
// module.js
export default () => 'Hello world';
export const name = 'Lydia';

// index.js
import * as data from './module';

console.log(data);
```

- A: `{ default: function default(), name: "Lydia" }`
- B: `{ default: function default() }`
- C: `{ default: "Hello world", name: "Lydia" }`
- D: Global object of `module.js`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: A

With the `import * as name` syntax, we import _all exports_ from the `module.js` file into the `index.js` file as a new object called `data` is created. In the `module.js` file, there are two exports: the default export, and a named export. The default export is a function that returns the string `"Hello World"`, and the named export is a variable called `name` which has the value of the string `"Lydia"`.

The `data` object has a `default` property for the default export, other properties have the names of the named exports and their corresponding values.

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

const member = new Person('John');
console.log(typeof member);
```

- A: `"class"`
- B: `"function"`
- C: `"object"`
- D: `"string"`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: C

Classes are syntactical sugar for function constructors. The equivalent of the `Person` class as a function constructor would be:

```javascript
function Person(name) {
  this.name = name;
}
```

Calling a function constructor with `new` results in the creation of an instance of `Person`, `typeof` keyword returns `"object"` for an instance. `typeof member` returns `"object"`.

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

The `.push` method returns the _new length_ of the array, not the array itself! By setting `newList` equal to `[1, 2, 3].push(4)`, we set `newList` equal to the new length of the array: `4`.

Then, we try to use the `.push` method on `newList`. Since `newList` is the numerical value `4`, we cannot use the `.push` method: a TypeError is thrown.

</p>
</details>

---

###### 92. এটার আউটপুট কোনটা?

```javascript
function giveLydiaPizza() {
  return 'Here is pizza!';
}

const giveLydiaChocolate = () =>
  "Here's chocolate... now go hit the gym already.";

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

Regular functions, such as the `giveLydiaPizza` function, have a `prototype` property, which is an object (prototype object) with a `constructor` property. Arrow functions however, such as the `giveLydiaChocolate` function, do not have this `prototype` property. `undefined` gets returned when trying to access the `prototype` property using `giveLydiaChocolate.prototype`.

</p>
</details>

---

###### 93. এটার আউটপুট কোনটা?

```javascript
const person = {
  name: 'Lydia',
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

`Object.entries(person)` returns an array of nested arrays, containing the keys and objects:

`[ [ 'name', 'Lydia' ], [ 'age', 21 ] ]`

Using the `for-of` loop, we can iterate over each element in the array, the subarrays in this case. We can destructure the subarrays instantly in the for-of loop, using `const [x, y]`. `x` is equal to the first element in the subarray, `y` is equal to the second element in the subarray.

The first subarray is `[ "name", "Lydia" ]`, with `x` equal to `"name"`, and `y` equal to `"Lydia"`, which get logged.
The second subarray is `[ "age", 21 ]`, with `x` equal to `"age"`, and `y` equal to `21`, which get logged.

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

`...args` is a rest parameter. The rest parameter's value is an array containing all remaining arguments, **and can only be the last parameter**! In this example, the rest parameter was the second parameter. This is not possible, and will throw a syntax error.

```javascript
function getItems(fruitList, favoriteFruit, ...args) {
  return [...fruitList, ...args, favoriteFruit];
}

getItems(['banana', 'apple'], 'pear', 'orange');
```

The above example works. This returns the array `[ 'banana', 'apple', 'orange', 'pear' ]`

</p>
</details>

---

###### 95. এটার আউটপুট কোনটা?

```javascript
function nums(a, b) {
  if (a > b) console.log('a is bigger');
  else console.log('b is bigger');
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

In JavaScript, we don't _have_ to write the semicolon (`;`) explicitly, however the JavaScript engine still adds them after statements. This is called **Automatic Semicolon Insertion**. A statement can for example be variables, or keywords like `throw`, `return`, `break`, etc.

Here, we wrote a `return` statement, and another value `a + b` on a _new line_. However, since it's a new line, the engine doesn't know that it's actually the value that we wanted to return. Instead, it automatically added a semicolon after `return`. You could see this as:

```javascript
return;
a + b;
```

This means that `a + b` is never reached, since a function stops running after the `return` keyword. If no value gets returned, like here, the function returns `undefined`. Note that there is no automatic insertion after `if/else` statements!

</p>
</details>

---

###### 96. এটার আউটপুট কোনটা?

```javascript
class Person {
  constructor() {
    this.name = 'Lydia';
  }
}

Person = class AnotherPerson {
  constructor() {
    this.name = 'Sarah';
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

We can set classes equal to other classes/function constructors. In this case, we set `Person` equal to `AnotherPerson`. The name on this constructor is `Sarah`, so the name property on the new `Person` instance `member` is `"Sarah"`.

</p>
</details>

---

###### 97. এটার আউটপুট কোনটা?

```javascript
const info = {
  [Symbol('a')]: 'b',
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

A Symbol is not _enumerable_. The Object.keys method returns all _enumerable_ key properties on an object. The Symbol won't be visible, and an empty array is returned. When logging the entire object, all properties will be visible, even non-enumerable ones.

This is one of the many qualities of a symbol: besides representing an entirely unique value (which prevents accidental name collision on objects, for example when working with 2 libraries that want to add properties to the same object), you can also "hide" properties on objects this way (although not entirely. You can still access symbols using the `Object.getOwnPropertySymbols()` method).

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

The `getList` function receives an array as its argument. Between the parentheses of the `getList` function, we destructure this array right away. You could see this as:

`[x, ...y] = [1, 2, 3, 4]`

With the rest parameter `...y`, we put all "remaining" arguments in an array. The remaining arguments are `2`, `3` and `4` in this case. The value of `y` is an array, containing all the rest parameters. The value of `x` is equal to `1` in this case, so when we log `[x, y]`, `[1, [2, 3, 4]]` gets logged.

The `getUser` function receives an object. With arrow functions, we don't _have_ to write curly brackets if we just return one value. However, if you want to instantly return an _object_ from an arrow function, you have to write it between parentheses, otherwise everything between the two braces will be interpreted as a block statement. In this case the code between the braces is not a valid JavaScript code, so a `SyntaxError` gets thrown.

The following function would have returned an object:

`const getUser = user => ({ name: user.name, age: user.age })`

</p>
</details>

---

###### 99. এটার আউটপুট কোনটা?

```javascript
const name = 'Lydia';

console.log(name());
```

- A: `SyntaxError`
- B: `ReferenceError`
- C: `TypeError`
- D: `undefined`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: C

The variable `name` holds the value of a string, which is not a function, and thus cannot be invoked.

TypeErrors get thrown when a value is not of the expected type. JavaScript expected `name` to be a function since we're trying to invoke it. It was a string however, so a TypeError gets thrown: name is not a function!

SyntaxErrors get thrown when you've written something that isn't valid JavaScript, for example when you've written the word `return` as `retrun`.
ReferenceErrors get thrown when JavaScript isn't able to find a reference to a value that you're trying to access.

</p>
</details>

---

###### 100. What's the value of output?

```javascript
// 🎉✨ This is my 100th question! ✨🎉

const output = `${[] && 'Im'}possible!
You should${'' && `n't`} see a therapist after so much JavaScript lol`;
```

- A: `possible! You should see a therapist after so much JavaScript lol`
- B: `Impossible! You should see a therapist after so much JavaScript lol`
- C: `possible! You shouldn't see a therapist after so much JavaScript lol`
- D: `Impossible! You shouldn't see a therapist after so much JavaScript lol`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: B

`[]` is a truthy value. With the `&&` operator, the right-hand value will be returned if the left-hand value is a truthy value. In this case, the left-hand value `[]` is a truthy value, so `"Im'` gets returned.

`""` is a falsy value. If the left-hand value is falsy, nothing gets returned. `n't` doesn't get returned.

</p>
</details>

---

###### 101. What's the value of output?

```javascript
const one = false || {} || null;
const two = null || false || '';
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

With the `||` operator, we can return the first truthy operand. If all values are falsy, the last operand gets returned.

`(false || {} || null)`: the empty object `{}` is a truthy value. This is the first (and only) truthy value, which gets returned. `one` is equal to `{}`.

`(null || false || "")`: all operands are falsy values. This means that the last operand, `""` gets returned. `two` is equal to `""`.

`([] || 0 || "")`: the empty array`[]` is a truthy value. This is the first truthy value, which gets returned. `three` is equal to `[]`.

</p>
</details>

---

###### 102. What's the value of output?

```javascript
const myPromise = () => Promise.resolve('I have resolved!');

function firstFunction() {
  myPromise().then((res) => console.log(res));
  console.log('second');
}

async function secondFunction() {
  console.log(await myPromise());
  console.log('second');
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

With a promise, we basically say _I want to execute this function, but I'll put it aside for now while it's running since this might take a while. Only when a certain value is resolved (or rejected), and when the call stack is empty, I want to use this value._

We can get this value with both `.then` and the `await` keywords in an `async` function. Although we can get a promise's value with both `.then` and `await`, they work a bit differently.

In the `firstFunction`, we (sort of) put the myPromise function aside while it was running, but continued running the other code, which is `console.log('second')` in this case. Then, the function resolved with the string `I have resolved`, which then got logged after it saw that the callstack was empty.

With the await keyword in `secondFunction`, we literally pause the execution of an async function until the value has been resolved before moving to the next line.

This means that it waited for the `myPromise` to resolve with the value `I have resolved`, and only once that happened, we moved to the next line: `second` got logged.

</p>
</details>

---

###### 103. What's the value of output?

```javascript
const set = new Set();

set.add(1);
set.add('Lydia');
set.add({ name: 'Lydia' });

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

The `+` operator is not only used for adding numerical values, but we can also use it to concatenate strings. Whenever the JavaScript engine sees that one or more values are not a number, it coerces the number into a string.

The first one is `1`, which is a numerical value. `1 + 2` returns the number 3.

However, the second one is a string `"Lydia"`. `"Lydia"` is a string and `2` is a number: `2` gets coerced into a string. `"Lydia"` and `"2"` get concatenated, which results in the string `"Lydia2"`.

`{ name: "Lydia" }` is an object. Neither a number nor an object is a string, so it stringifies both. Whenever we stringify a regular object, it becomes `"[object Object]"`. `"[object Object]"` concatenated with `"2"` becomes `"[object Object]2"`.

</p>
</details>

---

###### 104. What's its value?

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

We can pass any type of value we want to `Promise.resolve`, either a promise or a non-promise. The method itself returns a promise with the resolved value (`<fulfilled>`). If you pass a regular function, it'll be a resolved promise with a regular value. If you pass a promise, it'll be a resolved promise with the resolved value of that passed promise.

In this case, we just passed the numerical value `5`. It returns a resolved promise with the value `5`.

</p>
</details>

---

###### 105. What's its value?

```javascript
function compareMembers(person1, person2 = person) {
  if (person1 !== person2) {
    console.log('Not the same!');
  } else {
    console.log('They are the same!');
  }
}

const person = { name: 'Lydia' };

compareMembers(person);
```

- A: `Not the same!`
- B: `They are the same!`
- C: `ReferenceError`
- D: `SyntaxError`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: B

Objects are passed by reference. When we check objects for strict equality (`===`), we're comparing their references.

We set the default value for `person2` equal to the `person` object, and passed the `person` object as the value for `person1`.

This means that both values have a reference to the same spot in memory, thus they are equal.

The code block in the `else` statement gets run, and `They are the same!` gets logged.

</p>
</details>

---

###### 106. What's its value?

```javascript
const colorConfig = {
  red: true,
  blue: false,
  green: true,
  black: true,
  yellow: false,
};

const colors = ['pink', 'red', 'blue'];

console.log(colorConfig.colors[1]);
```

- A: `true`
- B: `false`
- C: `undefined`
- D: `TypeError`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: D

In JavaScript, we have two ways to access properties on an object: bracket notation, or dot notation. In this example, we use dot notation (`colorConfig.colors`) instead of bracket notation (`colorConfig["colors"]`).

With dot notation, JavaScript tries to find the property on the object with that exact name. In this example, JavaScript tries to find a property called `colors` on the `colorConfig` object. There is no property called `colors`, so this returns `undefined`. Then, we try to access the value of the first element by using `[1]`. We cannot do this on a value that's `undefined`, so it throws a `TypeError`: `Cannot read property '1' of undefined`.

JavaScript interprets (or unboxes) statements. When we use bracket notation, it sees the first opening bracket `[` and keeps going until it finds the closing bracket `]`. Only then, it will evaluate the statement. If we would've used `colorConfig[colors[1]]`, it would have returned the value of the `red` property on the `colorConfig` object.

</p>
</details>

---

###### 107. What's its value?

```javascript
console.log('❤️' === '❤️');
```

- A: `true`
- B: `false`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: A

Under the hood, emojis are unicodes. The unicodes for the heart emoji is `"U+2764 U+FE0F"`. These are always the same for the same emojis, so we're comparing two equal strings to each other, which returns true.

</p>
</details>

---

###### 108. Which of these methods modifies the original array?

```javascript
const emojis = ['✨', '🥑', '😍'];

emojis.map((x) => x + '✨');
emojis.filter((x) => x !== '🥑');
emojis.find((x) => x !== '🥑');
emojis.reduce((acc, cur) => acc + '✨');
emojis.slice(1, 2, '✨');
emojis.splice(1, 2, '✨');
```

- A: `All of them`
- B: `map` `reduce` `slice` `splice`
- C: `map` `slice` `splice`
- D: `splice`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: D

With `splice` method, we modify the original array by deleting, replacing or adding elements. In this case, we removed 2 items from index 1 (we removed `'🥑'` and `'😍'`) and added the ✨ emoji instead.

`map`, `filter` and `slice` return a new array, `find` returns an element, and `reduce` returns a reduced value.

</p>
</details>

---

###### 109. এটার আউটপুট কোনটা?

```javascript
const food = ['🍕', '🍫', '🥑', '🍔'];
const info = { favoriteFood: food[0] };

info.favoriteFood = '🍝';

console.log(food);
```

- A: `['🍕', '🍫', '🥑', '🍔']`
- B: `['🍝', '🍫', '🥑', '🍔']`
- C: `['🍝', '🍕', '🍫', '🥑', '🍔']`
- D: `ReferenceError`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: A

We set the value of the `favoriteFood` property on the `info` object equal to the string with the pizza emoji, `'🍕'`. A string is a primitive data type. In JavaScript, primitive data types don't interact by reference.

In JavaScript, primitive data types (everything that's not an object) interact by _value_. In this case, we set the value of the `favoriteFood` property on the `info` object equal to the value of the first element in the `food` array, the string with the pizza emoji in this case (`'🍕'`). A string is a primitive data type, and interact by value (see my [blogpost](https://www.theavocoder.com/complete-javascript/2018/12/21/by-value-vs-by-reference) if you're interested in learning more)

Then, we change the value of the `favoriteFood` property on the `info` object. The `food` array hasn't changed, since the value of `favoriteFood` was merely a _copy_ of the value of the first element in the array, and doesn't have a reference to the same spot in memory as the element on `food[0]`. When we log food, it's still the original array, `['🍕', '🍫', '🥑', '🍔']`.

</p>
</details>

---

###### 110. What does this method do?

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

With the `JSON.parse()` method, we can parse JSON string to a JavaScript value.

```javascript
// Stringifying a number into valid JSON, then parsing the JSON string to a JavaScript value:
const jsonNumber = JSON.stringify(4); // '4'
JSON.parse(jsonNumber); // 4

// Stringifying an array value into valid JSON, then parsing the JSON string to a JavaScript value:
const jsonArray = JSON.stringify([1, 2, 3]); // '[1, 2, 3]'
JSON.parse(jsonArray); // [1, 2, 3]

// Stringifying an object  into valid JSON, then parsing the JSON string to a JavaScript value:
const jsonArray = JSON.stringify({ name: 'Lydia' }); // '{"name":"Lydia"}'
JSON.parse(jsonArray); // { name: 'Lydia' }
```

</p>
</details>

---

###### 111. এটার আউটপুট কোনটা?

```javascript
let name = 'Lydia';

function getName() {
  console.log(name);
  let name = 'Sarah';
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

Each function has its own _execution context_ (or _scope_). The `getName` function first looks within its own context (scope) to see if it contains the variable `name` we're trying to access. In this case, the `getName` function contains its own `name` variable: we declare the variable `name` with the `let` keyword, and with the value of `'Sarah'`.

Variables with the `let` keyword (and `const`) are hoisted, but unlike `var`, don't get <i>initialized</i>. They are not accessible before the line we declare (initialize) them. This is called the "temporal dead zone". When we try to access the variables before they are declared, JavaScript throws a `ReferenceError`.

If we wouldn't have declared the `name` variable within the `getName` function, the javascript engine would've looked down the _scope chain_. The outer scope has a variable called `name` with the value of `Lydia`. In that case, it would've logged `Lydia`.

```javascript
let name = 'Lydia';

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
  yield ['a', 'b', 'c'];
}

function* generatorTwo() {
  yield* ['a', 'b', 'c'];
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

With the `yield` keyword, we `yield` values in a generator function. With the `yield*` keyword, we can yield values from another generator function, or iterable object (for example an array).

In `generatorOne`, we yield the entire array `['a', 'b', 'c']` using the `yield` keyword. The value of `value` property on the object returned by the `next` method on `one` (`one.next().value`) is equal to the entire array `['a', 'b', 'c']`.

```javascript
console.log(one.next().value); // ['a', 'b', 'c']
console.log(one.next().value); // undefined
```

In `generatorTwo`, we use the `yield*` keyword. This means that the first yielded value of `two`, is equal to the first yielded value in the iterator. The iterator is the array `['a', 'b', 'c']`. The first yielded value is `a`, so the first time we call `two.next().value`, `a` is returned.

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
console.log(`${((x) => x)('I love')} to program`);
```

- A: `I love to program`
- B: `undefined to program`
- C: `${(x => x)('I love') to program`
- D: `TypeError`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: A

Expressions within template literals are evaluated first. This means that the string will contain the returned value of the expression, the immediately invoked function `(x => x)('I love')` in this case. We pass the value `'I love'` as an argument to the `x => x` arrow function. `x` is equal to `'I love'`, which gets returned. This results in `I love to program`.

</p>
</details>

---

###### 114. What will happen?

```javascript
let config = {
  alert: setInterval(() => {
    console.log('Alert!');
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

Normally when we set objects equal to `null`, those objects get _garbage collected_ as there is no reference anymore to that object. However, since the callback function within `setInterval` is an arrow function (thus bound to the `config` object), the callback function still holds a reference to the `config` object.
As long as there is a reference, the object won't get garbage collected.
Since this is an interval, setting `config` to `null` or `delete`-ing `config.alert` won't garbage-collect the interval, so the interval will still be called.
It should be cleared with `clearInterval(config.alert)` to remove it from memory.
Since it was not cleared, the `setInterval` callback function will still get invoked every 1000ms (1s).

</p>
</details>

---

###### 115. Which method(s) will return the value `'Hello world!'`?

```javascript
const myMap = new Map();
const myFunc = () => 'greeting';

myMap.set(myFunc, 'Hello world!');

//1
myMap.get('greeting');
//2
myMap.get(myFunc);
//3
myMap.get(() => 'greeting');
```

- A: 1
- B: 2
- C: 2 and 3
- D: All of them

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: B

When adding a key/value pair using the `set` method, the key will be the value of the first argument passed to the `set` function, and the value will be the second argument passed to the `set` function. The key is the _function_ `() => 'greeting'` in this case, and the value `'Hello world'`. `myMap` is now `{ () => 'greeting' => 'Hello world!' }`.

1 is wrong, since the key is not `'greeting'` but `() => 'greeting'`.
3 is wrong, since we're creating a new function by passing it as a parameter to the `get` method. Object interacts by _reference_. Functions are objects, which is why two functions are never strictly equal, even if they are identical: they have a reference to a different spot in memory.

</p>
</details>

---

###### 116. এটার আউটপুট কোনটা?

```javascript
const person = {
  name: 'Lydia',
  age: 21,
};

const changeAge = (x = { ...person }) => (x.age += 1);
const changeAgeAndName = (x = { ...person }) => {
  x.age += 1;
  x.name = 'Sarah';
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

Both the `changeAge` and `changeAgeAndName` functions have a default parameter, namely a _newly_ created object `{ ...person }`. This object has copies of all the key/values in the `person` object.

First, we invoke the `changeAge` function and pass the `person` object as its argument. This function increases the value of the `age` property by 1. `person` is now `{ name: "Lydia", age: 22 }`.

Then, we invoke the `changeAgeAndName` function, however we don't pass a parameter. Instead, the value of `x` is equal to a _new_ object: `{ ...person }`. Since it's a new object, it doesn't affect the values of the properties on the `person` object. `person` is still equal to `{ name: "Lydia", age: 22 }`.

</p>
</details>

---

###### 117. Which of the following options will return `6`?

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

With the spread operator `...`, we can _spread_ iterables to individual elements. The `sumValues` function receives three arguments: `x`, `y` and `z`. `...[1, 2, 3]` will result in `1, 2, 3`, which we pass to the `sumValues` function.

</p>
</details>

---

###### 118. এটার আউটপুট কোনটা?

```javascript
let num = 1;
const list = ['🥳', '🤠', '🥰', '🤪'];

console.log(list[(num += 1)]);
```

- A: `🤠`
- B: `🥰`
- C: `SyntaxError`
- D: `ReferenceError`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: B

With the `+=` operator, we're incrementing the value of `num` by `1`. `num` had the initial value `1`, so `1 + 1` is `2`. The item on the second index in the `list` array is 🥰, `console.log(list[2])` prints 🥰.

</p>
</details>

---

###### 119. এটার আউটপুট কোনটা?

```javascript
const person = {
  firstName: 'Lydia',
  lastName: 'Hallie',
  pet: {
    name: 'Mara',
    breed: 'Dutch Tulip Hound',
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

With the optional chaining operator `?.`, we no longer have to explicitly check whether the deeper nested values are valid or not. If we're trying to access a property on an `undefined` or `null` value (_nullish_), the expression short-circuits and returns `undefined`.

`person.pet?.name`: `person` has a property named `pet`: `person.pet` is not nullish. It has a property called `name`, and returns `Mara`.
`person.pet?.family?.name`: `person` has a property named `pet`: `person.pet` is not nullish. `pet` does _not_ have a property called `family`, `person.pet.family` is nullish. The expression returns `undefined`.
`person.getFullName?.()`: `person` has a property named `getFullName`: `person.getFullName()` is not nullish and can get invoked, which returns `Lydia Hallie`.
`member.getLastName?.()`: variable `member` is non-existent therefore a `ReferenceError` gets thrown!

</p>
</details>

---

###### 120. এটার আউটপুট কোনটা?

```javascript
const groceries = ['banana', 'apple', 'peanuts'];

if (groceries.indexOf('banana')) {
  console.log('We have to buy bananas!');
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

We passed the condition `groceries.indexOf("banana")` to the if-statement. `groceries.indexOf("banana")` returns `0`, which is a falsy value. Since the condition in the if-statement is falsy, the code in the `else` block runs, and `We don't have to buy bananas!` gets logged.

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

The `language` method is a `setter`. Setters don't hold an actual value, their purpose is to _modify_ properties. When calling a `setter` method, `undefined` gets returned.

</p>
</details>

---

###### 122. এটার আউটপুট কোনটা?

```javascript
const name = 'Lydia Hallie';

console.log(!typeof name === 'object');
console.log(!typeof name === 'string');
```

- A: `false` `true`
- B: `true` `false`
- C: `false` `false`
- D: `true` `true`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: C

`typeof name` returns `"string"`. The string `"string"` is a truthy value, so `!typeof name` returns the boolean value `false`. `false === "object"` and `false === "string"` both return`false`.

(If we wanted to check whether the type was (un)equal to a certain type, we should've written `!==` instead of `!typeof`)

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

The `add` function returns an arrow function, which returns an arrow function, which returns an arrow function (still with me?). The first function receives an argument `x` with the value of `4`. We invoke the second function, which receives an argument `y` with the value `5`. Then we invoke the third function, which receives an argument `z` with the value `6`. When we're trying to access the value `x`, `y` and `z` within the last arrow function, the JS engine goes up the scope chain in order to find the values for `x` and `y` accordingly. This returns `4` `5` `6`.

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

The generator function `range` returns an async object with promises for each item in the range we pass: `Promise{1}`, `Promise{2}`, `Promise{3}`. We set the variable `gen` equal to the async object, after which we loop over it using a `for await ... of` loop. We set the variable `item` equal to the returned Promise values: first `Promise{1}`, then `Promise{2}`, then `Promise{3}`. Since we're _awaiting_ the value of `item`, the resolved promise, the resolved _values_ of the promises get returned: `1`, `2`, then `3`.

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

`myFunc` expects an object with properties `x`, `y` and `z` as its argument. Since we're only passing three separate numeric values (1, 2, 3) instead of one object with properties `x`, `y` and `z` ({x: 1, y: 2, z: 3}), `x`, `y` and `z` have their default value of `undefined`.

</p>
</details>

---

###### 126. এটার আউটপুট কোনটা?

```javascript
function getFine(speed, amount) {
  const formattedSpeed = new Intl.NumberFormat('en-US', {
    style: 'unit',
    unit: 'mile-per-hour',
  }).format(speed);

  const formattedAmount = new Intl.NumberFormat('en-US', {
    style: 'currency',
    currency: 'USD',
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

With the `Intl.NumberFormat` method, we can format numeric values to any locale. We format the numeric value `130` to the `en-US` locale as a `unit` in `mile-per-hour`, which results in `130 mph`. The numeric value `300` to the `en-US` locale as a `currency` in `USD` results in `$300.00`.

</p>
</details>

---

###### 127. এটার আউটপুট কোনটা?

```javascript
const spookyItems = ['👻', '🎃', '🕸'];
({ item: spookyItems[3] } = { item: '💀' });

console.log(spookyItems);
```

- A: `["👻", "🎃", "🕸"]`
- B: `["👻", "🎃", "🕸", "💀"]`
- C: `["👻", "🎃", "🕸", { item: "💀" }]`
- D: `["👻", "🎃", "🕸", "[object Object]"]`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: B

By destructuring objects, we can unpack values from the right-hand object, and assign the unpacked value to the value of the same property name on the left-hand object. In this case, we're assigning the value "💀" to `spookyItems[3]`. This means that we're modifying the `spookyItems` array, we're adding the "💀" to it. When logging `spookyItems`, `["👻", "🎃", "🕸", "💀"]` gets logged.

</p>
</details>

---

###### 128. এটার আউটপুট কোনটা?

```javascript
const name = 'Lydia Hallie';
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

With the `Number.isNaN` method, you can check if the value you pass is a _numeric value_ and equal to `NaN`. `name` is not a numeric value, so `Number.isNaN(name)` returns `false`. `age` is a numeric value, but is not equal to `NaN`, so `Number.isNaN(age)` returns `false`.

With the `isNaN` method, you can check if the value you pass is not a number. `name` is not a number, so `isNaN(name)` returns true. `age` is a number, so `isNaN(age)` returns `false`.

</p>
</details>

---

###### 129. এটার আউটপুট কোনটা?

```javascript
const randomValue = 21;

function getInfo() {
  console.log(typeof randomValue);
  const randomValue = 'Lydia Hallie';
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

Variables declared with the `const` keyword are not referenceable before their initialization: this is called the _temporal dead zone_. In the `getInfo` function, the variable `randomValue` is scoped in the functional scope of `getInfo`. On the line where we want to log the value of `typeof randomValue`, the variable `randomValue` isn't initialized yet: a `ReferenceError` gets thrown! The engine didn't go down the scope chain since we declared the variable `randomValue` in the `getInfo` function.

</p>
</details>

---

###### 130. এটার আউটপুট কোনটা?

```javascript
const myPromise = Promise.resolve('Woah some cool data');

(async () => {
  try {
    console.log(await myPromise);
  } catch {
    throw new Error(`Oops didn't work`);
  } finally {
    console.log('Oh finally!');
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

In the `try` block, we're logging the awaited value of the `myPromise` variable: `"Woah some cool data"`. Since no errors were thrown in the `try` block, the code in the `catch` block doesn't run. The code in the `finally` block _always_ runs, `"Oh finally!"` gets logged.

</p>
</details>

---

###### 131. এটার আউটপুট কোনটা?

```javascript
const emojis = ['🥑', ['✨', '✨', ['🍕', '🍕']]];

console.log(emojis.flat(1));
```

- A: `['🥑', ['✨', '✨', ['🍕', '🍕']]]`
- B: `['🥑', '✨', '✨', ['🍕', '🍕']]`
- C: `['🥑', ['✨', '✨', '🍕', '🍕']]`
- D: `['🥑', '✨', '✨', '🍕', '🍕']`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: B

With the `flat` method, we can create a new, flattened array. The depth of the flattened array depends on the value that we pass. In this case, we passed the value `1` (which we didn't have to, that's the default value), meaning that only the arrays on the first depth will be concatenated. `['🥑']` and `['✨', '✨', ['🍕', '🍕']]` in this case. Concatenating these two arrays results in `['🥑', '✨', '✨', ['🍕', '🍕']]`.

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

`counterOne` is an instance of the `Counter` class. The counter class contains a `count` property on its constructor, and an `increment` method. First, we invoked the `increment` method twice by calling `counterOne.increment()`. Currently, `counterOne.count` is `2`.

<img src="https://i.imgur.com/KxLlTm9.png" width="400">

Then, we create a new variable `counterTwo`, and set it equal to `counterOne`. Since objects interact by reference, we're just creating a new reference to the same spot in memory that `counterOne` points to. Since it has the same spot in memory, any changes made to the object that `counterTwo` has a reference to, also apply to `counterOne`. Currently, `counterTwo.count` is `2`.

We invoke `counterTwo.increment()`, which sets `count` to `3`. Then, we log the count on `counterOne`, which logs `3`.

<img src="https://i.imgur.com/BNBHXmc.png" width="400">

</p>
</details>

---

###### 133. এটার আউটপুট কোনটা?

```javascript
const myPromise = Promise.resolve(Promise.resolve('Promise'));

function funcOne() {
  setTimeout(() => console.log('Timeout 1!'), 0);
  myPromise.then((res) => res).then((res) => console.log(`${res} 1!`));
  console.log('Last line 1!');
}

async function funcTwo() {
  const res = await myPromise;
  console.log(`${res} 2!`);
  setTimeout(() => console.log('Timeout 2!'), 0);
  console.log('Last line 2!');
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

First, we invoke `funcOne`. On the first line of `funcOne`, we call the _asynchronous_ `setTimeout` function, from which the callback is sent to the Web API. (see my article on the event loop <a href="https://dev.to/lydiahallie/javascript-visualized-event-loop-3dif">here</a>.)

Then we call the `myPromise` promise, which is an _asynchronous_ operation. Pay attention, that now only the first then clause was added to the microtask queue.

Both the promise and the timeout are asynchronous operations, the function keeps on running while it's busy completing the promise and handling the `setTimeout` callback. This means that `Last line 1!` gets logged first, since this is not an asynchonous operation.

Since the callstack is not empty yet, the `setTimeout` function and promise in `funcOne` cannot get added to the callstack yet.

In `funcTwo`, the variable `res` gets `Promise` because `Promise.resolve(Promise.resolve('Promise'))` is equivalent to `Promise.resolve('Promise')` since resolving a promise just resolves it's value. The `await` in this line stops the execution of the function until it receives the resolution of the promise and then keeps on running synchronously until completion, so `Promise 2!` and then `Last line 2!` are logged and the `setTimeout` is sent to the Web API. If the first then clause in `funcOne` had its own log statement, it would be printed before `Promise 2!`. Howewer, it executed silently and put the second then clause in microtask queue. So, the second clause will be printed after `Promise 2!`.

Then the call stack is empty. Promises are _microtasks_ so they are resolved first when the call stack is empty so `Promise 1!` gets to be logged.

Now, since `funcTwo` popped off the call stack, the call stack is empty. The callbacks waiting in the queue (`() => console.log("Timeout 1!")` from `funcOne`, and `() => console.log("Timeout 2!")` from `funcTwo`) get added to the call stack one by one. The first callback logs `Timeout 1!`, and gets popped off the stack. Then, the second callback logs `Timeout 2!`, and gets popped off the stack.

</p>
</details>

---

###### 134. How can we invoke `sum` in `sum.js` from `index.js?`

```javascript
// sum.js
export default function sum(x) {
  return x + x;
}

// index.js
import * as sum from './sum';
```

- A: `sum(4)`
- B: `sum.sum(4)`
- C: `sum.default(4)`
- D: Default aren't imported with `*`, only named exports

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: C

With the asterisk `*`, we import all exported values from that file, both default and named. If we had the following file:

```javascript
// info.js
export const name = 'Lydia';
export const age = 21;
export default 'I love JavaScript';

// index.js
import * as info from './info';
console.log(info);
```

The following would get logged:

```javascript
{
  default: "I love JavaScript",
  name: "Lydia",
  age: 21
}
```

For the `sum` example, it means that the imported value `sum` looks like this:

```javascript
{ default: function sum(x) { return x + x } }
```

We can invoke this function, by calling `sum.default`

</p>
</details>

---

###### 135. এটার আউটপুট কোনটা?

```javascript
const handler = {
  set: () => console.log('Added a new property!'),
  get: () => console.log('Accessed a property!'),
};

const person = new Proxy({}, handler);

person.name = 'Lydia';
person.name;
```

- A: `Added a new property!`
- B: `Accessed a property!`
- C: `Added a new property!` `Accessed a property!`
- D: Nothing gets logged

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: C

With a Proxy object, we can add custom behavior to an object that we pass to it as the second argument. In this case, we pass the `handler` object which contains two properties: `set` and `get`. `set` gets invoked whenever we _set_ property values, and `get` gets invoked whenever we _get_ (access) property values.

The first argument is an empty object `{}`, which is the value of `person`. To this object, the custom behavior specified in the `handler` object gets added. If we add a property to the `person` object, `set` will get invoked. If we access a property on the `person` object, `get` gets invoked.

First, we added a new property `name` to the proxy object (`person.name = "Lydia"`). `set` gets invoked, and logs `"Added a new property!"`.

Then, we access a property value on the proxy object, and the `get` property on the handler object is invoked. `"Accessed a property!"` gets logged.

</p>
</details>

---

###### 136. Which of the following will modify the `person` object?

```javascript
const person = { name: 'Lydia Hallie' };

Object.seal(person);
```

- A: `person.name = "Evan Bacon"`
- B: `person.age = 21`
- C: `delete person.name`
- D: `Object.assign(person, { age: 21 })`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: A

With `Object.seal` we can prevent new properties from being _added_, or existing properties to be _removed_.

However, you can still modify the value of existing properties.

</p>
</details>

---

###### 137. Which of the following will modify the `person` object?

```javascript
const person = {
  name: 'Lydia Hallie',
  address: {
    street: '100 Main St',
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

The `Object.freeze` method _freezes_ an object. No properties can be added, modified, or removed.

However, it only _shallowly_ freezes the object, meaning that only _direct_ properties on the object are frozen. If the property is another object, like `address` in this case, the properties on that object aren't frozen, and can be modified.

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

First, we invoked `myFunc()` without passing any arguments. Since we didn't pass arguments, `num` and `value` got their default values: num is `2`, and `value` is the returned value of the function `add`. To the `add` function, we pass `num` as an argument, which had the value of `2`. `add` returns `4`, which is the value of `value`.

Then, we invoked `myFunc(3)` and passed the value `3` as the value for the argument `num`. We didn't pass an argument for `value`. Since we didn't pass a value for the `value` argument, it got the default value: the returned value of the `add` function. To `add`, we pass `num`, which has the value of `3`. `add` returns `6`, which is the value of `value`.

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

In ES2020, we can add private variables in classes by using the `#`. We cannot access these variables outside of the class. When we try to log `counter.#number`, a SyntaxError gets thrown: we cannot access it outside the `Counter` class!

</p>
</details>

---

###### 140. What's missing?

```javascript
const teams = [
  { name: 'Team 1', members: ['Paul', 'Lisa'] },
  { name: 'Team 2', members: ['Laura', 'Tim'] },
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

In order to iterate over the `members` in each element in the `teams` array, we need to pass `teams[i].members` to the `getMembers` generator function. The generator function returns a generator object. In order to iterate over each element in this generator object, we need to use `yield*`.

If we would've written `yield`, `return yield`, or `return`, the entire generator function would've gotten returned the first time we called the `next` method.

</p>
</details>

---

###### 141. এটার আউটপুট কোনটা?

```javascript
const person = {
  name: 'Lydia Hallie',
  hobbies: ['coding'],
};

function addHobby(hobby, hobbies = person.hobbies) {
  hobbies.push(hobby);
  return hobbies;
}

addHobby('running', []);
addHobby('dancing');
addHobby('baking', person.hobbies);

console.log(person.hobbies);
```

- A: `["coding"]`
- B: `["coding", "dancing"]`
- C: `["coding", "dancing", "baking"]`
- D: `["coding", "running", "dancing", "baking"]`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: C

The `addHobby` function receives two arguments, `hobby` and `hobbies` with the default value of the `hobbies` array on the `person` object.

First, we invoke the `addHobby` function, and pass `"running"` as the value for `hobby` and an empty array as the value for `hobbies`. Since we pass an empty array as the value for `hobbies`, `"running"` gets added to this empty array.

Then, we invoke the `addHobby` function, and pass `"dancing"` as the value for `hobby`. We didn't pass a value for `hobbies`, so it gets the default value, the `hobbies` property on the `person` object. We push the hobby `dancing` to the `person.hobbies` array.

Last, we invoke the `addHobby` function, and pass `"baking"` as the value for `hobby`, and the `person.hobbies` array as the value for `hobbies`. We push the hobby `baking` to the `person.hobbies` array.

After pushing `dancing` and `baking`, the value of `person.hobbies` is `["coding", "dancing", "baking"]`

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

We create the variable `pet` which is an instance of the `Flamingo` class. When we instantiate this instance, the `constructor` on `Flamingo` gets called. First, `"I'm pink. 🌸"` gets logged, after which we call `super()`. `super()` calls the constructor of the parent class, `Bird`. The constructor in `Bird` gets called, and logs `"I'm a bird. 🦢"`.

</p>
</details>

---

###### 143. Which of the options result(s) in an error?

```javascript
const emojis = ['🎄', '🎅🏼', '🎁', '⭐'];

/* 1 */ emojis.push('🦌');
/* 2 */ emojis.splice(0, 2);
/* 3 */ emojis = [...emojis, '🥂'];
/* 4 */ emojis.length = 0;
```

- A: 1
- B: 1 and 2
- C: 3 and 4
- D: 3

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: D

The `const` keyword simply means we cannot _redeclare_ the value of that variable, it's _read-only_. However, the value itself isn't immutable. The properties on the `emojis` array can be modified, for example by pushing new values, splicing them, or setting the length of the array to 0.

</p>
</details>

---

###### 144. What do we need to add to the `person` object to get `["Lydia Hallie", 21]` as the output of `[...person]`?

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

Objects aren't iterable by default. An iterable is an iterable if the iterator protocol is present. We can add this manually by adding the iterator symbol `[Symbol.iterator]`, which has to return a generator object, for example by making it a generator function `*[Symbol.iterator]() {}`. This generator function has to yield the `Object.values` of the `person` object if we want it to return the array `["Lydia Hallie", 21]`: `yield* Object.values(this)`.

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

The `if` condition within the `forEach` loop checks whether the value of `num` is truthy or falsy. Since the first number in the `nums` array is `0`, a falsy value, the `if` statement's code block won't be executed. `count` only gets incremented for the other 3 numbers in the `nums` array, `1`, `2` and `3`. Since `count` gets incremented by `1` 3 times, the value of `count` is `3`.

</p>
</details>

---

###### 146. এটার আউটপুট কোনটা?

```javascript
function getFruit(fruits) {
  console.log(fruits?.[1]?.[1]);
}

getFruit([['🍊', '🍌'], ['🍍']]);
getFruit();
getFruit([['🍍'], ['🍊', '🍌']]);
```

- A: `null`, `undefined`, 🍌
- B: `[]`, `null`, 🍌
- C: `[]`, `[]`, 🍌
- D: `undefined`, `undefined`, 🍌

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: D

The `?` allows us to optionally access deeper nested properties within objects. We're trying to log the item on index `1` within the subarray that's on index `1` of the `fruits` array. If the subarray on index `1` in the `fruits` array doesn't exist, it'll simply return `undefined`. If the subarray on index `1` in the `fruits` array exists, but this subarray doesn't have an item on its `1` index, it'll also return `undefined`.

First, we're trying to log the second item in the `['🍍']` subarray of `[['🍊', '🍌'], ['🍍']]`. This subarray only contains one item, which means there is no item on index `1`, and returns `undefined`.

Then, we're invoking the `getFruits` function without passing a value as an argument, which means that `fruits` has a value of `undefined` by default. Since we're conditionally chaining the item on index `1` of`fruits`, it returns `undefined` since this item on index `1` does not exist.

Lastly, we're trying to log the second item in the `['🍊', '🍌']` subarray of `['🍍'], ['🍊', '🍌']`. The item on index `1` within this subarray is `🍌`, which gets logged.

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

We set the variable `calc` equal to a new instance of the `Calc` class. Then, we instantiate a new instance of `Calc`, and invoke the `increase` method on this instance. Since the count property is within the constructor of the `Calc` class, the count property is not shared on the prototype of `Calc`. This means that the value of count has not been updated for the instance calc points to, count is still `0`.

</p>
</details>

---

###### 148. এটার আউটপুট কোনটা?

```javascript
const user = {
  email: 'e@mail.com',
  password: '12345',
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

const updatedUser = updateUser({ email: 'new@email.com' });

console.log(updatedUser === user);
```

- A: `false`
- B: `true`
- C: `TypeError`
- D: `ReferenceError`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: B

The `updateUser` function updates the values of the `email` and `password` properties on user, if their values are passed to the function, after which the function returns the `user` object. The returned value of the `updateUser` function is the `user` object, which means that the value of updatedUser is a reference to the same `user` object that `user` points to. `updatedUser === user` equals `true`.

</p>
</details>

---

###### 149. এটার আউটপুট কোনটা?

```javascript
const fruit = ['🍌', '🍊', '🍎'];

fruit.slice(0, 1);
fruit.splice(0, 1);
fruit.unshift('🍇');

console.log(fruit);
```

- A: `['🍌', '🍊', '🍎']`
- B: `['🍊', '🍎']`
- C: `['🍇', '🍊', '🍎']`
- D: `['🍇', '🍌', '🍊', '🍎']`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: C

First, we invoke the `slice` method on the fruit array. The slice method does not modify the original array, but returns the value that it sliced off the array: the banana emoji.
Then, we invoke the `splice` method on the fruit array. The splice method does modify the original array, which means that the fruit array now consists of `['🍊', '🍎']`.
At last, we invoke the `unshift` method on the `fruit` array, which modifies the original array by adding the provided value, ‘🍇’ in this case, as the first element in the array. The fruit array now consists of `['🍇', '🍊', '🍎']`.

</p>
</details>

---

###### 150. এটার আউটপুট কোনটা?

```javascript
const animals = {};
let dog = { emoji: '🐶' };
let cat = { emoji: '🐈' };

animals[dog] = { ...dog, name: 'Mara' };
animals[cat] = { ...cat, name: 'Sara' };

console.log(animals[dog]);
```

- A: `{ emoji: "🐶", name: "Mara" }`
- B: `{ emoji: "🐈", name: "Sara" }`
- C: `undefined`
- D: `ReferenceError`

<details><summary><b>উত্তর দেখুন</b></summary>
<p>

#### উত্তর: B

Object keys are converted to strings.

Since the value of `dog` is an object, `animals[dog]` actually means that we’re creating a new property called `"[object Object]"` equal to the new object. `animals["[object Object]"]` is now equal to `{ emoji: "🐶", name: "Mara"}`.

`cat` is also an object, which means that `animals[cat]` actually means that we’re overwriting the value of `animals["[object Object]"]` with the new cat properties.

Logging `animals[dog]`, or actually `animals["[object Object]"]` since converting the `dog` object to a string results `"[object Object]"`, returns the `{ emoji: "🐈", name: "Sara" }`.

</p>
</details>

---

###### 151. এটার আউটপুট কোনটা?

```javascript
const user = {
  email: 'my@email.com',
  updateEmail: (email) => {
    this.email = email;
  },
};

user.updateEmail('new@email.com');
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
const promise1 = Promise.resolve('First');
const promise2 = Promise.resolve('Second');
const promise3 = Promise.reject('Third');
const promise4 = Promise.resolve('Fourth');

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
const keys = ['name', 'age'];
const values = ['Lydia', 22];

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
  if (!validEmail) throw new Error('Valid email pls');

  return {
    email,
    address: address ? address : null,
  };
};

const member = createMember({ email: 'my@email.com' });
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
let randomValue = { name: 'Lydia' };
randomValue = 23;

if (!typeof randomValue === 'string') {
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
