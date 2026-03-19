# 🎯 Hackathon IBM - Use Case 3 : Assistant AFE (Aide aux Frais d'Études)

## 📋 Contexte du cas d'usage

### Qu'est-ce que l'AFE ?

L'**Aide aux Frais d'Études (AFE)** est une aide financière versée par EDF aux salariés pour soutenir les études supérieures de leurs enfants.

**Montant** : 183,20€ par mois  
**Durée** : Jusqu'à 60 mois (5 ans) - 84 mois (7 ans) si handicap

### Le problème à résoudre

Actuellement, les gestionnaires RH doivent :
1. 📄 Recevoir et lire manuellement les certificats de scolarité (PDF)
2. ✍️ Extraire les informations (dates, formation, établissement, code RNCP)
3. 🔍 Vérifier l'éligibilité selon des règles complexes
4. 🧮 Calculer les montants
5. 📧 Générer les réponses

**Problèmes** :
- ⏱️ Processus long et répétitif
- ❌ Risques d'erreurs de calcul
- 📊 Règles métier complexes

---

## 🎯 Votre mission

Créer un **assistant intelligent** avec IBM Watsonx Orchestrate qui automatise la vérification d'éligibilité AFE.

### Objectifs

1. **Extraire automatiquement** les informations des certificats de scolarité (PDF)
2. **Vérifier les codes RNCP** sur France Compétences
3. **Calculer l'éligibilité** selon les règles AFE
4. **Générer un rapport** clair pour le salarié

---

## 🤖 Votre allié : Bob, l'assistant IA

### Qui est Bob ?

**Bob** est votre assistant IA personnel pendant ce hackathon ! Il est là pour vous aider à réussir.

### Ce que Bob peut faire pour vous :

- 💬 **Répondre à vos questions** sur Watsonx Orchestrate, Python, ou le cas d'usage AFE
- 📄 **Lire et analyser des documents** (PDF, documentation, code)
- 🔍 **Faire des recherches** sur internet pour vous
- 💻 **Vous assister dans le code** (debugging, suggestions, explications)
- 🎯 **Vous guider** dans votre approche et architecture
- 📚 **Expliquer les concepts** techniques ou métier

### Comment utiliser Bob efficacement ?

**Posez-lui des questions claires** :
- ❌ "Comment faire ?"
- ✅ "Comment extraire la date de début d'une formation depuis un PDF avec Python ?"

**Demandez-lui de lire des documents** :
- "peux-tu lire ce document AFE et m'expliquer les règles d'éligibilité ?"
- "analyse ce code et dis-moi s'il y a des erreurs"

**Utilisez-le pour débugger** :
- "mon agent ne répond pas correctement, voici mon code YAML..."
- "j'ai cette erreur Python, comment la corriger ?"

**Demandez des conseils** :
- "quelle est la meilleure approche pour vérifier les codes RNCP ?"
- " comment structurer mon agent pour ce cas d'usage ?"

### 💡 Astuce

Bob est particulièrement utile pour :
- Comprendre la documentation Watsonx Orchestrate
- Analyser les documents AFE fournis
- Trouver des exemples de code
- Résoudre des problèmes techniques

**N'hésitez pas à lui demander de l'aide à tout moment !**

---

## 📚 Règles d'éligibilité AFE (simplifiées)

### Conditions principales

1. **Ancienneté** : 1 an de présence continue à EDF
2. **Âge limite** : 
   - 26 ans (standard)
   - 28 ans (si handicap)
3. **Durée maximale** :
   - 60 mois (standard)
   - 84 mois (si handicap)
4. **Formation éligible** :
   - Diplôme d'État
   - Formation inscrite au RNCP
   - Diplôme visé par le Ministère
5. **Localisation** : France, UE ou AELE uniquement

### Informations à extraire du certificat

- Nom de la formation
- Établissement d'enseignement
- Date de début de formation
- Date de fin de formation
- Code RNCP (si présent)

---

## 🛠️ Technologies à utiliser

### IBM Watsonx Orchestrate

**Documentation officielle** : https://developer.watson-orchestrate.ibm.com/

Watsonx Orchestrate vous permet de créer des agents conversationnels intelligents qui peuvent :
- 💬 Dialoguer en langage naturel
- 📄 Lire et analyser des documents (PDF)
- 🔧 Utiliser des outils personnalisés
- 🤖 Automatiser des processus métier

---

## 🚀 Approches possibles

Il existe **plusieurs façons** de résoudre ce cas d'usage. À vous de choisir l'approche qui vous convient le mieux !

### Approche exemple : LLM-First (Recommandée pour débutants)

Laisser le LLM (Granite) faire le maximum de travail :
- Le LLM lit le PDF et extrait les informations
- Le LLM fait les calculs d'éligibilité
- Vous créez seulement un outil pour les règles métier complexes

**Avantages** : Simple, rapide à développer  
**Inconvénients** : Moins de contrôle sur la précision

💡 **Conseil** : Demandez à Bob de vous expliquer cette approche en détail !

---

## 🔍 Vérification des codes RNCP

### Qu'est-ce que le RNCP ?

Le **Répertoire National des Certifications Professionnelles** est une base de données officielle des certifications reconnues par l'État français.

### Où trouver les codes RNCP ?

**Site officiel** : https://www.francecompetences.fr/recherche/rncp/

Vous pouvez :
- Rechercher un code RNCP spécifique
- Vérifier si une formation est active ou inactive
- Obtenir des informations sur la certification

### Comment vérifier un code RNCP ?

Plusieurs options :
1. **Recherche web** : Utiliser une API de recherche (Tavily, Google, etc.)
2. **API France Compétences** : Si disponible
3. **Base de données locale** : Télécharger et indexer les codes RNCP

💡 **Astuce** : Demandez à Bob de faire une recherche sur France Compétences pour vous montrer comment ça marche !

---

## 📦 Ce que vous devez créer

### 1. Un Agent Watsonx Orchestrate

Fichier YAML qui définit :
- Le comportement de l'agent
- Les instructions pour l'agent
- Les outils disponibles
- Le workflow de traitement

### 2. Des Outils (Tools)

Selon votre approche, créez des outils pour :
- Calculer l'éligibilité AFE
- Vérifier les codes RNCP
- Extraire les données des PDF (optionnel)

---

## 🎓 Ressources utiles

### Documentation Watsonx Orchestrate

- **Guide principal** : https://developer.watson-orchestrate.ibm.com/
- **Création d'agents** : https://developer.watson-orchestrate.ibm.com/docs/agents
- **Création d'outils** : https://developer.watson-orchestrate.ibm.com/docs/tools
- **Exemples** : https://developer.watson-orchestrate.ibm.com/docs/examples

### Ressources AFE

- **France Compétences** : https://www.francecompetences.fr/
- **Recherche RNCP** : https://www.francecompetences.fr/recherche/rncp/


## 💡 Conseils pour réussir

### 1. Commencez simple

Ne cherchez pas à tout faire parfaitement du premier coup :
- Commencez par un agent qui pose des questions
- Ajoutez progressivement les fonctionnalités
- Testez régulièrement

**💬 Demandez à Bob** : "Comment commencer mon agent AFE de manière simple ?"

### 2. Utilisez le LLM intelligemment

Le LLM Granite est puissant :
- Il peut lire et comprendre des PDF
- Il peut faire des calculs simples
- Il peut structurer des réponses

**💬 Demandez à Bob** : "Quelles sont les capacités du LLM Granite pour lire des PDF ?"

**💬 Demandez à Bob** : "Peux-tu m'expliquer les règles AFE en détail via les documents du use case ?"

### 4. N'hésitez pas à demander de l'aide

**Bob est là pour vous !** Utilisez-le comme :
- 📚 Un tuteur pour comprendre les concepts
- 🔍 Un chercheur pour trouver des informations
- 💻 Un pair-programmer pour débugger
- 🎯 Un coach pour vous guider

---

## 🚀 Pour démarrer

1. **Lisez la documentation** : https://developer.watson-orchestrate.ibm.com/

2. **Demandez à Bob de vous aider** :
   - "Bob, peux-tu m'expliquer comment créer un agent Watsonx Orchestrate ?"
   - "Bob, montre-moi un exemple d'agent simple"

3. **Expérimentez !**

---

## 📞 Support

- **Bob** : Votre assistant IA personnel (disponible 24/7)
- **Documentation** : https://developer.watson-orchestrate.ibm.com/
- **Mentors** : Disponibles pendant le hackathon

---

## 🎉 Bonne chance !

N'oubliez pas : **Bob est votre meilleur allié** pour ce hackathon. Utilisez-le intelligemment et vous réussirez ! 🚀# hackaton-use-case-3
