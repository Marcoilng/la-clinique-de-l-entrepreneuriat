# Guide pour mettre à jour votre site Vercel

## Résumé de la situation

Vos modifications sont **déjà sur GitHub**. Le dernier commit est :
- **036d77b** - "Ajout du fichier .gitignore pour Ignorer les fichiers temporaires et système"

Cela signifie que Vercel devrait avoir automatiquement déployé ces modifications.

---

## Problème possible

Si vos modifications n'apparaissent pas sur le site, il y a deux causes possibles :

1. **Le déploiement automatique n'a pas encore terminé** (parfois prend quelques minutes)
2. **Votre navigateur affiche une version en cache** (version mémorisée)

---

## Solution : Forcer le redéploiement sur Vercel

### Étape 1 : Redeployer sur Vercel

1. Allez sur : https://vercel.com/dashboard
2. Cliquez sur votre projet : **la-clinique-de-l-entrepreneuriat**
3. Cliquez sur l'onglet **Deployments** (Déploiements)
4. Cliquez sur les **trois points (...)** à côté du dernier déploiement
5. Cliquez sur **Redeploy** (Redéployer)

### Étape 2 : Vider le cache du navigateur

Après le redéploiement :

1. Ouvrez votre site : https://la-clinique-de-l-entrepreneuriat.vercel.app/
2. Appuyez sur **F12** pour ouvrir les outils de développement
3. Faites un clic droit sur le bouton d'actualisation (🔄) en haut à gauche
4. Cliquez sur **"Vider le cache et actualiser"** (Empty Cache and Hard Reload)

---

## Comment éviter ce problème à l'avenir

Après avoir fait des modifications dans VSCode :

1. **Sauvegarder** le fichier (Ctrl+S)
2. **Ajouter** les modifications : `git add .`
3. **Commiter** avec un message : `git commit -m "Description de vos modifications"`
4. **Pousser** vers GitHub : `git push`

Vercel détectera automatiquement le nouveau commit et redéployera le site.

---

## Commandes Git utiles

```
bash
# Voir le statut des fichiers modifiés
git status

# Ajouter tous les fichiers modifiés
git add .

# Créer un commit
git commit -m "Votre message ici"

# Pousser vers GitHub
git push

# Voir l'historique des commits
git log --oneline
```

---

## Délai normal

- Après `git push`, Vercel commence le déploiement en **30-60 secondes**
- Le déploiement complet prend environ **1-2 minutes**
- Une fois terminé, vous verrez un point **vert** dans l'onglet Deployments
