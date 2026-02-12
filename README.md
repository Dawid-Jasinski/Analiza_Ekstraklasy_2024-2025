# Analiza_Ekstraklasy_2024-2025

Źródło: https://fbref.com/en/comps/36/2024-2025/2024-2025-Ekstraklasa-Stats#all_rank_key 


## Data Cleaning & Integration
Tabele z FBref skopiowane ręcznie do Excela (zabezpieczenia anty-scrapingowe).
Wyzwanie: Niejednoznaczne nagłówki, zduplikowane kolumny, dziwne formaty (daty zamiast liczb).
Rozwiązanie:

Funkcja automatycznie wykrywa wiersz nagłówków na podstawie kolumny Squad.
Standaryzacja nazw drużyn.
Usuwanie duplikujących się kolumn i pustych kolumn.
Merge arkuszy w jeden spójny dataset na poziomie drużyn.














