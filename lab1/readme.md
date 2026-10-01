# LAB 01 — Application Shell i restauracje

## Cel

Utworzenie podstawowej struktury aplikacji FoodApp oraz pierwszego widoku umożliwiającego przeglądanie restauracji.

Na tym etapie aplikacja nie korzysta z backendu. Dane są dostarczone jako dane testowe w aplikacji.

---

## Stan początkowy

Nowy projekt Angular.

Aplikacja powinna posiadać podstawowy layout:

```text
┌─────────────────────────────────────┐
│              Header                 │
├─────────────────────────────────────┤
│                                     │
│          Lista restauracji.         │
│                                     │
├─────────────────────────────────────┤
│              Footer                 │
└─────────────────────────────────────┘
```

---

## Wymagania funkcjonalne

### FR-01. Lista restauracji

Aplikacja musi wyświetlać listę co najmniej 3 restauracji.

Każda restauracja powinna zawierać:

- nazwę,
- opis,
- rodzaj kuchni,
- zdjęcie,
- rating,
- czas dostawy,
- koszt dostawy,
- informację, czy restauracja jest aktywna.

---

### FR-02. Restaurant Card

Każda restauracja musi być prezentowana jako osobny element interfejsu.

Karta powinna umożliwiać użytkownikowi rozpoznanie:

- nazwy restauracji,
- rodzaju kuchni,
- ratingu,
- czasu dostawy,
- kosztu dostawy.

---

### FR-03. Status restauracji

Dla restauracji nieaktywnej należy wyświetlić odpowiednią informację.

Przykład:

```text
Burger House
OPEN
```

lub:

```text
Sushi World
CLOSED
```

---

### FR-04. Header

Header powinien zawierać nazwę aplikacji - np. FoodApp,

---

### FR-05. Footer

Aplikacja powinna posiadać podstawowy footer - dane kontaktowe (mock)

---

## Wymagania techniczne

Model restauracji:

```ts
type Restaurant {
  id: number;
  name: string;
  description: string;
  cuisine: CuisineType;
  imageUrl?: string;
  rating: number;
  deliveryTimeMin: number;
  deliveryTimeMax: number;
  deliveryFee: number;
  minimumOrderValue: number;
  isActive: boolean;
}
type CousineType = 'italian' | 'polish' | 'chinese' | 'thai' | 'american' // ...
// type zamienisz prawdopodobnie na enum - będzie łatwiej zrobić <select id="cousin-type">
```

---

## Kryteria akceptacji

Lab jest ukończony, jeśli:

- aplikacja uruchamia się bez błędów,
- wyświetla minimum 3 restauracje,
- każda restauracja jest prezentowana osobno,
- informacje są poprawnie wyświetlane,
- można odróżnić restaurację aktywną od nieaktywnej,
- istnieje Header i Footer.