---
name: tim-studio
description: "Единый набор из 50 скиллов — видео на HyperFrames (ролики на любую тему, объяснялки, субтитры, музыкальные клипы, промо), дизайн сайтов и интерфейсов (impeccable, taste-skill, редизайн, брендкиты, прототипы), анимации UI (Emil Kowalski), Swift. Использовать для ЛЮБОЙ задачи про видео, моушн-графику, анимацию, дизайн сайта/приложения/UI, лендинги, бренд, интерфейсную анимацию или Swift. Команды: «/tim-studio видео <тема>», «/tim-studio сайт <описание>», «/tim-studio анимация <что>», «/tim-studio дизайн-аудит <путь>»."
argument-hint: "[видео|сайт|анимация|аудит|бренд|...] <тема или задача>"
user-invocable: true
---

# Tim Studio — все скиллы в одном

Запрос: **$ARGUMENTS**

Это «зонтичный» скилл. Внутри папки `skills/` лежат 50 оригинальных скиллов целиком.
Сам по себе этот файл — только маршрутизатор.

## Как работать
1. По запросу выбери 1–3 подходящих скилла из таблицы ниже (по разделу и колонке «Когда»).
2. **Прочитай их `skills/<имя>/SKILL.md` полностью** (Read) и дальше следуй им как основным инструкциям.
3. Все относительные пути внутри под-скилла (`references/…`, `scripts/…`, `assets/…`) считаются
   от папки этого под-скилла: `<папка tim-studio>/skills/<имя>/`. Если под-скилл пишет
   `.claude/skills/<имя>/…` — подставляй `<папка tim-studio>/skills/<имя>/…`.
4. Если под-скилл ссылается на другой скилл по имени (например, «загрузи hyperframes-animation»),
   читай `skills/<то-имя>/SKILL.md` отсюда же.
5. Не грузи всё подряд — только нужное под задачу.

## Быстрые маршруты
- **«видео / ролик про <тему>»** → `video` (полный пайплайн: факты → сценарий → озвучка → HyperFrames → рендер),
  затем по ходу `hyperframes`, `hyperframes-animation`, `hyperframes-creative`, `media-use`.
- **объяснялка без лица из текста/статьи** → `faceless-explainer`.
- **субтитры к видео** → `embedded-captions`. **Нарезка интервью / говорящая голова** → `talking-head-recut`.
- **клип под музыку** → `music-to-video`. **Промо продукта / сайта** → `product-launch-video`. **Слайд-шоу** → `slideshow`.
- **сайт / лендинг с нуля** → `impeccable` (+ `design-taste-frontend` для вкуса, `high-end-visual-design`).
- **переделать существующий сайт** → `redesign-existing-projects` + `impeccable` (audit/polish).
- **стиль: минимализм** → `minimalist-ui`; **брутализм** → `industrial-brutalist-ui`; **как у Apple** → `apple-design`.
- **картинка-макет → код** → `image-to-code`; **макеты экранов картинками** → `imagegen-frontend-web` / `imagegen-frontend-mobile`.
- **логотип / брендбук** → `brandkit`. **Несколько вариантов UI на выбор** → `prototype`.
- **анимация в интерфейсе** → `animate` (React Native — `animate-expo`), ревью — `review-animations`,
  где добавить анимацию — `find-animation-opportunities`, как это называется — `animation-vocabulary`.
- **проверить UI на кривых данных** → `break-ui`. **Выбрать библиотеку** → `pick-ui-library`. **Тосты** → `ask-sonner`.
- **сайт как приложение на телефоне** → `mobile-native`. **Swift** → `write-swift`.
- **длинный код без обрезаний** → `full-output-enforcement`.

## Требования окружения
- Видео: Node 18+ (`npx hyperframes …`), `ffmpeg` (macOS: `brew install ffmpeg`), Chrome скачивается сам.
- `impeccable`: лаунчер `skills/impeccable/scripts/impeccable` сам скачивает бинарник при первом запуске.
- В claude.ai (веб/телефон) без терминала видео не отрендерить — там пиши сценарий, код композиции
  и дизайн; рендер делай в Claude Code на компьютере.

## Все скиллы

### 🎬 Видео (HyperFrames)

| Скилл | Когда |
|---|---|
| `video` | Делает анимированное видео (HyperFrames + GSAP + CSS 3D) на заданную тему — от сбора фактов и сценария до рендера mp4. |
| `hyperframes` | Mandatory entry point: read this first for any request to make, create, edit, animate, or render a video, animation, or motion graphic, including a promo, explainer, captioned clip, title card, overlay, slideshow or inte… |
| `hyperframes-core` | The HyperFrames composition contract — build one renderable project. |
| `hyperframes-cli` | Use the HyperFrames CLI development loop: init, add, catalog, capture, lint, check, snapshot, compare, grade-compare, preview, play, present, beats, keyframes, single or batch render, publish, cloud, cloudrun, feedback, … |
| `hyperframes-animation` | All animation knowledge for HyperFrames — atomic motion rules, multi-phase scene blueprints, scene transitions, broader motion-design techniques, AND the seven runtime adapters (GSAP default, plus Lottie, Three.js, Anime… |
| `hyperframes-keyframes` | Use when a HyperFrames composition needs a punch-in, punch-out, zoom, reframe, Ken Burns treatment, camera move, visual match/whip handoff, or other seek-safe 2D/3D keyframes; also for GSAP, CSS keyframes, Anime.js, WAAP… |
| `hyperframes-creative` | Non-animation creative direction for HyperFrames videos. |
| `hyperframes-audio` | Use when audio already placed in a HyperFrames composition needs to be mixed: fade-in/fade-out, crossfade, track gain or volume, volume automation, ducking, a music bed that fights a voiceover (voiceover carve), effects … |
| `hyperframes-registry` | Search, install, and wire registry blocks and components into HyperFrames compositions. |
| `hyperframes-studio` | Use when working with a person on a HyperFrames project in Studio: first, whether their message asks for a change at all (questions, loose ideas and "don't change anything" get an answer and a plan, not an edit); for a n… |
| `media-use` | Agent Media OS, the single skill for every media need in a HyperFrames project. |
| `motion-graphics` | A short, design-led motion graphic where motion is the message — kinetic typography, stat count-up, chart/data-viz hit, logo sting / brand lockup, lower-third / callout / social overlay, animated map (highlight regions, … |
| `general-video` | Author or edit a custom HyperFrames composition when no specialized workflow fits, or when BRIEF.md sets flow: companion. |
| `faceless-explainer` | Turn arbitrary text — an article, notes, a topic, a brief — into a faceless explainer video: there is no site or footage to capture, so the visuals are invented per scene (typography, abstract graphics, diagrams, data-vi… |
| `slideshow` | Author a HyperFrames slideshow — a presentation, pitch deck, or interactive deck with discrete slides, fragment reveals, branching, hotspot navigation, and built-in presenter mode with speaker notes; also converts an exi… |
| `embedded-captions` | Add captions or subtitles to an existing single-subject talking-head video without editing the footage. |
| `talking-head-recut` | Package an existing talking-head / interview / podcast video with timed, designed GRAPHIC OVERLAY cards — kinetic titles, lower-thirds, data callouts, quotes, side panels, picture-in-picture — synced to the transcript, o… |
| `music-to-video` | Turn a music track (an audio file, a video to pull audio from, or a track generated from a mood brief) into a beat-synced video — lyric video, slideshow, or kinetic promo. |
| `product-launch-video` | Turn a product or marketing URL, pasted script, or brief into a product launch / promo video — SaaS promos, feature reveals, product demos, app and company launches. |
| `pr-to-video` | Turn a GitHub pull request (a PR URL, owner/repo#N, or 'this PR' in a checked-out repo) into a code-change explainer video — changelog, feature reveal, fix, or refactor walkthrough built from the diff, commits, and files… |
| `figma` | Import Figma content into a HyperFrames composition — rendered assets, brand tokens, components, storyboard sections → reconstructed motion (frames read as states, not slides) (REST/CLI), connector-assisted motion when a… |
| `remotion-to-hyperframes` | Port an existing Remotion (React) composition''s source to HyperFrames HTML. |

### 🎨 Дизайн сайтов и интерфейсов

| Скилл | Когда |
|---|---|
| `impeccable` | Use when the user wants to design, redesign, shape, critique, audit, polish, clarify, distill, harden, optimize, adapt, animate, colorize, extract, or otherwise improve a frontend interface. |
| `design-taste-frontend` | Anti-slop frontend skill for landing pages, portfolios, and redesigns. |
| `design-taste-frontend-v1` | The original v1 taste-skill, preserved for projects depending on its exact behavior. |
| `gpt-taste` | Elite UX/UI & Advanced GSAP Motion Engineer. |
| `high-end-visual-design` | Teaches the AI to design like a high-end agency. |
| `minimalist-ui` | Clean editorial-style interfaces. |
| `industrial-brutalist-ui` | Raw mechanical interfaces fusing Swiss typographic print with military terminal aesthetics. |
| `redesign-existing-projects` | Upgrades existing websites and apps to premium quality. |
| `stitch-design-taste` | Semantic Design System Skill for Google Stitch. |
| `image-to-code` | Elite website image-to-code skill for Codex. |
| `imagegen-frontend-web` | Elite frontend image-direction skill for generating premium, conversion-aware website design references. |
| `imagegen-frontend-mobile` | Elite mobile app image-generation skill for creating premium, app-native screen concepts and flows. |
| `brandkit` | Premium brand-kit image generation skill for creating high-end brand-guidelines boards, logo systems, identity decks, and visual-world presentations. |
| `prototype` | Build multiple genuinely different versions of a UI piece you describe, rendered behind a visual picker so you can flip through them live and promote the one that feels right. |
| `pick-ui-library` | Pick the right library for a given frontend task from a curated, opinionated list — numbers, OTP inputs, charts, command menus, virtualization, drag and drop, toasts, state, styling, and more. |
| `break-ui` | Try to break a piece of UI by feeding it worst-case data — long names, unbreakable emails, one-letter names, missing fields, huge counts, zero items, long labels, non-Latin text, emoji, extreme numbers — then render it b… |
| `mobile-native` | Make a web app feel native on a phone — the small CSS and meta-tag fixes that separate "a website in a browser" from something that feels installed. |
| `apple-design` | Apple's approach to interface design and fluid, physical motion, translated for the web. |
| `emil-design-eng` | This skill encodes Emil Kowalski's philosophy on UI polish, component design, animation decisions, and the invisible details that make software feel great. |
| `full-output-enforcement` | Overrides default LLM truncation behavior. |

### ✨ Анимации в UI

| Скилл | Когда |
|---|---|
| `animate` | Build an animation from scratch, making the decisions in the order that determines whether it feels right — should it animate at all, what purpose, which tool, which properties, which curve and duration, how it interrupt… |
| `animate-expo` | Build animations in React Native and Expo, making the decisions in the order that determines whether they feel right — should it animate, which thread it runs on, which properties, spring or timing, how the gesture hands… |
| `animation-vocabulary` | Reverse-lookup glossary that turns a vague description of a web animation or motion effect into its exact term ("the bouncy thing when a popover opens" → Pop in; "the iOS rubber-band scroll" → Rubber-banding). |
| `find-animation-opportunities` | Search a codebase or UI for places that don't animate but should, and reject everything that shouldn't. |
| `improve-animations` | Survey a codebase's animation and motion code as a senior motion advisor, then produce a prioritized audit and self-contained implementation plans for other agents (or cheaper models) to execute. |
| `review-animations` | Reviews animation and motion code against a high craft bar derived from Emil Kowalski's design engineering philosophy. |
| `ask-sonner` | Guide to Sonner, the React toast library — install and wire up the Toaster, pick the right toast() call, promise and loading toasts, updating, dismissing and persisting toasts, styling, theming and icons, positioning and… |

### 📱 Swift / iOS

| Скилл | Когда |
|---|---|
| `write-swift` | How to write modern Swift well — modeling with value types, Swift 6 data-race safety and approachable concurrency (@concurrent, main-actor-by-default, actors, task groups), protocols and generics (some vs any), API desig… |

Источники и версии оригиналов — `skills/SOURCES.json`.
