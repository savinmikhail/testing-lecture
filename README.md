# Testing Lecture

## 1. **Introduction to Testing**
- Зачем писать тесты?
    - Ускорение рефакторинга.
    - Минимизация багов.
    - Документация поведения кода.
    - Code lens
      -  [Dependency Elimination](https://qualityisspeed.blogspot.com/2014/09/beyond-solid-dependency-elimination.html).
      - Auth::id()
---

## 2. **Practical Testing in PHP**
- Примеры инструментов:
  - **[PHPUnit](https://github.com/sebastianbergmann/phpunit)**: Базовый инструмент для модульного тестирования.
  - **[Codeception](https://github.com/Codeception/Codeception)**: Подходит для E2E и интеграционного тестирования.
  - **[Pest](https://github.com/pestphp/pest)**: Современный и лаконичный фреймворк для тестирования.
  - **[Faker](https://github.com/fzaninotto/Faker?tab=readme-ov-file#basic-usage)**: Генерация тестовых данных.
  - **[Infection](https://infection.github.io/)**: Мутационное тестирование.
- [AAA pattern](https://semaphoreci.com/blog/aaa-pattern-test-automation)
- Fixtures
---

## 3. **Unit vs Integrated Tests**
- Unit-тесты:
  - Тестирование одного законченного элемента: функции, метода, класса.
  - **In-process**: Не взаимодействуют с внешними зависимостями (база данных, файлы).
  - Все зависимости замоканы или застабаны.
- Интеграционные тесты:
  - Проверка взаимодействия между компонентами системы.
  - Проверяют связь между реальными зависимостями.
- Ссылки на статьи:
  - [Integrated Tests Are a Scam](https://blog.thecodewhisperer.com/permalink/integrated-tests-are-a-scam).
- e2e

---

## 4. **Stubs vs Mocks (Test Doubles)**
- State vs behavior
- Разница между Stub и Mock:
    - **Stub**: Заглушка, возвращающая предсказуемый результат (фокус на данных).
    - **Mock**: Проверяет вызовы (фокус на поведении).
- Подходы к тестированию:
    - **Classical**: Использует Stubs, акцент на проверке конечного результата.
    - **Mockist**: Использует Mocks, проверяя взаимодействие объектов.
- Ссылки на статьи:
    - [Mocks Aren't Stubs](https://martinfowler.com/articles/mocksArentStubs.html).
    - [Classical vs. Mockist Testing](https://martinfowler.com/articles/mocksArentStubs.html#ClassicalAndMockistTesting).
- Usage (awkward to work with/ actually testing behavior)
- [Специфика](https://github.com/dg/bypass-finals) тестирование финальных классов

---

## 5. **Test-Driven Development (TDD)**
- Принципы TDD:
  - **Red** (Написание провального теста).
  - **Green** (Реализация функциональности, чтобы тест прошёл).
  - **Refactor** (Оптимизация кода без изменения поведения).
- Применимость:
  - Выделенный домен

---

## 6. **Metrics**

### Code Coverage
- Что такое покрытие тестами?
    - **Логическое покрытие**: Все ли ветки кода проверены?
    - Почему 100% покрытия не означает отсутствие багов.
- Инструменты:
    - PHPUnit Coverage Report.

### Mutation Score Indicator (MSI)
- Что это такое:
    - MSI показывает, насколько ваши тесты эффективны в нахождении багов.
    - Использует мутационное тестирование.
- Инструмент:
    - [Infection](https://infection.github.io/).

---
