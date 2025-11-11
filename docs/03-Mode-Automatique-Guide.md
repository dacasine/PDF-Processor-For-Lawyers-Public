---
layout: default
title: Mode Automatique - Guide Détaillé
nav_order: 4
---

# ⚡ Mode Automatique - Guide Détaillé

Le **Mode Automatique** traite un dossier entier de PDF en une seule opération, idéal pour gagner du temps sur de gros volumes.

---

## 🎯 Quand Utiliser le Mode Automatique ?

- Traitement de dizaines ou centaines de PDF
- Fichiers déjà numérotés et nommés selon une convention
- Besoin de traiter rapidement un dossier complet
- Paramètres identiques pour tous les documents

---

## 📋 Prérequis

### Convention de Nommage

**Format obligatoire** :
```
[Numéro].[Description].pdf
```

**Exemples valides** :
```
1.Contrat de vente.pdf
2.Facture n°12345.pdf
3.Courrier recommandé du 15 janvier.pdf
10.Annexe - Conditions générales.pdf
1.1.Sous-pièce A.pdf
```

**Exemples invalides** :
```
❌ Contrat de vente.pdf (pas de numéro)
❌ 1-Contrat de vente.pdf (tiret au lieu du point)
❌ Pièce 1.pdf (le point est après "Pièce", pas après le numéro)
```

### Structure du Dossier

**Organisation recommandée** :
```
MonDossier/
├── 1.Document A.pdf
├── 2.Document B.pdf
├── 3.Document C.pdf
├── 4.Document D.pdf
└── 5.Document E.pdf
```

**Résultat après traitement** :
```
MonDossier/
├── 1.Document A.pdf (original)
├── 2.Document B.pdf (original)
├── ...
└── _Traité/
    ├── 1_Document_A.pdf (traité)
    ├── 2_Document_B.pdf (traité)
    ├── ...
    └── bordereau.pdf
```

---

## 📝 Interface du Mode Automatique

### Section 1 : Informations du Dossier

#### Cabinet d'avocat
- **Obligatoire** : Non, mais recommandé
- **Format** : Texte libre
- **Exemple** : `Cabinet Dupont & Associés`
- **Usage** : Apparaît sur tous les documents et dans le bordereau

#### Désignation de l'affaire
- **Obligatoire** : Oui
- **Format** : Texte libre
- **Exemple** : `Dupont c/ Martin - RG 2024/123`
- **Usage** : Nom du sous-dossier de sortie + en-tête des documents

---

### Section 2 : Type de Pièce

Sélectionnez le type qui s'appliquera à **tous** les documents :

| Type | Description | Usage |
|------|-------------|--------|
| **Pièce** | Document numéroté standard | Pièces à conviction, documents probatoires |
| **Annexe** | Annexe à un document principal | Documents complémentaires |
| **Document** | Document non tamponné | Brouillons, notes internes |
| **Exhibit** | Pour procédures internationales | Procédures en anglais |

**Note** : Impossible de mélanger plusieurs types en mode automatique. Utilisez le mode manuel si nécessaire.

---

### Section 3 : Pagination

#### Activer la pagination automatique
- ✅ **Activée** : Chaque page est numérotée
- Format : `Page 1/10`, `Page 2/10`, etc.
- Position : En bas à droite de chaque page

#### Terme pour "Page"
Personnalisez selon la langue :
- **Français** : `Page`, `P.`
- **Allemand** : `Seite`, `S.`
- **Italien** : `Pagina`, `Pag.`
- **Anglais** : `Page`, `Pg.`

**Exemple** : Si vous mettez `P.`, le résultat sera `P. 1/10`.

---

### Section 4 : Personnalisation

#### Afficher texte courbe autour des cercles
- ✅ **Activé** : Le texte suit la courbure des cercles
- ❌ **Désactivé** : Texte horizontal

**Conseil** : Le texte courbe est plus esthétique mais peut être moins lisible sur certains PDF.

#### Mention de partie

Sélectionnez la partie qui dépose les pièces :

| Mention | Signification | Langue |
|---------|---------------|--------|
| **Aucune** | Pas de mention | - |
| **DEM** | Demandeur | Français |
| **DÉF** | Défendeur | Français |
| **REQ** | Requérant | Français |
| **INT** | Intervenant | Français |
| **BEKL.** | Beklagte (Défendeur) | Allemand |
| **KL.** | Kläger (Demandeur) | Allemand |
| **Personnalisé** | Votre propre abréviation | Toutes |

**Mention personnalisée** :
- Maximum 6 caractères recommandé
- Exemples : `PLT`, `PLA`, `APP`, `1ER DÉF`

---

## 🎬 Processus de Traitement

### Étape 1 : Préparation des Fichiers

1. **Créez un dossier** pour votre affaire
2. **Nommez vos PDF** selon le format `[Numéro].[Description].pdf`
3. **Placez tous les PDF** dans ce dossier
4. **Vérifiez** que tous les noms sont corrects

**Astuce** : Utilisez un outil de renommage en masse si vous avez beaucoup de fichiers.

### Étape 2 : Configuration

1. Ouvrez **Mode Automatique**
2. Renseignez **Cabinet** (optionnel)
3. Renseignez **Désignation de l'affaire** (obligatoire)
4. Sélectionnez **Type de pièce** (Pièce par défaut)
5. Choisissez **Mention de partie** si nécessaire
6. Configurez **Pagination** (activée par défaut)
7. Ajustez **Personnalisation** selon vos préférences

### Étape 3 : Sélection du Dossier

1. Cliquez sur **"Parcourir..."**
2. Naviguez jusqu'à votre dossier
3. Sélectionnez-le
4. Le chemin s'affiche sous le bouton

**Important** : Sélectionnez le dossier **contenant** les PDF, pas un PDF individuel.

### Étape 4 : Traitement

1. Vérifiez tous les paramètres
2. Cliquez sur **"Traiter les documents"**
3. Une barre de progression s'affiche
4. **Ne fermez pas** l'application pendant le traitement

**Durée** :
- ~2-5 secondes par PDF
- 10 PDF = ~30 secondes
- 100 PDF = ~5 minutes

### Étape 5 : Vérification des Résultats

Les fichiers traités se trouvent dans :
```
VotreDossier/_Traité/
```

**Contenu** :
- Tous les PDF traités (numérotés, paginés, tamponnés)
- Un fichier `bordereau.pdf` récapitulatif
- Les PDF originaux restent **intacts** dans le dossier principal

---

## 💡 Cas d'Usage Avancés

### 1. Gros Volumes (100+ PDF)

**Recommandations** :
- Traitez par lots de 50-100 PDF
- Vérifiez l'espace disque disponible
- Ne lancez pas d'autres applications gourmandes

**Astuce** : Créez des sous-dossiers thématiques et traitez-les séparément.

### 2. Numérotation Hiérarchique

**Format** : `1.1`, `1.2`, `2.1`, `2.2.1`

**Exemple** :
```
1.Contrat principal.pdf
1.1.Annexe A.pdf
1.2.Annexe B.pdf
2.Facture.pdf
2.1.Détail de facturation.pdf
```

**Résultat** : Le bordereau affiche la hiérarchie correctement.

### 3. Numérotation Non Séquentielle

**Format** : `1`, `3`, `5`, `10`, `15`

**Exemple** :
```
1.Introduction.pdf
3.Développement.pdf (pièce 2 manquante)
5.Conclusion.pdf (pièce 4 manquante)
```

**Note** : L'application traite les numéros tels quels, sans validation de séquence.

### 4. Lettres au Lieu de Numéros

**Format** : `A`, `B`, `C`

**Exemple** :
```
A.Assignation.pdf
B.Conclusions.pdf
C.Pièces.pdf
```

**Résultat** : Fonctionne parfaitement, le bordereau affiche A, B, C.

---

## ✅ Bonnes Pratiques

### Avant le Traitement

1. **Vérifiez le nommage** :
   ```bash
   # Bon
   1.Document.pdf

   # Mauvais
   1-Document.pdf
   Document 1.pdf
   1.pdf
   ```

2. **Testez avec quelques fichiers** :
   - Créez un sous-dossier de test
   - Copiez 3-5 PDF dedans
   - Traitez ce sous-dossier
   - Vérifiez le résultat

3. **Sauvegardez les originaux** :
   - L'application ne modifie pas les originaux
   - Mais une sauvegarde externe est toujours recommandée

### Pendant le Traitement

- ⏱️ **Patience** : Ne fermez pas l'application
- 💻 **Performance** : Évitez les tâches gourmandes
- 📊 **Progression** : Surveillez la barre de progression

### Après le Traitement

1. **Vérification visuelle** :
   - Ouvrez quelques PDF traités aléatoirement
   - Vérifiez les tampons et la pagination
   - Contrôlez le bordereau

2. **Organisation** :
   - Renommez `_Traité` si nécessaire
   - Archivez ou supprimez les originaux

3. **Distribution** :
   - Partagez le dossier `_Traité` avec votre client/tribunal
   - Le bordereau fait office de table des matières

---

## 🎨 Personnalisation Avancée

### Réglages Globaux (Onglet Réglages)

**Police** :
- Impacte la lisibilité des tampons
- Polices sans-serif recommandées : Arial, Calibri
- Polices serif pour un style classique : Georgia, Times

**Couleurs** :
- **Pièce** : Couleur du cercle et du numéro
- **Pagination** : Couleur des numéros de page
- **Recommandation** : Contraste fort (ex : noir/rouge sur fond blanc)

**Prévisualisation** :
- Testez avec un seul PDF avant de tout traiter
- Ajustez les couleurs si nécessaire

---

## ⚠️ Limites et Contraintes

### Nommage Strict

- ❌ **Pas de flexibilité** sur le format `[Numéro].[Description].pdf`
- ❌ **Impossible** de mélanger différents formats dans un même dossier
- ✅ **Solution** : Renommez en masse avant traitement

### Paramètres Uniformes

- Tous les PDF reçoivent les **mêmes paramètres**
- Impossible d'avoir des types de pièces mixtes
- ✅ **Solution** : Utilisez le mode manuel pour plus de contrôle

### Sous-dossiers

- L'application ne traite **pas** les sous-dossiers récursivement
- Seuls les PDF à la racine du dossier sélectionné sont traités
- ✅ **Solution** : Aplatissez votre structure si nécessaire

---

## 🔧 Dépannage

### "Aucun fichier trouvé"

**Causes possibles** :
- Le dossier est vide
- Les fichiers ne suivent pas le format `[Numéro].[Description].pdf`
- Les fichiers sont dans des sous-dossiers

**Solutions** :
1. Vérifiez que les PDF sont bien dans le dossier sélectionné
2. Contrôlez le nommage des fichiers
3. Déplacez les PDF des sous-dossiers vers la racine

### "Erreur de traitement sur fichier X"

**Causes possibles** :
- PDF corrompu
- PDF protégé par mot de passe
- Permissions insuffisantes

**Solutions** :
1. Ouvrez le PDF dans Adobe Reader pour vérifier
2. Déverrouillez le PDF si protégé
3. Copiez le PDF dans un dossier où vous avez les droits

### Le bordereau est incomplet

**Causes possibles** :
- Certains PDF ont échoué
- Numérotation invalide

**Solutions** :
1. Consultez le log d'erreur
2. Retraitez les PDF problématiques en mode manuel
3. Regénérez le bordereau complet

### Les tampons ne sont pas visibles

**Causes possibles** :
- Couleur trop claire
- PDF avec fond sombre

**Solutions** :
1. Allez dans **Réglages**
2. Changez la couleur du tampon (rouge vif recommandé)
3. Retraitez les documents

---

## 🎓 Exercice Pratique

**Objectif** : Traiter un dossier complet automatiquement

**Préparation** :
1. Créez un dossier `Test-Auto`
2. Ajoutez 10 PDF et nommez-les :
   ```
   1.Introduction.pdf
   2.Contexte.pdf
   3.Analyse.pdf
   ...
   10.Conclusion.pdf
   ```

**Configuration** :
- Cabinet : `Votre cabinet`
- Affaire : `Test automatique - 2024`
- Type : `Pièce`
- Mention : `DEM`
- Pagination : Activée

**Traitement** :
1. Parcourez et sélectionnez `Test-Auto`
2. Cliquez sur "Traiter"
3. Attendez la fin

**Vérification** :
1. Ouvrez `Test-Auto/_Traité/`
2. Vérifiez quelques PDF
3. Consultez le bordereau
4. Notez le temps de traitement

---

## 🚀 Optimisation des Performances

### Fichiers Volumineux

**Problème** : PDF de 10+ MB

**Solutions** :
- Compressez les PDF avant traitement
- Utilisez des outils comme Adobe Acrobat ou PDF24
- Visez 1-5 MB par fichier

### Nombreuses Pages

**Problème** : PDF de 100+ pages

**Impact** : Traitement plus long

**Recommandation** :
- Pagination peut être désactivée pour gagner du temps
- Traitez en priorité les documents importants

### Système Lent

**Symptômes** : Application gelée, ventilateurs bruyants

**Solutions** :
- Fermez les autres applications
- Attendez la fin complète du traitement
- Redémarrez l'ordinateur si nécessaire

---

**Suite** : Consultez la [FAQ](./04-FAQ-Depannage.md) pour plus d'informations.
