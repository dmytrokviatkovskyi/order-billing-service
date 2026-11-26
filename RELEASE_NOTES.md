# Release Notes — v1.1.0

## Added
- Спеціальний базовий тариф доставки `80.0` для міста `"Kyiv"`.
- Явний параметр податкової ставки `tax_rate` (за замовчуванням `0.20`) у функції розрахунку стандартного рахунку.
- Окремі спеціалізовані функції `process_standard_invoice` та `process_tax_exempt_invoice`.

## Changed
- Коефіцієнт вартості доставки за вагу збільшено з `12.0` до `15.0` за 1 кг.
- Виконано архітектурний рефакторинг модуля білінгу з переходом від Common, Stamp та Control Coupling до еталонного Data Coupling.

## Breaking Changes
- Видалено глобальну змінну `GLOBAL_TAX_RATE`.
- Видалено універсальну функцію `process_invoice` та керуючий прапорець `mode_flag`.
- Змінено сигнатуру `calculate_delivery_cost`: замість об'єкта `CustomerProfile` тепер передається рядок `city`.
