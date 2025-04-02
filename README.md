# Analyseur d'Émotions avec DeepFace

Ce module utilise la bibliothèque `DeepFace` pour analyser des images et détecter les émotions dominantes.

## Pré-requis

1. Python 3.x
2. Installer la bibliothèque `DeepFace`:
    ```bash
    pip install deepface
    ```

## Utilisation

Vous pouvez télécharger et exécuter le notebook pour analyser une image et détecter l'émotion dominante. 

[Télécharger le notebook](emotion.ipynb)
## Explication du Code

1. **Importation de la bibliothèque**:
    ```python
    from deepface import DeepFace
    ```

2. **Définition de l'URL de l'image**:
    ```python
    image_url = "https://as2.ftcdn.net/jpg/02/46/14/95/1000_F_246149573_1dbnEopMZjSflWG4ZvojXhVVV8cTewTW.jpg"
    ```

3. **Analyse de l'image**:
    ```python
    results = DeepFace.analyze(image_url, actions=['emotion'])
    ```

4. **Traitement des résultats**:
    - Si le résultat est une liste, on extrait le premier élément.
    - Sinon, on utilise directement le résultat.

5. **Extraction de l'émotion dominante**:
    ```python
    dominant_emotion = result['dominant_emotion']
    ```

6. **Affichage de l'émotion dominante**:
    ```python
    print(f"Emotion dominante: {dominant_emotion}")
    ```

7. **Gestion des exceptions**:
    ```python
    except Exception as e:
        print(f"Erreur lors de l'analyse de l'image {image_url}: {e}")
    ```

