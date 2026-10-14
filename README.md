# Tim Studio — 50 скиллов для Claude в одном

Один «зонтичный» скилл для Claude (Claude Code, claude.ai, приложение): **видео на HyperFrames**,
**дизайн сайтов и интерфейсов**, **анимации UI** и **Swift**. Внутри лежат полные копии
скиллов из четырёх открытых репозиториев и один собственный, `video`. Главный `SKILL.md` работает
как маршрутизатор: по задаче Claude выбирает 1–3 нужных под-скилла и читает только их.

## Установка

**Claude Code на любом компьютере**
```bash
npx skills add rn8mwsb6pf-alt/tim-studio -g
```
или вручную:
```bash
git clone https://github.com/rn8mwsb6pf-alt/tim-studio ~/.claude/skills/tim-studio
```

**claude.ai / Claude Desktop / телефон:** скачай `tim-studio.zip` из
[Releases](https://github.com/rn8mwsb6pf-alt/tim-studio/releases/latest), затем
Settings → Capabilities → Skills → Upload skill. Скилл появится и в приложении на телефоне.
Там нет терминала, поэтому сценарий, дизайн и код он сделает, а рендер mp4 нужно запускать в Claude Code.

**Для видео на компьютере нужны:** Node 18+ и ffmpeg (`brew install ffmpeg`). Chrome для рендера скачивается сам.

## Как пользоваться

```
/tim-studio видео Сталинградская битва, 2 минуты, 16:9, без голоса
/tim-studio видео История RSA за 30 секунд, 9:16 для Reels
/tim-studio сайт лендинг для кофейни, минимализм
/tim-studio аудит дизайна ./src
/tim-studio анимация модалки и кнопок в моём проекте
/tim-studio брендбук для барбершопа
```
Можно и без команды, обычным текстом: «сделай видео про…», «переделай дизайн сайта…».

## Что внутри — 50 скиллов

### 🎬 Видео — HyperFrames (22)

| Скилл | Что делает | Откуда |
|---|---|---|
| `video` | Мой пайплайн «видео под ключ»: факты → сценарий → озвучка → анимация → рендер mp4 | свой |
| `hyperframes` | Точка входа HyperFrames: видео из HTML + GSAP, рендер в mp4 | [heygen-com/hyperframes](https://github.com/heygen-com/hyperframes) |
| `hyperframes-core` | Устройство композиции: data-start/duration, таймлайн, клипы, сцены | [heygen-com/hyperframes](https://github.com/heygen-com/hyperframes) |
| `hyperframes-cli` | Команды CLI: init, preview, check, snapshot, render | [heygen-com/hyperframes](https://github.com/heygen-com/hyperframes) |
| `hyperframes-animation` | Вся анимация: правила движения, сцены, переходы, 3D, текст | [heygen-com/hyperframes](https://github.com/heygen-com/hyperframes) |
| `hyperframes-keyframes` | Анимация по ключевым кадрам, кривые, точный тайминг | [heygen-com/hyperframes](https://github.com/heygen-com/hyperframes) |
| `hyperframes-creative` | Арт-дирекшн: палитры, шрифты, раскадровка, дизайн-спека | [heygen-com/hyperframes](https://github.com/heygen-com/hyperframes) |
| `hyperframes-audio` | Сведение звука: фейды, громкость, приглушение музыки под голос | [heygen-com/hyperframes](https://github.com/heygen-com/hyperframes) |
| `hyperframes-registry` | Готовые блоки и компоненты из реестра HyperFrames | [heygen-com/hyperframes](https://github.com/heygen-com/hyperframes) |
| `hyperframes-studio` | Совместная работа с человеком в HyperFrames Studio | [heygen-com/hyperframes](https://github.com/heygen-com/hyperframes) |
| `media-use` | Всё про медиа: музыка, звуки, картинки, иконки, логотипы, голос | [heygen-com/hyperframes](https://github.com/heygen-com/hyperframes) |
| `motion-graphics` | Короткая моушн-графика: кинетический текст, цифры, графики, карты | [heygen-com/hyperframes](https://github.com/heygen-com/hyperframes) |
| `general-video` | Произвольное видео, когда не подходит ни один готовый сценарий | [heygen-com/hyperframes](https://github.com/heygen-com/hyperframes) |
| `faceless-explainer` | Объясняющее видео без лица по тексту, статье или теме | [heygen-com/hyperframes](https://github.com/heygen-com/hyperframes) |
| `slideshow` | Презентации и слайд-шоу с режимом докладчика | [heygen-com/hyperframes](https://github.com/heygen-com/hyperframes) |
| `embedded-captions` | Красивые субтитры к видео с говорящим человеком | [heygen-com/hyperframes](https://github.com/heygen-com/hyperframes) |
| `talking-head-recut` | Графика поверх интервью или подкаста: титры, плашки, цитаты | [heygen-com/hyperframes](https://github.com/heygen-com/hyperframes) |
| `music-to-video` | Клип под музыку: lyric video, слайд-шоу, промо в такт | [heygen-com/hyperframes](https://github.com/heygen-com/hyperframes) |
| `product-launch-video` | Промо-ролик продукта или сайта по ссылке или брифу | [heygen-com/hyperframes](https://github.com/heygen-com/hyperframes) |
| `pr-to-video` | Видео-объяснение изменений из GitHub pull request | [heygen-com/hyperframes](https://github.com/heygen-com/hyperframes) |
| `figma` | Перенос макетов и токенов из Figma в анимацию | [heygen-com/hyperframes](https://github.com/heygen-com/hyperframes) |
| `remotion-to-hyperframes` | Перенос проекта с Remotion на HyperFrames | [heygen-com/hyperframes](https://github.com/heygen-com/hyperframes) |

### 🎨 Дизайн сайтов и интерфейсов (20)

| Скилл | Что делает | Откуда |
|---|---|---|
| `impeccable` | Главный дизайн-скилл: создание, аудит, полировка, анимация, цвет и шрифты UI (30+ команд) | [pbakaus/impeccable](https://github.com/pbakaus/impeccable) |
| `design-taste-frontend` | Анти-«ИИ-шаблон» для лендингов и портфолио: сам выбирает стиль | [Leonxlnx/taste-skill](https://github.com/Leonxlnx/taste-skill) |
| `design-taste-frontend-v1` | Старая версия taste-skill (для совместимости) | [Leonxlnx/taste-skill](https://github.com/Leonxlnx/taste-skill) |
| `gpt-taste` | Продвинутая GSAP-анимация сайта + структура AIDA | [Leonxlnx/taste-skill](https://github.com/Leonxlnx/taste-skill) |
| `high-end-visual-design` | Дизайн уровня топового агентства: шрифты, отступы, тени, карточки | [Leonxlnx/taste-skill](https://github.com/Leonxlnx/taste-skill) |
| `minimalist-ui` | Минимализм в редакционном стиле, монохром, бенто-сетки | [Leonxlnx/taste-skill](https://github.com/Leonxlnx/taste-skill) |
| `industrial-brutalist-ui` | Брутализм: швейцарская типографика + эстетика терминала | [Leonxlnx/taste-skill](https://github.com/Leonxlnx/taste-skill) |
| `redesign-existing-projects` | Апгрейд существующего сайта до премиум-уровня | [Leonxlnx/taste-skill](https://github.com/Leonxlnx/taste-skill) |
| `stitch-design-taste` | DESIGN.md для Google Stitch с премиальными правилами | [Leonxlnx/taste-skill](https://github.com/Leonxlnx/taste-skill) |
| `image-to-code` | Сначала генерирует макет-картинку, потом верстает по нему | [Leonxlnx/taste-skill](https://github.com/Leonxlnx/taste-skill) |
| `imagegen-frontend-web` | Генерация макетов сайтов картинками | [Leonxlnx/taste-skill](https://github.com/Leonxlnx/taste-skill) |
| `imagegen-frontend-mobile` | Генерация макетов экранов мобильного приложения | [Leonxlnx/taste-skill](https://github.com/Leonxlnx/taste-skill) |
| `brandkit` | Брендбук: логотип, айдентика, бренд-доски | [Leonxlnx/taste-skill](https://github.com/Leonxlnx/taste-skill) |
| `prototype` | Несколько разных вариантов UI с переключателем, чтобы выбрать | [emilkowalski/skills](https://github.com/emilkowalski/skills) |
| `pick-ui-library` | Подбор библиотеки под задачу: графики, OTP, меню, таблицы | [emilkowalski/skills](https://github.com/emilkowalski/skills) |
| `break-ui` | Проверка интерфейса на худшие данные: длинные имена, пустые поля | [emilkowalski/skills](https://github.com/emilkowalski/skills) |
| `mobile-native` | Чтобы сайт на телефоне ощущался как приложение | [emilkowalski/skills](https://github.com/emilkowalski/skills) |
| `apple-design` | Подход Apple к интерфейсам и «физичной» анимации жестов | [emilkowalski/skills](https://github.com/emilkowalski/skills) |
| `emil-design-eng` | Философия Emil Kowalski: полировка, компоненты, мелкие детали | [emilkowalski/skills](https://github.com/emilkowalski/skills) |
| `full-output-enforcement` | Запрет обрезать код и писать заглушки | [Leonxlnx/taste-skill](https://github.com/Leonxlnx/taste-skill) |

### ✨ Анимации в интерфейсе (7)

| Скилл | Что делает | Откуда |
|---|---|---|
| `animate` | Анимация с нуля: нужна ли она, тип, кривая, длительность | [emilkowalski/skills](https://github.com/emilkowalski/skills) |
| `animate-expo` | То же для React Native / Expo | [emilkowalski/skills](https://github.com/emilkowalski/skills) |
| `animation-vocabulary` | Словарь: по описанию «та прыгающая штука» даёт точный термин | [emilkowalski/skills](https://github.com/emilkowalski/skills) |
| `find-animation-opportunities` | Ищет в проекте места, где не хватает анимации | [emilkowalski/skills](https://github.com/emilkowalski/skills) |
| `improve-animations` | Аудит всей анимации проекта + план улучшений | [emilkowalski/skills](https://github.com/emilkowalski/skills) |
| `review-animations` | Строгое ревью кода анимаций | [emilkowalski/skills](https://github.com/emilkowalski/skills) |
| `ask-sonner` | Тосты-уведомления на React (Sonner) | [emilkowalski/skills](https://github.com/emilkowalski/skills) |

### 📱 Swift / iOS (1)

| Скилл | Что делает | Откуда |
|---|---|---|
| `write-swift` | Современный Swift 6: типы, конкурентность, стиль | [emilkowalski/skills](https://github.com/emilkowalski/skills) |

## Как устроено

```
SKILL.md            ← маршрутизатор (выбирает под-скиллы)
skills/<имя>/       ← оригинальные скиллы целиком (SKILL.md, references, scripts, assets)
skills/SOURCES.json ← откуда и какой версии взят каждый скилл
licenses/           ← лицензии оригиналов
```
Удалён только 14-мегабайтный бинарник `impeccable` для macOS: лаунчер
`skills/impeccable/scripts/impeccable` скачивает его сам при первом запуске.

## Лицензии и авторы

Это сборка чужих открытых проектов. Все права принадлежат их авторам:
- [heygen-com/hyperframes](https://github.com/heygen-com/hyperframes): Apache-2.0, 21 скилл про видео
- [pbakaus/impeccable](https://github.com/pbakaus/impeccable): Apache-2.0, `impeccable`
- [Leonxlnx/taste-skill](https://github.com/Leonxlnx/taste-skill): MIT, 13 дизайн-скиллов
- [emilkowalski/skills](https://github.com/emilkowalski/skills): MIT, 14 скиллов про анимацию и UI

Тексты лицензий лежат в [`licenses/`](licenses/). Скилл `video` и маршрутизатор написаны для этой сборки.
