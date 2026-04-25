# R4Bot-Module-Tickets

Внешний модуль тикетов для [R4Bot](https://github.com/Rarmash/R4Bot).

## Что делает
- добавляет `/ticket`
- создаёт тикет-канал в указанной категории
- даёт модераторам кнопки и селект для управления тикетом
- сохраняет текстовый лог при закрытии тикета и отправляет его в admin-канал
- использует runtime services из `bot.r4_services`

## Конфиг
Настройки модуля хранятся в:

```txt
config/modules/tickets.json
```

Структура конфига:

```json
{
  "123456789012345678": {
    "admin_channel": 123456789012345678,
    "ticket_category": 123456789012345678
  }
}
```

## Требования
- R4Bot `>= 2.0`
- runtime context с `bot.r4_services`
- сервисы `config`, `module_config`

## Структура
- `module.json` — метаданные модуля
- `cog.py` — Discord cog
- `tickets.example.json` — пример модульного конфига
- `requirements.txt` — зависимости для IDE и локальной проверки

## Установка в R4Bot
```powershell
python manage_modules.py install github:Rarmash/R4Bot-Module-Tickets@master --enable
```

## Разработка
Для нормальной подсветки импортов в IDE и локальной проверки модуля рекомендуется установить зависимости:

```powershell
python -m pip install -r requirements.txt
```
