![pngwing com (5)](https://user-images.githubusercontent.com/85753549/181843191-6a656b2c-3df9-4d24-bccf-4369a6458141.png)

# ***Wallet by Crimson Coalition***

<p>
  <img alt="Версия" src="https://img.shields.io/badge/version-0.6-blue.svg?cacheSeconds=2592000" />
  <a href="https://github.com/kefranabg/readme-md-generator#readme" target="_blank">
    <img alt="Документация" src="https://img.shields.io/badge/documentation-yes-brightgreen.svg" />
  </a>
  <a href="https://github.com/kefranabg/readme-md-generator/graphs/commit-activity" target="_blank">
    <img alt="В разработке" src="https://img.shields.io/badge/Maintained%3F-yes-green.svg" />
  </a>
  <a href="https://github.com/kefranabg/readme-md-generator/blob/master/LICENSE" target="_blank">
    <img alt="Лицензия: GPL3" src="https://img.shields.io/github/license/CrimsonCoalition/wallet" />
  </a>
</p>


***Crimson Wallet или же просто Wallet - криптокошелек от [@CrimsonCoalition](https://t.me/CrimnsonCoalition)***

***Wallet*** - это telegram-бот для хранения Ethereum, Bitcoin, Toncoin, USDT и других криптовалют. Этот кошелек основан на [этом](https://github.com/googleQ7/fastcoinbot) проекте

## ***Содержание***
***[Описание]()***

***[Логика работы бота]()***

***[Структура]()***

* ***[Bot-core]()***

* ***[Modules]()***

***[Криптовалюты]()***

* ***[Bitcoin]()***

* ***[Ethereum]()***

## ***Логика работы бота***

```
       Меню
   ┌─────┼────────────────┬────────────────┐
   │     │                │                │
   │     │                │                │
   │     │                │                │
КОШЕЛЕК  │             ПОЛУЧЕНИЕ           │                   ## будет обновляться
 баланс  │          показ адреса           │
кошелька │            и QR-кода            │
         │                                 │  
       ОТПРАВКА                          КУПИТЬ
    Ввод адреса                 Ввод BTC, TON, ETH, USDT, TRON
                                         или RUB
      и отправка                 Информации о пользователе
       средств                     Отправка средств 
```

## ***Структура бота***
### ***Bot-Core***
***Ядро бота состоит из двух модулей в корне проекта: `app.py` и `bot.py`***

***Первый модуль представляет из себя стартовый модуль, который запускает и инициализирует бота, он отвечает за создание Flask веб-приложения, создание объекта бота, инициализацию бота и вебхуков, получение и обработку данных с вебхуков.***

***`Bot.py`*** ***отвечает за класс Bot, который как представляет из себя центральную часть приложения, которая отвечает за работу бота. В нем описаны методы работы с: базой данных, ***Telegram API***, обработку сообщений пользователя, загрузку модулей бота, работу с пользовательской сессией, генерирование пользовательских клавиатур и сообщений из шаблонов.***

### ***Modules***
***Модули представляют из себя некоторые скрипты, сценарии, которым бот передает сообщения от пользователя, а они в свою очередь решают что делать в той или иной ситуации. Модули состоят из некоторых функций обработчиков handler'ов. Самое первое сообщение пользователя обрабатывается стандартным хендлером, который указан в конфиге в дальнейшей работе бота хендлеры могут не только получать данные, но и указывать какой хендлер будет обрабатывать следующее сообщение. Таким образом строится неявный граф обработки сообщений пользователя.***

***Внутри модулей хендлеры могут оперировать любой информацией:***

***Получать и записывать данные в базу данных
Отправлять сообщение через `Telegram API`
Запрашивать или отправлять средства по средствам `Bitcoin API`
Отрисовывать пользовательские клавиатуры
И многое другое.***

### ***Config***
***Конфиги представляют из себя статические JSON-файлы, которые хранят необходимую боту информацию. На данный момент в боте существует три конфиг-файлов: `init.json`, `keyboards.json`, `messages.json`.***

***Первый файл отвечает за основные настройки бота:***

***`default-handler` - стандартный обработчик сообщения, когда пользователь пишет первый раз или не указан обработчик который будет обрабатывать следующее сообщение***

***`menu-button` - сообщение при получении которого, бот всегда будет возвращаться в главное меню***

***`commission` - Bitcoin комиссия для совершения транзакции, указывается в сатоши!***

***`keyboards.json` - отвечает за хранение шаблонов клавиатур, о работе с которыми вы можете прочитать далее messages.json - отвечает за хранение шаблонов сообщений, о работе с которыми вы можете прочитать далее***

## ***Bitcoin***
***Для работы с Bitcoin используется библиотека `pybitcointools`.***


## ***Ethereum***
*** ****
