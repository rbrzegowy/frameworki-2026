# LAB 05 — Konta użytkowników, logowanie i autoryzacja

## Cel

Wprowadzenie ról użytkowników, autoryzacji oraz rozdzielenie dostępu Customer/Admin.

---

## Wymagane nowe routes

```text
/
 /login
 /register
 /profile

/admin/users
/admin/users/new
```

---

## Wymagania funkcjonalne

## FR-01. Rejestracja konta Customer

Każda osoba może samodzielnie założyć konto z rolą `customer`, podając co najmniej imię, adres e-mail, hasło i adres dostawy (model poniżej).

Adres e-mail musi być unikalny. Rola nowego konta jest nadawana przez system — formularz publicznej rejestracji nie może umożliwiać wyboru roli.

Po poprawnej rejestracji użytkownik może się zalogować.

---

## FR-02. Logowanie

Użytkownik może się zalogować przy użyciu adresu e-mail i hasła.

W nagłówku aplikacji wyświetla się informacja o aktualnie zalogowanym użytkowniku (np. imię).

---

## FR-03. Role i zakładanie kont administracyjnych

System rozpoznaje role:

```text
customer
admin
```

Tylko zalogowany Admin może utworzyć konto administracyjne. Podczas tworzenia konta Admin podaje co najmniej imię, adres e-mail i hasło, system nadaje rolę `admin`.

Rola Customer nie może utworzyć konta administracyjnego ani zmienić swojej roli. Operacja utworzenia admina jest niedostępna w rejestracji publicznej.

---

## FR-04. Edycja własnego profilu

Zalogowany użytkownik (admin i customer) może wyświetlić i edytować własny profil.

Adres e-mail po edycji musi pozostać unikalny. Użytkownik nie może w ten sposób zmieniać swojej roli ani edytować profilu innego użytkownika.

---

## FR-05. Ochrona panelu

Customer nie może wejść do:

```text
/admin/*
```

---

## FR-06. Redirect

Niezalogowany użytkownik próbujący wejść do chronionej części aplikacji powinien zostać przekierowany do logowania.

---

## FR-07. Logout

Zalogowany użytkownik może się wylogować.

---

## FR-08. Lista użytkowników

Admin może przeglądać listę użytkowników. Z poziomu listy możliwy jest reset hasła oraz usunięcie konta.

---

## Przykładowy model konta użytkownika

```ts
type UserRole = 'customer' | 'admin';

type Address = {
  street: string;
  buildingNumber: string;
  apartmentNumber?: string;
  postalCode: string;
  city: string;
}

type UserAccountBase = {
  id: string;
  name: string;
  email: string;
  password: string
  phone?: string;
}

type CustomerAccount =  UserAccountBase & {
  role: 'customer';
  deliveryAddress: Address;
}

type AdminAccount = UserAccountBase & {
  role: 'admin';
}

type UserAccount = CustomerAccount | AdminAccount;
```

Adres dostawy jest wymagany dla konta Customer, ale nie dotyczy konta Admin. Hasło jest wymagane przy rejestracji i logowaniu, ale nie powinno być zwracane w danych profilu ani przechowywane w postaci jawnej. API przechowuje wyłącznie bezpieczny skrót hasła. Pole `role` może ustawić system podczas rejestracji lub Admin podczas tworzenia konta, ale użytkownik nie może go zmienić podczas edycji profilu.

---

## Kryteria akceptacji

### Customer

Może:

```text
zarejestrować konto
zalogować się
edytować profil
```

Nie może:

```text
wejść na strony administracyjne
```

### Admin

Może:

```text
tworzyć konta administracyjne
przeglądać listę adminów
edytować własny profil
usuwać konta administracyjne
```

Publiczna rejestracja zawsze tworzy konto `customer`; tylko Admin może utworzyć konto `admin`.

---

## Zadania dodatkowe

- lazy loading panelu admina,
- redirect po loginie do poprzednio żądanej strony,

---