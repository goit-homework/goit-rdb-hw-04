# goit-rdb-hw-04: DML, DDL і складні SQL-вирази на Olist

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/goit-homework/goit-rdb-hw-04/blob/main/hw4_olist_dml_joins.ipynb)

Домашнє завдання до Теми 4 курсу «Реляційні бази даних для Data Science» (GoIT Neoversity).

## Дані

[Brazilian E-Commerce Public Dataset by Olist](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce), версія 2, ліцензія CC BY-NC-SA 4.0. Використано 6 із 9 таблиць повністю, без семплінгу: клієнти (99 441), замовлення (99 441), позиції (112 650), товари (32 951), продавці (3 095) і відгуки (99 224).

Ноутбук сам завантажує CSV через `kagglehub` без облікових даних Kaggle і звіряє SHA-256 кожного файлу, тому в репозиторії даних немає.

## Таблиці

- raw `olist_*_raw`: CSV, прочитані як текст.
- typed `olist_*`: схема з умови з PK, FK і `CHECK`.
- службові з умови: `seller_alerts`, `seller_score`, `olist_customer_dim`, `customer_segments`.

## Запуск

Ноутбук відкривається кнопкою Colab, далі Runtime > Run all. Локально потрібен Python 3.12:

```bash
pip install pgserver psycopg2-binary "sqlalchemy>=2.0,<2.1" pandas kagglehub jupyter
```

```bash
jupyter nbconvert --to notebook --execute --inplace hw4_olist_dml_joins.ipynb
```
