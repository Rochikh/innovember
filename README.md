# Outils IA pour l'enseignement supérieur

Présentation interactive sur les outils IA pour l'enseignement supérieur par Rochane Kherbouche.

## 🌐 Site en ligne

Le site est hébergé sur : [https://ia-innovember.rochane.fr](https://ia-innovember.rochane.fr)

## 📋 Configuration de l'hébergement

Ce site est hébergé via GitHub Pages avec un domaine personnalisé.

### Étape 1 : Activer GitHub Pages

1. Allez dans les paramètres du dépôt GitHub
2. Dans la section "Pages" (menu de gauche)
3. Configurez :
   - **Source** : Deploy from a branch
   - **Branch** : `claude/host-on-ia-domain-011CUpEbTQqghKcEiDEbtZpT`
   - **Folder** : `/ (root)`
4. Cliquez sur "Save"

### Étape 2 : Configurer le DNS

Vous devez configurer les enregistrements DNS chez votre fournisseur de domaine (rochane.fr) :

#### Option A : Utiliser un enregistrement CNAME (Recommandé)

Ajoutez un enregistrement CNAME :
```
Type: CNAME
Nom: ia-innovember
Valeur: Rochikh.github.io
TTL: 3600 (ou Auto)
```

#### Option B : Utiliser des enregistrements A

Si CNAME ne fonctionne pas, utilisez ces enregistrements A :
```
Type: A
Nom: ia-innovember
Valeur: 185.199.108.153
```

Ajoutez également ces trois autres enregistrements A :
- `185.199.109.153`
- `185.199.110.153`
- `185.199.111.153`

### Étape 3 : Attendre la propagation DNS

- La propagation DNS peut prendre de quelques minutes à 48 heures
- Vous pouvez vérifier l'état avec : `nslookup ia-innovember.rochane.fr`

### Étape 4 : Activer HTTPS (optionnel mais recommandé)

1. Une fois le domaine configuré, retournez dans les paramètres GitHub Pages
2. Cochez "Enforce HTTPS"
3. Le certificat SSL sera généré automatiquement (peut prendre quelques minutes)

## 🔧 Développement local

Pour tester le site localement :

```bash
# Option 1 : Avec Python 3
python3 -m http.server 8000

# Option 2 : Avec Python 2
python -m SimpleHTTPServer 8000

# Option 3 : Avec Node.js (npx)
npx http-server -p 8000
```

Puis ouvrez votre navigateur sur `http://localhost:8000`

## 📂 Structure du projet

```
innovember/
├── index.html          # Présentation interactive
├── CNAME              # Configuration du domaine personnalisé
└── README.md          # Ce fichier
```

## 🛠️ Contenu de la présentation

La présentation couvre 4 problèmes et leurs solutions :

1. **NotebookLM** - Synthèse d'articles
2. **Napkin** - Visualisation de concepts
3. **Google AI Studio** - Outils personnalisés
4. **Open Source** - Indépendance technologique

## 📝 Support

Pour toute question, contactez Rochane Kherbouche - Université de Lille

---

*Dernière mise à jour : Novembre 2025*
