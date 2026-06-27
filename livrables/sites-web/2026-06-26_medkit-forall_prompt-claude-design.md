# Prompt pour Claude Design — MedKit ForAll
# Plateforme médicale francophone de référence

> Ce document est un prompt de conception complet destiné à Claude Design.
> Il décrit intégralement le produit MedKit ForAll pour permettre la génération
> d'un site médical haut de gamme sans qu'aucune question supplémentaire ne soit nécessaire.

---

## CONTEXTE ET MISSION DU PROMPT

Tu es chargé de concevoir et générer le site complet **MedKit ForAll**, une plateforme médicale francophone de référence destinée aux étudiants en médecine, internes, médecins et professionnels de santé.

Ce prompt contient tout ce dont tu as besoin : vision, identité visuelle, architecture, pages, base de données, fonctionnalités, UX, responsive, SEO, performance, accessibilité, technologies, animations, composants et administration.

Génère un site complet, fonctionnel, premium, prêt pour une utilisation réelle. Ne simplifie rien. Chaque section décrite ici doit être implémentée.

---

# 1. VISION DU PRODUIT

## Mission

MedKit ForAll est la plateforme médicale francophone de référence. Elle regroupe en un seul endroit tout ce dont un étudiant en médecine, un interne ou un professionnel de santé a besoin pour apprendre, réviser, pratiquer et rester à jour : cours structurés, fiches de révision, cas cliniques interactifs, QCM, flashcards, guidelines internationales, actualités médicales, images médicales annotées, vidéos pédagogiques et outils d'intelligence artificielle appliqués à la médecine.

La mission : rendre le savoir médical accessible, structuré et agréable à consulter, que l'on soit étudiant en première année ou praticien confirmé cherchant à maintenir ses compétences.

## Public cible

**Primaire :**
- Étudiants en médecine (PACES/PASS/L.AS, DFGSM, DFASM) — recherchent des cours complets, des résumés, des QCM pour préparer leurs examens
- Internes en médecine — recherchent des guidelines, des algorithmes, des cas cliniques complexes, des outils pratiques
- Médecins généralistes et spécialistes — recherchent des mises à jour, des recommandations internationales, des outils d'aide à la décision

**Secondaire :**
- Infirmiers, pharmaciens, kinésithérapeutes et autres professionnels paramédicaux
- Enseignants en médecine cherchant des ressources pédagogiques
- Journalistes et chercheurs en santé publique

**Géographie cible initiale :** Maroc, France, Belgique, Suisse, Tunisie, Algérie, Sénégal et ensemble de la francophonie médicale.

## Objectifs à long terme

- Devenir la première plateforme médicale francophone par le volume de contenu et la qualité pédagogique
- Atteindre 500 000 utilisateurs actifs en 3 ans
- Proposer une couverture complète de toutes les spécialités médicales (30+ spécialités)
- Développer une application mobile native iOS/Android
- Lancer une version anglophone et arabophone
- Introduire des fonctionnalités IA avancées : diagnostic différentiel assisté, résumé automatique d'articles scientifiques, génération de cas cliniques personnalisés
- Proposer des partenariats avec des facultés de médecine et des CHU
- Lancer un programme de certification reconnu par des sociétés savantes
- Monétiser via abonnement premium tout en gardant une large base gratuite (freemium)

---

# 2. IDENTITÉ VISUELLE

## Philosophie du design

Le design de MedKit ForAll s'inspire des meilleures plateformes technologiques mondiales : la clarté d'Apple, la sophistication de Stripe, la simplicité radicale de Notion, la rigueur de Linear, et l'élégance de Vercel. Appliquées à la médecine, ces influences donnent un résultat qui tranche radicalement avec les sites médicaux traditionnels (visuellement datés, surchargés, peu accessibles).

Le mot clé : **confiance par le design**. Un site beau inspire confiance. Un site clair rend l'apprentissage efficace. Un site premium valorise le savoir médical.

## Palette de couleurs

**Couleurs primaires :**
- `--color-primary: #1B4FD8` — Bleu médical profond, couleur signature de la marque. Utilisé pour les CTA principaux, les liens actifs, les badges de catégorie.
- `--color-primary-dark: #1338A8` — Version sombre pour les états hover.
- `--color-primary-light: #EEF2FF` — Fond des badges, des tags, des sections légères.

**Couleurs neutres (base du design system) :**
- `--color-background: #FFFFFF` — Fond principal en mode clair
- `--color-surface: #F8FAFC` — Cartes, panneaux latéraux, sections alternées
- `--color-border: #E2E8F0` — Bordures légères
- `--color-text-primary: #0F172A` — Texte principal (quasi noir)
- `--color-text-secondary: #475569` — Texte secondaire, métadonnées
- `--color-text-muted: #94A3B8` — Texte désactivé, placeholders

**Couleurs d'état et d'accentuation :**
- `--color-success: #059669` — Vert émeraude. Progression, réussite, validé
- `--color-warning: #D97706` — Ambre. Alertes modérées, en cours, attention
- `--color-danger: #DC2626` — Rouge. Erreurs, contre-indications, urgence
- `--color-info: #0284C7` — Bleu ciel. Informations neutres, notes

**Mode sombre (Dark Mode) :**
- `--color-background-dark: #0B0F1A`
- `--color-surface-dark: #111827`
- `--color-border-dark: #1E2A3A`
- `--color-text-primary-dark: #F1F5F9`
- `--color-text-secondary-dark: #94A3B8`

**Gradient de marque :**
- `background: linear-gradient(135deg, #1B4FD8 0%, #06B6D4 100%)` — Utilisé dans le hero, les CTA premium, les illustrations d'accent

## Typographie

**Police principale : Inter**
- Variable font (Inter Variable) pour les performances optimales
- Chargée depuis Google Fonts avec `display: swap`
- Couvre parfaitement les caractères latins, arabes (avec extension) et tous les signes médicaux

**Hiérarchie typographique :**

```
Display XL :  font-size: 72px / line-height: 1.1 / font-weight: 800 / tracking: -2px
             → Hero principal, titre de marque

Display L :   font-size: 56px / line-height: 1.15 / font-weight: 700 / tracking: -1.5px
             → Titres de section majeure sur la homepage

H1 :          font-size: 40px / line-height: 1.2 / font-weight: 700 / tracking: -1px
             → Titres de page interne

H2 :          font-size: 32px / line-height: 1.3 / font-weight: 600 / tracking: -0.5px
             → Sous-sections

H3 :          font-size: 24px / line-height: 1.4 / font-weight: 600
             → Titres de cartes, sous-sections

H4 :          font-size: 20px / line-height: 1.4 / font-weight: 600
             → Titres dans les articles, sidebar

Body L :      font-size: 18px / line-height: 1.7 / font-weight: 400
             → Corps d'article, texte long

Body :        font-size: 16px / line-height: 1.65 / font-weight: 400
             → Texte standard

Body S :      font-size: 14px / line-height: 1.6 / font-weight: 400
             → Métadonnées, labels

Caption :     font-size: 12px / line-height: 1.5 / font-weight: 500
             → Tags, badges, captions d'image

Code :        font-family: 'JetBrains Mono', monospace / font-size: 14px
             → Formules, données biologiques, dosages
```

## Ambiance et direction artistique

- **Minimaliste et aéré** : beaucoup d'espace blanc, grille claire, contenu qui respire
- **Premium sans être froid** : le design inspire confiance, rigueur et soin — comme un bon ouvrage médical relié
- **Pas de clipart médical kitsch** : pas de stéthoscopes génériques, pas de croix rouge basique. Les illustrations sont abstraites, géométriques ou des photographies authentiques
- **Cohérence absolue** : chaque pixel respecte le design system. Pas de couleur, d'espacement ou de taille de police hors système

## Illustrations et iconographie

**Illustrations :**
- Style : illustrations vectorielles abstraites en dégradé bleu/teal, avec des formes géométriques évoquant la précision médicale (cercles, grilles, courbes douces)
- Utiliser des illustrations de type "blob" ou "orb" en arrière-plan du hero avec un flou gaussien (glassmorphism léger)
- Photographies : vraies photos authentiques de professionnels de santé en action, sans mise en scène artificielle. Tonalité chaude et professionnelle.

**Icônes :**
- Librairie : Lucide Icons (cohérente, minimaliste, open source)
- Style : outline, stroke width 1.5px, taille standard 20px, 24px pour les grandes interfaces
- Chaque spécialité médicale a une icône dédiée (cardiologie : cœur, neurologie : cerveau, pneumologie : poumons, etc.)

## Design System — Tokens d'espacement

```
--space-1:  4px
--space-2:  8px
--space-3:  12px
--space-4:  16px
--space-5:  20px
--space-6:  24px
--space-8:  32px
--space-10: 40px
--space-12: 48px
--space-16: 64px
--space-20: 80px
--space-24: 96px
```

**Border radius :**
```
--radius-sm:  6px   → Badges, inputs, small cards
--radius-md:  12px  → Cards standard
--radius-lg:  16px  → Large cards, modals
--radius-xl:  24px  → Hero cards, featured sections
--radius-full: 9999px → Pills, avatars, tags
```

**Ombres :**
```
--shadow-sm:  0 1px 3px rgba(0,0,0,0.06), 0 1px 2px rgba(0,0,0,0.04)
--shadow-md:  0 4px 12px rgba(0,0,0,0.08), 0 2px 4px rgba(0,0,0,0.04)
--shadow-lg:  0 10px 30px rgba(0,0,0,0.10), 0 4px 8px rgba(0,0,0,0.06)
--shadow-xl:  0 20px 50px rgba(0,0,0,0.12), 0 8px 16px rgba(0,0,0,0.06)
--shadow-primary: 0 8px 24px rgba(27,79,216,0.25)
```

---

# 3. ARCHITECTURE COMPLÈTE

## Arborescence des routes

```
/                          → Homepage
/a-propos                  → À propos de MedKit ForAll
/cours                     → Catalogue des cours
/cours/[slug]              → Page d'un cours
/cours/[slug]/[lecon-slug] → Page d'une leçon
/specialites               → Toutes les spécialités médicales
/specialites/[slug]        → Page d'une spécialité (ex: cardiologie)
/bibliotheque              → Bibliothèque de ressources
/bibliotheque/[slug]       → Fiche d'une ressource
/cas-cliniques             → Catalogue des cas cliniques
/cas-cliniques/[slug]      → Page d'un cas clinique interactif
/qcm                       → Catalogue de QCM
/qcm/[slug]                → Session de QCM
/qcm/resultats/[id]        → Résultats d'une session
/flashcards                → Catalogue de decks flashcards
/flashcards/[slug]         → Session de révision flashcards
/guidelines                → Bibliothèque de guidelines internationales
/guidelines/[slug]         → Page d'une guideline
/actualites                → Actualités médicales
/actualites/[slug]         → Article d'actualité
/outils-ia                 → Hub des outils IA
/outils-ia/assistant       → Assistant IA médical
/outils-ia/diagnostic      → Aide au diagnostic différentiel
/outils-ia/resume-article  → Résumé d'article scientifique
/communaute                → Hub communauté
/communaute/forums         → Forums de discussion
/communaute/forums/[slug]  → Thread de forum
/recherche                 → Recherche globale
/faq                       → Foire aux questions
/contact                   → Formulaire de contact
/profil                    → Profil utilisateur
/profil/parametres         → Paramètres du compte
/tableau-de-bord           → Dashboard utilisateur
/favoris                   → Contenus mis en favoris
/historique                → Historique de consultation
/progression               → Suivi de progression
/certificats               → Certificats obtenus
/notifications             → Centre de notifications
/authentification/connexion    → Page de connexion
/authentification/inscription  → Page d'inscription
/authentification/mot-de-passe → Réinitialisation mot de passe
/admin                     → Dashboard administration
/admin/cours               → Gestion des cours
/admin/articles            → Gestion des articles
/admin/utilisateurs        → Gestion des utilisateurs
/admin/qcm                 → Gestion des QCM
/admin/cas-cliniques       → Gestion des cas cliniques
/admin/media               → Médiathèque
/admin/categories          → Gestion des catégories
/admin/commentaires        → Modération des commentaires
/admin/statistiques        → Tableau de bord analytique
/admin/specialites         → Gestion des spécialités
```

## Navigation principale

**Header :**
- Logo MedKit ForAll (à gauche) — icône abstraite de kit médical + typographie Inter Bold
- Navigation centrale : Cours | Spécialités | Bibliothèque | Cas cliniques | Outils IA | Actualités
- Actions droite : Icône recherche | Mode sombre | Bouton "Connexion" (outline) | Bouton "S'inscrire" (primary)
- En état connecté : icône notifications + avatar utilisateur + dropdown profil

**Footer :**
- Logo + tagline "La médecine, accessible à tous."
- Colonnes : Plateforme | Spécialités | Ressources | Communauté | Légal
- Barre de bas : copyright + liens légaux + sélecteur de langue (FR | EN | AR)
- Newsletter signup intégré dans le footer

---

# 4. HOMEPAGE

## Métadonnées SEO de la homepage

```
title: "MedKit ForAll — La plateforme médicale francophone de référence"
description: "Cours médicaux, cas cliniques, QCM, flashcards, guidelines et outils IA pour étudiants en médecine et professionnels de santé. Gratuit et premium."
og:image: /images/og/homepage.png (1200x630px)
```

## Section 1 : Hero principal

**Layout :** Centré, pleine largeur, hauteur minimum 90vh.

**Contenu :**
- Badge animé en haut : `✦ Nouveau — Assistant IA médical disponible →` (pill avec gradient de bordure, animation pulse légère)
- Titre principal Display XL : `La médecine.\nAccessible à tous.`
  - Le mot "tous" écrit avec un effet de gradient bleu→teal animé (texte gradient animé en keyframe)
- Sous-titre Body L (max-width 600px centré) : `MedKit ForAll regroupe cours médicaux, cas cliniques, QCM, guidelines et intelligence artificielle en une seule plateforme pensée pour les professionnels de santé francophones.`
- Deux CTA côte à côte :
  - Bouton primaire large : `Commencer gratuitement →` (background primary, shadow-primary, animation légère au hover : translate-y -2px)
  - Bouton secondaire : `Voir la démo` (outline, icône play intégrée)
- Social proof sous les boutons : `Rejoins 12 000+ professionnels de santé` avec 5 avatars empilés (overlap) + étoiles ★★★★★

**Arrière-plan :**
- Fond blanc avec deux orbes floutés en position absolue :
  - Orbe 1 (en haut à droite) : 600px, color primary avec opacity 0.12, blur 80px
  - Orbe 2 (en bas à gauche) : 400px, color teal avec opacity 0.08, blur 60px
- Grille de points subtile en arrière-plan (radial-gradient pattern) avec opacity 0.4
- Animation : les orbes se déplacent lentement en keyframe (mouvement de 20px en 8 secondes, ease-in-out)

**Illustration hero :**
- Mockup du dashboard MedKit en version desktop (screenshot stylisé avec ombre xl et border-radius xl)
- Positionné à droite sur desktop, en dessous sur mobile
- Animation d'entrée : fade-in + translate-y 20px → 0 avec delay 400ms

---

## Section 2 : Barre de logos partenaires / confiance

**Layout :** Fond `--color-surface`, pleine largeur, padding vertical 32px.

**Contenu :**
- Texte centré : `Recommandé par des professionnels de` (font-size 13px, text-secondary, uppercase, tracking-wide)
- Ligne de logos en niveaux de gris (opacity 0.5 au repos, 1 au hover) :
  - Logos de facultés de médecine, sociétés savantes, hôpitaux partenaires (ex: "Faculté de Médecine de Fès", "CHU Ibn Sina", "SFR", etc.)
- Animation : défilement horizontal auto-scroll infini (marquee) sur mobile

---

## Section 3 : Proposition de valeur — "Tout ce dont vous avez besoin"

**Layout :** Fond blanc, centré, max-width 1200px, padding vertical 96px.

**Titre H2 :** `Tout ce dont vous avez besoin,\nen un seul endroit.`
**Sous-titre :** `Des ressources médicales soigneusement sélectionnées, organisées et mises à jour en permanence.`

**Grille de features (3 colonnes desktop, 1 colonne mobile) :**

Chaque feature card contient : icône dans un container coloré (12px radius, background primary-light), titre H4, description Body S, lien "Explorer →".

```
Carte 1 — Cours structurés
Icône : BookOpen (bleu)
Titre : "Des cours complets par spécialité"
Description : "Plus de 500 cours médicaux structurés, rédigés par des médecins et validés scientifiquement. De la cardiologie à la neurologie."

Carte 2 — Cas cliniques
Icône : Stethoscope (violet)
Titre : "Cas cliniques interactifs"
Description : "Entraîne-toi sur des cas réels avec un mode pas-à-pas, un raisonnement guidé et un feedback immédiat."

Carte 3 — QCM intelligents
Icône : CheckSquare (vert)
Titre : "QCM et quiz adaptatifs"
Description : "Des milliers de questions classées par thème, difficulté et spécialité. Le système s'adapte à ton niveau."

Carte 4 — Flashcards
Icône : Layers (orange)
Titre : "Flashcards avec répétition espacée"
Description : "Mémorise les notions clés grâce à l'algorithme de répétition espacée SM-2. Révise intelligemment."

Carte 5 — Guidelines
Icône : FileText (bleu ciel)
Titre : "Guidelines internationales"
Description : "Accède aux recommandations des grandes sociétés savantes (ESC, AHA, WHO, HAS) organisées et traduites."

Carte 6 — Assistant IA
Icône : Sparkles (gradient)
Titre : "Intelligence artificielle médicale"
Description : "Pose tes questions médicales à notre assistant IA, résume des articles scientifiques, génère des cas cliniques personnalisés."
```

Animation : chaque carte apparaît avec un stagger animation (fade-in + slide-up) au scroll avec Intersection Observer.

---

## Section 4 : Aperçu du dashboard — "Votre espace d'apprentissage"

**Layout :** Fond `--color-surface`, pleine largeur, padding vertical 96px.

**Côté gauche (texte) :**
- Badge : `Tableau de bord` (pill, primary-light)
- Titre H2 : `Un espace de travail\npensé pour vous.`
- Description : `Suivez votre progression, accédez à vos favoris, reprenez là où vous vous êtes arrêtés. Votre tableau de bord est votre QG médical.`
- Liste de points clés (avec icône check en vert) :
  - Progression par spécialité en temps réel
  - Résumé de vos dernières sessions de QCM
  - Flashcards du jour recommandées
  - Nouvelles guidelines dans vos spécialités favorites
  - Activité de la communauté

**Côté droit :** Mockup du dashboard (screenshot du composant Dashboard, légèrement incliné avec perspective CSS, ombre xl). Animation : parallax léger au scroll (translate-y de -20px à +20px sur le scroll range de la section).

---

## Section 5 : Spécialités médicales

**Layout :** Fond blanc, pleine largeur, padding vertical 96px.

**Titre H2 :** `30+ spécialités médicales couvertes`
**Sous-titre :** `Chaque spécialité dispose de son écosystème complet : cours, cas, QCM et guidelines.`

**Grille de spécialités (6 colonnes desktop, 3 tablette, 2 mobile) :**
Chaque spécialité = une card avec :
- Icône (20x20px, couleur de la spécialité)
- Nom de la spécialité
- Nombre de ressources disponibles
- Hover effect : elevation (shadow-md), légère translation vers le haut

Spécialités affichées (avec couleur et icône) :
```
Cardiologie (rouge), Neurologie (violet), Pneumologie (bleu ciel),
Gastroentérologie (orange), Endocrinologie (jaune), Rhumatologie (brun),
Dermatologie (rose), Pédiatrie (vert clair), Gynécologie-Obstétrique (lilas),
Ophtalmologie (bleu marine), ORL (teal), Urologie (bleu gris),
Psychiatrie (indigo), Hématologie (rouge bordeaux), Infectiologie (vert),
Chirurgie générale (gris), Urgences (rouge vif), Médecine interne (bleu),
Oncologie (violet foncé), Néphrologie (bleu), Gériatrie (or),
Rhumatologie (ambre), Immunologie (vert émeraude), Pharmacologie (turquoise),
Anatomie (beige), Biochimie (jaune-vert), Sémiologie (bleu royal),
Radiologie (gris anthracite), Médecine du travail (vert kaki), Médecine légale (noir)
```

Bouton en bas : `Voir toutes les spécialités →` (outline, centré)

---

## Section 6 : Fonctionnalité vedette — Cas cliniques interactifs

**Layout :** Fond `--color-primary` (bleu), texte blanc, pleine largeur, padding vertical 96px.

**Côté gauche :** Mockup d'un cas clinique en mode interactif : fenêtre stylisée montrant la présentation du cas, les questions pas-à-pas, le feedback en temps réel. Léger effet glassmorphism (fond avec blur) sur le container.

**Côté droit (texte blanc) :**
- Badge : `Nouveau` (pill blanc avec texte primary)
- Titre H2 blanc : `Des cas cliniques comme en service.`
- Description : `Plonge dans des cas cliniques construits par des praticiens. Analyse, décide, apprends. Le mode interactif simule le raisonnement médical réel.`
- Liste de points (icône check blanc) :
  - Présentation progressive du cas (anamnèse → examen → bilan → traitement)
  - Feedback détaillé à chaque étape
  - Score de performance et comparaison avec les autres utilisateurs
  - Mode enseignant pour les formateurs
- CTA blanc : `Essayer un cas clinique →`

---

## Section 7 : Statistiques et chiffres clés

**Layout :** Fond blanc, centré, padding vertical 80px.

**Grille 4 colonnes (2 sur mobile) :**
```
500+      Cours disponibles
12 000+   Utilisateurs actifs
30+       Spécialités couvertes
98%       Taux de satisfaction
```

Chaque chiffre : Display L (gradient primary), sous-titre Body.
Animation : compteur animé (count-up) déclenché au scroll (Intersection Observer).

---

## Section 8 : Témoignages

**Layout :** Fond `--color-surface`, padding vertical 96px.

**Titre H2 :** `Ce que disent nos utilisateurs`

**Carrousel de témoignages (3 visibles desktop, 1 mobile) :**

Chaque card de témoignage :
- Citation en italique Body L
- Avatar + Nom + Titre (ex: "Interne en cardiologie, CHU de Lyon")
- Étoiles ★★★★★
- Fond blanc, shadow-sm, border-radius-lg

```
Témoignage 1 :
"MedKit ForAll a transformé ma façon de réviser. Les cas cliniques interactifs m'ont permis de me préparer aux gardes bien mieux que n'importe quel livre."
— Dr. Yasmine B., Interne en médecine interne, Rabat

Témoignage 2 :
"La qualité des cours est impressionnante. Chaque leçon est structurée, claire, illustrée. C'est la première fois que je trouve une ressource aussi complète en français."
— Karim L., Étudiant DFASM3, Université Paris Descartes

Témoignage 3 :
"L'assistant IA est bluffant. Je lui pose des questions sur des interactions médicamenteuses à 2h du matin et j'ai une réponse claire et sourced en 10 secondes."
— Dr. Mariam T., Médecin généraliste, Casablanca

Témoignage 4 :
"Les flashcards avec répétition espacée m'ont fait économiser des heures de révision. L'algorithme est vraiment efficace."
— Sophie K., Étudiante P2, Faculté de Médecine de Lille
```

Navigation : dots de pagination + flèches gauche/droite. Auto-scroll toutes les 5 secondes.

---

## Section 9 : Section IA — "L'intelligence artificielle au service de la médecine"

**Layout :** Fond avec gradient subtil (blanc → bleu très clair), padding vertical 96px.

**Badge :** `Intelligence Artificielle` (pill avec icône sparkles, gradient bordure)
**Titre H2 :** `Un assistant médical IA\ndisponible 24h/24.`
**Description :** `Posez vos questions médicales, obtenez des résumés d'articles PubMed, générez des cas cliniques sur mesure. Notre IA est spécialisée en médecine et formée sur des sources scientifiques validées.`

**Démo interactive en ligne :**
- Fausse fenêtre de chat (simulée, non fonctionnelle pour les non-inscrits) montrant un échange type :
  - User : "Quelles sont les contre-indications des bêta-bloquants dans l'insuffisance cardiaque ?"
  - IA : Réponse structurée en bullet points avec sources (ESC Guidelines 2023)
- Bouton : `Essayer l'assistant IA →` (CTA primary)

**3 mini-outils en dessous :**
- Aide au diagnostic différentiel
- Résumé d'article PubMed (colle un DOI, reçois un résumé)
- Générateur de cas cliniques personnalisés

---

## Section 10 : CTA final — Inscription

**Layout :** Fond `--color-primary`, pleine largeur, padding vertical 96px, centré.

**Titre H2 blanc :** `Prêt à transformer\nvotre pratique médicale ?`
**Sous-titre blanc :** `Rejoins 12 000+ professionnels de santé. Accès gratuit immédiat.`

**Formulaire d'inscription inline :**
- Input email (fond blanc, border-radius-md)
- Bouton "Commencer gratuitement" (fond blanc, texte primary, shadow)
- Texte sous le formulaire : `✓ Gratuit ✓ Sans carte bancaire ✓ Accès immédiat`

Orbes de fond en blanc opacity 0.05 pour l'ambiance.

---

# 5. PAGES INTERNES

## Page /cours — Catalogue des cours

**Layout :** 2 colonnes — sidebar filtres (260px) + grille de cours (reste).

**Header de page :**
- Titre H1 : "Cours médicaux"
- Sous-titre : "500+ cours rédigés et validés par des médecins"
- Barre de recherche interne (avec icône loupe, placeholder "Rechercher un cours, une maladie, un médicament...")

**Sidebar filtres :**
- Spécialité (multi-select avec checkboxes)
- Niveau (Préclinique | Clinique | Internat | DES)
- Type de contenu (Cours | Résumé | Fiche | Protocole)
- Durée estimée (< 15 min | 15-30 min | 30-60 min | > 60 min)
- Langue (Français | Anglais | Arabe)
- Bouton "Réinitialiser les filtres"

**Grille de cours (3 colonnes desktop, 2 tablette, 1 mobile) :**

Chaque card de cours :
- Image de couverture (ratio 16:9, couleur de fond selon spécialité si pas d'image)
- Badge spécialité (pill coloré)
- Badge niveau (pill gris)
- Titre du cours (H4)
- Auteur avec avatar + nom + titre
- Métadonnées : durée | nombre de leçons | étoile + note
- Barre de progression (si déjà commencé) de 0 à 100%
- Bouton "Continuer" ou "Commencer"

**Pagination :** infinite scroll avec skeleton loader.

---

## Page /cours/[slug] — Page d'un cours

**Layout :** 2 colonnes — content (70%) + sidebar (30%).

**Header du cours :**
- Breadcrumb : Accueil > Cours > Cardiologie > Insuffisance cardiaque
- Badge spécialité + Badge niveau
- Titre H1 du cours
- Description (Body L, max 3 lignes avec "Lire plus")
- Auteur : avatar + nom + titre + bouton "Voir le profil"
- Stats : X leçons | X heures | X étudiants inscrits | Note ★ X.X (X avis)
- Actions : Bookmark | Partager | Télécharger PDF
- CTA principal : "Commencer le cours" ou "Continuer la leçon X"

**Sidebar (sticky) :**
- Table des matières (liste numérotée des leçons)
- Barre de progression globale (circular progress)
- Informations : langue, durée totale, mis à jour le X
- Bouton "Télécharger le PDF complet"

**Contenu principal :**
- Description complète du cours
- Ce que vous apprendrez (liste de bullets)
- Prérequis
- Public visé
- Leçons (accordion) avec icône état (pas commencé / en cours / terminé)

---

## Page /cours/[slug]/[lecon-slug] — Page d'une leçon

**Layout :** Pleine largeur avec sidebar gauche rétractable.

**Sidebar gauche (200px, rétractable) :**
- Table des matières du cours
- Navigation entre leçons (précédente / suivante)
- Progression par leçon (icônes état)

**Zone de contenu principale :**
- Titre de la leçon (H2)
- Temps de lecture estimé | Date de mise à jour
- Contenu riche :
  - Texte formaté avec typographie optimale
  - Images médicales avec légendes et zoom au clic
  - Tableaux de données (bordures légères, alternance de lignes)
  - Encadrés colorés : Définition (bleu) | Attention (orange) | Astuce (vert) | Rappel (violet)
  - Formules et équations médicales (fond code, monospace)
  - Vidéos intégrées (lecteur custom, plein écran)
  - Liens vers cas cliniques associés, QCM de la leçon
- Actions en bas de leçon : Marquer comme terminée | Leçon suivante | Signaler une erreur

**Barre d'outils flottante (fixed bottom) :**
- Progression de lecture (barre horizontale)
- Boutons : Bookmark | Taille de police | Mode sombre | Imprimer

---

## Page /specialites/[slug] — Page d'une spécialité

**Layout :** Pleine largeur.

**Hero de spécialité :**
- Couleur de fond thématique (chaque spécialité a sa couleur)
- Icône grande (48px)
- Titre H1 : "Cardiologie"
- Description de la spécialité
- Stats : X cours | X cas cliniques | X QCM | X guidelines

**Sections :**
1. Cours les plus consultés (grille 4 cards)
2. Cas cliniques récents (grille 3 cards)
3. Guidelines (liste avec source et date)
4. Actualités de la spécialité (liste 5 articles)
5. QCM populaires (liste 5 decks)

---

## Page /cas-cliniques/[slug] — Cas clinique interactif

**Layout :** Mode focus — fond sombre, interface épurée, sans navbar ni footer.

**Interface en mode étapes (stepper) :**

Étape 1 : Présentation initiale
- Texte narratif : "Mme X, 65 ans, se présente aux urgences pour..."
- Anamnèse détaillée
- Question : "Quels examens demandez-vous en premier ?"
- Boutons de choix (radio ou multi-select)

Étape 2 : Résultats des examens demandés
- Affichage des résultats en fonction des choix
- Feedback : choix pertinents / non pertinents
- Question suivante

Étape 3 : Diagnostic
- Hypothèses diagnostiques à classer
- Feedback avec explication détaillée

Étape 4 : Traitement
- Propositions thérapeutiques
- Validation + explication des recommandations en vigueur

Étape 5 : Bilan de performance
- Score global (X/100)
- Détail des points gagnés/perdus
- Comparaison avec les autres utilisateurs (percentile)
- "Voir les résultats détaillés" | "Refaire le cas" | "Cas similaires"

---

## Page /qcm/[slug] — Session de QCM

**Layout :** Mode focus.

**Header :**
- Titre du deck
- Progress bar de complétion
- Timer (si mode chronométré)
- Bouton "Pause"

**Zone question :**
- Numéro de question (Q.12/50)
- Énoncé de la question (Body L)
- Image ou tableau si pertinent
- Options de réponse (boutons radio, style carte)

**Après sélection :**
- Feedback immédiat : réponse correcte en vert, incorrecte en rouge
- Explication détaillée (corps du feedback)
- Source de la question (cours associé, guideline)
- Bouton "Question suivante →"

**Page de résultats /qcm/resultats/[id] :**
- Score global avec cercle de progression animé
- Analyse par thème (barre horizontale par catégorie)
- Liste de toutes les questions avec statut (répondu juste / faux)
- Recommandations : cours à revoir selon les erreurs
- CTA : "Réessayer" | "Voir les erreurs" | "Partager mon score"

---

## Page /flashcards/[slug] — Session flashcards

**Layout :** Mode focus, centré.

**Interface :**
- Carte 3D (500x300px) avec animation flip CSS (rotateY 180deg)
- Face recto : question / concept
- Face verso : réponse / définition + image optionnelle
- Boutons après flip : "Difficile" (rouge) | "Moyen" (orange) | "Facile" (vert)
- Compteur : X cartes restantes dans la session
- Barre de progression
- Statistiques de session en temps réel (X facile | X moyen | X difficile)

---

## Page /guidelines — Bibliothèque de guidelines

**Layout :** 2 colonnes — filtres + liste.

**Filtres :** Société savante (ESC, AHA, WHO, HAS, NICE...) | Spécialité | Année | Langue

**Liste des guidelines :**
Chaque item :
- Logo de la société savante
- Titre de la guideline
- Résumé en 2 lignes
- Tags : spécialité, année, langue
- Boutons : "Lire le résumé" | "Voir le PDF original" | "Résumé IA"

---

## Page /outils-ia — Hub IA

**Layout :** Pleine largeur, cards d'outils.

**Hero :**
- Titre H1 : "Intelligence artificielle médicale"
- Sous-titre : "Des outils IA construits sur des sources médicales validées."

**Grille d'outils (3 colonnes) :**

Outil 1 : Assistant médical IA
- Interface de chat complète
- Modèle spécialisé médecine
- Historique des conversations

Outil 2 : Aide au diagnostic différentiel
- Input : symptômes + signes cliniques + contexte
- Output : liste de diagnostics différentiels avec probabilités et examens recommandés

Outil 3 : Résumé d'article scientifique
- Input : DOI ou URL PubMed
- Output : résumé structuré (objectif, méthode, résultats, conclusion, limites)

Outil 4 : Générateur de cas cliniques
- Paramètres : spécialité, niveau de difficulté, pathologie cible (optionnel)
- Output : cas clinique complet en mode interactif

Outil 5 : Extracteur de guidelines
- Input : question clinique
- Output : recommandations pertinentes issues des guidelines indexées

Outil 6 : Quiz personnalisé
- L'IA génère des questions adaptées au niveau et aux faiblesses détectées

---

## Page /tableau-de-bord — Dashboard utilisateur

**Layout :** Sidebar + zone principale.

**Sidebar gauche (240px) :**
- Avatar + nom + niveau
- Navigation : Vue d'ensemble | Progression | Favoris | Historique | Certificats | Paramètres

**Zone principale :**

Row 1 — Widgets clés (4 colonnes) :
- Cours en cours (X/Y)
- Score QCM moyen (%)
- Flashcards maîtrisées (X)
- Streak de révision (X jours consécutifs) — avec icône flamme

Row 2 — Graphique de progression :
- Graphique en barres (activité par jour sur 30 jours)
- Filtres : 7j | 30j | 3m | 1an

Row 3 — Reprendre là où vous êtes :
- 3 cards horizontales : cours en cours avec progression

Row 4 — Flashcards du jour :
- "Vous avez X cartes à réviser aujourd'hui" avec bouton "Réviser maintenant"

Row 5 — Activité récente :
- Timeline d'activité (leçon terminée, QCM passé, cas clinique résolu)

---

# 6. BASE DE DONNÉES

## Schéma des tables (Supabase / PostgreSQL)

### Table : users
```sql
id              UUID PRIMARY KEY DEFAULT gen_random_uuid()
email           TEXT UNIQUE NOT NULL
username        TEXT UNIQUE NOT NULL
full_name       TEXT
avatar_url      TEXT
role            ENUM('student', 'resident', 'doctor', 'admin') DEFAULT 'student'
specialty       TEXT
institution     TEXT
country         TEXT DEFAULT 'MA'
language        ENUM('fr', 'en', 'ar') DEFAULT 'fr'
is_premium      BOOLEAN DEFAULT FALSE
premium_until   TIMESTAMP
streak_days     INTEGER DEFAULT 0
last_active     TIMESTAMP
created_at      TIMESTAMP DEFAULT NOW()
updated_at      TIMESTAMP DEFAULT NOW()
```

### Table : courses
```sql
id              UUID PRIMARY KEY
slug            TEXT UNIQUE NOT NULL
title           TEXT NOT NULL
description     TEXT
cover_image_url TEXT
specialty_id    UUID REFERENCES specialties(id)
category_id     UUID REFERENCES categories(id)
author_id       UUID REFERENCES users(id)
level           ENUM('preclinical', 'clinical', 'residency', 'specialist')
language        ENUM('fr', 'en', 'ar') DEFAULT 'fr'
duration_min    INTEGER
lesson_count    INTEGER DEFAULT 0
is_published    BOOLEAN DEFAULT FALSE
is_premium      BOOLEAN DEFAULT FALSE
meta_title      TEXT
meta_description TEXT
created_at      TIMESTAMP DEFAULT NOW()
updated_at      TIMESTAMP DEFAULT NOW()
```

### Table : lessons
```sql
id              UUID PRIMARY KEY
course_id       UUID REFERENCES courses(id) ON DELETE CASCADE
slug            TEXT NOT NULL
title           TEXT NOT NULL
content         JSONB  -- Rich content (Tiptap/ProseMirror format)
order_index     INTEGER
duration_min    INTEGER
is_published    BOOLEAN DEFAULT FALSE
has_quiz        BOOLEAN DEFAULT FALSE
created_at      TIMESTAMP DEFAULT NOW()
updated_at      TIMESTAMP DEFAULT NOW()
UNIQUE(course_id, slug)
```

### Table : specialties
```sql
id              UUID PRIMARY KEY
slug            TEXT UNIQUE NOT NULL
name            TEXT NOT NULL
icon            TEXT
color           TEXT -- Hex color
description     TEXT
course_count    INTEGER DEFAULT 0
```

### Table : categories
```sql
id              UUID PRIMARY KEY
slug            TEXT UNIQUE NOT NULL
name            TEXT NOT NULL
specialty_id    UUID REFERENCES specialties(id)
parent_id       UUID REFERENCES categories(id)
```

### Table : clinical_cases
```sql
id              UUID PRIMARY KEY
slug            TEXT UNIQUE NOT NULL
title           TEXT NOT NULL
specialty_id    UUID REFERENCES specialties(id)
difficulty      ENUM('easy', 'medium', 'hard', 'expert')
steps           JSONB  -- Array d'étapes du cas clinique
author_id       UUID REFERENCES users(id)
is_published    BOOLEAN DEFAULT FALSE
is_premium      BOOLEAN DEFAULT FALSE
play_count      INTEGER DEFAULT 0
avg_score       DECIMAL(5,2)
created_at      TIMESTAMP DEFAULT NOW()
```

### Table : questions (QCM)
```sql
id              UUID PRIMARY KEY
deck_id         UUID REFERENCES question_decks(id)
content         TEXT NOT NULL
options         JSONB  -- Array {id, text, is_correct}
explanation     TEXT
image_url       TEXT
specialty_id    UUID REFERENCES specialties(id)
difficulty      ENUM('easy', 'medium', 'hard')
source          TEXT  -- Référence (guideline, cours)
created_at      TIMESTAMP DEFAULT NOW()
```

### Table : question_decks
```sql
id              UUID PRIMARY KEY
slug            TEXT UNIQUE NOT NULL
title           TEXT NOT NULL
description     TEXT
specialty_id    UUID REFERENCES specialties(id)
question_count  INTEGER DEFAULT 0
is_published    BOOLEAN DEFAULT FALSE
is_premium      BOOLEAN DEFAULT FALSE
created_at      TIMESTAMP DEFAULT NOW()
```

### Table : flashcard_decks
```sql
id              UUID PRIMARY KEY
slug            TEXT UNIQUE NOT NULL
title           TEXT NOT NULL
specialty_id    UUID REFERENCES specialties(id)
card_count      INTEGER DEFAULT 0
is_published    BOOLEAN DEFAULT FALSE
created_at      TIMESTAMP DEFAULT NOW()
```

### Table : flashcards
```sql
id              UUID PRIMARY KEY
deck_id         UUID REFERENCES flashcard_decks(id) ON DELETE CASCADE
front           TEXT NOT NULL
back            TEXT NOT NULL
image_url       TEXT
order_index     INTEGER
```

### Table : guidelines
```sql
id              UUID PRIMARY KEY
slug            TEXT UNIQUE NOT NULL
title           TEXT NOT NULL
society         TEXT  -- ESC, AHA, WHO, HAS...
specialty_id    UUID REFERENCES specialties(id)
year            INTEGER
summary         TEXT
pdf_url         TEXT
original_url    TEXT
language        ENUM('fr', 'en', 'ar')
ai_summary      TEXT
created_at      TIMESTAMP DEFAULT NOW()
```

### Table : articles (actualités)
```sql
id              UUID PRIMARY KEY
slug            TEXT UNIQUE NOT NULL
title           TEXT NOT NULL
excerpt         TEXT
content         JSONB
cover_image_url TEXT
author_id       UUID REFERENCES users(id)
specialty_id    UUID REFERENCES specialties(id)
tags            TEXT[]
is_published    BOOLEAN DEFAULT FALSE
published_at    TIMESTAMP
view_count      INTEGER DEFAULT 0
created_at      TIMESTAMP DEFAULT NOW()
```

### Table : user_progress
```sql
id              UUID PRIMARY KEY
user_id         UUID REFERENCES users(id) ON DELETE CASCADE
entity_type     ENUM('lesson', 'course', 'clinical_case', 'qcm_deck', 'flashcard_deck')
entity_id       UUID NOT NULL
status          ENUM('not_started', 'in_progress', 'completed')
progress_pct    INTEGER DEFAULT 0  -- 0 à 100
score           DECIMAL(5,2)
time_spent_min  INTEGER DEFAULT 0
last_accessed   TIMESTAMP
completed_at    TIMESTAMP
created_at      TIMESTAMP DEFAULT NOW()
UNIQUE(user_id, entity_type, entity_id)
```

### Table : bookmarks
```sql
id              UUID PRIMARY KEY
user_id         UUID REFERENCES users(id) ON DELETE CASCADE
entity_type     TEXT NOT NULL
entity_id       UUID NOT NULL
created_at      TIMESTAMP DEFAULT NOW()
UNIQUE(user_id, entity_type, entity_id)
```

### Table : flashcard_reviews (Spaced Repetition)
```sql
id              UUID PRIMARY KEY
user_id         UUID REFERENCES users(id) ON DELETE CASCADE
flashcard_id    UUID REFERENCES flashcards(id) ON DELETE CASCADE
ease_factor     DECIMAL(4,2) DEFAULT 2.5  -- Algorithme SM-2
interval_days   INTEGER DEFAULT 1
repetitions     INTEGER DEFAULT 0
next_review     DATE NOT NULL
last_review     DATE
rating          ENUM('hard', 'medium', 'easy')
created_at      TIMESTAMP DEFAULT NOW()
```

### Table : notifications
```sql
id              UUID PRIMARY KEY
user_id         UUID REFERENCES users(id) ON DELETE CASCADE
type            TEXT  -- new_course, new_guideline, streak_reminder...
title           TEXT NOT NULL
body            TEXT
link            TEXT
is_read         BOOLEAN DEFAULT FALSE
created_at      TIMESTAMP DEFAULT NOW()
```

### Table : comments
```sql
id              UUID PRIMARY KEY
user_id         UUID REFERENCES users(id) ON DELETE SET NULL
entity_type     TEXT NOT NULL
entity_id       UUID NOT NULL
parent_id       UUID REFERENCES comments(id)
content         TEXT NOT NULL
is_approved     BOOLEAN DEFAULT TRUE
created_at      TIMESTAMP DEFAULT NOW()
updated_at      TIMESTAMP DEFAULT NOW()
```

### Table : certificates
```sql
id              UUID PRIMARY KEY
user_id         UUID REFERENCES users(id) ON DELETE CASCADE
course_id       UUID REFERENCES courses(id)
issued_at       TIMESTAMP DEFAULT NOW()
certificate_url TEXT
verification_code TEXT UNIQUE
```

---

# 7. FONCTIONNALITÉS

## Fonctionnalités gratuites

- Accès à 20% des cours (sélection par spécialité, rotatif)
- Accès à 50 QCM par mois
- 10 flashcards par session
- Lecture des actualités médicales (illimitée)
- Accès aux résumés des guidelines (PDFs complets payants)
- Recherche globale limitée (10 résultats par requête)
- Profil utilisateur basique
- Favoris (max 20)
- 3 cas cliniques par mois
- Assistant IA : 5 messages par jour

## Fonctionnalités premium

- Accès illimité à tous les cours et leçons
- QCM et flashcards illimités
- Cas cliniques illimités avec analytics de performance
- Téléchargement PDF de tout le contenu
- Lecture hors ligne (PWA)
- Lecture audio (text-to-speech des leçons)
- Assistant IA illimité
- Outils IA avancés (diagnostic différentiel, résumé PubMed)
- Statistiques de performance avancées
- Certificats de complétion
- Notifications personnalisées
- Accès prioritaire aux nouvelles fonctionnalités

## Fonctionnalités techniques à implémenter

### Recherche intelligente
- Moteur : Algolia ou Meilisearch
- Recherche full-text dans cours, articles, QCM, cas cliniques, guidelines
- Filtres en temps réel
- Suggestions de recherche (autocomplete)
- Recherche par symptôme, maladie, médicament, procédure
- Mise en valeur des termes trouvés dans les résultats (highlighting)

### Système de progression
- Calcul automatique du pourcentage de complétion par cours
- Streak de révision (jours consécutifs)
- Badges et niveaux (Étudiant → Interne → Praticien → Expert)
- Graphiques de progression sur le temps

### Répétition espacée (Flashcards)
- Algorithme SM-2 implémenté côté serveur
- Calcul des dates de révision optimales
- Statistiques de maîtrise par deck

### Mode sombre
- Toggle manuel (icône lune/soleil dans le header)
- Respect de la préférence système (`prefers-color-scheme`)
- Persistance via localStorage

### Téléchargement PDF
- Génération côté serveur (React PDF ou Puppeteer)
- Filigrane avec nom d'utilisateur + date
- PDF structuré avec table des matières

### Lecture audio
- Text-to-speech via Web Speech API ou ElevenLabs
- Contrôles : play/pause, vitesse (0.75x à 2x), avance/recul 15s

### Notifications
- In-app (centre de notifications)
- Email (Resend ou SendGrid)
- Push web (Service Worker, optionnel)

### Partage et réseaux sociaux
- Partage d'un cours, d'un résultat de QCM, d'un certificat
- Génération d'une image OG dynamique par page

### Commentaires
- Système de commentaires threaded par leçon/article
- Modération par l'équipe
- Réactions (like, helpful)

---

# 8. EXPÉRIENCE UTILISATEUR

## Parcours utilisateur — Étudiant en médecine (nouveau)

1. **Découverte** : L'étudiant arrive sur la homepage via Google (SEO) ou partage d'un ami
2. **Accroche** : Le hero communique clairement la valeur en 3 secondes ("La médecine, accessible à tous")
3. **Exploration** : Il parcourt les spécialités, clique sur Cardiologie
4. **Premier cours** : Il commence un cours gratuit, lit 3 leçons, se retrouve face à une leçon premium
5. **Inscription** : La modal d'inscription apparaît — formulaire en 2 étapes (email + mot de passe | informations de profil)
6. **Onboarding** : Après inscription, un flow d'onboarding en 3 étapes : "Quel est ton niveau ?" | "Quelles spécialités t'intéressent ?" | "Comment préfères-tu réviser ?"
7. **Activation** : Le dashboard personnalisé apparaît avec des recommandations basées sur l'onboarding
8. **Rétention** : Notification de rappel si absent 3 jours | Streak motivant | Flashcards du jour

## Parcours utilisateur — Interne cherchant une guideline urgente

1. **Arrivée directe** : Via Google "guideline insuffisance cardiaque ESC 2023"
2. **Page guideline** : Trouve la fiche en 5 secondes, lit le résumé IA, télécharge le PDF
3. **Upsell naturel** : Invite à créer un compte pour sauvegarder en favoris et recevoir les mises à jour

## Micro-interactions UX importantes

- **Chargement des cartes** : Skeleton loaders (animation pulse gris clair) pendant le fetch
- **Toast notifications** : En haut à droite, apparaissent pour confirmer les actions (favori ajouté, cours commencé, score enregistré)
- **État vide** : Illustrations empty state avec message encourageant et CTA (ex: "Aucun favori pour l'instant — commencez par explorer les cours")
- **Feedback de complétion** : Confettis légers (react-confetti) lors de la complétion d'un cours ou d'un excellent score QCM
- **Hover states** : Tous les éléments interactifs ont des hover states clairement définis (transition 150ms ease)
- **Focus states** : Accessibles, visibles (outline 2px primary, offset 2px) pour la navigation clavier

---

# 9. RESPONSIVE DESIGN

## Desktop (≥ 1280px)

- Container max-width: 1280px, centré
- Grilles : 3-4 colonnes pour les cards
- Sidebars visibles en permanence
- Navigation horizontale complète avec tous les liens
- Hover effects actifs
- Typographie en taille maximale (Display XL pour le hero)

## Tablette (768px – 1279px)

- Container: 100% avec padding 24px
- Grilles : 2 colonnes pour les cards
- Sidebars : repliables (accordéon ou drawer)
- Navigation : menu hamburger ou navigation condensée
- Hero : 2 colonnes → 1 colonne (texte + image empilés)
- Typographie réduite d'un niveau (Display XL → Display L)

## Mobile (< 768px)

- Container: 100% avec padding 16px
- Grilles : 1 colonne pour les cards
- Navigation : hamburger → drawer latéral full-height
- Hero : pleine largeur, image en dessous du texte
- Typographie réduite (H1 → 32px, Display → 40px)
- Boutons CTA en pleine largeur
- Sidebar filtres : modal bottom sheet (slide-up depuis le bas)
- Tables des matières : collapsibles par défaut
- Player de leçon : mode portrait optimisé
- Tab bar fixe en bas pour les pages principales : Accueil | Cours | Recherche | Dashboard | Profil

---

# 10. SEO

## Stratégie SEO technique

- **Rendu côté serveur (SSR) ou génération statique (SSG)** via Next.js — indispensable pour l'indexation des cours et articles
- **Sitemap XML dynamique** généré automatiquement à chaque publication de contenu
- **robots.txt** configuré pour autoriser tout sauf `/admin`
- **Balises canoniques** sur toutes les pages pour éviter le duplicate content
- **Structured Data (JSON-LD)** sur les pages clés :
  - `Course` schema pour les cours
  - `Article` schema pour les actualités
  - `FAQPage` schema pour la FAQ
  - `MedicalWebPage` schema pour les fiches de spécialité
  - `Organization` schema pour la homepage
- **Core Web Vitals** optimisés : LCP < 2.5s, FID < 100ms, CLS < 0.1

## Métadonnées par type de page

Chaque page doit avoir :
```html
<title>{titre_page} | MedKit ForAll</title>
<meta name="description" content="{description_unique_150-160_chars}">
<meta property="og:title" content="{titre_page}">
<meta property="og:description" content="{description}">
<meta property="og:image" content="{image_og_1200x630}">
<meta property="og:url" content="{url_canonique}">
<meta name="twitter:card" content="summary_large_image">
<link rel="canonical" href="{url_canonique}">
```

## Stratégie de contenu SEO

- URLs en français, descriptives et courtes : `/cours/insuffisance-cardiaque-aigue` plutôt que `/cours/123`
- Titres H1 uniques sur chaque page
- Contenu minimum 800 mots pour les leçons indexées
- Images avec attributs `alt` descriptifs en français
- Liens internes systématiques entre cours liés, cas cliniques et guidelines
- Temps de chargement < 2s (critique pour le SEO mobile Google)

---

# 11. PERFORMANCE

## Objectif : Score Lighthouse > 95 sur tous les axes

**Performance :**
- Next.js Image Optimization (format WebP/AVIF, lazy loading, taille adaptative)
- Code splitting automatique par route
- Prefetching des routes liées (Link prefetch)
- Fonts : `font-display: swap` + self-hosted Inter (évite les round-trips Google Fonts)
- CSS : Tailwind avec purge automatique (aucune règle inutilisée en production)
- Compression : Brotli sur Vercel
- Cache : `stale-while-revalidate` sur les pages statiques, ISR (Incremental Static Regeneration) pour les cours

**Accessibilité (Lighthouse) :**
- Toutes les images avec alt
- Contraste WCAG AA minimum (4.5:1 pour le texte)
- Landmarks HTML5 sémantiques (nav, main, aside, footer)
- Formulaires avec labels associés

**Bonnes pratiques :**
- HTTPS forcé
- Pas de console errors en production
- Meta viewport configuré
- Pas de librairies dépréciées

**SEO (Lighthouse) :**
- Toutes les balises meta présentes
- Robots.txt valide
- Liens avec texte descriptif
- Structure de headings logique

---

# 12. ACCESSIBILITÉ (WCAG 2.1 AA)

## Exigences implémentées

**Navigation clavier :**
- Tous les éléments interactifs atteignables au Tab
- Ordre de focus logique (suit le flux visuel)
- Skip link "Aller au contenu principal" visible au focus en haut de page
- Gestion du focus dans les modals (focus trap)
- Fermeture des modals au touche Escape

**Contraste des couleurs :**
- Texte sur fond blanc : ratio minimum 4.5:1 (WCAG AA)
- Texte sur fond primary (bleu) : utiliser blanc (#FFFFFF) — ratio 8:1
- Texte secondaire (#475569 sur #FFFFFF) : ratio 4.74:1 ✓

**Attributs ARIA :**
- `aria-label` sur les boutons iconiques (ex: bouton favori : `aria-label="Ajouter aux favoris"`)
- `aria-expanded` sur les accordéons et dropdowns
- `aria-current="page"` sur le lien de navigation actif
- `role="alert"` sur les notifications toast
- `aria-live="polite"` sur les zones mises à jour dynamiquement
- `aria-describedby` pour associer les messages d'erreur aux champs de formulaire

**Contenu alternatif :**
- Toutes les images informatives avec `alt` descriptif
- Images décoratives avec `alt=""`
- Vidéos avec sous-titres (`.vtt`)
- Graphiques avec description textuelle accessible

**Formulaires :**
- Labels visibles associés à chaque champ (`<label for>`)
- Messages d'erreur descriptifs et associés au champ concerné
- Pas de validation uniquement basée sur la couleur

---

# 13. TECHNOLOGIES

## Stack recommandé

### Frontend
- **Next.js 14+** (App Router) — Framework React avec SSR/SSG/ISR, routing file-based, Server Components
- **TypeScript** — Typage strict, meilleure DX et moins de bugs
- **Tailwind CSS v3** — Utility-first CSS, purge automatique, Dark Mode natif
- **shadcn/ui** — Composants UI accessibles basés sur Radix UI, personnalisables avec Tailwind
- **Framer Motion** — Animations déclaratives, gestures, layout animations

### Backend / Infrastructure
- **Supabase** — PostgreSQL managé, authentification (magic link, OAuth Google/Apple), Row Level Security, Storage pour les médias, Realtime
- **Vercel** — Déploiement Next.js optimisé, CDN global, Edge Functions, Analytics
- **Resend** — Emails transactionnels (inscription, reset password, newsletters)

### IA
- **Anthropic Claude API** (claude-sonnet-4-6) — Assistant médical, résumé d'articles, génération de cas cliniques
- Prompts système spécialisés en médecine avec garde-fous (refus de diagnostic direct, redirection vers un professionnel)

### Contenu et recherche
- **Tiptap** — Éditeur rich text pour l'admin (extensible, headless)
- **Meilisearch** (self-hosted sur un VPS) ou **Algolia** — Recherche full-text ultra-rapide

### Médias
- **Supabase Storage** — Stockage des images, PDFs, vidéos courtes
- **Cloudflare Stream** ou **Mux** — Streaming vidéo optimisé pour les leçons vidéo

### Monitoring et analytics
- **Vercel Analytics** — Core Web Vitals en temps réel
- **PostHog** — Product analytics (funnels, heatmaps, session replay) open source
- **Sentry** — Error tracking en production

### Packages clés
```json
{
  "dependencies": {
    "next": "^14.0.0",
    "react": "^18.0.0",
    "typescript": "^5.0.0",
    "tailwindcss": "^3.4.0",
    "@radix-ui/react-*": "latest",
    "framer-motion": "^11.0.0",
    "@tiptap/react": "^2.0.0",
    "@supabase/supabase-js": "^2.0.0",
    "@anthropic-ai/sdk": "latest",
    "lucide-react": "latest",
    "react-hook-form": "^7.0.0",
    "zod": "^3.0.0",
    "zustand": "^4.0.0",
    "react-query": "^5.0.0",
    "react-pdf": "^7.0.0",
    "react-confetti": "latest",
    "date-fns": "^3.0.0",
    "next-themes": "latest",
    "next-seo": "latest"
  }
}
```

---

# 14. ANIMATIONS

## Principes d'animation

- Durée courte : 150ms pour les micro-interactions (hover, focus), 300ms pour les transitions de page, 500ms pour les animations complexes
- Easing : `ease-out` pour les entrées (éléments qui arrivent), `ease-in` pour les sorties, `ease-in-out` pour les états
- Respecter `prefers-reduced-motion` : toutes les animations désactivées si la préférence système est activée
- Framer Motion comme outil principal, CSS transitions pour les cas simples

## Catalogue d'animations

### Animations d'entrée de page
```jsx
// Page transition
const pageVariants = {
  hidden: { opacity: 0, y: 16 },
  visible: { opacity: 1, y: 0, transition: { duration: 0.4, ease: "easeOut" } }
}
```

### Stagger d'apparition des grilles de cards
```jsx
const containerVariants = {
  hidden: {},
  visible: { transition: { staggerChildren: 0.08 } }
}
const cardVariants = {
  hidden: { opacity: 0, y: 20 },
  visible: { opacity: 1, y: 0, transition: { duration: 0.35, ease: "easeOut" } }
}
```

### Orbes du hero (CSS keyframes)
```css
@keyframes orb-float {
  0%, 100% { transform: translate(0, 0) scale(1); }
  33% { transform: translate(20px, -15px) scale(1.05); }
  66% { transform: translate(-15px, 10px) scale(0.95); }
}
.orb { animation: orb-float 8s ease-in-out infinite; }
.orb-2 { animation: orb-float 12s ease-in-out infinite reverse; }
```

### Compteurs animés (hero stats)
- Utiliser une fonction count-up avec requestAnimationFrame
- Durée : 1800ms, easing cubique
- Déclenchement au scroll (Intersection Observer)

### Flip des flashcards
```css
.card-inner {
  transition: transform 0.5s cubic-bezier(0.4, 0, 0.2, 1);
  transform-style: preserve-3d;
}
.card-inner.flipped { transform: rotateY(180deg); }
.card-front, .card-back { backface-visibility: hidden; }
.card-back { transform: rotateY(180deg); }
```

### Skeleton loaders
```jsx
// Composant Skeleton
<div className="animate-pulse bg-gray-200 rounded-md h-4 w-full" />
// Animation CSS : pulse (opacity 0.5 → 1 → 0.5, 2s infini)
```

### Toast notifications (Framer Motion)
```jsx
const toastVariants = {
  hidden: { opacity: 0, y: -20, scale: 0.9 },
  visible: { opacity: 1, y: 0, scale: 1 },
  exit: { opacity: 0, y: -20, scale: 0.9 }
}
```

### Progress bar de lecture (article)
- Thin bar (3px) sticky en haut de page, couleur primary
- Largeur proportionnelle au scroll de la page (0% → 100%)

### Hover sur les cards cours
```css
.course-card {
  transition: transform 0.2s ease-out, box-shadow 0.2s ease-out;
}
.course-card:hover {
  transform: translateY(-4px);
  box-shadow: var(--shadow-lg);
}
```

### Confettis de complétion
- react-confetti, déclenché 500ms après la notification de complétion d'un cours
- Durée : 3 secondes, nombre de pièces : 150, couleurs : primary + gold + green

### Animation du gradient du titre hero
```css
@keyframes gradient-shift {
  0% { background-position: 0% 50%; }
  50% { background-position: 100% 50%; }
  100% { background-position: 0% 50%; }
}
.gradient-text {
  background: linear-gradient(90deg, #1B4FD8, #06B6D4, #1B4FD8);
  background-size: 200% 200%;
  animation: gradient-shift 3s ease infinite;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}
```

---

# 15. COMPOSANTS UI

## Design System — Composants à créer

### Composants de base (atoms)

```
Button          → variants: primary | secondary | outline | ghost | destructive
                 sizes: sm | md | lg | xl
                 states: default | hover | active | disabled | loading

Input           → types: text | email | password | search | number
                 states: default | focus | error | disabled
                 avec label, helper text, message d'erreur

Textarea        → idem Input

Select          → natif ou Radix Select, avec placeholder et options

Checkbox        → Radix Checkbox, avec label

RadioGroup      → Radix RadioGroup

Switch          → Toggle on/off (mode sombre par exemple)

Badge           → variants: primary | success | warning | danger | neutral
                 sizes: sm | md

Avatar          → avec image, fallback initiales, tailles: sm | md | lg | xl

Tooltip         → Radix Tooltip, apparaît au hover avec delay 300ms

Skeleton        → placeholders de chargement pour cards, texte, images

Spinner         → loader circulaire animé

Separator       → ligne horizontale ou verticale

Progress        → barre de progression linéaire

CircularProgress → progression circulaire (dashboard)
```

### Composants composés (molecules)

```
Card            → container avec shadow, border-radius, padding
CourseCard      → Card spécialisée pour les cours (image, badge, titre, auteur, stats, progress)
ClinicalCaseCard → Card pour les cas cliniques (badge difficulté, spécialité, titre, stats)
QuestionCard    → Card pour une question QCM (énoncé, options, feedback)
FlashCard       → Card avec animation flip recto/verso
GuidelineCard   → Card pour les guidelines (logo société, titre, tags, boutons)
ArticleCard     → Card pour les articles actualités (image, catégorie, titre, auteur, date)
SpecialtyCard   → Card spécialité (icône, nom, nombre de ressources)

SearchBar       → Input avec icône loupe, suggestions autocomplete en dropdown
SearchResults   → Page de résultats avec highlighting

FilterSidebar   → Sidebar de filtres avec checkboxes, sliders, bouton reset
FilterChip      → Tag cliquable pour filtres actifs (avec bouton X pour supprimer)

Breadcrumb      → Navigation fil d'Ariane

Tabs            → Onglets de navigation (Radix Tabs)

Accordion       → Questions/réponses (Radix Accordion)

Modal           → Dialog avec overlay, focus trap, fermeture Escape (Radix Dialog)

Sheet           → Drawer latéral (Radix Sheet)

Popover         → Menu contextuel (Radix Popover)

DropdownMenu    → Menu déroulant (Radix DropdownMenu)

AlertDialog     → Confirmation destructive (Radix AlertDialog)

Toast           → Notification temporaire (Radix Toast + Sonner)

CommandPalette  → Recherche rapide type Cmd+K (Radix Command/cmdk)

EmptyState      → État vide avec illustration, titre, description, CTA

ErrorState      → État d'erreur avec message et bouton retry

StepIndicator   → Indicateur d'étapes (cas cliniques, onboarding)

RatingStars     → Étoiles de notation (lecture seule et interactive)

UserAvatar      → Avatar + nom + titre en ligne

AuthorCard      → Card auteur avec avatar, nom, spécialité, bio courte

StatCard        → Card chiffre clé (icône + nombre + label)

ProgressRing    → Cercle de progression SVG animé

ActivityTimeline → Timeline d'activité utilisateur

NotificationItem → Item de notification (icône type + texte + date + état lu/non lu)
```

### Composants de mise en page (organisms)

```
Navbar          → Header principal (logo + nav + actions)
MobileNav       → Drawer de navigation mobile
Footer          → Footer complet multi-colonnes
PageHeader      → Header de page interne (titre + sous-titre + breadcrumb + actions)
Sidebar         → Sidebar générique (filtres, table des matières, dashboard nav)
DashboardLayout → Layout 2 colonnes pour le dashboard
CourseLayout    → Layout cours (sidebar table des matières + contenu leçon)
ContentEditor   → Éditeur Tiptap riche pour l'administration
RichContent     → Rendu du contenu riche (HTML ou JSON Tiptap) côté lecture
```

### Pages spéciales

```
Onboarding      → Flow 3 étapes post-inscription
SubscriptionGate → Mur de paiement (modal ou inline) pour le contenu premium
CertificateView → Page/modal affichant le certificat avec code de vérification
```

---

# 16. PAGES D'ADMINISTRATION

## /admin — Dashboard principal

**Layout :** Sidebar gauche fixe + zone principale.

**Sidebar admin :**
```
Logo MedKit Admin
──────────────────
Vue d'ensemble
Cours
├── Tous les cours
├── Créer un cours
├── Leçons
└── Catégories
Cas cliniques
QCM
├── Decks
└── Questions
Flashcards
Guidelines
Articles
Utilisateurs
Médias
Commentaires
Spécialités
Statistiques
Paramètres
──────────────────
Retour au site →
```

**Dashboard (/admin) :**
- KPIs du jour : Nouveaux inscrits | Sessions actives | Cours complétés | Revenus (si premium)
- Graphiques : inscrits par jour (30j) | Contenu le plus consulté
- Tableau des dernières inscriptions
- Alertes : commentaires signalés | erreurs signalées

---

## /admin/cours — Gestion des cours

**Vue liste :**
- Tableau avec colonnes : Image | Titre | Spécialité | Auteur | Statut | Leçons | Inscrits | Créé le | Actions
- Filtres : spécialité, statut (publié / brouillon), niveau
- Recherche par titre
- Bouton "Créer un cours"
- Actions par ligne : Modifier | Publier/Dépublier | Dupliquer | Supprimer

**Formulaire de création/édition (/admin/cours/[id]) :**
- Onglets : Général | Contenu | SEO | Paramètres

Onglet Général :
- Titre, slug (auto-généré depuis le titre, modifiable)
- Description courte
- Spécialité (select)
- Niveau (select)
- Auteur (select)
- Image de couverture (upload drag & drop)
- Langue, durée estimée
- Statut (brouillon / publié)

Onglet Contenu :
- Gestion des leçons (drag & drop pour réordonner)
- Bouton "Ajouter une leçon"
- Chaque leçon : titre, slug, éditeur Tiptap riche

Onglet SEO :
- Meta title, meta description (avec compteur de caractères)
- Preview de l'apparence dans Google

Onglet Paramètres :
- Cours premium (toggle)
- Autoriser les commentaires
- Certificat à l'issue

---

## /admin/utilisateurs — Gestion des utilisateurs

**Tableau :**
- Colonnes : Avatar | Nom | Email | Rôle | Pays | Premium | Inscrit le | Dernière connexion | Actions
- Filtres : rôle, statut premium, pays
- Recherche par nom / email
- Actions : Voir le profil | Modifier | Suspendre | Promouvoir en admin | Supprimer

**Vue utilisateur individuelle :**
- Informations du profil
- Abonnement et historique de paiement
- Progression (cours en cours, complétés)
- Activité récente
- Commentaires publiés

---

## /admin/qcm — Gestion des QCM

**Vue decks :**
- Liste des decks avec nombre de questions, spécialité, statut
- Bouton "Créer un deck"

**Vue questions (/admin/qcm/[deck-id]/questions) :**
- Tableau des questions avec énoncé court, difficulté, statut
- Bouton "Ajouter une question"

**Formulaire de question :**
- Énoncé (textarea)
- Options A/B/C/D/E avec checkbox "Correcte"
- Explication (éditeur riche)
- Image optionnelle (upload)
- Difficulté, spécialité, source

---

## /admin/statistiques — Analytics

**Sections :**
- Trafic : pages vues, utilisateurs uniques, sessions (graphique par jour/semaine/mois)
- Contenu : Top 10 cours les plus consultés | Top 10 leçons | Temps moyen passé par contenu
- Utilisateurs : Croissance des inscrits | Pays | Répartition par rôle | Taux de rétention
- Engagement : QCM joués | Flashcards révisées | Cas cliniques complétés
- Performances : Scores moyens QCM par spécialité

**Exports :** Tous les tableaux exportables en CSV.

---

## /admin/media — Médiathèque

- Grille de tous les fichiers uploadés (images, PDFs, vidéos)
- Upload drag & drop avec preview
- Filtres : type de fichier, date, utilisé / non utilisé
- Recherche par nom
- Click sur un media : preview + URL copiable + infos (taille, dimensions, date)
- Suppression avec vérification que le media n'est pas utilisé

---

## /admin/commentaires — Modération

- Liste de tous les commentaires avec contexte (sur quelle leçon / article)
- Filtres : En attente | Approuvés | Signalés | Supprimés
- Actions : Approuver | Rejeter | Supprimer | Bannir l'auteur

---

# 17. ÉVOLUTIONS FUTURES

## Version 2.0 (6-12 mois)

- **Application mobile native** (React Native / Expo) — iOS et Android avec accès offline complet
- **Multilingue** — Version anglaise complète + version arabe avec RTL
- **Marketplace de contenu** — Permettre aux médecins experts de publier leurs propres cours (revenue sharing)
- **Forums médicaux** — Discussions structurées par spécialité avec modération communautaire
- **Carnet de stage numérique** — Pour les internes, avec suivi des gestes, objectifs, compétences validées
- **Simulation 3D** — Anatomie interactive en 3D (Three.js ou Babylon.js)

## Version 3.0 (12-24 mois)

- **IA de diagnostic différentiel avancée** — Intégration avec des bases de données médicales (SNOMED, ICD-11)
- **Partenariats facultés** — Intégration du contenu dans les curricula de facultés partenaires
- **Certification officielle** — Accréditation par des sociétés savantes (FMC — Formation Médicale Continue)
- **Téléconsultation médicale entre étudiants et seniors** — Feature communautaire premium
- **Génération automatique de fiches de synthèse** — IA génère des fiches personnalisées basées sur les erreurs des QCM
- **Réseau professionnel médical** — Profils vérifiés, connexions entre professionnels

## Version 4.0 (24-36 mois)

- **API publique MedKit** — Permettre aux développeurs tiers d'accéder au contenu (partenariats)
- **White-label** — Version personnalisable pour les CHU et facultés (leur branding, leur contenu)
- **Réalité augmentée** — Visualisation d'anatomie en AR sur mobile
- **IA de tutorat personnalisé** — Agent IA qui suit l'étudiant sur le long terme, adapte les contenus, prédit les lacunes

---

## INSTRUCTIONS FINALES POUR CLAUDE DESIGN

1. **Génère le site complet** en respectant intégralement ce prompt. Ne simplifie pas.
2. **Commence par le design system** (couleurs, typographie, composants de base) avant de construire les pages.
3. **La homepage est la priorité numéro 1.** Elle doit être parfaite, premium, convaincante.
4. **Chaque page a une logique fonctionnelle claire.** Respecte les layouts et les composants décrits.
5. **Le dark mode doit fonctionner dès le départ** sur toutes les pages.
6. **Responsive mobile d'abord** : teste chaque composant en mobile avant de passer au desktop.
7. **Les animations ne sont pas optionnelles** : elles font partie de l'identité premium du produit.
8. **L'accessibilité est non négociable** : focus states, ARIA labels, contrastes.
9. **Utilise le stack décrit** : Next.js + TypeScript + Tailwind + shadcn/ui + Framer Motion + Supabase.
10. **Nomenclature en français** pour tout le contenu visible, en anglais pour le code (variables, fonctions, composants).

MedKit ForAll doit être le meilleur site médical francophone jamais construit. C'est l'objectif. Ne compromets pas.
