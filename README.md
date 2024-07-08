# MSAI_Vought_Project
Réalisation d'un projet sur Microsoft Azure AI qui permet d'analyser les sentiments des appels audios passés à la compagnie Vought

# Amélioration du Service Client et Optimisation des Processus Internes de Vought International

## Contexte
Vought International, leader mondial dans la gestion des super-héros, fait face à des défis croissants en matière de gestion des super-héros (Supes), de satisfaction client et de sécurité des informations. Avec l'augmentation des incidents impliquant les super-héros et des demandes croissantes des fans, Vought International doit moderniser ses opérations pour rester à la pointe de l'innovation.

## Mission
La mission de ce projet est d'analyser les principaux défis auxquels Vought International est confronté, basés sur les appels téléphoniques reçus par le service client, et de proposer des solutions innovantes en utilisant les services Azure AI. L'objectif est d'améliorer l'efficacité des opérations et de garantir une gestion fluide et sécurisée des activités.

## Principaux Points Identifiés
### Service Client
- Temps de réponse long aux questions et préoccupations des fans.
- Gestion inefficace des incidents signalés par les citoyens.
- Difficulté à fournir des informations précises et traduites dans plusieurs langues.

### Processus Internes
- Extraction manuelle et analyse laborieuse des informations des rapports d'incidents.
- Gestion inefficace des performances des super-héros et des ressources humaines.
- Risques accrus de fuite d'informations sensibles.

## Solution Proposée
Pour répondre aux défis identifiés, une solution intégrée utilisant plusieurs services Azure AI a été développée. La solution se compose des éléments suivants :

1. **Azure Speech to Text** : Convertit les fichiers audio des appels téléphoniques en texte, avec détection automatique de la langue pour gérer les appels dans différentes langues.
2. **Azure Translator** : Traduit les transcriptions en français pour assurer une réponse cohérente et compréhensible aux clients.
3. **Azure Text Analytics** : Analyse les sentiments des transcriptions traduites pour identifier la tendance des appels (positif, neutre, négatif) et classe les sentiments en "très positif" ou "très négatif" si le score de confiance est supérieur à 0.7. Extrait également les phrases clés pour identifier les sujets récurrents et les préoccupations des clients.

## Plan de Mise en Œuvre
1. **Configuration des Services Azure** :
   - Créer les ressources Azure nécessaires (Speech to Text, Translator, Text Analytics).
   - Configurer les clés API et les points de terminaison.

2. **Développement du Script** :
   - Écrire un script Python pour télécharger les fichiers audio depuis Azure Blob Storage, les transcrire, les traduire et analyser les sentiments.
   - Stocker les résultats dans des fichiers texte individuels et un fichier global.

3. **Intégration et Tests** :
   - Intégrer le script avec les services Azure.
   - Tester le script avec différents fichiers audio pour vérifier la précision des transcriptions, traductions et analyses de sentiments.

4. **Déploiement** :
   - Déployer le script dans un environnement de production.
   - Former le personnel sur l'utilisation des nouveaux outils et processus.

## Structure du Projet
```plaintext
root
│
├── README.md
├── requirements.txt
├── script.py
└── temp/

