# Недопустимый символ (InvalidCharacterInFile)

| Тип | Поддерживаются<br/>языки | Важность | Включена<br/>по умолчанию | Время на<br/>исправление (мин) | Тэги |
| :-: | :-: | :-: | :-: | :-: | :-: |
| `Ошибка` | `BSL`<br/>`OS` | `Важный` | `Да` | `1` | `error`<br/>`standard`<br/>`unpredictable` |

<!-- Блоки выше заполняются автоматически, не трогать -->
## Описание диагностики

В текстах модулей (включая комментарии) не допускается использовать неразрывные пробелы и знак минус "-" в других кодировках (короткое, длинное тире, мягкий перенос и т.д.).

Такие символы часто оказываются в тексте модулей при копировании из офисных документов и приводят к ряду сложностей при разработке.

Например:

- не работает поиск фрагментов текста, включающих «неправильные» минусы и пробелы
- некорректно выводятся подсказки типов параметров процедур и функций в конфигураторе и расширенная проверка в 1С:EDT
- указание «неправильного» минуса в выражениях приведет к синтаксической ошибке

Диагностика обнаруживает следующие недопустимые символы

- Среднее тире
- Цифровое тире
- Длинное тире 
- Горизонтальная линия
- "Неправильный" минус
- Мягкий перенос
- Неразрывный пробел

## Источники

* [Стандарт: Тексты модулей](https://its.1c.ru/db/v8std#content:456:hdoc)

## Сниппеты

<!-- Блоки ниже заполняются автоматически, не трогать -->
### Экранирование кода

```bsl
// BSLLS:InvalidCharacterInFile-off
// BSLLS:InvalidCharacterInFile-on
```

### Параметр конфигурационного файла

```json
"InvalidCharacterInFile": false
```
