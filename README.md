# Bioinformatica-primo-progetto
primo progetto di prova
print("Inserisci la prima stringa:")
s1 = input()

print("Inserisci la seconda stringa:")
s2 = input()

best = ""               # sottostringa migliore
best_len = 0            # lunghezza della migliore trovata

# ciclo su tutte le posizioni di s1
for i in range(len(s1)):
    # ciclo su tutte le posizioni di s2
    for j in range(len(s2)):

        k = 0           # quanto siamo avanzati nella sottostringa in corso

        # finché non usciamo dalle stringhe e i caratteri coincidono
        while (i + k < len(s1)) and (j + k < len(s2)) and (s1[i + k] == s2[j + k]):
            k += 1

        # se ho trovato una sottostringa più lunga della migliore
        if k > best_len:
            best_len = k
            best = s1[i:i+k]   # questo slicing È AMMESSO (solo costruzione, non ricerca)

# Visualizzazione del risultato
print(best)
