# LAB 04 — Panel administracyjny i CRUD
Sandbox z konwersatoriów: [Repo z konwersatoriów](https://github.com/rbrzegowy/FoodApp-Angular---sandbox-do-konw)
## Cel

Utworzenie pierwszej części panelu administracyjnego umożliwiającej zarządzanie danymi systemu.

---

## Wymagania funkcjonalne

## FR-01. Lista restauracji administratora

Admin może zobaczyć wszystkie restauracje.

Lista zawiera:

```text
Name
Cuisine
Rating
Active
Actions
```

---

## FR-02. Utworzenie restauracji

Admin może utworzyć restaurację.

Formularz zawiera:

- nazwę,
- opis,
- rodzaj kuchni,
- zdjęcie,
- czasy dostaw,
- koszt dostawy,
- minimalną wartość zamówienia,
- adres,
- status.

---

## FR-03. Edycja restauracji

Admin może zmienić dane istniejącej restauracji (te same dane co przy tworzeniu restauracji)

---

## FR-04. Dezaktywacja

Admin może dezaktywować restaurację.

Dezaktywacja nie usuwa danych.

---

## FR-05. Walidacja

Formularz powinien sprawdzać minimum:

- nazwę,
- opis,
- koszty dostaw,
- minimalną wartość zamówienia,
- czas dostawy.

---

## Kryteria akceptacji

Administrator może:

```text
List
 ↓
Create
 ↓
Edit
 ↓
Deactivate
```

Po zmianie dane powinny być widoczne również w części Customer.

---

## Zadania dodatkowe

- potwierdzenie przed dezaktywacją,
- sortowanie tabeli,
- wyszukiwanie,
- filtrowanie aktywnych/nieaktywnych,
- CRUD kategorii,
- CRUD produktów.

---
