# Bioinformatica-primo-progetto
primo progetto di prova
import pandas as pd

# Carico il dataset
df = pd.read_csv("dataset.csv")

# Mostro le prime righe
print("Prime righe del dataset:")
print(df.head())

# Calcolo media dei valori
media = df["valore"].mean()
print("\nMedia dei valori:", media)
