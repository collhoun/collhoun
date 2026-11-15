<h1 align="center">Привет, я Ярослав 👋</h1>

<h3 align="center">Студент МАИ • Ищу стажировку в Data Science, ML или Data Analytics</h3>

<p align="center">
  <img src="https://img.shields.io/badge/Формат-Стажировка%20%2F%20Part--time-blue?style=flat-square" />
  <img src="https://img.shields.io/badge/Занятость-20--40%20ч%2Fнеделю-blue?style=flat-square" />
  <img src="https://img.shields.io/badge/Курс-2%20курс%20МАИ-blue?style=flat-square" />
</p>

---

### 🧠 Обо мне

Студент 2 курса **МАИ** (Прикладная математика и информатика, профиль — программная инженерия систем машинного обучения, ТОП ИТ). Средний балл **4.4**.

Ищу **стажировку или part-time в Data Science, Machine Learning или Data Analytics**. В проектах занимаюсь анализом данных, строю ML-модели и работаю над их внедрением.

- 📊 **Аналитика данных** — EDA, SQL, моделирование данных и аналитические витрины
- 🔁 **ML-пайплайны** — подготовка данных, обучение и валидация моделей
- ⚙️ **MLOps** — API, контейнеризация и тестирование

Дополнительно знаком с разработкой **AI-агентов** на практике. Работал с асинхронной клиентской библиотекой, подключал инструменты и настраивал трейсинг LLM-вызовов.

---

### 🚀 Проекты

#### 🚚 [Отгрузки без простоев — прогноз для логистики RWB](https://github.com/L3iHS/rwb-shipment-forecasting) — *ML Engineer*
На кейс-чемпионате RWB вместе с командой разработали прогноз объёма отгрузок для **1 000 маршрутов на 4 часа вперёд** с шагом 30 минут. На основе прогноза собрали прототип пульта диспетчера, который подсказывает, когда вызвать машину на склад.

- **Инициировал применение градиентного бустинга и ансамблирование бустингов.** Вместе с командой обсуждал подходы к задаче и гипотезы для проверки, использовал ИИ-инструменты при проработке и реализации решений.
- **Командное решение** учитывало, что к моменту прогноза первая половина ближайшего часового окна уже известна. Отдельно прогнозировали объём на оставшиеся полчаса. Финальный ансамбль объединил XGBoost, два варианта LightGBM (Huber и Tweedie) и MLP. Он набрал **0,323 на лидерборде** по метрике `WAPE + |Relative Bias|`.
- **Эксперимент с Chronos-2.** Проверили предобученную модель для временных рядов в zero-shot-режиме. На валидации Chronos-2 получила **0,355** по `WAPE + |Relative Bias|`: лучше среднего за 7 дней (**0,384**), но хуже градиентного бустинга (**0,328**).

> 🥈 **2 место из 10 команд**. Вышли в финал и уступили команде-победителю.

**Стек:** `Python` `XGBoost` `LightGBM` `CatBoost` `PyTorch`

---

#### 🏬 [Аналитическая платформа маркетплейса](https://github.com/L3iHS/RWB-marketplace-model) — *Data Analyst / Data Architect*
В составе команды на хакатоне RWB спроектировал аналитическую платформу на данных маркетплейса (Olist): 550 тыс. записей из 8 источников, ~99 тыс. заказов, архитектура **raw → core → mart** (13 таблиц ядра, 7 витрин). Отвечал за стратегию развития продукта и ключевые архитектурные решения команды — реализация при этом велась в формате вайб-кодинга с активным использованием AI-инструментов.

- Провёл разведывательный анализ данных (EDA), который лёг в основу SQL-модели
- Спроектировал полный пайплайн обработки данных — от загрузки сырых снимков до публикации витрин, предложил шедулер для регулярного обновления данных
- Определил стратегию масштабирования: последовательный переход от полных снимков к инкрементальной загрузке, предрасчитанным витринам и партиционированию, а при существенном росте аналитической нагрузки — к ClickHouse и брокерам сообщений
- Реализованы транзакционная публикация версий данных, защита от повторной загрузки, историзация категорий товаров и адресов заказов, 28 автоматических проверок целостности
- Построены REST API и интерактивный дашборд на React/TypeScript с согласованными показателями, фильтрами и версионируемыми CSV-выгрузками

> 🏆 **2 место из 24 команд** на хакатоне RWB

**Стек:** `Python` `SQL` `PostgreSQL` `Docker Compose` `Caddy`

---

#### 📊 [Система мониторинга стресса ликвидности](https://github.com/collhoun/psb_case) — *Team Lead*
Возглавлял команду разработки системы раннего предупреждения аномалий на рублёвом денежном рынке (Школа МАИ & Финуниверситета). Разработал ML-пайплайн (Unsupervised Learning) для поиска скрытых макроэкономических паттернов, спроектировал интерпретируемый композитный индекс **LSI** (Liquidity Stress Index, 0–100) и интерактивный дашборд.

🏆 **1 место** среди всех кейсов школы, оценка подтверждена жюри ПСБ — [диплом](https://github.com/collhoun/psb_case/blob/main/docs/диплом.pdf)

**Отдел казначейства ПСБ** взял наше решение за основу для внедрения в инфраструктуру банка.

**Стек:** `Python` `Pandas` `Scikit-learn` `NumPy` `Matplotlib` `Streamlit`

---

#### 🏭 [Production-Ready ML Pipeline & Serving Service](https://github.com/collhoun/Full-ML-pipeline) — *MLOps / ML Engineer*
Полный MLOps-цикл для ML-модели на датасете Ames Housing (2212 место, 0.13819 score) — от EDA до контейнеризированного REST API.
- Рефакторинг исследовательского кода в продакшн-модули: кастомные Scikit-learn-совместимые трансформеры (fit/transform) с ООП-архитектурой
- CatBoost снизил MAPE с 12.7% до 10%, устойчивая обработка неизвестных категорий на инференсе
- Юнит-тесты на **PyTest**, бэкенд на **FastAPI** с валидацией через **Pydantic**, упаковка в **Docker**

**Стек:** `Python` `Scikit-learn` `CatBoost` `FastAPI` `PyTest` `Docker` `Pandas` `Pydantic` `Git Flow`

---

#### 🧩 [Клиентская библиотека для AI-агентов](https://github.com/collhoun) — *дополнительный проект*
Работал над асинхронной библиотекой для управления AI-агентами со стримингом ответов и обработкой ошибок. Интегрировал внешний инструментарий агентов через **Composio**, настроил трейсинг и мониторинг LLM-вызовов через **Langfuse**.

> В демо агент извлёк субтитры из плейлиста на 75 видео YouTube и собрал единый Markdown-файл на ~10 000 строк. Весь пайплайн обошёлся менее чем в 10 центов на DeepSeek V4.

**Стек:** `Python` `Asyncio` `Langfuse` `Composio` `REST API`

---

### 🏅 Достижения

- 🥈 **2 место из 10 команд** на кейс-чемпионате — прогноз отгрузок для логистики RWB (2026)
- 🥈 **2 место из 24 команд** на хакатоне RWB — аналитическая платформа маркетплейса (2026)
- 🥈 Полуфиналист хакатона от **ПСБ** — интеллектуальная система обработки входящей корреспонденции (2025)
- 🥇 **1 место** в кейсе от ПСБ по разработке системы раннего предупреждения LSI — лучший результат среди всех команд школы (2026)

### 📚 Дополнительное образование

- [Основы статистики — Stepik](https://stepik.org/cert/3305941)
- [Classic ML — Stepik](https://stepik.org/cert/3316020)

---

### 🛠️ Технологии

**Языки:** ![Python](https://img.shields.io/badge/-Python-3776AB?style=flat-square&logo=python&logoColor=white) ![C](https://img.shields.io/badge/-C-A8B9CC?style=flat-square&logo=c&logoColor=white) ![SQL](https://img.shields.io/badge/-SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white)

**Data Science:** ![NumPy](https://img.shields.io/badge/-NumPy-013243?style=flat-square&logo=numpy&logoColor=white) ![Pandas](https://img.shields.io/badge/-Pandas-150458?style=flat-square&logo=pandas&logoColor=white) ![Matplotlib](https://img.shields.io/badge/-Matplotlib-11557C?style=flat-square) ![scikit-learn](https://img.shields.io/badge/-scikit--learn-F7931E?style=flat-square&logo=scikit-learn&logoColor=white)

**MLOps / DevOps:** ![Docker](https://img.shields.io/badge/-Docker-2496ED?style=flat-square&logo=docker&logoColor=white) ![Git](https://img.shields.io/badge/-Git-F05032?style=flat-square&logo=git&logoColor=white) ![FastAPI](https://img.shields.io/badge/-FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white) ![CI/CD](https://img.shields.io/badge/-CI%2FCD-2088FF?style=flat-square&logo=githubactions&logoColor=white)

**AI/LLM:** ![Langfuse](https://img.shields.io/badge/-Langfuse-black?style=flat-square) ![Composio](https://img.shields.io/badge/-Composio-black?style=flat-square)

---

### 📫 Контакты

<p align="left">
  <a href="https://t.me/chupappo"><img src="https://img.shields.io/badge/Telegram-@chupappo-26A5E4?style=flat-square&logo=telegram&logoColor=white" /></a>
  <a href="mailto:2904yr@mail.ru"><img src="https://img.shields.io/badge/Email-2904yr%40mail.ru-D14836?style=flat-square&logo=gmail&logoColor=white" /></a>
</p>

<p align="left"><i>🇬🇧 English — Upper-Intermediate (B2) · Открыт к стажировкам и part-time в DS, ML и Data Analytics</i></p>
