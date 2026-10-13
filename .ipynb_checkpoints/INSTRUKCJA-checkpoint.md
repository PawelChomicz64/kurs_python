# Instrukcja Instalacji i Uruchomienia Kursu

## Wymagania Systemowe

Aby korzystać z tego kursu, potrzebujesz:

- **Python 3.8 lub nowszy** - Sprawdź wersję: `python --version` lub `python3 --version`
- **Jupyter Notebook** - Zostanie zainstalowany w kroku 2
- **System operacyjny:** Windows, macOS lub Linux
- **Przeglądarka internetowa** - Chrome, Firefox, Safari lub Edge

## Krok 1: Instalacja Pythona

### Windows

1. Pobierz instalator Pythona ze strony [python.org](https://www.python.org/downloads/)
2. Uruchom instalator
3. **WAŻNE:** Zaznacz opcję "Add Python to PATH"
4. Kliknij "Install Now"
5. Po instalacji otwórz wiersz poleceń (cmd) i sprawdź: `python --version`

### macOS

Python 3 jest zazwyczaj preinstalowany. Jeśli nie:

```bash
# Zainstaluj Homebrew (jeśli nie masz)
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

# Zainstaluj Pythona
brew install python3
```

### Linux (Ubuntu/Debian)

```bash
sudo apt update
sudo apt install python3 python3-pip
```

## Krok 2: Instalacja Jupyter Notebook

Otwórz terminal (lub wiersz poleceń) i wykonaj:

```bash
# Windows
pip install jupyter notebook

# macOS/Linux
pip3 install jupyter notebook
```

## Krok 3: Pobieranie Materiałów Kursu

1. Pobierz archiwum `python_course.tar.gz` (lub `python_course.zip`)
2. Rozpakuj archiwum do wybranego katalogu
3. Zapamiętaj lokalizację katalogu `python_course`

### Rozpakowywanie

**Windows:**
- Kliknij prawym przyciskiem na archiwum → "Wyodrębnij wszystko"

**macOS/Linux:**
```bash
tar -xzf python_course.tar.gz
```

## Krok 4: Uruchomienie Jupyter Notebook

1. Otwórz terminal (lub wiersz poleceń)
2. Przejdź do katalogu kursu:

```bash
cd ścieżka/do/python_course
```

3. Uruchom Jupyter Notebook:

```bash
jupyter notebook
```

4. Przeglądarka automatycznie otworzy panel Jupyter pod adresem `http://localhost:8888`

## Krok 5: Rozpoczęcie Nauki

1. W panelu Jupyter przejdź do katalogu `lessons`
2. Kliknij na `Lekcja_01_Wprowadzenie.ipynb`
3. Notebook otworzy się w nowej karcie
4. Czytaj treść i uruchamiaj komórki z kodem:
   - Kliknij na komórkę z kodem
   - Naciśnij `Shift + Enter` aby uruchomić
   - Lub użyj przycisku "Run" w górnym menu

## Skróty Klawiszowe w Jupyter

### Tryb poleceń (naciśnij `Esc`)
- `A` - dodaj komórkę powyżej
- `B` - dodaj komórkę poniżej
- `D, D` - usuń komórkę (dwa razy D)
- `M` - zmień na komórkę Markdown
- `Y` - zmień na komórkę Code

### Tryb edycji (naciśnij `Enter`)
- `Shift + Enter` - uruchom komórkę i przejdź do następnej
- `Ctrl + Enter` - uruchom komórkę i zostań w niej
- `Alt + Enter` - uruchom komórkę i wstaw nową poniżej

## Rozwiązywanie Problemów

### Problem: "jupyter: command not found"

**Rozwiązanie:**
```bash
# Sprawdź, gdzie jest zainstalowany Jupyter
pip show jupyter

# Dodaj ścieżkę do PATH lub użyj pełnej ścieżki
python -m jupyter notebook
```

### Problem: Kernel nie działa

**Rozwiązanie:**
```bash
# Zainstaluj kernel Pythona
python -m ipykernel install --user
```

### Problem: Nie mogę zapisać zmian w notebooku

**Rozwiązanie:**
- Sprawdź uprawnienia do katalogu
- Uruchom Jupyter z odpowiednimi uprawnieniami
- Upewnij się, że plik nie jest otwarty w innym miejscu

## Dodatkowe Biblioteki

Niektóre lekcje (szczególnie Lekcja 10) wymagają dodatkowych bibliotek:

```bash
pip install numpy pandas matplotlib
```

## Wsparcie

Jeśli napotkasz problemy:

1. Sprawdź sekcję "Rozwiązywanie problemów" powyżej
2. Przeczytaj dokumentację Jupyter: [https://jupyter.org/documentation](https://jupyter.org/documentation)
3. Sprawdź dokumentację Pythona: [https://docs.python.org/3/](https://docs.python.org/3/)

## Alternatywne Środowiska

Jeśli masz problemy z lokalną instalacją, możesz użyć:

- **Google Colab** - [https://colab.research.google.com/](https://colab.research.google.com/)
  - Darmowe, działa w przeglądarce
  - Nie wymaga instalacji
  - Prześlij pliki `.ipynb` do Colab

- **Anaconda** - [https://www.anaconda.com/](https://www.anaconda.com/)
  - Kompletna dystrybucja z Pythonem, Jupyter i bibliotekami
  - Łatwa instalacja jednym kliknięciem

---

**Powodzenia w nauce!** 🚀
