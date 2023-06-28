# Домашнее задание к лекции «Работа с PostgreSQL из Python»

Создайте программу для управления клиентами на Python.

Требуется хранить персональную информацию о клиентах:

- имя,
- фамилия,
- email,
- телефон.

Сложность в том, что телефон у клиента может быть не один, а два, три и даже больше. А может и вообще не быть телефона, например, он не захотел его оставлять.

Вам необходимо разработать структуру БД для хранения информации и несколько функций на Python для управления данными.

1. Функция, создающая структуру БД (таблицы).
1. Функция, позволяющая добавить нового клиента.
1. Функция, позволяющая добавить телефон для существующего клиента.
1. Функция, позволяющая изменить данные о клиенте.
1. Функция, позволяющая удалить телефон для существующего клиента.
1. Функция, позволяющая удалить существующего клиента.
1. Функция, позволяющая найти клиента по его данным: имени, фамилии, email или телефону.

Функции выше являются обязательными, но это не значит, что должны быть только они. При необходимости можете создавать дополнительные функции и классы.

Также предоставьте код, демонстрирующий работу всех написанных функций.

Результатом работы будет `.py` файл.

---

## Подсказка

> Не читайте этот раздел сразу, попытайтесь сначала решить задачу самостоятельно :)

<details>

<summary>Каркас кода</summary>

```py
import psycopg2

def create_db(conn):
    pass

def add_client(conn, first_name, last_name, email, phones=None):
    pass

def add_phone(conn, client_id, phone):
    pass

def change_client(conn, client_id, first_name=None, last_name=None, email=None, phones=None):
    pass

def delete_phone(conn, client_id, phone):
    pass

def delete_client(conn, client_id):
    pass

def find_client(conn, first_name=None, last_name=None, email=None, phone=None):
    pass


with psycopg2.connect(database="clients_db", user="postgres", password="postgres") as conn:
    pass  # вызывайте функции здесь

conn.close()
```

</details>
