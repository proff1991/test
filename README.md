# Александр Пархоменко

## Contacts
* **Location:** Kharkiv, Ukraine
* **Telegram:** [@username118](https://t.me/username118)
* **Email:** parkhomenko.business@gmail.com
* **GitHub:** [proff1991](https://github.com/proff1991)
* **Codewars:** [proff1991](https://www.codewars.com/users/proff1991)
* **YouTube:** [Обзоры S-M](https://www.youtube.com/channel/UCV1oB1TOfm6CNKfwRZVFzWQ)

## About Me
У меня есть слишком много хобби: программирование, электроника, музыка, видеоигры, видеомонтаж, дизайн. Благодаря своим увлечениям я смог устроиться на работу контент менеджером в интернет-магазине электроники, создать YouTube канал и быть желанным гостем с гитарой на корпоративах компании. Но лучше всего мне даётся программирование и на своей текущей работе из обычного контент-менеджера я смог стать еще и программистом сделав десятки локальных программных продукта для контроля учёта товаров, заказов, аналитики рынка и т.д.. Из-за того что все свои приложения я делал сам - мой код недостаточно оптимизирован и имеет ошибки новичка. Моя цель - стать полноценным бекенд разработчиком. Надеюсь учёба в RS School на курсе FE Pre-School поможет мне заполнить все пробелы в начальных знаниях разработки приложений.

## Skills 
* HTML (basic)
* CSS (basic)
* JS (5 kyu codewars)
* Node.js (basic)
* Google Apps Script
* Google Sheets / Microsoft Excell 
* Adobe Photoshop 
* Adobe Premiere Pro / Magix Vegas Pro
* Ableton Live

## Code example
### codewars 
##### Task ["Simple Pig Latin"](https://www.codewars.com/kata/520b9d2ad5c005041100000f/typescript) 

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

##### Google Script with Cheerio library, parser
```
const link = "https://unknownwebsite.ua/uk/cellphones/"
const tableId = "unknownGoogleSheetsId"
const answerPriceRange = "J1:M"
const sheetName = "parser"
const parserResult = []
const filterType = "?s=price"
let disabledGoods = ""


function goParser(){
  pageIterrator(link)
}

function pageIterrator(firstLink){

  SpreadsheetApp.openById( tableId )
    .getSheetByName( sheetName )
    .getRange( answerPriceRange )
    .clearContent();

  parserWebsite(firstLink+filterType)

  for(let i1 = 2; disabledGoods.length < 2; ++i1){
    parserWebsite(`${firstLink}p${i1}/${filterType}`)
  }

  SpreadsheetApp.openById( tableId )
    .getSheetByName( sheetName )
    .getRange( answerPriceRange + parserResult.length )
    .setValues( parserResult );

  SpreadsheetApp.flush()
}


function parserWebsite(link){

  let response = UrlFetchApp.fetch(link).getContentText()

  let $ = Cheerio.load(response)
  let cheerioAnswer
  let cheerioCode
  let cheerioName
  let cheerioPrice
  let cheerioButton

  for( let i = 0 ; i < 30 ; ++i){
    cheerioAnswer = Cheerio.load($('div.products-listing-item.details-two-column')
      .eq([i])
      .html());

    disabledGoods += cheerioAnswer('span.buy-btn.disabled').text()

    cheerioButton = cheerioAnswer('button.buy-btn').text()

    cheerioCode = cheerioAnswer('div.sku-block')
      .text()
      .match(/\d/g)
      .join('');

    cheerioName = cheerioAnswer('a.name-block')
      .text().replace(/Смартфон /,"")
      .replace(/\s\/\s/,"/");

    cheerioPrice = cheerioAnswer('div.regular-price')
      .text().match(/\d/g)
      .join('');

    cheerioButton ? parserResult.push([ cheerioCode, cheerioName, cheerioPrice, cheerioButton]) : "";
  }
  
}
```

## Experience
2017 - настоящее время: разработка приложений на Goole Sheets и Google Apps Script

## Education
#### Donbas State Technical University
Ferrous metallurgy, Steelmaker
* **2009-2013:** bachelor
* **2013-2014:** master

## English level
A2 (Pre-Intermediate) English test result (Test passed on 12.04.2023 in 20 min. by [training.epam.ua](https://training.epam.ua/))






