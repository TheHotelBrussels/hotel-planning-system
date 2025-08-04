# 🏨 Système de Planning Front Office Hôtelier

Application web pour générer automatiquement des plannings optimisés pour les équipes de front office hôtelier. Développée avec Streamlit, elle respecte toutes les contraintes légales et opérationnelles tout en s'adaptant à l'affluence de votre établissement.

## ✨ Fonctionnalités Principales

### 🎯 **Génération Automatique de Planning**
- Planning hebdomadaire optimisé avec algorithme mathématique
- Respect automatique des contraintes légales (2 jours off/semaine, max 5 jours consécutifs)
- Adaptation selon l'affluence (ratio 50 clients/réceptionniste)
- Validation en temps réel de toutes les règles métier

### 👥 **Gestion d'Équipe Complète (15 personnes)**
- **5 superviseurs** (font aussi office de réceptionnistes)
- **9 réceptionnistes** (6 jour + 3 nuit)
- **1 concierge** (présent 5j/7, matin uniquement)
- Modification des noms et compétences linguistiques

### 📊 **Analyse et Prévisions**
- Calcul automatique des besoins selon check-ins/check-outs
- Présets d'occupation : haute/moyenne/basse saison
- Statistiques détaillées : heures, conformité, violations
- Graphiques interactifs de répartition

### 📥 **Export Excel Professionnel**
- Format tableau : employés en lignes, jours avec dates en colonnes
- Sous-colonnes Matin/Après-midi/Nuit pour chaque jour
- 3 feuilles : Planning + Validation + Analyse
- Mise en forme couleur et icônes visuelles

### 🌍 **Gestion des Langues**
- 20+ langues pré-incluses (Anglais, Français, Espagnol, etc.)
- Ajout de langues personnalisées illimité
- Statistiques linguistiques de l'équipe
- Langue principale automatiquement identifiée

## 🚀 Accès à l'Application

### **🌐 Version en Ligne (Recommandée)**
**URL d'accès :** `https://votre-hotel-planning.streamlit.app`

*Aucune installation requise - Accessible depuis n'importe quel appareil avec internet*

### **💻 Installation Locale (Optionnelle)**
Si vous souhaitez faire tourner l'application sur votre propre machine :

```bash
# Cloner le repository
git clone https://github.com/TheHotelBrussels/hotel-planning-system.git
cd hotel-planning-system

# Installer les dépendances
pip install -r requirements.txt

# Lancer l'application
streamlit run planning.py
```

**Accès local :** `http://localhost:8501`

## 📋 Guide d'Utilisation Rapide

### **1. 👥 Configurer l'Équipe**
- L'équipe de 15 personnes est pré-configurée
- Modifiez les noms dans l'onglet "Équipe" > "Modifier un Employé"
- Ajoutez des langues personnalisées si nécessaire

### **2. 📊 Saisir les Prévisions**
- Onglet "Occupation" : saisissez check-ins et check-outs par jour
- Utilisez les présets (Haute/Moyenne/Basse saison) pour gagner du temps
- Cliquez "Calculer les Besoins" pour voir les besoins en personnel

### **3. 📅 Générer le Planning**
- Onglet "Planning" : cliquez "Générer le Planning Optimisé"
- Visualisez le tableau avec dates et sous-colonnes par shift
- Vérifiez la validation automatique des contraintes

### **4. 📥 Exporter en Excel**
- Onglet "Export" : cliquez "Générer le fichier Excel"
- Téléchargez le fichier avec planning + validation + analyse
- Imprimez ou partagez avec l'équipe

## 🎯 Contraintes Respectées

### ✅ **Contraintes Légales**
- Maximum 5 jours consécutifs de travail
- 2 jours de repos minimum par semaine  
- Respect des contrats (temps plein, mi-temps 4j, mi-temps 3j)
- Au moins 1 superviseur par shift jour obligatoire

### ✅ **Contraintes Opérationnelles**
- Ratio 50 clients maximum par réceptionniste
- Maximum 4 personnes par shift
- Exactement 2 réceptionnistes de nuit par shift
- Concierge présent uniquement en semaine le matin
- Aucun superviseur ou concierge la nuit

## 📊 Format du Planning

### **Affichage Web**
```
| Employé        | Rôle    | Lundi 15/01 |      |      | Mardi 16/01 |      |      |
|               |         | Matin | AM   | Nuit | Matin | AM   | Nuit |
|---------------|---------|-------|------|------|-------|------|------|
| Jean Dupont   | Superviseur | 🌅   |      |      |       | 🌆   |      |
| Marie Martin  | Réceptionniste |      | 🌆   |      | 🌅    |      |      |
```

### **Export Excel**
- **Feuille 1** : Planning avec dates et couleurs
- **Feuille 2** : Validation automatique (✅ OK / ❌ Problème)
- **Feuille 3** : Analyse heures par employé + statistiques

## 🏗️ Technologies Utilisées

- **Frontend** : Streamlit (interface web interactive)
- **Optimisation** : PuLP (programmation linéaire)
- **Visualisation** : Plotly (graphiques interactifs)
- **Export** : OpenPyXL (fichiers Excel professionnels)
- **Données** : Pandas (manipulation de données)

## 🎮 Cas d'Usage Concrets

### **👔 Front Office Manager**
*"Je dois faire le planning de mes 15 employés pour la semaine prochaine"*
1. Ouvre l'application web
2. Vérifie la composition de l'équipe
3. Saisit les prévisions d'occupation
4. Génère le planning en 1 clic
5. Exporte en Excel pour affichage

### **🏨 Directeur d'Hôtel**
*"Je veux analyser l'efficacité de mon équipe front office"*
1. Consulte les statistiques de couverture
2. Vérifie le respect des ratios client/réceptionniste
3. Analyse la répartition des heures par employé
4. Identifie les violations de contraintes

### **👥 Équipe RH**
*"Je dois vérifier la conformité légale des plannings"*
1. Consulte l'onglet Validation
2. Vérifie le respect des contrats de travail
3. Contrôle les jours de repos
4. Exporte l'analyse de conformité

## 🌟 Avantages

### **⚡ Gain de Temps**
- Planning généré en quelques clics vs plusieurs heures manuellement
- Validation automatique évite les erreurs
- Export prêt à imprimer

### **📏 Conformité Garantie**
- Respect automatique de toutes les contraintes légales
- Détection des violations en temps réel
- Audit trail complet

### **🎯 Optimisation**
- Couverture optimale selon l'affluence
- Répartition équitable des shifts
- Minimisation des coûts de personnel

### **🌍 Accessibilité**
- Interface web moderne et intuitive
- Accessible depuis n'importe quel appareil
- Pas d'installation logicielle requise

## 🆘 Support

### **📞 Besoin d'Aide ?**
- **Documentation** : Ce README contient toutes les informations
- **Issues** : [Ouvrir un ticket GitHub](https://github.com/votre-username/hotel-planning-system/issues)
- **Email** : support@votre-hotel.com

### **🐛 Problèmes Courants**
- **Application lente** : Rafraîchir la page
- **Planning non généré** : Vérifier la composition de l'équipe (15 personnes)
- **Export ne fonctionne pas** : Vérifier que le planning est généré

## 🔄 Mises à Jour

L'application est automatiquement mise à jour. Les nouvelles fonctionnalités apparaissent sans action de votre part.

### **Version Actuelle : 1.0**
- ✅ Génération de planning optimisé
- ✅ Gestion d'équipe de 15 personnes
- ✅ Export Excel professionnel
- ✅ Gestion des langues personnalisées
- ✅ Validation temps réel

### **Prochaines Fonctionnalités**
- 🔄 Sauvegarde de plannings favoris
- 📱 Version mobile optimisée
- 📈 Historique des plannings
- 🔔 Notifications de conflits

## 📄 Licence

Ce projet est développé spécifiquement pour l'industrie hôtelière. Tous droits réservés.

---

**Développé avec ❤️ pour simplifier la gestion des plannings hôteliers** 🏨

*Application web moderne • Sans installation • Accessible partout • Gratuite*