# Fernlow: a warm site for a small therapy and counselling practice with a Formgong form

**Live demo:** https://fernlow.formgong.com · Download: the [latest release](https://github.com/formgong/fernlow-template/releases/latest) zip.

[![Deploy to Cloudflare](https://deploy.workers.cloudflare.com/button)](https://deploy.workers.cloudflare.com/?url=https://github.com/formgong/fernlow-template) [![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2Fformgong%2Ffernlow-template&project-name=fernlow&repository-name=fernlow)

Each button copies the site to your GitHub and publishes it. Then replace `fk_your_access_key` in `index.html` of your copy with your Formgong access key (free at https://formgong.com/new) and commit: the host republishes on its own.

Теплий сайт для невеликої практики психотерапії та консультування з формою Formgong

A bright, one-page site for a psychotherapy or counselling practice, in a single `index.html` plus an `img/` folder. The demo practice, Fernlow Therapy, its four therapists, the reviews, the prices, the address and the phone number are fictional sample content.

- **Header.** The logo, the menu and a "Book a free intro call" button float as rounded pills over the page. On phones and tablets the menu folds into a round menu button.
- **Hero.** A full-screen photo of the therapy room with a giant "fernlow." wordmark across the bottom. The letters rise one by one, the photo settles in, and a round "Free 15-minute intro call" badge turns slowly. When you scroll, the page slides up over the photo like a sheet of paper.
- **The practice.** A large opening statement with a hand-drawn underline that draws itself, two photos (the door and the waiting nook), three short notes about access and neurodivergent-friendly sessions, and four key figures. Flat sun, fern and cloud shapes drift at their own speed.
- **What we help with.** Five numbered services: individual therapy, couples therapy, anxiety and stress, online sessions and the free 15-minute intro call. The photo on the left changes to match the service you point at. "Ask about this" picks that topic in the form.
- **How it works.** Four step cards in a stack. As you scroll, the top card lifts and flies away, the next one takes its place, and the background colour changes with each step.
- **Team.** Four therapists in arched portrait frames, with role and a one-line description.
- **Fees.** Three paper notes with tape (intro call, individual session, couples session) that straighten when you point at them, plus notes on lower-fee places and cancelling.
- **Reviews.** Four sample reviews in a sideways slider with arrows and a counter.
- **FAQ.** Six questions, including that the practice is not an emergency service.
- **Booking.** Topics as tilted paper notes, then name, email, phone, the best time to reach you and where to meet, on an envelope-style card with a stamp.
- **Footer.** Address, hours, phone, email and the line "In an emergency, call your local emergency number."

Blocks rise into view as you scroll. Without JavaScript, everything is visible and the step cards show as a plain grid. With `prefers-reduced-motion: reduce` nothing moves: no stack, no drifting shapes, no rising letters.

## English

**Set up the form**

1. Create a form in the Formgong dashboard and copy its access key.
2. In `index.html`, replace `fk_your_access_key` with that key.
3. The form sends `name`, `email`, `phone`, `service` (the topic), `time` (best time to reach you), `format` (in the room, online or either), `message` and a hidden `subject`. `name` and `email` are required; the others are optional and always have a value, so you can filter on them.
4. It shows the thank-you note only when Formgong answers `success: true`. If the answer is anything else, it shows the error message and keeps what was typed.

**Edit**

- Colours are at the top of the styles: `--paper` for the page, `--ink` for text, `--berry` for buttons and the chosen topic, `--fern` for the services section and footer, `--sun` for the fees section, and `--butter`, `--blush`, `--mint`, `--peach` for the notes and portrait frames.
- Fonts: Bricolage Grotesque for headings and the wordmark, Lexend for text, both from Google Fonts.
- The step cards are `<li class="card">` inside `.stack`. The background colours for each step are in `tones` in the script.
- Each service row has `data-pic` (which photo to show) and an "Ask about this" link with `data-topic`, which must match a topic `value` in the form.
- The flat sun, fern, leaf and cloud shapes are SVG symbols at the top of `<body>`; `data-speed` on a shape sets how fast it drifts.
- Replace the photos in `img/`, keeping the file names, or change the paths in `index.html`. Each photo has a coloured frame, so the page looks fine before the photos are added.

**Images.** The photos were generated for this template with ChatGPT image generation (OpenAI); the prompts are in `img-prompts.json`. The people and places are fictional. You may use them in your own site, but replace them with photos of your own practice and team before launch.

**Health data.** This form is for appointment requests. Don't use it to collect diagnoses, medical history, prescriptions or insurance numbers; keep those in your clinic's own patient system. The note under the message field asks people not to include medical details.

**Sample content.** The therapists, reviews, prices, address, phone number and email are examples. Replace them with your own before launch, and only publish reviews from real clients who agreed to it.

## Українська

Яскравий односторінковий сайт для практики психотерапії чи консультування: один `index.html` і папка `img/`. Практика Fernlow Therapy, чотири терапевти, відгуки, ціни, адреса й телефон вигадані, це зразок вмісту.

На сторінці:

- шапка з логотипом, меню й кнопкою «Book a free intro call», що висять над сторінкою як заокруглені плашки; на телефоні меню ховається за круглою кнопкою;
- перший екран: фото кабінету на весь екран і величезний напис «fernlow.» унизу, літери виринають по черзі, круглий значок «безкоштовний 15-хвилинний дзвінок» повільно обертається; під час прокрутки сторінка насувається на фото, як аркуш паперу;
- про практику: велике вступне речення з підкресленням, що малюється саме, два фото, три короткі примітки про доступність і зручність для нейровідмінних людей, чотири цифри; пласкі фігури сонця, папороті й хмари пливуть з різною швидкістю;
- п'ять послуг із номерами: фото ліворуч змінюється під послугу, на яку наведено курсор, а «Ask about this» вибирає цю тему у формі;
- «Як це працює»: чотири картки в стосі, під час прокрутки верхня злітає, а фон змінює колір;
- команда: чотири портрети в арках;
- ціни на трьох паперових записках зі скотчем;
- відгуки-зразки в слайдері зі стрілками;
- запитання й відповіді, зокрема що це не служба екстреної допомоги;
- форма запису: теми як нахилені паперові записки, ім'я, email, телефон, зручний час і формат зустрічі на картці-конверті з маркою;
- футер з адресою, годинами, телефоном, email і рядком «In an emergency, call your local emergency number.»

Без JavaScript увесь вміст видно, а картки кроків стоять звичайною сіткою. З `prefers-reduced-motion: reduce` нічого не рухається.

**Налаштування форми.** Створіть форму в кабінеті Formgong і замініть `fk_your_access_key` у `index.html` на свій ключ. Форма надсилає `name`, `email`, `phone`, `service` (тема), `time` (зручний час), `format` (у кабінеті, онлайн чи будь-як), `message` і приховане `subject`. Обов'язкові `name` і `email`. Подяка з'являється лише тоді, коли Formgong відповідає `success: true`; інакше форма показує помилку й не стирає введене.

**Редагування.** Кольори задано на початку стилів: `--paper` для сторінки, `--ink` для тексту, `--berry` для кнопок і вибраної теми, `--fern` для блоку послуг і футера, `--sun` для цін. Шрифти: Bricolage Grotesque для заголовків і Lexend для тексту. Кольори фону для кроків лежать у масиві `tones` у скрипті. Посилання «Ask about this» мають `data-topic`, який має збігатися з `value` теми у формі. Фото замінюйте в `img/` з тими самими назвами файлів; поки фото немає, на їхньому місці кольорові рамки.

**Зображення.** Фото згенеровано для цього шаблону в ChatGPT (OpenAI), промпти лежать у `img-prompts.json`. Люди й місця вигадані. Їх можна використовувати, але перед запуском замініть їх фото своєї практики й команди.

**Дані про здоров'я.** Ця форма лише для запису на зустріч. Не збирайте через неї діагнози, історію хвороби, рецепти чи номери страховок; зберігайте це у власній системі обліку пацієнтів. Під полем повідомлення є прохання не писати медичних подробиць.

**Зразок вмісту.** Терапевти, відгуки, ціни, адреса, телефон і email вигадані. Замініть їх своїми перед запуском і публікуйте лише відгуки реальних клієнтів, які на це погодилися.

MIT license.
