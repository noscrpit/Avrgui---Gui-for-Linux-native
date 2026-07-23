# Avrgui – Natywna nakładka na avrdude - Linux GUI v1.0

## 📄 Licencja

Projekt jest udostępniany w stanie "takim, jaki jest" na licencji

**GNU General Public License v3.0 (GPLv3)**. 

Używasz go na własną odpowiedzialność.


Starano się bardzo, aby program ten nic nie popsuł.

Kod jest wolny, otwarty i chroniony przed zamknięciem w płatnych, komercyjnych rozwiązaniach – idea wolnego oprogramowania i systemu Linux jest tu w pełni kontynuowana!

Lekki, asynchroniczny i w 100% natywny interfejs graficzny (GUI) dla narzędzia **AVRDUDE**, napisany w języku Python 3 z wykorzystaniem nowoczesnej biblioteki PyQt6.

Jest  kompletny i zoptymalizowany  pod systemy Linux:

– działa błyskawicznie, 

-nie wymaga ociężałego środowiska *Mono*

*-* został zabezpieczony przed zamrażaniem okna podczas operacji sprzętowych.


## 🚀 Kluczowe możliwości

- **Asynchroniczne działanie (`QThread`)**: 

- Wszystkie operacje AVRDUDE wykonują się w osobnym wątku. 

- Okno programu nigdy się nie zawiesza i pozwala na płynne podglądanie logów w czasie rzeczywistym.


- **Przycisk Przerwij (`Cancel`)**: 

- Czerwony przycisk umożliwia natychmiastowe ubicie procesu komunikacji, jeśli sprzęt utknie z powodu braku zasilania lub odłączonego kabla.


- **Automatyczne wykrywanie programatorów (Autodetect przy starcie)**: 

- Program sam przeczesuje szynę USB za pomocą `lsusb` i automatycznie konfiguruje parametry oraz porty `/dev/ttyUSB\*` dla układów **USBasp**, **CH340** oraz **CH341A**.


- **Wykrywanie procesora (`Detect MCU`)**: 

- Niebieski przycisk wysyła zapytanie do programatora, odczytuje sygnaturę fabryczną podłączonego chipu (np. ATmega328P, ATtiny85) i sam automatycznie ustawia właściwy model na liście.

- **Ochrona przed spamem błędów**: 

- Dla programatorów seryjnych automatycznie wymusza tylko 1 próbę połączenia (`attempts=1`), zapobiegając czekaniu na timeout i sypaniu błędami.


- **Pamięć i Bezpieczniki**: 

- Obsługuje zapis/odczyt pamięci FLASH i EEPROM (wraz z weryfikacją `Verify` i funkcją `Chip Erase`) oraz pełną edycję i kalkulator bezpieczników (`lfuse`, `hfuse`, `efuse`, `lock`).

- **Zapamiętywanie ustawień**: Program zapisuje konfigurację do pliku `gui\_config.txt`, dzięki czemu po restarcie pamięta ostatnio używane flagi i ścieżki plików.


## 🛠️ Wymagania systemowe i instalacja

Program do działania potrzebuje Pythona 3 oraz kilku narzędzi systemowych.

- wymagane zależności :

```
python3 python3-pyqt6 avrdude usbutils
```

***Uwaga!:***

*Rekomendowana jest wersja **AVRDUDE 8.0 lub nowsza** dla pełnej kompatybilności z nowoczesnymi układami.*

## 🏃 Uruchomienie programu

1. Pobierz plik avr`gui.py` na swój komputer.

2. Nadaj mu uprawnienia do wykonywania jako program (wystarczy raz):

```
chmod +x ./avr`gui.py`
```

3. Uruchom program bezpośrednio z konsoli (lub klikaj na niego):

```
./avr`gui.py`
```


📬 Przetestuj wersję v1.0-RC i daj znać jeśli chcesz!


Jeśli przetestowałeś program na swoim komputerze, jeśli chcesz, napisz, do mnie na

maila: noscrpit@gmail.com

- Jakiej dystrybucji Linuksa używasz i jak działa program?

- Czy automatyczne wykrywanie poprawnie znalazło Twój programator i port?

- Czy wyszukiwarka układów i podgląd pinów działają prawidłowo?

- Czy dokonałeś jakichś zmian – i jakich?


Razem możemy udoskonalić program. 


Miłego i owocnego programowania scalaków! - noscrpit

