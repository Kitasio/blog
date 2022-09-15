---
title: "AI Training description"
date: 2022-09-15T13:30:50+04:00
draft: false
hidden: true
---

## Abstract
* Выбрать любую книгу
* Написать (самому или нет, неважно) короткое описание, оно должно включать в себя общее настроение, например: Любовный роман или Жестокий триллер о бла бла бла
* Описать обложку словами в стиле prompt для Stable Diffusion AI
* Повторить 500 раз

## Workflow

### Работа над описанием

#### Выбор книги
Можно разбить 50/50 взяв половину книг из [litnet](litnet.com) например [Тиран моей мечты](https://litnet.com/ru/book/tiran-moei-mechty-b410846), и вторую половину "нормальных" книг, например Мастер и Маргарита

#### Перевод на англ
Если книга из литнета, нужно перевести ее аннотацию в [yandex translate](https://translate.yandex.com/)

#### Создание описания
Если книга из литнета, можно использовать следующий prompt для конвертации аннотации в описание с помощью OpenAI:

```
Convert this annotation to a book description: 

Annotation: тут идет аннотация книги

Description:
```

К готовому описанию нужно добавить общее настроение чтобы AI было понятно с чем он имеет дело

Далее, если книга известная, то  можно сразу идти в OpenAI и использовать этот prompt,
Вместо Lord of the Rings вставляем название нужной книги:

```
Summarize Lord of the Rings depicting its overall feel:
```

#### запись в таблицу
Переходм в [таблицу](https://docs.google.com/spreadsheets/d/1TfoaKIHMfUsHEsVoYb6w_L_g8LCfs7okDjKBKoZR4NQ/edit#gid=0) и вставляем описание в колонку prompt


### Работа над обложкой

#### виды обложек
Примерно половина обложек должна быть про объект/сеттинг, например горы или кольцо или здание, все что не персонаж/персонажи

Вторая половина про субъект/протагонист, но тут есть нюансы
* Можно создавать только портреты (так чтобы не было видно рук)
* Только один человек на портрете
* Можно создавать человека в полный рост если вид сзади. В этом случае можно пытаться сделать двоих или больше людей, пример:
```
Romantic couple in the woods, view from behind, artstation winner by victo ngai, kilian eng and by jake parker, vibrant colors, winning-award masterpiece, fantastically gaudy, aesthetic octane render, 8k hd resolution
```

#### Создание идеи
Заходим в OpenAI и используем этот prompt, его можно подкорректировать под нужды:
```
Suggest a book cover idea

Description: Twilight is a novel by Stephenie Meyer that tells the story of a young girl, Bella Swan, who falls in love with a vampire, Edward Cullen. The novel explores the themes of love, death, and immortality.
Book cover: Portrait of Kristen Stewart with long hair

Description: The Hitchhiker's Guide to the Galaxy is a novel by Douglas Adams that tells the story of a group of friends who travel through the universe in search of the meaning of life. The novel explores the themes of friendship, adventure, and discovery.
Book cover: A spaceship flying through a bright, colorful galaxy

Description: Ваше описание книги

Book Cover:
```


#### Создание обложки
1. Переходим в [lexica.art](lexica.art) или другой подобный ресурс, и ищем там референсы к вашей идее для обложки
2. Заходим в [dreamstudio](https://beta.dreamstudio.ai/home) и генерим 4 картинки 512/704, если 3 из 4 картинок подходят и не "поломаны" знчит этот prompt можно сохранять в колонку completions и переходить к следующей книге
