# ValiNum + Django (Test Project)

Ce projet démontre l'intégration de la bibliothèque **ValiNum** dans un environnement **Django**. Il permet de valider et d'identifier les opérateurs mobiles de la République Démocratique du Congo (RDC) directement dans un formulaire web.



## 🌟 Points clés
- **Zéro dépendance NPM** : Utilisation du CDN pour une intégration légère.
- **Validation Temps Réel** : Retour visuel instantané pour l'utilisateur.
- **Sécurité** : Bouton de soumission désactivé tant que le numéro n'est pas conforme.

## 🛠️ Installation et Lancement

### 1. Prérequis
Assurez-vous d'avoir Python installé sur votre machine.

### 2. Configuration du projet
```bash
# Cloner le projet ou entrer dans le dossier
cd test-valinum-django

# Créer l'environnement virtuel
python -m venv venv

# Activer l'environnement
# Sur Windows :
venv\Scripts\activate
# Sur Mac/Linux :
source venv/bin/activate

# Installer Django
pip install django
```

### 3. Lancer l'application
```bash
python manage.py runserver
```
Rendez-vous ensuite sur `http://127.0.0.1:8000`

## 📂 Structure du Projet
```plaintext
test-valinum-django/
├── core/               # Application principale
│   ├── templates/      # Fichiers HTML
│   │   └── index.html  # Formulaire avec ValiNum JS
│   └── views.py        # Logique de navigation
├── config/             # Configuration Django (settings, urls)
└── manage.py           # Point d'entrée Django
```

## 💡 Comment ça marche ?
Le projet utilise le script de validation côté client pour améliorer l'expérience utilisateur.
```js
// Exemple d'utilisation dans le template
const data = ValiNum.validateDRC("0812345678");
console.log(data.operator); // "Vodacom"
console.log(data.isValid);  // true
```

## 🤝 Crédits
Bibliothèque de validation : <a href="https://www.npmjs.com/package/valinum">**`ValiNum`**</a> par <a href="https://github.com/fomadev/">fomadev</a>

Framework Web : **`Django`**