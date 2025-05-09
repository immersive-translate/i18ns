# DeepL

## Прямой доступ к услугам перевода DeepL после открытия [Immersive Translate Pro Membership](https://immersivetranslate.com/en/pricing/) (Рекомендуется)

[Узнать больше](https://immersivetranslate.com/en/pricing/)

## Получите официальный DeepL API через DeepL

1. Официальное введение: [DeepL API](https://www.deepl.com/en/pro#developer)

   - Обратите внимание, что: [DeepL API](https://www.deepl.com/en/pro#developer) и [DeepL Pro](https://www.deepl.com/pro) — это два разных типа аккаунтов, и аккаунт [DeepL API](https://www.deepl.com/en/pro/select-country#developer).

2. [Почему](https://www.deepl.com/en/whydeepl) выбрать DeepL?

   - Английский ⇄ Китайский в 5 раз точнее
   - Английский ⇄ Японский в 6 раз точнее
   - Переводческий движок на основе технологий искусственного интеллекта (нейронные сети)

3. DeepL API делится на [Free API и Pro API](https://www.deepl.com/en/pro#developer)

   - Free API предоставляет 500,000 бесплатных символов в месяц.
   - [Официальная плата](https://www.deepl.com/en/pro#developer) за Pro API составляет: $25 за 1 миллион символов.
   - Для пользователя с высокой частотой использования количество символов, потребляемых в месяц, составляет около 10 миллионов символов, и цена составляет около: 250 USD

4. Чтобы зарегистрировать аккаунт и открыть [DeepL API](https://www.deepl.com/en/pro#developer).

## общие проблемы

### 1. Введенный ключ недоступен.

DeepL API Pro и DeepL Pro — это два разных типа аккаунтов, Auth Key, который можно использовать в Immersive Translate, — это аккаунт DeepL API, пожалуйста, нажмите здесь для [DeepL API Pro](https://www.deepl.com/en/pro/select-country#developer)

### 2. Устранение ошибок аутентификации 401, 403

Эти ошибки обычно возникают, когда вы используете неправильный тип ключа аутентификации. Обратите внимание:

1. DeepL предлагает два разных продукта: DeepL Pro (услуга перевода) и DeepL API (интерфейс для разработчиков)
2. Ключи, найденные в настройках вашего аккаунта DeepL Pro, **не совместимы** с вызовами API
3. Вам необходимо специально зарегистрироваться для аккаунта DeepL API, чтобы получить ключ API
4. Ключи DeepL Free API идентифицируются окончанием на `:fx`
5. Ключи DeepL Pro API не имеют суффикса `:fx` и выглядят как обычная строка символов

Пожалуйста, убедитесь, что вы правильно зарегистрировались для сервиса DeepL API, а не только для сервиса перевода DeepL Pro.

### 3. 456, Достигнут лимит квоты для пользователя.

Использование превысило официальный жесткий лимит DeepL на пользователя, возможно, вы нарушили политику добросовестного использования DeepL и вам рекомендуется избегать такого поведения. Если вы являетесь платным подписчиком, использование будет автоматически сброшено в следующем месяце.
