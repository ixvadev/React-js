

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
# React Query

React Query - bu React ilovalarida ma'lumotlarni olish, kesh qilish va sinxronizatsiya qilish uchun mo'ljallangan kutubxona. U ma'lumotlarni boshqarishni soddalashtirish va serverdan olingan ma'lumotlar bilan ishlashni qulayroq qilish uchun yordam beradi.

## Asosiy Xususiyatlar

1. **Avtomatik Kesh**: Ma'lumotlarni avtomatik ravishda kesh qiladi va keyingi so'rovlar uchun qayta ishlatadi.
2. **Sinxronizatsiya**: Ma'lumotlar avtomatik ravishda yangilanadi, real vaqt rejimida yangilangan ma'lumotlarni ko'rsatadi.
3. **So'rovni Qayta Amalga Oshirish**: Agar so'rov muvaffaqiyatsiz bo'lsa yoki ma'lumotlar yangilangan bo'lsa, so'rovni qayta amalga oshiradi.
4. **So'rovlar va Keshni Boshqarish**: Turli so'rovlar va keshlarni boshqarish imkoniyatlari mavjud.
5. **Sodda API**: Oddiy va tushunarli API.
6. **Qulay DevTools**: So'rovlar va ma'lumotlar holatini kuzatishni osonlashtiradi.

## Misol

```jsx
import React from 'react';
import { useQuery } from 'react-query';
import axios from 'axios';

const fetchPosts = async () => {
  const { data } = await axios.get('https://jsonplaceholder.typicode.com/posts');
  return data;
};

const Posts = () => {
  const { data, error, isLoading } = useQuery('posts', fetchPosts);

  if (isLoading) return <div>Loading...</div>;
  if (error) return <div>An error occurred: {error.message}</div>;

  return (
    <ul>
      {data.map(post => (
        <li key={post.id}>{post.title}</li>
      ))}
    </ul>
  );
};

export default Posts;

