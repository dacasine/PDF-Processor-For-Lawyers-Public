---
layout: default
title: FAQ & Dépannage
nav_order: 5
---

# ❓ FAQ & Dépannage

Réponses aux questions fréquentes et solutions aux problèmes courants.

---

## 📱 Installation & Démarrage

### Windows - Avertissement SmartScreen

**Question** : Windows affiche "Windows a protégé votre PC"

**Réponse** :
1. Cliquez sur **"Informations complémentaires"**
2. Cliquez sur **"Exécuter quand même"**
3. L'application se lance normalement

**Explication** : C'est un avertissement standard pour les applications non signées par Microsoft. PDF Processor est sûr à utiliser.

---

### macOS - "L'application ne peut pas être ouverte"

**Question** : macOS bloque l'ouverture de l'application

**Réponse** :
1. **Clic droit** (ou Ctrl+Clic) sur l'application
2. Sélectionnez **"Ouvrir"**
3. Cliquez sur **"Ouvrir"** dans la fenêtre de confirmation

**Alternative** :
1. Allez dans **Préférences Système** → **Sécurité et confidentialité**
2. Onglet **"Général"**
3. Cliquez sur **"Ouvrir quand même"** à côté du message concernant PDF Processor

---

### L'application ne se lance pas

**Causes possibles** :
- ❌ Fichiers manquants ou corrompus
- ❌ Antivirus bloquant l'application
- ❌ Version incompatible

**Solutions** :
1. **Retéléchargez** l'application depuis la source officielle
2. **Désactivez temporairement** l'antivirus
3. **Vérifiez** que vous avez téléchargé la bonne version :
   - Windows x64 pour Intel/AMD
   - Windows ARM64 pour processeurs ARM
   - macOS ARM64 pour Apple Silicon (M1/M2/M3)

---

## 📄 Traitement de PDF

### "Impossible d'ouvrir le fichier PDF"

**Causes** :
- PDF corrompu
- PDF protégé par mot de passe
- Format non standard

**Solutions** :
1. **Testez le PDF** dans Adobe Reader
2. **Déverrouillez** le PDF s'il est protégé :
   - Outils en ligne : iLovePDF, SmallPDF
   - Adobe Acrobat : Document → Sécurité → Supprimer la sécurité
3. **Reconvertissez** le PDF s'il est corrompu

---

### "Le fichier ne suit pas le format requis"

**Contexte** : Mode automatique

**Format attendu** : `[Numéro].[Description].pdf`

**Exemples valides** :
```
✅ 1.Contrat.pdf
✅ 2.Facture n°123.pdf
✅ 10.Document important.pdf
✅ 1.1.Annexe A.pdf
```

**Exemples invalides** :
```
❌ Contrat.pdf (pas de numéro)
❌ 1-Contrat.pdf (tiret au lieu de point)
❌ 1 Contrat.pdf (espace au lieu de point)
❌ Piece 1.pdf (point après "Piece" au lieu d'après le numéro)
```

**Solution** :
1. Renommez manuellement les fichiers
2. Utilisez un outil de renommage en masse (Total Commander, Bulk Rename Utility)
3. Utilisez le **mode manuel** si le renommage est complexe

---

### Les tampons ne s'affichent pas

**Causes** :
- Couleur trop claire
- PDF avec fond coloré
- Type "Document" sélectionné

**Solutions** :
1. **Onglet Réglages** → Changez la couleur du tampon
   - Recommandé : Rouge vif (#FF0000) ou Noir (#000000)
2. **Vérifiez le type** : "Document" n'affiche pas de tampon
3. **Ouvrez le PDF dans un lecteur différent** (certains lecteurs ont des bugs d'affichage)

---

### La pagination n'apparaît pas

**Causes** :
- Pagination désactivée
- Couleur trop claire
- Position hors du PDF

**Solutions** :
1. **Activez la pagination** :
   - Mode Manuel : Cochez "Activer la pagination"
   - Mode Automatique : Cochez "Activer la pagination automatique"
2. **Changez la couleur** dans Réglages → Couleur Pagination
3. **Vérifiez le PDF original** : S'il a déjà une pagination, elle peut interférer

---

## 🗂️ Bordereau

### Le bordereau est vide

**Causes** :
- Aucune pièce ajoutée (Mode Manuel)
- Aucun fichier trouvé (Mode Automatique)
- Erreur lors de la génération

**Solutions** :
- **Mode Manuel** : Ajoutez au moins un PDF avant de traiter
- **Mode Automatique** : Vérifiez que le dossier contient des PDF correctement nommés
- **Format CSV** : Essayez le format PDF à la place

---

### Le bordereau ne liste pas tous les fichiers

**Causes** :
- Certains PDF ont échoué lors du traitement
- Nommage incorrect (Mode Automatique)

**Solutions** :
1. **Consultez les messages d'erreur** pendant le traitement
2. **Retraitez les fichiers manquants** individuellement
3. **Vérifiez le nommage** de tous les fichiers

---

### Le bordereau contient des caractères étranges

**Cause** : Problème d'encodage des caractères spéciaux

**Solution** :
1. **Évitez les caractères spéciaux** dans les désignations :
   - Évitez : `é, è, à, ô, ü, ñ` si problème
   - Utilisez : `e, a, o, u, n`
2. **Format CSV** : Ouvrez avec Excel/LibreOffice qui gère mieux l'encodage

---

## 🎨 Personnalisation

### Les couleurs ne changent pas

**Cause** : Modifications non sauvegardées

**Solution** :
1. **Onglet Réglages** → Modifiez les couleurs
2. **Cliquez en dehors** du sélecteur de couleurs pour valider
3. **Retraitez** les documents (les PDF déjà traités ne changent pas)

---

### La police ne s'affiche pas correctement

**Causes** :
- Police non disponible sur le système
- PDF avec polices embarquées conflictuelles

**Solutions** :
1. **Choisissez une police standard** : Arial, Calibri, Georgia
2. **Réinstallez les polices** du système si nécessaire
3. **Testez avec différentes polices** pour trouver celle qui fonctionne

---

## 💾 Sauvegarde & Organisation

### Où sont sauvegardés les fichiers traités ?

**Mode Manuel** :
```
Documents/PDFProcessor/[Nom de l'affaire]/
├── 1_Document_A.pdf
├── 2_Document_B.pdf
└── bordereau.pdf
```

**Mode Automatique** :
```
[Votre dossier source]/_Traité/
├── 1_Document_A.pdf
├── 2_Document_B.pdf
└── bordereau.pdf
```

---

### Puis-je changer le dossier de sortie ?

**Réponse** : Non, actuellement les dossiers de sortie sont fixes.

**Workaround** : Déplacez manuellement le dossier `_Traité` ou le contenu de `Documents/PDFProcessor/` après traitement.

---

### Les fichiers originaux sont-ils modifiés ?

**Réponse** : **Non**, jamais.

**Explication** :
- Les originaux restent intacts
- Une copie est créée et traitée
- Vous pouvez supprimer les originaux après vérification

---

## 🔑 Licence

### Combien de temps dure l'essai ?

**Réponse** : **7 jours** à partir de la première utilisation.

**Fonctionnalités** : Toutes les fonctionnalités sont disponibles en essai.

---

### Comment activer ma licence ?

**Étapes** :
1. Onglet **Licence**
2. Cliquez sur **"Acheter une licence"** (ouvre le site de vente)
3. Achetez une clé de licence
4. Copiez la clé reçue par email
5. Retournez dans l'onglet **Licence**
6. Collez la clé dans le champ
7. Cliquez sur **"Activer"**

---

### "Clé de licence invalide"

**Causes** :
- Clé mal copiée (espaces, caractères manquants)
- Clé déjà utilisée sur un autre ordinateur
- Clé expirée

**Solutions** :
1. **Recopiez la clé** soigneusement (évitez les espaces avant/après)
2. **Vérifiez l'email** de confirmation pour la clé exacte
3. **Contactez le support** si le problème persiste

---

### Puis-je utiliser ma licence sur plusieurs ordinateurs ?

**Réponse** : Cela dépend du type de licence acheté.

- **Licence individuelle** : 1 ordinateur
- **Licence cabinet** : Plusieurs ordinateurs (selon le nombre de postes achetés)

**Transfert** : Vous pouvez désactiver la licence sur un ordinateur pour l'activer sur un autre.

---

## ⚡ Performance

### L'application est lente

**Causes** :
- PDF volumineux
- Nombreux PDF
- Ordinateur ancien

**Solutions** :
1. **Fermez les autres applications**
2. **Traitez par lots** de 20-50 PDF
3. **Compressez les PDF** avant traitement
4. **Désactivez la pagination** si non nécessaire

---

### L'application se fige

**Causes** :
- Traitement en cours (normal)
- PDF corrompu bloquant le traitement
- Mémoire insuffisante

**Solutions** :
1. **Attendez** : Le traitement peut prendre plusieurs minutes
2. **Surveillez la progression** : La barre doit avancer
3. **Redémarrez l'application** si rien ne bouge après 5 minutes
4. **Isolez le PDF problématique** :
   - Retirez des PDF un par un
   - Retraitez pour identifier le coupable

---

## 🌍 Langues

### Comment changer la langue de l'interface ?

**Méthode** :
1. En haut de **Mode Manuel** ou **Mode Automatique**
2. Menu déroulant **"Langue"**
3. Sélectionnez votre langue

**Langues disponibles** :
- Français
- English
- Deutsch (Allemand)
- Italiano (Italien)

---

### Certaines traductions sont incorrectes

**Solution** : Signalez-le au support avec :
- La langue concernée
- Le texte incorrect
- La correction proposée

---

## 🆘 Support & Contact

### Où trouver de l'aide supplémentaire ?

**Ressources** :
1. **Cette documentation** : La source la plus complète
2. **Site web officiel** : Tutoriels vidéo et articles
3. **Email support** : Pour questions techniques

---

### Comment signaler un bug ?

**Informations à fournir** :
- Version de l'application (Onglet Licence → en bas)
- Système d'exploitation (Windows 10/11, macOS 13/14/15)
- Description détaillée du problème
- Étapes pour reproduire le bug
- Captures d'écran si possible

**Email** : [Insérer email de support ici]

---

### Puis-je demander une nouvelle fonctionnalité ?

**Réponse** : Oui !

**Processus** :
1. Envoyez un email au support avec :
   - Description de la fonctionnalité souhaitée
   - Cas d'usage concret
   - Pourquoi c'est important pour vous
2. L'équipe évaluera la demande
3. Les fonctionnalités les plus demandées sont prioritaires

---

## 🔒 Sécurité & Confidentialité

### Mes données sont-elles envoyées quelque part ?

**Réponse** : **Non**.

**Explication** :
- PDF Processor fonctionne **100% en local**
- Aucune donnée n'est envoyée sur internet
- Aucun serveur externe n'est contacté (sauf pour l'activation de licence)
- Vos PDF restent sur votre ordinateur

---

### L'application collecte-t-elle des statistiques ?

**Réponse** : **Non**.

**Explication** :
- Aucune télémétrie
- Aucun tracking
- Aucune collecte de données d'usage
- Respect total de votre vie privée

---

## 🔄 Mises à Jour

### Comment mettre à jour l'application ?

**Actuellement** : Mise à jour manuelle

**Processus** :
1. Téléchargez la nouvelle version depuis le site
2. Fermez l'application actuelle
3. Remplacez l'ancienne version par la nouvelle
4. Lancez la nouvelle version
5. Votre licence reste active

**Note** : Une fonction de mise à jour automatique est prévue dans une future version.

---

### Mes paramètres sont-ils conservés après mise à jour ?

**Réponse** : Oui, la plupart du temps.

**Sauvegardés** :
- Préférences (langue, police, couleurs)
- Licence

**À reconfigurer** :
- Informations de dossier (cabinet, affaire)
- Paramètres de traitement (type, mention)

---

## 📊 Limitations Connues

### Formats de Fichier

- ✅ **Supporté** : PDF uniquement
- ❌ **Non supporté** : Word (.docx), Excel (.xlsx), Images (.jpg, .png)

**Solution** : Convertissez vos fichiers en PDF avant traitement.

---

### Taille Maximale

- **PDF individuel** : 100 MB (théorique), 50 MB recommandé
- **Nombre de pages** : Illimité (performances réduites au-delà de 500 pages)
- **Nombre de PDF** : Illimité (traitez par lots de 50-100 pour de meilleures performances)

---

### Systèmes d'Exploitation

**Supportés** :
- ✅ Windows 10 / 11 (x64, ARM64)
- ✅ macOS 13+ (Apple Silicon)

**Non supportés** :
- ❌ Windows 7 / 8
- ❌ macOS Intel (pas de build disponible actuellement)
- ❌ Linux

---

**Besoin d'aide supplémentaire ?** → Contactez le support avec des informations détaillées sur votre problème.
