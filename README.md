# QnA-ChatBot-for-T-bank

## Обзор
Проект представляет собой чат-бот для ответов на вопросы (QnA) для T-Bank. Чат-бот обрабатывает датасет вопросов, создает эмбеддинги и сохраняет их в векторную базу данных Chroma. Использует подход RAG для поиска релевантных чанков вопросов, передает их вместе с вопросом пользователя языковой модели (LLM), которая генерирует наиболее подходящий ответ. Также реализована проверка на галлюцинации, где модель оценивает правильность ответа. Если ответ не найден в базе, бот сообщает, что не знает ответа.

## Особенности
Загрузка данных: Считывание датасета вопросов.
Создание эмбеддингов: Генерация эмбеддингов для вопросов.
Хранение в Chroma: Сохранение эмбеддингов в Chroma.
Поиск с RAG: Поиск релевантных чанков вопросов.
Интеграция LLM: Поддержка Yandex GPT и ChatGPT.
Проверка на галлюцинации: Проверка ответа на точность с помощью LLM.
Резервный ответ: Сообщение об отсутствии ответа в базе.

## Проверка на галлюцинации
Ответы проверяются вторичной LLM на точность. Если ответ неточный, бот сообщает, что не знает ответа.

## Конфигурация
Файл конфигурации (config.json) содержит настройки подключения к базе данных и API ключи.
