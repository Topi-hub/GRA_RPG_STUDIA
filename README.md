# GRA_STUDIA_RPG

## Opis projektu
**GRA_STUDIA_RPG** to klasyczna gra RPG 2D stworzona w **Unity**, osadzona w świecie dwóch wysp: wyspy zamkowej i wyspy poziomów. Gracz steruje postacią przemierzającą mapę, walczącą z przeciwnikami i awansującą na kolejne poziomy.  
Głównym celem biznesowym projektu jest **nauka oraz prezentacja umiejętności programowania obiektowego i tworzenia gier w Unity**.

## Technologie użyte w projekcie
- Unity 2022+
- C# (programowanie obiektowe)
- Tileset: Tiny Swords (grafika 64x64 px)
- TextMeshPro (do UI gracza)
- Visual Studio (do edycji kodu)

## Lista funkcjonalności

| Funkcjonalność             | Opis                                      | Screenshot                |
|:----------------------------|:-----------------------------------------|:---------------------------|
| **Ruch gracza**             | Swobodne poruszanie się po mapie          | ![image](https://github.com/user-attachments/assets/79d37da6-2a20-4843-a471-488d353dfe24) |
| **Walka**                   | Atakowanie przeciwników w zwarciu         | ![image](https://github.com/user-attachments/assets/0811acfb-c519-401e-9087-717f6a20ddcf) |
| **Cooldown ataku**          | Pasek pokazujący czas ładowania ataku     | ![image](https://github.com/user-attachments/assets/63569e07-841d-4d19-ba91-87f72393b0a2) |
| **Pasek zdrowia**           | Pasek HP nad przeciwnikami i graczem      | ![image](https://github.com/user-attachments/assets/8ebf17c4-c806-4d2c-b553-48b06647b57b) |
| **Sztuczna inteligencja wroga** | Wróg ściga i atakuje gracza           | ![image](https://github.com/user-attachments/assets/004102b9-ce0a-4039-8181-33713c387937) |
| **System Game Over**        | Śmierć gracza powoduje wyświetlenie UI    | ![image](https://github.com/user-attachments/assets/bb14340f-1a04-4de5-905b-ecb91d7a1959) |
| **Menu główne i pauzy**     | Start gry i zatrzymywanie rozgrywki       | ![image](https://github.com/user-attachments/assets/f8f800a7-f9b2-4c92-8659-75f9d32c164d) |

## Instalacja i uruchomienie

 1. Pobierz załączony folder E.rar, w którym zawarta jest gra.
 2. Wypakuje folder.
 3. Otwórz program o nazwie RPG_Studia.exe

## Opis architektury projektu

Projekt został zbudowany w oparciu o paradygmat obiektowy (OOP).

Główne założenia OOP w projekcie:
- **Dziedziczenie**: 
  - `Player` i `Enemy` dziedziczą po wspólnej klasie `Character`, która definiuje podstawowe właściwości (`hp`, `TakeDamage()`, `Die()`).
- **Enkapsulacja**: 
  - Atrybuty takie jak `hp`, `attackCooldown` są ukryte (`private` lub `protected`) i dostępne poprzez metody.
- **Polimorfizm**: 
  - `Enemy` oraz `Player` mogą nadpisywać lub rozszerzać zachowania z `Character`.
- **Kompozycja**: 
  - `CooldownBar`, `HealthBar`, `PlayerHealthBar` są osobnymi komponentami przypisanymi do obiektów.

Dzięki takiej architekturze kod jest modularny, łatwy do rozbudowy i utrzymania.

## Diagram klas UML

Poniżej znajduje się diagram UML przedstawiający główne klasy i zależności w projekcie:

![UML Diagram](Diagram_UML_RPG.png)

