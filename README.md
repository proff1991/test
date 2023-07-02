# Александр Пархоменко

## Contacts
* **Location:** Kharkiv, Ukraine
* **Telegram:** [@username118](https://t.me/username118)
* **Email:** parkhomenko.business@gmail.com
* **GitHub:** [proff1991](https://github.com/proff1991)
* **Codewars:** [proff1991](https://www.codewars.com/users/proff1991)
* **YouTube:** [Обзоры S-M](https://www.youtube.com/channel/UCV1oB1TOfm6CNKfwRZVFzWQ)

## About Me
Имею много различных хобби: программирование, компьютеры, электроника, музыка, видеоигры, видеомонтаж, дизайн. Благодаря перечисленным увлечениям смог устроиться на работу контент менеджером в интернет-магазине по продаже электроники. Внутри компании удалось создать YouTube канал по мобильным видеоиграм со своим активными комьюнити. Увлечение музыкой (игрой на гитаре) помогло и вести ютуб канала (делать музыкальные вставки), и быть желанным гостем на корпоративах компании. Но лучше всего раскрылось моё увлечение программированием благодаря чему на своей текущей работе из обычного контент-менеджера я смог стать программистом сделав десятки программных продуктов для ведения и контроля учёта товаров, заказов, аналитики рынка и т.д.. Из-за того что все свои приложения я делал сам - мой код недостаточно оптимизирован. Моя цель - стать полноценным бекенд разработчиком. Надеюсь учёба в RS School поможет мне заполнить все пробелы в знаниях фронтенд разработки что поможет мне делать более оптимальные бекенд приложения.

## Skills 
* HTML (basic)
* CSS (basic)
* JS (5kyu codewars)
* Node.js (basic)
* Google Apps Script
* Google Sheets / Microsoft Excell 
* Adobe Photoshop 
* Adobe Premiere Pro / Magix Vegas Pro
* Ableton Live

## Code example
### 

```
export const pigIt = (a : string) : string =>  {
  let stringArray = a.split(" ")
  let newArray = []
  for (let elem of stringArray){
    if (/[A-Za-z]/g.test(elem)) {
      newArray.push(elem.split("").slice(1).join("")+elem[0]+"ay")
    } else {
      newArray.push(elem)
    }
  }
  return newArray.join(" ")
}
```
