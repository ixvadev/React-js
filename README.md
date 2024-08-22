# React Nima?

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

# `useState` Nima?

**`useState`** — bu React'dagi *hook* bo'lib, funksional komponentlarda state (holat) boshqarish uchun ishlatiladi. `useState` yordamida komponentning ichki holatini belgilash va keyinchalik o'zgartirish mumkin.

## `useState` Hook'ining Ishlatilishi

Quyida `useState` qanday ishlatilishini ko'rsatadigan oddiy misol keltirilgan:

```javascript
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

