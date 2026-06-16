# Object Oriented Programming Lab - Bookstore

A Python OOP lab that models two objects found in a bookstore: a **Book** and a **Coffee**. Each class demonstrates `__init__`, property validation, and instance methods.

---

## What It Does

### Book (`lib/book.py`)

Represents a book with a title and page count.

| Attribute / Method | Description |
|--------------------|-------------|
| `title` | The book's title (string) |
| `page_count` | Number of pages — must be an integer; prints an error otherwise |
| `turn_page()` | Prints `"Flipping the page...wow, you read fast!"` |

**Example:**

```python
from lib.book import Book

book = Book("And Then There Were None", 272)
book.turn_page()
# → Flipping the page...wow, you read fast!

book.page_count = "lots"
# → page_count must be an integer
```

---

### Coffee (`lib/coffee.py`)

Represents a coffee order with a size and price.

| Attribute / Method | Description |
|--------------------|-------------|
| `size` | Must be `"Small"`, `"Medium"`, or `"Large"`; prints an error otherwise |
| `price` | The cost of the coffee (float) |
| `tip()` | Prints a thank-you message and increases the price by 1 |

**Example:**

```python
from lib.coffee import Coffee

coffee = Coffee(size="Large", price=3.50)
coffee.tip()
# → This coffee is great, here's a tip!
print(coffee.price)
# → 4.50

coffee.size = "Venti"
# → size must be Small, Medium, or Large
```

---

## Screenshot

![All 7 tests passing](./assets/tests_passing.png)

---

## Setup

```console
pipenv install
pipenv shell
```

## Running Tests

```console
# Run all tests
pytest lib/testing/ -v

# Run tests for a single class
pytest -x lib/testing/book_test.py
pytest -x lib/testing/coffee_test.py
```

---

## Project Structure

```
python-oop1-lab/
├── lib/
│   ├── book.py          # Book class
│   ├── coffee.py        # Coffee class
│   └── testing/
│       ├── book_test.py
│       ├── coffee_test.py
│       └── conftest.py
├── debug.py
└── README.md
```

---

## Tools & Resources

- [Python Classes Docs](https://docs.python.org/3/tutorial/classes.html)
- [GitHub Repo](https://github.com/learn-co-curriculum/python-oop1-lab)
