# Photo Analysis Service

Сервис анализа фотографий для определения качества еды, свежести продуктов и других параметров.

## Функциональность
- Анализ качества еды
- Определение свежести продуктов
- Оценка размера порций
- Детекция вредных веществ

## API Endpoints
- `POST /analyze/quality` - Анализ качества еды
- `POST /analyze/freshness` - Проверка свежести
- `GET /health` - Health check

## Порты
- 3005 - HTTP API

## Зависимости
- OpenCV
- TensorFlow/PyTorch
- ImageIO
