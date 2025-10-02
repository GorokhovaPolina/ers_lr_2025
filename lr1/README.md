# Translation API Comparator

Приложение для сравнения качества переводов с двух разных API.

## Описание

Этот проект реализует качественное сравнение переводов, получаемых из различных бесплатных API. Приложение предоставляет GUI интерфейс для ввода текста, выбора языков и отображения результатов сравнения переводов.

## Функциональность

- **GUI интерфейс** на PySide6 (Qt)
- **API интеграция** с LingvaTranslate и MyMemory (бесплатные, без ключей)
- **Сравнение переводов** с анализом схожести и качества
- **Множественные языки** поддержка 10+ языков
- **Тестирование** через pytest и Postman
- **Модульная архитектура** с четким разделением ответственности

## Структура проекта

```
lr1/
├── src/                    # Исходный код
│   ├── api_client/        # HTTP клиент для API переводов
│   ├── analizer/          # Модуль сравнения переводов
│   ├── gui/               # GUI интерфейс
│   ├── config.py          # Конфигурация
│   └── run_app.py         # Точка входа
├── tests/                 # Тесты
├── run.py                # Простой скрипт запуска
└── requirements.txt      # Зависимости
```

## API

Приложение использует два бесплатных API для переводов:

### LingvaTranslate
- **URL**: https://lingva.ml/api/v1
- **Тип**: GET запросы
- **Особенности**: Публичный фронтенд Google Translate, большая база данных

### MyMemory
- **URL**: https://api.mymemory.translated.net
- **Тип**: GET запросы
- **Особенности**: Быстрые переводы, большая база данных

## Поддерживаемые языки

- **Английский** (en)
- **Русский** (ru)
- **Испанский** (es)
- **Французский** (fr)
- **Немецкий** (de)
- **Итальянский** (it)
- **Португальский** (pt)
- **Японский** (ja)
- **Корейский** (ko)
- **Китайский** (zh)

## Метрики сравнения

- **Схожесть переводов** (0-100%) - насколько похожи переводы
- **Разница в длине** - разница в количестве символов
- **Разница в словах** - разница в количестве слов
- **Разница в уверенности** - разница в уверенности API
- **Оценка качества** - общая оценка качества перевода

## Тестирование

### Unit тесты:
```bash
python3 -m pytest tests/ -v
```

## Требования

- Python 3.8+
- PySide6
- requests
- python-dotenv
- pytest

## Особенности

- **Обработка ошибок**: Приложение корректно обрабатывает ошибки API
- **Статус-бар**: Показывает текущее состояние операции
- **Цветовая индикация**: Качество переводов отображается цветами
- **Множественные языки**: Поддержка 10+ языков

### Популярные фразы для тестирования:
- "Hello, how are you today?"
- "Привет, как дела?"
- "Bonjour, comment allez-vous?"
- "Hola, ¿cómo estás?"
- "Guten Tag, wie geht es dir?"
- "The scientist, who had spent decades researching the intricate mechanisms by which proteins fold into their functional conformations, published a groundbreaking paper that not only challenged long-held assumptions in molecular biology but also proposed a novel methodology for predicting folding pathways that could revolutionize drug design."
- "Despite the numerous objections raised by both critics, who questioned the validity of the experimental setup, and colleagues, who doubted the feasibility of replicating the results under different environmental conditions, the research team persisted in their efforts, meticulously documenting every step of the procedure and ultimately producing data that, although controversial, could not be ignored."
- "Hoping to circumvent the limitations imposed by traditional analytical techniques and motivated by the urgent need to address the unprecedented challenges posed by climate change, the interdisciplinary consortium, composed of climatologists, economists, and policy makers, embarked on an ambitious project to develop predictive models capable of simulating complex interactions between ecological, social, and economic systems over multiple decades."
- "If, as many skeptics suggest, the rapid proliferation of artificial intelligence technologies were to outpace the development of corresponding ethical frameworks, leading to scenarios in which autonomous systems operate without adequate human oversight, then society might find itself confronting dilemmas that are not only unprecedented in scale but also extraordinarily difficult to resolve through conventional legislative or regulatory mechanisms."
- "The notion that consciousness could emerge from purely computational processes, while appealing to proponents of strong artificial intelligence, raises profound questions regarding the ontological status of subjective experience, the limits of empirical investigation, and the philosophical distinction between functional equivalence and phenomenological reality, which philosophers and cognitive scientists continue to debate vigorously."

### Ожидаемые результаты:
- Переводы на выбранный язык
- Анализ схожести переводов
- Оценка качества каждого перевода
- Сравнение уверенности API

## Устранение неполадок

1. **Приложение не запускается**: Проверьте установку PySide6
2. **Ошибки API**: Проверьте интернет-соединение
3. **Неправильный перевод**: Проверьте правильность выбора языков
4. **Медленная работа**: API могут быть перегружены, попробуйте позже

## PEP8 Соответствие

Весь код написан в соответствии с PEP8:
- Максимальная длина строки: 88 символов
- Использование 4 пробелов для отступов
- Документация функций в стиле Google
- Явная типизация всех параметров
- Понятные названия переменных и функций
