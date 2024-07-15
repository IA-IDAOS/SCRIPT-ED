# Recherche d'Incidents et de Crises d'Entreprises en France

Ce projet contient un Jupyter Notebook conçu pour rechercher des incidents et des crises spécifiques d'entreprises en France à l'aide de mots clés prédéfinis. Le notebook utilise la bibliothèque `googlesearch-python` pour effectuer des recherches Google et extrait des informations pertinentes de chaque page trouvée.

## Table des Matières

- [Installation](#installation)
- [Utilisation](#utilisation)
- [Fonctionnalités](#fonctionnalités)
- [Contributions](#contributions)
- [Licence](#licence)

## Installation

### Prérequis

Assurez-vous d'avoir Python et Jupyter Notebook installés sur votre machine. Ce projet utilise les bibliothèques suivantes :

- `googlesearch-python`
- `beautifulsoup4`
- `requests`

### Étapes d'installation

1. Clonez ce repository GitHub :

    ```bash
    git clone https://github.com/IA-IDAOS/Script-ED-.git
    cd votre-repository
    ```

2. Installez les bibliothèques nécessaires :

    ```bash
    pip install googlesearch-python google-api-python-client beautifulsoup4 requests
    ```

## Utilisation

1. Lancez Jupyter Notebook :

    ```bash
    jupyter notebook
    ```

2. Ouvrez le fichier `ED.ipynb` dans l'interface Jupyter.

3. Exécutez chaque cellule du notebook pour effectuer les recherches Google pour une liste de mots-clés prédéfinis et afficher les résultats filtrés.

### Exemple de mots-clés

- "crise éthique entreprise en France juillet 2024"
- "action de boycott consommateurs en France en juillet 2024"
- "scandale de durabilité entreprise en France juillet 2024"
- etc.

## Fonctionnalités

### Fonction `extract_info`

Cette fonction prend une URL en entrée et retourne simplement l'URL. Elle envoie une requête GET à l'URL et utilise BeautifulSoup pour parser le contenu. Actuellement, le contenu de la page n'est pas utilisé, mais la fonction peut être modifiée pour extraire des informations spécifiques si nécessaire.

### Fonction `search_google`

Cette fonction effectue une recherche Google pour un mot-clé donné et retourne une liste de résultats uniques provenant de sites spécifiques. Elle :

- Filtre les résultats pour inclure uniquement ceux qui proviennent des domaines autorisés.
- Utilise un ensemble (set) pour stocker les URLs uniques et éviter les doublons.

### Recherche avancée avec `pandas`

Le notebook utilise pandas pour stocker et afficher les résultats de la recherche sous forme de DataFrame. La fonction `search_ao` :

- Combine la recherche Google pour plusieurs mots-clés.
- Filtre les résultats pour inclure uniquement les URLs valides appartenant aux domaines spécifiés.
- Affiche les résultats et les retourne sous forme de DataFrame.

## Contributions

Les contributions sont les bienvenues ! Pour proposer une modification, veuillez créer une branche de votre fork, y apporter vos changements, puis créer une pull request.

## Licence

Ce projet est sous licence MIT. Voir le fichier [LICENSE](LICENSE) pour plus de détails.
