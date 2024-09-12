

# React Nima ? 

**React** — bu *JavaScript* kutubxonasi bo'lib, foydalanuvchi interfeyslarini (UI) yaratish uchun ishlatiladi. U **Facebook** tomonidan ishlab chiqilgan va hozirda keng qo'llaniladi. React asosan veb ilovalarda modulli va qayta foydalanishga yaroqli UI komponentlarini yaratishga yordam beradi.

## React-ning Asosiy Xususiyatlari:
- **Komponentlar:** React ilovalarini kichik, mustaqil komponentlarga bo'lish imkonini beradi.
- **Virtual DOM:** React-da Virtual DOM texnologiyasi yordamida o'zgarishlar samarali tarzda qo'llaniladi, bu esa ilova tezligini oshiradi.
- **Bir yo'nalishli ma'lumot oqimi:** React-da ma'lumotlar bir yo'nalishda oqadi, bu esa dastur loģikasini soddalashtiradi.

## React bilan Ishlash:
- **JSX:** HTML va JavaScript-ni birlashtiruvchi sintaksis bo'lib, komponentlarni yozish uchun ishlatiladi.
- **State va Props:** Komponentlar o'rtasida ma'lumot almashish va ichki holatlarni boshqarish uchun ishlatiladi.
- **React Hooks:** Funksional komponentlarda state va boshqa React xususiyatlaridan foydalanishga imkon beradi.

React dasturchilarga zamonaviy, dinamik va murakkab foydalanuvchi interfeyslarini yaratishda katta yordam beradi.

# JSX (JavaScript XML) Haqida

JSX (JavaScript XML) — bu React'da ishlatiladigan sintaksis kengaytmasi bo‘lib, JavaScript kodida HTML-ga o‘xshash sintaksisda UI komponentlarini yaratishga imkon beradi. JSX oddiy JavaScript emas, ammo React bu kodni shaxsiy `createElement` funksiyasiga kompilyatsiya qiladi.

## JSXning Afzalliklari

# React-da `props`ning Vazifalari

React-da `props` (bu "properties"ning qisqartmasi) komponentlarga ma'lumotlarni uzatish va ularni moslashuvchan qilish uchun ishlatiladi. Har bir React komponenti funksional yoki sinf (class) komponent bo'lib, `props` orqali tashqi ma'lumotlarni qabul qiladi. Ushbu ma'lumotlar komponentga quyidan yuqoriga, ya'ni ota-komponentdan bola-komponentga uzatiladi.

## Props vazifalari:

1. **Ma'lumotlarni uzatish**: 
   `props` orqali ota-komponentdan bola-komponentga ma'lumotlarni uzatish mumkin. Masalan, biror komponentda foydalanuvchi nomi, rasmi yoki boshqa ma'lumotlarni ko'rsatish kerak bo'lsa, bu ma'lumotlar ota-komponentdan bola-komponentga `props` orqali yuboriladi.

2. **Komponentni moslashuvchan qilish**: 
   `props` komponentlarni qayta foydalanish imkonini beradi. Bir xil komponentni turli joylarda turli ma'lumotlar bilan ishlatish mumkin. Misol uchun, bir xil karta komponenti har xil kontent bilan foydalanilishi mumkin.

3. **Qayta foydalanish**: 
   `props` orqali komponentlar qayta ishlatiladi, chunki har bir yangi chaqiriqda turli `props` qiymatlari bilan bir xil komponentni ishlatish mumkin.

## Misol:


      function Hello(props) {
        return <h1>Hello, {props.name}!</h1>;
      }
      
      // Ushbu komponentni chaqirish
      <Hello name="ixva" />
      <Hello name="ixvadev" />


### 1. **Tushunarli sintaksis**
   JSX yordamida UI komponentlarini yozish ancha sodda va tushunarli bo‘ladi, chunki u HTML-ga o‘xshash ko‘rinishda. Bu esa ishlab chiquvchilar uchun kodni o‘qish va tushunishni osonlashtiradi.

### 2. **JSXda ifodalar**
   JSX ichida JavaScript ifodalaridan foydalanish mumkin. Bu imkoniyat orqali dinamik tarkib yaratish osonlashadi.

       const name = "Dunyo";
       const element = <h1>Salom, {name}!</h1>;

# `useRef` nima?

`useRef` — bu React hooki bo'lib, komponentning o'zgarmas qiymatlarini saqlash va to'g'ridan-to'g'ri DOM elementlariga murojaat qilish imkonini beradi. `useRef` qaytaradigan ob'ekt (reference) komponentlar o'rtasida o'zgarmasdan saqlanadi va komponent qayta render qilinganda o'zgarmaydi.

## `useRef` ning asosiy xususiyatlari

### 1. **O'zgarmas qiymat saqlash:**
`useRef` komponent ichida biror qiymatni saqlab turadi, va bu qiymat komponent qayta render qilinganda o'zgarmaydi. Bu xuddi bir xil holatni saqlab turishdek, ammo render jarayoniga ta'sir qilmaydi.


      import { useRef } from 'react';
      
      const MyComponent = () => {
        const countRef = useRef(0);  // Dastlabki qiymat 0
        return <div>{countRef.current}</div>;
      };



# Axios haqida

**Axios** — bu JavaScript kutubxonasi bo'lib, HTTP so'rovlarini yuborish va serverdan ma'lumot olishni osonlashtiradi. Asosan, API bilan ishlashda qo'llaniladi.

## Asosiy xususiyatlar

- **Oddiy va qulay foydalanish**: Axios sintaksisi sodda va tushunarli.
- **Promise asosida ishlaydi**: So'rovlar `Promise` bilan boshqariladi (`then` va `catch` yordamida).
- **Brauzerlarni qo'llab-quvvatlash**: Axios eski va yangi brauzerlar bilan yaxshi ishlaydi.
- **Ma'lumotlarni avtomatik formatlash**: JSON formatidagi ma'lumotlarni avtomatik yuboradi va qabul qiladi.

## Oddiy Misollar

### GET so'rovi

Serverdan ma'lumot olish uchun GET so'rovi yuborish:

      import axios from 'axios';
      
      axios.get('https://jsonplaceholder.typicode.com/posts/1')
        .then(response => {
          console.log(response.data); // Ma'lumotlar keldi
        })
        .catch(error => {
          console.error('Xato:', error); // Xatolarni ushlash
        });


# `useState` Nima?

**`useState`** — bu React'dagi *hook* bo'lib, funksional komponentlarda state (holat) boshqarish uchun ishlatiladi. `useState` yordamida komponentning ichki holatini belgilash va keyinchalik o'zgartirish mumkin.

## `useState` Hook'ining Ishlatilishi

Quyida `useState` qanday ishlatilishini ko'rsatadigan oddiy misol keltirilgan:

    
      import React, { useState } from 'react';
      
      function Counter() {
        // useState hook bilan count o'zgaruvchisini va uni o'zgartiruvchi setCount funksiyasini yaratamiz
        const [count, setCount] = useState(0);
      
        return (
          <div>
            <p>Siz {count} marta bosdingiz</p>
            <button onClick={() => setCount(count + 1)}>
              Bosish
            </button>
          </div>
        );
      }
      
      export default Counter;

# `useEffect` Haqida

`useEffect` — bu React kutubxonasining asosiy `hook`laridan biri bo‘lib, komponentning yanada murakkab holatlarida yon ta’sirlarni (side effects) boshqarish uchun ishlatiladi. Yon ta’sirlar — bu komponentning render jarayonidan tashqaridagi funksiyalar, masalan, brauzerdan ma’lumotlarni olish, tashqi API ga murojaat qilish, vaqt o‘tkazgichlar (`timers`) yoki subskribtsiyalarni sozlash va ularni tozalash.

### 1. `useEffect`ning Asosiy Ishlatilishi


      import React, { useEffect } from 'react';
      
      function MyComponent() {
        useEffect(() => {
          // Bu yerda yon ta’sirlarni amalga oshirish mumkin
          console.log('Komponent render qilindi yoki yangilandi.');
   
       // Bu yerda tozalash funksiyasini qaytarish mumkin
       return () => {
         console.log('Komponent tozalanmoqda.');
       };
     }, []);
   
     return (
       <div>
         <p>Salom, bu mening komponentim!</p>
       </div>
     );
    }

### React `useCallback` Hooki

`useCallback` hooki Reactda callback funksiyalarni memoizatsiya qilish uchun ishlatiladi. Bu har bir renderda qayta yaratilishining oldini oladi. Bu, ayniqsa, callbacklarni bolalar komponentlariga uzatishda foydalidir, chunki u funksiyaning manzili bir xil bo'lib qolishini ta'minlaydi, agar uning bog'liqliklari o'zgarmasa.

#### Sintaksis

      const memoizedCallback = useCallback(() => {
        // Bu yerda sizning callback logikangiz bo'ladi
      }, [bog'liqlik1, bog'liqlik2, ...]);

# `useContext` Hooki

`useContext` hooki React kutubxonasining kontekstni boshqarish uchun mo'ljallangan hookidir. U komponentlar orasida ma'lumotlarni uzatishda qulaylik yaratadi va prop drilling (props orqali ma'lumotlarni chuqurroq komponentlarga uzatish) muammosini hal qilishga yordam beradi.

## Kontekstni yaratish

Kontekst yaratish uchun `React.createContext` funksiyasidan foydalanamiz. Bu funksiya ikki narsani qaytaradi:
1. **Kontekst obyekti** - bu `Provider` va `Consumer` komponentlarini o'z ichiga oladi.
2. **Default qiymat** - bu kontekst yaratilganda berilgan default qiymat bo'ladi.

Misol:

      import React from 'react';
      
      const MyContext = React.createContext('defaultValue');


# State Management nima?

**State Management** — bu dastur ichidagi holat (state)ni samarali boshqarish va sinxronlash jarayoni. React yoki boshqa UI kutubxonalarida komponentlar ichidagi ma'lumotlar (holat)ni boshqarish, ularga o'zgartirish kiritish va o'zaro ulashish kerak bo'ladi. Dastur kattalashgan sari holatlarni samarali boshqarish muhim ahamiyatga ega bo'ladi.

## Nima uchun State Management kerak?

- **Murakkablik oshishi**: Dastur kattalashgan sari ko'proq komponentlar va ma'lumotlarni o'zaro ulashish zaruriyati paydo bo'ladi.
- **Holatni sinxronlashtirish**: Bir nechta komponentlar bitta ma'lumotga tayanishi kerak bo'lganda, buni to'g'ri sinxronlashtirish talab qilinadi.
- **Ma'lumotlar oqimi**: State management orqali ma'lumotlar oqimini tartibli saqlash va bir xil ko'rinishdagi o'zgarishlarni boshqarish osonlashadi.

## Reactda State Management

Reactda holat (state)ni boshqarish uchun bir nechta usullar mavjud. Kichik loyihalar uchun oddiy `useState` va `useReducer` yetarli bo'lishi mumkin, lekin katta va murakkab loyihalarda keng qamrovli state management kutubxonalaridan foydalanish kerak bo'ladi.

### Reactda Holatni boshqarish usullari:

### 1. **useState**
- React komponentlarida lokal holatni boshqarish uchun ishlatiladi. Kichik va oddiy holatlar uchun qulay.

      import React, { useState } from 'react';
      
      const Counter = () => {
        const [count, setCount] = useState(0);
      
        return (
          <div>
            <p>{count}</p>
            <button onClick={() => setCount(count + 1)}>Increase</button>
          </div>
        );
      };




# SWR (Stale-While-Revalidate)

SWR (Stale-While-Revalidate) — bu React dasturlari uchun ma'lumot olish va keshlashni osonlashtiruvchi kutubxona. Ushbu kutubxona Vercel tomonidan ishlab chiqilgan va zamonaviy ma'lumot olish strategiyalarini o'z ichiga oladi. SWR nomi **"stale-while-revalidate"** tamoyiliga asoslangan, ya'ni dastlab keshdagi (eskirgan) ma'lumot olinadi, keyin esa yangi ma'lumot fon jarayonida qayta olinadi va yangilanadi.

## SWR asosiy imkoniyatlari:
1. **Ma'lumot olish va keshlash**: Ma'lumotlar avtomatik ravishda keshlanadi va yangi ma'lumotlar kelguniga qadar ishlatiladi.
2. **Revalidatsiya**: Ma'lumotlar fon jarayonida yangilanadi va foydalanuvchiga yangi ma'lumot yetkaziladi.
3. **Avtomatik qayta sinxronlash**: Ma'lumotlar real vaqt rejimida yangilanadi.
4. **Xatolar bilan ishlash**: Ma'lumot olishda yuzaga kelgan xatolarni samarali boshqarish imkonini beradi.

## SWR ishlatilishi:
         import useSWR from 'swr'
         
         // Ma'lumot olish uchun fetcher funksiyasi
         const fetcher = (url) => fetch(url).then((res) => res.json())
         
         export default function Component() {
           // Ma'lumot olish uchun SWR hook
           const { data, error } = useSWR('/api/data', fetcher)
         
           if (error) return <div>Xato yuz berdi</div>
           if (!data) return <div>Yuklanmoqda...</div>
         
           return <div>Ma'lumot: {data.message}</div>
         }





