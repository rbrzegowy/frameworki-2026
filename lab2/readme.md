# LAB 02 — Wyszukiwanie, filtrowanie i sortowanie

## Cel

Rozbudowanie listy restauracji o interakcję użytkownika i dynamiczne przetwarzanie danych.

---

## Stan początkowy

Projekt z LAB 01.

---

## Wymagania funkcjonalne

### FR-01. Wyszukiwanie

Użytkownik może wyszukiwać restauracje po nazwie.

Przykład:

```text
Search:
[ burger             ]
```

Lista powinna zawierać tylko restauracje pasujące do wyszukiwania.

---

### FR-02. Filtrowanie po kuchni

Użytkownik może wybrać rodzaj kuchni:

```text
All
Burger
Pizza
Sushi
Asian
Italian
Polish
Healthy
```

---

### FR-03. Filtrowanie po statusie

Użytkownik może wybrać:

```text
All
Open only
```

---

### FR-04. Sortowanie

Użytkownik może sortować restauracje według:

- ratingu,
- czasu dostawy,
- kosztu dostawy.

---

### FR-05. Brak wyników

Jeżeli żadne dane nie spełniają kryteriów, aplikacja musi wyświetlić komunikat:

```text
Nie znaleziono restauracji.
```

---

### FR-06. Reset filtrów

Użytkownik powinien mieć możliwość przywrócenia początkowego widoku.

---

## Kryteria akceptacji

Przykład:

```text
Search = "burger"
Cuisine = All
Status = Open
Sort = Rating
```

powinien zwrócić wyłącznie aktywne restauracje zawierające „burger” w nazwie.

Zmiana dowolnego filtra powinna natychmiast aktualizować listę.

---

## Zadania dodatkowe

- filtrowanie po minimalnej wartości zamówienia,
- filtrowanie po czasie dostawy,
- wielokrotne kryteria jednocześnie,
- liczba znalezionych restauracji.

---
