---
layout: default
title: Mode Manuel - Guide Détaillé
nav_order: 3
---

# 📄 Mode Manuel - Guide Détaillé

Le **Mode Manuel** vous permet de traiter des fichiers PDF individuellement avec un contrôle total sur chaque paramètre.

---

## 🎯 Quand Utiliser le Mode Manuel ?

- Traitement de quelques PDF seulement
- Besoin de paramètres différents pour chaque fichier
- Documents avec des numérotations spécifiques
- Création de bordereaux manuels personnalisés

---

## 📋 Interface du Mode Manuel

### Section 1 : Informations du Dossier

#### Cabinet d'avocat
- **Objectif** : Identifie votre cabinet sur les documents
- **Format** : Texte libre
- **Exemple** : `Cabinet Dupont & Associés`
- **Optionnel** : Peut être laissé vide

#### Désignation de l'affaire
- **Objectif** : Identifie l'affaire traitée
- **Format** : Texte libre
- **Exemple** : `Dupont c/ Martin - RG 2024/123`
- **Recommandé** : Incluez le numéro RG pour traçabilité

---

### Section 2 : Liste des Pièces

#### Ajouter des PDF

**Bouton "Ajouter PDF"** :
1. Cliquez sur le bouton
2. Sélectionnez un ou plusieurs PDF
3. Les fichiers apparaissent dans la liste

**Liste des PDF** :
- Affiche tous les PDF ajoutés
- Ordre = ordre d'apparition dans le bordereau
- **Réorganiser** : Drag & drop (glisser-déposer)
- **Supprimer** : Clic droit → Supprimer

#### Paramètres par Fichier

Pour chaque PDF, configurez :

1. **Numéro de pièce**
   - Numéro unique pour cette pièce
   - Format libre : `1`, `1.1`, `A`, `I`, etc.
   - **Auto-incrémentation** : Par défaut, +1 automatique

2. **Désignation**
   - Description de la pièce
   - Exemple : `Contrat de vente`, `Facture n°12345`
   - Apparaît dans le bordereau

3. **Mention de partie**
   - **Aucune** : Pas de mention
   - **DEM** : Demandeur
   - **DÉF** : Défendeur
   - **REQ** : Requérant
   - **INT** : Intervenant
   - **BEKL.** : Beklagte (Allemand - Défendeur)
   - **KL.** : Kläger (Allemand - Demandeur)
   - **Personnalisé** : Votre propre abréviation

4. **Type de pièce**
   - **Pièce** : Document numéroté standard
   - **Annexe** : Annexe à un document principal
   - **Document** : Document non tamponné
   - **Exhibit** : Pour procédures anglophones

---

### Section 3 : Personnalisation

#### Type de pièce par défaut
Sélectionnez le type qui s'appliquera à tous les nouveaux PDF ajoutés.

#### Mention de partie par défaut
Choisissez la mention qui s'appliquera par défaut (peut être modifiée individuellement).

#### Pagination
- ✅ **Activée** : Chaque page est numérotée
- Format : `Page 1/10`, `Page 2/10`, etc.
- Position : En bas à droite

#### Terme pour "Page"
Personnalisez le mot affiché :
- Français : `Page`, `P.`
- Allemand : `Seite`, `S.`
- Italien : `Pagina`, `Pag.`
- Anglais : `Page`, `Pg.`

#### Format du bordereau
- **PDF** : Génère un fichier PDF
- **CSV** : Exporte en tableau Excel

#### Texte courbe
- ✅ **Activé** : Le texte suit la courbe des cercles
- ❌ **Désactivé** : Texte horizontal

---

## 🎬 Processus de Traitement

### Étape 1 : Préparation

1. Ouvrez l'onglet **Mode Manuel**
2. Renseignez le cabinet (optionnel)
3. Renseignez la désignation de l'affaire
4. Configurez les paramètres par défaut

### Étape 2 : Ajout des Fichiers

1. Cliquez sur **"Ajouter PDF"**
2. Sélectionnez vos fichiers (multi-sélection possible)
3. Les fichiers apparaissent avec :
   - Numéro auto-incrémenté
   - Nom du fichier comme désignation
   - Paramètres par défaut appliqués

### Étape 3 : Personnalisation

Pour chaque fichier :
1. **Modifiez le numéro** si nécessaire
2. **Ajustez la désignation** pour la rendre plus explicite
3. **Changez la mention de partie** si différente
4. **Modifiez le type** si ce n'est pas une "Pièce"

**Astuce** : Utilisez la touche Tab pour naviguer rapidement entre les champs.

### Étape 4 : Réorganisation (optionnel)

- **Glisser-déposer** les lignes pour changer l'ordre
- L'ordre dans la liste = ordre dans le bordereau
- Les numéros de pièce ne changent PAS automatiquement

### Étape 5 : Traitement

1. Vérifiez que tous les champs sont corrects
2. Cliquez sur **"Traiter les documents"**
3. Une barre de progression s'affiche
4. Attendez la fin du traitement

### Étape 6 : Résultats

Les fichiers traités sont enregistrés dans :
```
Documents/PDFProcessor/[Nom de l'affaire]/
├── 1_Contrat_de_vente.pdf
├── 2_Facture.pdf
├── 3_Courrier.pdf
└── bordereau.pdf (ou bordereau.csv)
```

---

## 💡 Cas d'Usage Avancés

### 1. Pièces avec Annexes

**Objectif** : Créer une pièce principale avec des annexes

**Configuration** :
```
Pièce 1 : "Contrat de vente" → Type: Pièce
Pièce 1.1 : "Annexe 1 - Conditions générales" → Type: Annexe
Pièce 1.2 : "Annexe 2 - Plan du bien" → Type: Annexe
Pièce 2 : "Facture" → Type: Pièce
```

**Résultat** : Les annexes sont visuellement liées à la pièce principale dans le bordereau.

### 2. Numérotation Romaine

**Configuration** :
```
Pièce I : "Assignation"
Pièce II : "Conclusions"
Pièce III : "Mémoire"
```

**Astuce** : Utilisez des lettres ou chiffres romains selon vos préférences.

### 3. Multiple Parties

**Scénario** : Dossier avec plusieurs intervenants

**Configuration** :
```
Pièce 1 - DEM : "Conclusions demandeur"
Pièce 2 - DÉF : "Conclusions défendeur"
Pièce 3 - INT : "Conclusions intervenant volontaire"
```

### 4. Documents Sans Numérotation

**Configuration** :
- Type : **Document**
- Numéro : Peut être laissé vide
- Le PDF est traité mais sans tampon de numérotation

**Usage** : Courriers, notes internes, brouillons.

---

## ✅ Bonnes Pratiques

### Nommage des Fichiers

**Avant traitement** :
- Noms de fichiers clairs et descriptifs
- Évitez les caractères spéciaux : `/ \ : * ? " < > |`
- Préférez les tirets ou underscores : `Contrat-de-vente.pdf`

### Organisation

1. **Ordre logique** : Organisez les pièces par thème ou chronologie
2. **Numérotation cohérente** : Ne sautez pas de numéros sans raison
3. **Désignations précises** : Soyez explicite sur le contenu
4. **Mentions cohérentes** : Une partie = une mention

### Vérification

Avant de traiter :
- ✅ Tous les numéros sont uniques
- ✅ Toutes les désignations sont remplies
- ✅ L'ordre est correct
- ✅ Les mentions de partie sont appropriées

---

## 🎨 Personnalisation Avancée

### Réglages (Onglet Réglages)

**Police** :
- Impact sur la lisibilité des tampons
- Polices recommandées : Arial, Calibri, Georgia

**Couleurs** :
- **Pièce** : Couleur du tampon de numérotation
- **Pagination** : Couleur des numéros de page
- **Contraste** : Assurez-vous que les couleurs ressortent sur vos PDF

### Mentions Personnalisées

Pour créer votre propre mention :
1. Sélectionnez **"Personnalisé"**
2. Un champ apparaît
3. Entrez votre abréviation (ex : `PLT`, `PLA`, `APP`)
4. Maximum 6 caractères recommandé

---

## ⚠️ Limites et Contraintes

### Formats Supportés
- ✅ **PDF** : Uniquement
- ❌ **Word, Excel, Images** : Doivent être convertis en PDF d'abord

### Taille des Fichiers
- **Maximum recommandé** : 50 MB par PDF
- **Pages** : Illimité, mais performances réduites au-delà de 500 pages

### Encodage
- Les PDF doivent être valides et non corrompus
- Les PDF protégés par mot de passe doivent être déverrouillés d'abord

---

## 🔧 Dépannage

### Le PDF n'est pas ajouté
- **Cause** : Fichier corrompu ou protégé
- **Solution** : Essayez de l'ouvrir dans Adobe Reader pour vérifier

### Le traitement échoue
- **Cause** : Permissions insuffisantes, disque plein
- **Solution** : Vérifiez l'espace disque et les droits d'écriture

### Le bordereau est vide
- **Cause** : Aucune pièce n'a été ajoutée
- **Solution** : Ajoutez au moins un PDF avant de traiter

---

## 🎓 Exercice Pratique

**Objectif** : Créer un dossier de 5 pièces avec annexes

**Instructions** :
1. Ajoutez 5 PDF de votre choix
2. Configurez :
   - Pièce 1-2 : DEM
   - Pièce 3 : DÉF
   - Pièce 4 : Type Document (sans numéro)
   - Pièce 5 : Type Annexe
3. Activez la pagination
4. Générez le bordereau en PDF
5. Vérifiez les résultats

---

**Suite** : Découvrez le [Mode Automatique](./03-Mode-Automatique-Guide.md) pour traiter des dossiers entiers.
