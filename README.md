# Machine learning - badanie wytrzymalosci betonu, wpływ poszczególnych komponentów na wytrzymałość betonu na ściskanie

# Wstęp
Projekt oparty na analizie danych dotyczących wytrzymałości betonu na ściskanie. Celem projektu jest zastosowanie algorytmu Machine Learning do przewidywania wytrzymałości betonu na podstawie różnych składników. Poniżej przedstawiono najistotniejsze informacje dotyczące przeprowadzenia algorytmu, kod całościowy znajduje się w pliku ipynb.

#Źródło danych
[Dataset on Kaggle] https://www.kaggle.com/datasets/prathamtripathi/regression-with-neural-networking,
Autorzy oraz współtwórcy: Pratham Tripathi

# Załadowanie i Wstępna Analiza Danych:
 - Wykorzystano Pandas do wczytania danych z pliku CSV.
 - Przegląd informacji o danych (df.info()) oraz analiza brakujących danych (df.isnull().sum()).

# Eksploracyjna Analiza Danych (EDA):
 - Utworzono wykres korelacji pomiędzy zmiennymi za pomocą heatmapy.
   
   ![image](https://github.com/Jakub-Drabikowski/Machine-learning-badanie-wytrzymalosci/assets/83064196/2afdc35c-f6c6-466f-b344-70597434f341)

 - Przedstawiono histogram wytrzymałości betonu.
   
   ![image](https://github.com/Jakub-Drabikowski/Machine-learning-badanie-wytrzymalosci/assets/83064196/c5100958-182e-4e88-b227-1500d104c861)

# Przetwarzanie Danych przed przeprowadzeniem algorytmu:
 - Zdefiniowano zmienną zależną (y) i niezależną (X) poprzez usunięcie kolumny 'strength'.
 - Zastosowano podział danych na zbiór treningowy i testowy.
   
# Algorytm GradientBoostingRegressor i jego ewaluacja:
 - Wykorzystano algorytm Gradient Boosting Regressor z biblioteki scikit-learn do przewidywania wytrzymałości betonu.
 - Ocena modelu za pomocą różnych metryk, takich jak mean absolute error, mean squared error, root mean squared error i R2 score.

   ![image](https://github.com/Jakub-Drabikowski/Machine-learning-badanie-wytrzymalosci/assets/83064196/0167d528-cfd9-45c8-9b7d-3294232a6ed3)

 - Z uwagi na poprawienie wydajności i uniknięcie błędów w różnicy skali, zbiór testowy oraz treningowy został wcześniej przeskalowany.
 - Przedstawiono znaczenie cech za pomocą wykresu słupkowego.
   
![image](https://github.com/Jakub-Drabikowski/Machine-learning-badanie-wytrzymalosci/assets/83064196/f14bf155-b1eb-4bae-949d-dc22635aa968)

## Podsumowanie

Projekt pozwolił na zastosowanie modelu uczenia maszynowego do przewidywania wytrzymałości betonu na podstawie różnych czynników. Wizualizacje oraz oceny modelu umożliwiają lepsze zrozumienie wpływu poszczególnych komponentów na wytrzymałość betonu na ściskanie. Najważniejszy wniosek jest taki, że największy wpływ na wytrzymałość betonu ze wszystkich składników ma cement oraz wiek betonu.
