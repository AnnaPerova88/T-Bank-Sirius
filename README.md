# T-Bank-Sirius
NLP
## Описание проекта

Данный проект представляет собой реализацию русскоязычной системы вопросов и ответов (QA System), обученной на аннотированном датасете **Sberquad**. Система построена на основе современных методов машинного обучения и позволяет находить ответы на вопросы, используя заранее созданную базу знаний.

Проект включает:

- Тренировку/настройку модели с использованием датасета Sberquad.
- Реализацию сервиса на Flask, который развёрнут в Docker для удобства проверки.
- Вариант создания телеграм-бота для взаимодействия с пользователями.
- Поддержку различных подходов к решению задачи QA (information retrieval, encoder-decoder, поиск start/end токенов и др.).

## Архитектура решения

Для решения задачи были использованы следующие методы:

1. **Information retrieval + ranking**: Для поиска наиболее релевантных ответов на основе заданных вопросов.
2. **Encoder-decoder models (T5)**: Использование моделей типа T5 для генерации и обработки текста.
3. **Поиск start/end токенов**: Для нахождения ответа в пределах вопроса.
4. **Валидация на основе Sberquad**: Контекст из Sberquad был использован в качестве базы знаний для обучения модели.

## Стек технологий

- Python 3.8+
- TensorFlow / PyTorch (в зависимости от выбранного подхода)
- Flask
- Docker
- Telegram API (если выбран вариант с телеграм-ботом)

## Как запустить проект

1. **Клонирование репозитория**:
   ```bash
   git clone https://github.com/yourusername/qa-system.git
   cd qa-system
