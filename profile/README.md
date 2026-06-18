# OneCatalog

Плагины импорта централизованного каталога **[OneCatalog](https://docs.onecatalog.net/)**
(Wiki API) в товарные системы разных CMS и CRM. Один стандарт интеграции —
множество платформенных реализаций.

## 📐 Стандарт

**[onecatalog-standard](https://github.com/OneCatalog/onecatalog-standard)** —
платформо-независимый стандарт интеграции (канонический источник истины): внешние
контракты API, доменная модель и маппинг, обязательные инварианты, фоновая очередь,
точки расширения, чек-лист переноса на новую платформу. Здесь же — планы портирования
по всем платформам.

## 🧩 Плагины

| Платформа | Репозиторий | Статус |
|---|---|---|
| WordPress + WooCommerce *(эталон)* | [onecatalog-woocommerce](https://github.com/OneCatalog/onecatalog-woocommerce) | ✅ |
| 1С:Предприятие — Управление Торговлей 11.5 *(импорт в ERP)* | [onecatalog-1c](https://github.com/OneCatalog/onecatalog-1c) | ✅ `v1.1.3` |
| 1С-Битрикс | [onecatalog-bitrix](https://github.com/OneCatalog/onecatalog-bitrix) | 🚧 в разработке |
| Bitrix24 · PrestaShop · OpenCart · Magento 2 · Shopify · BigCommerce · Drupal Commerce · Joomla · МойСклад · RetailCRM · Megaplan · Moguta · NetCat · Shop-Script · PHPShop · UMI · SAP | — | 🔜 планируются ([планы](https://github.com/OneCatalog/onecatalog-standard/tree/main/integration-reviews)) |

## 🎯 Принципы

- **Идемпотентность** по стабильному внешнему ключу (`public_id`) — повторный импорт обновляет, не дублирует.
- **Тонкое универсальное ядро + сайтовый слой через события** — модуль переносится между проектами без правок.
- **Источник истины — внешний**; чего нет в API (например, цены) — не выдумывать.
- **Деградация без падений** — один битый товар не прерывает пакет.

Документация OneCatalog: **<https://docs.onecatalog.net/>**
