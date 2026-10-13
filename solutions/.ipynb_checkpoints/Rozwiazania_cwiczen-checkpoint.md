# Rozwiązania ćwiczeń - Kurs Pythona

Ten dokument zawiera przykładowe rozwiązania ćwiczeń z wszystkich lekcji kursu.

## Lekcja 1: Wprowadzenie do Pythona

### Ćwiczenie 1: Kalkulator BMI
```python
waga = 70  # w kilogramach
wzrost = 1.75  # w metrach

bmi = waga / (wzrost ** 2)
print(f"Twoje BMI: {bmi:.2f}")
```

### Ćwiczenie 2: Konwersja temperatur
```python
celsius = 20
fahrenheit = celsius * 9/5 + 32
print(f"{celsius}°C = {fahrenheit}°F")
```

### Ćwiczenie 3: Personalizowana wiadomość
```python
moje_imie = "Jan"
moj_wiek = 25
moje_hobby = "programowanie"

wiadomosc = f"Cześć! Mam na imię {moje_imie}, mam {moj_wiek} lat i lubię {moje_hobby}."
print(wiadomosc)
```

### Ćwiczenie 4: Pole i obwód prostokąta
```python
dlugosc = 5
szerokosc = 3

pole = dlugosc * szerokosc
obwod = 2 * (dlugosc + szerokosc)

print(f"Pole: {pole}")
print(f"Obwód: {obwod}")
```

---

## Lekcja 2: Operatory i wyrażenia

### Ćwiczenie 1: Sprawdzanie parzystości
```python
liczba = 17
jest_parzysta = (liczba % 2 == 0)
print(f"Czy {liczba} jest parzysta? {jest_parzysta}")
```

### Ćwiczenie 2: Sprawdzanie zakresu wieku
```python
wiek = 45
w_zakresie = (wiek >= 18) and (wiek <= 65)
print(f"Czy wiek {wiek} jest w zakresie 18-65? {w_zakresie}")
```

### Ćwiczenie 3: Kalkulator rabatu
```python
cena = 150
prog_rabatu = 100
rabat = 0.10

if cena > prog_rabatu:
    cena_koncowa = cena * (1 - rabat)
else:
    cena_koncowa = cena

print(f"Cena końcowa: {cena_koncowa} zł")
```

### Ćwiczenie 6: Sprawdzanie roku przestępnego
```python
rok = 2024

przestepny = (rok % 4 == 0 and rok % 100 != 0) or (rok % 400 == 0)
print(f"Czy {rok} jest rokiem przestępnym? {przestepny}")
```

---

## Lekcja 3: Struktury kontrolne

### Ćwiczenie 1: Kalkulator ocen
```python
punkty = 85

if punkty >= 90:
    ocena = "A"
elif punkty >= 80:
    ocena = "B"
elif punkty >= 70:
    ocena = "C"
elif punkty >= 60:
    ocena = "D"
else:
    ocena = "F"

print(f"Ocena: {ocena}")
```

### Ćwiczenie 2: Suma liczb parzystych
```python
suma = 0
for liczba in range(1, 51):
    if liczba % 2 == 0:
        suma += liczba
print(f"Suma liczb parzystych od 1 do 50: {suma}")
```

### Ćwiczenie 3: Odliczanie
```python
for i in range(10, 0, -1):
    print(i)
print("Start!")
```

### Ćwiczenie 4: Silnia
```python
n = 5
silnia = 1

for i in range(1, n + 1):
    silnia *= i

print(f"{n}! = {silnia}")
```

### Ćwiczenie 5: FizzBuzz
```python
for liczba in range(1, 31):
    if liczba % 3 == 0 and liczba % 5 == 0:
        print("FizzBuzz")
    elif liczba % 3 == 0:
        print("Fizz")
    elif liczba % 5 == 0:
        print("Buzz")
    else:
        print(liczba)
```

### Ćwiczenie 6: Piramida
```python
wysokosc = 5

for i in range(1, wysokosc + 1):
    spacje = " " * (wysokosc - i)
    gwiazdki = "*" * (2 * i - 1)
    print(spacje + gwiazdki)
```

---

## Lekcja 4: Listy i krotki

### Ćwiczenie 1: Statystyki listy
```python
liczby = [23, 45, 12, 67, 34, 89, 15, 56, 78, 90]

suma = sum(liczby)
srednia = suma / len(liczby)
minimum = min(liczby)
maksimum = max(liczby)

print(f"Suma: {suma}")
print(f"Średnia: {srednia:.2f}")
print(f"Minimum: {minimum}")
print(f"Maksimum: {maksimum}")
```

### Ćwiczenie 2: Filtrowanie listy
```python
liczby = [23, 45, 67, 12, 89, 34, 56, 78, 15, 90]
wieksze_niz_50 = [x for x in liczby if x > 50]
print(f"Liczby większe niż 50: {wieksze_niz_50}")
```

### Ćwiczenie 3: Usuwanie duplikatów
```python
lista = [1, 2, 3, 2, 4, 1, 5, 3, 6, 4]
unikalne = []

for element in lista:
    if element not in unikalne:
        unikalne.append(element)

print(f"Bez duplikatów: {unikalne}")
```

### Ćwiczenie 4: Odwracanie słów
```python
slowa = ["python", "programowanie", "lista", "krotka"]
odwrocone = [slowo[::-1] for slowo in slowa]
print(f"Odwrócone słowa: {odwrocone}")
```

### Ćwiczenie 5: Transpozycja macierzy
```python
macierz = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]

transponowana = [[macierz[j][i] for j in range(len(macierz))] for i in range(len(macierz[0]))]

print("Transponowana:")
for wiersz in transponowana:
    print(wiersz)
```

---

## Lekcja 5: Słowniki i zbiory

### Ćwiczenie 1: Książka telefoniczna
```python
ksiazka_tel = {}

# Dodawanie kontaktów
ksiazka_tel["Jan"] = "123-456-789"
ksiazka_tel["Anna"] = "987-654-321"
ksiazka_tel["Piotr"] = "555-123-456"

# Wyszukiwanie
print(f"Numer Jana: {ksiazka_tel.get('Jan', 'Nie znaleziono')}")

# Usuwanie
del ksiazka_tel["Piotr"]
print(f"Po usunięciu: {ksiazka_tel}")
```

### Ćwiczenie 3: Analiza tekstu
```python
tekst = "python jest super python jest łatwy python jest popularny"
slowa = tekst.split()

licznik = {}
for slowo in slowa:
    licznik[slowo] = licznik.get(slowo, 0) + 1

print("Liczba wystąpień słów:")
for slowo, ilosc in licznik.items():
    print(f"  {slowo}: {ilosc}")
```

### Ćwiczenie 4: Wspólni znajomi
```python
znajomi_jan = ["Anna", "Piotr", "Maria", "Tomek"]
znajomi_ewa = ["Piotr", "Kasia", "Maria", "Wojtek"]

zbior_jan = set(znajomi_jan)
zbior_ewa = set(znajomi_ewa)

wspolni = zbior_jan & zbior_ewa
tylko_jan = zbior_jan - zbior_ewa
tylko_ewa = zbior_ewa - zbior_jan

print(f"Wspólni znajomi: {wspolni}")
print(f"Tylko Jan: {tylko_jan}")
print(f"Tylko Ewa: {tylko_ewa}")
```

---

## Lekcja 6: Funkcje

### Ćwiczenie 1: Sprawdzanie liczby pierwszej
```python
def czy_pierwsza(n):
    if n < 2:
        return False
    for dzielnik in range(2, int(n ** 0.5) + 1):
        if n % dzielnik == 0:
            return False
    return True

# Testowanie
for liczba in [2, 3, 4, 17, 20, 29]:
    print(f"{liczba}: {czy_pierwsza(liczba)}")
```

### Ćwiczenie 2: Konwerter temperatur
```python
def celsius_na_fahrenheit(c):
    return c * 9/5 + 32

def fahrenheit_na_celsius(f):
    return (f - 32) * 5/9

def celsius_na_kelvin(c):
    return c + 273.15

# Testowanie
print(f"20°C = {celsius_na_fahrenheit(20)}°F")
print(f"68°F = {fahrenheit_na_celsius(68):.2f}°C")
print(f"0°C = {celsius_na_kelvin(0)}K")
```

### Ćwiczenie 3: Palindrom
```python
def czy_palindrom(slowo):
    slowo = slowo.lower()
    return slowo == slowo[::-1]

# Testowanie
slowa = ["kajak", "python", "radar", "poziom", "test"]
for slowo in slowa:
    print(f"{slowo}: {czy_palindrom(slowo)}")
```

### Ćwiczenie 4: Kalkulator
```python
def kalkulator(a, b, operacja):
    if operacja == '+':
        return a + b
    elif operacja == '-':
        return a - b
    elif operacja == '*':
        return a * b
    elif operacja == '/':
        if b != 0:
            return a / b
        else:
            return "Błąd: dzielenie przez zero"
    else:
        return "Nieznana operacja"

# Testowanie
print(f"10 + 5 = {kalkulator(10, 5, '+')}")
print(f"10 - 5 = {kalkulator(10, 5, '-')}")
print(f"10 * 5 = {kalkulator(10, 5, '*')}")
print(f"10 / 5 = {kalkulator(10, 5, '/')}")
```

---

## Lekcja 8: Klasy i obiekty

### Ćwiczenie 1: Klasa Prostokąt
```python
class Prostokat:
    def __init__(self, dlugosc, szerokosc):
        self.dlugosc = dlugosc
        self.szerokosc = szerokosc
    
    def pole(self):
        return self.dlugosc * self.szerokosc
    
    def obwod(self):
        return 2 * (self.dlugosc + self.szerokosc)
    
    def __str__(self):
        return f"Prostokąt({self.dlugosc}x{self.szerokosc})"

# Testowanie
p = Prostokat(5, 3)
print(p)
print(f"Pole: {p.pole()}")
print(f"Obwód: {p.obwod()}")
```

### Ćwiczenie 2: Klasa Student
```python
class Student:
    def __init__(self, imie, nazwisko):
        self.imie = imie
        self.nazwisko = nazwisko
        self.oceny = []
    
    def dodaj_ocene(self, ocena):
        if 1 <= ocena <= 6:
            self.oceny.append(ocena)
        else:
            print("Ocena musi być w zakresie 1-6")
    
    def srednia(self):
        if len(self.oceny) == 0:
            return 0
        return sum(self.oceny) / len(self.oceny)
    
    def __str__(self):
        return f"{self.imie} {self.nazwisko} (średnia: {self.srednia():.2f})"

# Testowanie
student = Student("Jan", "Kowalski")
student.dodaj_ocene(5)
student.dodaj_ocene(4)
student.dodaj_ocene(5)
print(student)
print(f"Średnia: {student.srednia():.2f}")
```

---

## Lekcja 9: Obsługa plików

### Ćwiczenie 1: Licznik słów
```python
def policz_slowa(nazwa_pliku):
    try:
        with open(nazwa_pliku, 'r', encoding='utf-8') as plik:
            zawartosc = plik.read()
            
            liczba_linii = len(zawartosc.split('\n'))
            liczba_slow = len(zawartosc.split())
            liczba_znakow = len(zawartosc)
            
            return liczba_linii, liczba_slow, liczba_znakow
    except FileNotFoundError:
        print(f"Plik {nazwa_pliku} nie istnieje!")
        return 0, 0, 0
```

### Ćwiczenie 2: Kopia pliku
```python
def kopiuj_plik(zrodlo, cel):
    try:
        with open(zrodlo, 'r', encoding='utf-8') as plik_zrodlowy:
            zawartosc = plik_zrodlowy.read()
        
        with open(cel, 'w', encoding='utf-8') as plik_docelowy:
            plik_docelowy.write(zawartosc)
        
        print(f"Skopiowano {zrodlo} do {cel}")
    except FileNotFoundError:
        print(f"Plik źródłowy {zrodlo} nie istnieje!")
    except Exception as e:
        print(f"Wystąpił błąd: {e}")
```

---

## Dodatkowe wskazówki

- Zawsze testuj swoje rozwiązania z różnymi danymi wejściowymi
- Obsługuj przypadki brzegowe (puste listy, zero, wartości ujemne, itp.)
- Dodawaj komentarze do skomplikowanego kodu
- Używaj znaczących nazw zmiennych
- Dziel złożone problemy na mniejsze funkcje

**Pamiętaj:** To tylko przykładowe rozwiązania. Często istnieje wiele prawidłowych sposobów rozwiązania tego samego problemu!
