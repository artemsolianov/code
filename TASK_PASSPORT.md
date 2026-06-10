# Паспорт задачи: Рекламная воронка SAVVY KID

## Проект
**SAVVY KID** — мобильное приложение для родителей детей с ADHD.  
Помогает превращать сложное поведение (импульсивность, невнимательность, вспышки эмоций) в суперспособности ребёнка через геймифицированные упражнения.

---

## Задача
Создать **рекламную воронку (quiz funnel)** на платформе **FunnelFox** из 30 экранов.  
Каждый экран вставляется как **Raw HTML** в отдельный шаг FunnelFox.

---

## Дизайн-система

| Параметр | Значение |
|---|---|
| Шрифт | Figtree (Google Fonts) — 400/500/600/700/800/900 |
| Основной акцент | `#EE942A` (оранжевый) |
| Кнопки CTA | `#5B6BF5` (синий/индиго) |
| Фон quiz-экранов | `#FFFFFF` |
| Фон info-экранов | `#FFF8F0` (тёплый бежевый) |
| Основной текст | `#262528` |
| Второстепенный текст | `rgba(38,37,40,0.55)` |
| Карточки вариантов | `#F8F7F5` |
| Прогресс-бар | `#EE942A` |

---

## Типы экранов

### 1. Quiz-экран (вопрос)
- Прогресс-бар сверху (оранжевый)
- Кнопка «назад» (круглая, серая)
- Заголовок вопроса (22px, 800)
- Карточки ответов: иконка-эмодзи + текст, фон `#F8F7F5`, hover — синяя рамка
- Без кнопки CTA — клик по карточке = переход

### 2. Info-экран (обучающий)
- Фото сверху (высота 240px)
- Белая карточка с закруглёнными углами 28px снизу наезжает на фото (margin-top: -24px)
- Заголовок с оранжевым выделением ключевого слова (`.hi { color: #EE942A }`)
- Текст body: `rgba(38,37,40,0.60)`, 14px
- Синяя кнопка CTA внизу

### 3. Photo-grid экран
- Сетка 2×2 (или 2×1 для гендера)
- Квадратные карточки с фото + подпись снизу
- Hover — синяя рамка

### 4. Multi-select экран
- Карточки с чекбоксом справа
- Серая кнопка «Continue» внизу (ghost style)

### 5. Testimonial экран
- Бейдж «Trusted by…»
- Большие кавычки оранжевым `"`
- Цитата 22px bold
- Аватар + имя + должность
- Рейтинг ★★★★★ оранжевый

### 6. Analyzing (финальный loader)
- Фото женщины с телефоном сверху
- Заголовок «Analyzing your answers»
- 3 прогресс-бара (синие): Behavioral Insights 100%, Custom Plan 28%, Parenting Blueprint 0%

---

## Все 30 экранов — порядок и тип

| # | Тип | Содержание |
|---|---|---|
| 1 | Hero | 3 iPhone mockups + "We help turn big feelings..." + прогресс 100% + кнопка "Get the Plan" |
| 2 | Photo-grid | Who are you to the child? (Mom / Dad / Grandparents / Other caregiver) |
| 3 | Photo-grid | How old is your child? (Under 6 / 6–8 / 9–11 / 12+) |
| 4 | Photo-grid | Choose the gender (Boy / Girl) |
| 5 | Info | ADHD shows up differently in boys and girls (сравнительная таблица Boys vs Girls) |
| 6 | Quiz | Is it hard for your child to focus? (3 варианта) |
| 7 | Info | Help your child stay focused — app screenshot Organization & Planning |
| 8 | Quiz | How often does your child have tantrums? (4 варианта) |
| 9 | Info | Help your kids overcome tantrums — app screenshot Tantrums Tamed |
| 10 | Quiz | Has your kid been diagnosed with ADHD? (4 варианта) |
| 11 | Quiz | Does your child take medication? (4 варианта) |
| 12 | Quiz | Does your child work with a therapist? (3 варианта) |
| 13 | Testimonial | Teresa Jonson quote — "15 minutes = regular therapy in 1 month" |
| 14 | Quiz | Does managing hyperactivity leave you drained? (3 варианта) |
| 15 | Quiz | Is it difficult to manage energy in public? (3 варианта) |
| 16 | Info | You are already the best parent (3 чекбокса) + фото мамы с ребёнком |
| 17 | Quiz | Traditional parenting advice doesn't work? (3 варианта) |
| 18 | Info | ADHD brings incredible strengths + фото мальчика с доской |
| 19 | Multi-select | Creativity areas: Art / Storytelling / Problem-solving / Humor / Building |
| 20 | Testimonial | Dr. Gabor Maté quote — "Kids with ADHD are highly intuitive…" |
| 21 | Multi-select | When is child most filled with energy? (6 вариантов) |
| 22 | Info | Energy is child's greatest resource + фото прыгающего мальчика |
| 23 | Quiz | Does child show signs of empathy? (3 варианта) |
| 24 | Info | ADHD and Empathy: A Heartfelt Superpower + фото двух мальчиков |
| 25 | Quiz | Child thinking/speaking quickly? (3 варианта) |
| 26 | Quiz | Unique solutions to problems? (3 варианта) |
| 27 | Info | Kids think in nonlinear and creative ways + фото девочки с пазлом |
| 28 | Quiz | In what way is child curious? (3 варианта) |
| 29 | Info | Curiosity: The Power to Explore + фото мальчика с водой |
| 30 | Analyzing | Прогресс-бары + фото женщины с телефоном |

---

## Изображения (для загрузки в CDN/FunnelFox)

| Файл | Используется на |
|---|---|
| `Gabor.png` | Экран 20 — аватар Dr. Gabor Maté |
| `Teresa.png` | Экран 13 — аватар Teresa Jonson (CHADD therapist) |
| `1e97451b...jpeg` (×2) | Мальчик наливает воду — экран 29 |
| `2acb2259...jpeg` | Папа с мальчиком — экран 3 или hero |
| `31ed3005...jpeg` | Мальчик с маркером и доской — экран 18 |
| `55b49aeb...jpeg` | Девочка с пазлом — экран 27 |
| `5cf90f46...jpeg` | Мама с ребёнком (мальчик с руками вверх) — экран 22 |
| `b898f0d2...jpeg` | Мама с ребёнком (тёмнокожие) — экран 16 |
| `c515e370...jpeg` | Женщина с телефоном — экран 30 |
| `cdea0cec...jpeg` | Два мальчика разговаривают — экран 24 |
| `ec10cfa5...jpg` | Мальчик прыгает с руками вверх — экран 22 |
| `image 3104.png` | iPhone mockup для Hero-экрана |
| `Mockuuups...png` | iPhone 17e mockup — референс |

---

## Текущий прогресс

- [x] Дизайн-система определена
- [x] HTML-прототип всех 30 экранов создан (`funnel-preview.html`)
- [x] Экраны обёрнуты в iPhone-рамку для просмотра
- [ ] Заменить placeholder-блоки на реальные фото
- [ ] Вытащить код каждого экрана отдельно для вставки в FunnelFox
- [ ] Добавить реальные ссылки на изображения (CDN)
- [ ] Протестировать на мобильном

---

## Технические требования для FunnelFox

- Формат вставки: **Raw HTML** (каждый экран — отдельный HTML-блок)
- Внешние зависимости: только Google Fonts (`Figtree`)
- Изображения: URL на внешний хостинг (Cloudinary, S3, или FunnelFox CDN)
- Никаких JS-фреймворков — чистый HTML+CSS
- Ширина контента: 390px max-width, центрирование через `margin: 0 auto`
- Кнопки: ссылки на следующий шаг воронки (FunnelFox подставляет автоматически)

---

## Репозиторий

- **Repo:** `artemsolianov/code`
- **Branch:** `claude/practical-lamport-qybf3o`
- **Preview file:** `funnel-preview.html`

---

## Контакт

- **Email:** artem@seneka.team
