# LAB 03 — Szczegóły restauracji i menu
Sandbox z konwersatoriów: [Repo z konwersatoriów](https://github.com/rbrzegowy/FoodApp-Angular---sandbox-do-konw)

## Cel

Rozbudowanie aplikacji o hierarchię:

```text
Restaurant
    ↓
Menu
    ↓
Product
```

---

## Stan początkowy

Projekt z LAB 02.

---

## Wymagania funkcjonalne

## FR-01. Otwieranie restauracji

Kliknięcie restauracji powinno otworzyć widok szczegółów.

Widok powinien zawierać:

- nazwę,
- opis,
- zdjęcie,
- rating,
- czas dostawy,
- koszt dostawy,
- adres,
- menu.

---

## FR-02. Menu

Menu powinno być podzielone na kategorie.

Przykład:

```text
Burger House

Burgers
----------------
Classic Burger
Cheeseburger
Bacon Burger

Fries
----------------
French Fries
Cheese Fries

Drinks
----------------
Cola
Water
```

---

## FR-03. Product Card - szczegóły produktu

Produkt musi zawierać:

- nazwę,
- opis,
- cenę,
- zdjęcie,
- informację o dostępności.

---

## FR-04. Niedostępny produkt

Produkt niedostępny:

- powinien być wizualnie oznaczony,
- nie może zostać dodany do koszyka.

---

## Wymagania dotyczące danych

Użyj AI do zamockowania danych. Przekaż mu model i warunki, poproś o JSON-A.

---

## Kryteria akceptacji

Użytkownik może wykonać:

```text
Restaurant List
      ↓
Restaurant
      ↓
Menu
      ↓
Product
```

---

## Zadania dodatkowe

- modal szczegółów produktu,
- nawigacja pomiędzy kategoriami,
- opcje produktu,
- przycisk „Add to cart”.

---
