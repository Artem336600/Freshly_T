# Freshly T - Telegram Bot для здорового питания

Telegram бот для отслеживания питания, анализа фотографий еды и предоставления персонализированных рекомендаций по здоровому образу жизни.

## Архитектура

Проект построен на микросервисной архитектуре с использованием Docker и Kubernetes.

## Структура репозитория

```
/project-root
├── services/                  # Микросервисы
│   ├── bot-gateway-service/   # Шлюз для Telegram бота
│   ├── user-management-service/ # Управление пользователями
│   ├── food-recognition-service/ # Распознавание еды на фото
│   ├── emotional-support-service/ # Эмоциональная поддержка
│   ├── scheduler-service/     # Планировщик задач
│   ├── photo-analysis-service/ # Анализ фотографий
│   ├── analytics-service/     # Аналитика и метрики
│   └── database-service/      # База данных PostgreSQL
├── packages/                  # Общие библиотеки
│   ├── shared-lib-1/
│   └── shared-lib-2/
├── k8s/                       # Манифесты Kubernetes
│   ├── namespaces/            # Пространства имен
│   ├── rbac/                  # Роли и права доступа
│   ├── quotas/                # Квоты ресурсов
│   └── network/               # Сетевая конфигурация
├── .github/workflows/         # CI/CD пайплайны
├── .gitignore
└── README.md
```

## Сервисы

### 🤖 Bot Gateway Service (Порт: 3000)
- Маршрутизация запросов от Telegram бота
- Аутентификация и авторизация
- Rate limiting и защита от спама

### 👤 User Management Service (Порт: 3001)
- Регистрация и аутентификация пользователей
- Управление профилями и настройками
- Система ролей и прав доступа

### 🍎 Food Recognition Service (Порт: 3002)
- Распознавание блюд на фотографиях
- Определение калорийности и пищевой ценности
- Классификация типов еды с использованием ML

### 💚 Emotional Support Service (Порт: 3003)
- Генерация мотивационных сообщений
- Персонализированные советы по здоровому питанию
- Трекинг эмоционального состояния

### ⏰ Scheduler Service (Порт: 3004)
- Планирование уведомлений и напоминаний
- Управление задачами и расписанием
- Интеграция с календарем

### 📸 Photo Analysis Service (Порт: 3005)
- Анализ качества еды на фотографиях
- Определение свежести продуктов
- Оценка размера порций

### 📊 Analytics Service (Порт: 3006)
- Сбор метрик использования
- Анализ пользовательского поведения
- Генерация отчетов и дашбордов

### 🗄️ Database Service (Порт: 5432)
- PostgreSQL база данных
- Хранение всех данных приложения
- Резервное копирование и восстановление

## Технологический стек

- **Backend**: Node.js, Python
- **Database**: PostgreSQL
- **ML/AI**: TensorFlow, PyTorch, OpenCV
- **Containerization**: Docker
- **Orchestration**: Kubernetes
- **CI/CD**: GitHub Actions
- **Monitoring**: Prometheus, Grafana

## Как работать

1. Ветка от main: `git checkout -b feature/TASK-123-short-description`
2. Максимум 2 дня работы в feature branch
3. Создать PR, пройти CI и ревью
4. После merge — ветка автоматически удаляется

## Разработка

### Локальный запуск
```bash
# Запуск всех сервисов через Docker Compose
docker-compose up -d

# Или запуск отдельных сервисов
cd services/bot-gateway-service
npm install
npm start
```

### Тестирование
```bash
# Запуск тестов для всех сервисов
npm test

# Запуск тестов для конкретного сервиса
cd services/user-management-service
npm test
```

## Деплой

Развертывание происходит автоматически через GitHub Actions при merge в main ветку.
