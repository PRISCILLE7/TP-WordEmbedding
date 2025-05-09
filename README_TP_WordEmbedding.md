# TP - Word Embedding avec Gensim & NLTK

Projet réalisé dans le cadre du TP sur le **plongement lexical des mots** (word embedding)  
Master 2 IFI – Traitement Automatique du Langage Naturel  
Enseignant : Ahmed Hamdi

## Objectifs pédagogiques

Ce TP a pour but de manipuler des représentations vectorielles des mots à l'aide de modèles Word2Vec, en trois parties :

1. Utilisation d’un modèle Word2Vec pré-entraîné.
2. Entraînement d’un modèle Word2Vec à partir d’un article Wikipédia.
3. Application à l’analyse de sentiments.

---

## Technologies utilisées

- Python 3
- Gensim
- NLTK
- BeautifulSoup (bs4)
- Matplotlib / Scikit-learn

---

## Contenu du projet

- `word_embedding_tp.ipynb` : Notebook principal du TP.
- Téléchargement automatique du modèle `word2vec-google-news-300`.

---

## Étapes du TP

### I. Utilisation d’un modèle Word2Vec pré-entraîné

- Chargement du modèle `word2vec-google-news-300` via Gensim.
- Analyse de proximité sémantique entre mots :
  - Mots similaires à "computer", "software", ou un prénom.
  - Identification d’un mot intrus.
  - Opérations sémantiques : capitale du Chili, participe passé de "buy", etc.

### II. Entraînement d’un modèle Word2Vec personnalisé

- Extraction et parsing de la page Wikipédia [Computer](https://en.wikipedia.org/wiki/Computer).
- Nettoyage et segmentation du texte.
- Suppression des stopwords avec `nltk.corpus.stopwords`.
- Entraînement du modèle avec Gensim.
- Comparaison des similarités avec celles du modèle pré-entraîné.

###  III. Analyse de sentiments

- Calcul de la **polarité lexicale** d’un mot avec NLTK.
- Représentation vectorielle de phrases selon la polarité des mots.
- Proposition d’une fonction de classification **binaire (positif / négatif)** des phrases selon leur vecteur moyen pondéré.

---

## Exemples de résultats

- **Similaires à "computer" (pré-entraîné)** : hardware, pc, workstation, ...
- **Similaires à "computer" (modèle entraîné)** : science, system, input, ...
- **Similarité "computer" vs "software"** : proche de 0.7 (pré-entraîné), varie avec ton modèle

---

## Auteur

Priscille Ebwala  
Université Nationale du Vietnam – IFI  
Email : ebwalette@gmail.com

---

Ce projet est à but pédagogique dans le cadre du module de **traitement du langage naturel**.