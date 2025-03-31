# Bi-Clustering avec QUBIC2  

Ce projet utilise l'algorithme de bi-clustering [QUBIC2](https://github.com/OSU-BMBL/QUBIC2/tree/master/data) pour analyser des données filtrées après un test statistique avec une p-value de 5 %.  

## Compilation  

Le programme a été compilé avec `g++`.  

## Données d'entrée  

L'algorithme prend en entrée des données au format **TSV** après filtrage statistique.  

## Commande d'exécution  

Pour exécuter le bi-clustering, utilisez la commande suivante :  

```bash
./qubic -i ./data/filtered_melanoma_data.tsv -d -k 3 -f 1.00 -c 1.00 -o 200
```  

### Paramètres :  
- `-i` : fichier d'entrée (doit être au format TSV)  
- `-d` : active l'affichage des détails  
- `-k 3` : définit le nombre minimal de gènes par cluster  
- `-f 1.00` : paramètre de flexibilité  
- `-c 1.00` : seuil de corrélation  
- `-o 200` : nombre maximal de clusters générés  

## Fichiers de sortie  

L'algorithme produit deux fichiers :  
- **`.blocks`** : fichier contenant les résultats du bi-clustering (utilisé pour l'analyse).  
- **`.chars`** : fichier supplémentaire, non utilisé dans notre cas.  

