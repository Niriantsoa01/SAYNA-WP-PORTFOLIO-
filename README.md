# SAYNA-WP-PORTFOLIO-PRO
Portfolio professionnel WordPress - Projet SAYNA

# Nishop

Boutique en ligne orientée gaming (équipements, accessoires et setup personnalisé).

## Accès au projet complet

Le projet complet (fichiers WordPress + base de données) est disponible sur Google Drive :

[Lien de téléchargement du projet](https://drive.google.com/drive/folders/1kjF-cjGIF03W8SEZFSZsyWdlcyISrdQz?usp=drive_link)

## Prérequis

- PHP (version 8.2.27)
- MySQL 
- Serveur local (Local)

## Installation en local

1. Télécharger l’archive du projet depuis le lien Google Drive.
2. Placer le dossier du site dans le répertoire web de votre serveur local.
3. Créer une base de données vide.
4. Importer le fichier `.sql` fourni dans cette base via phpMyAdmin ou un outil équivalent.
5. Mettre à jour les informations de connexion à la base dans `wp-config.php` si nécessaire.
6. Accéder au site via l’URL locale configurée (par exemple : http://nishop.local).

## Choix techniques

- **CMS :** WordPress, utilisé pour gérer l’ensemble du contenu et de la logique du site.
- **Thème :** Kadence, choisi pour sa légèreté, sa compatibilité avec WooCommerce et ses options de personnalisation sans modifier directement les fichiers du thème.
- **E‑commerce :** WooCommerce pour la gestion du catalogue produits, du panier, des commandes et des moyens de paiement.
- **Construction des pages :** Elementor pour construire certaines sections/pages de manière visuelle tout en gardant la possibilité d’ajouter du CSS et du JavaScript personnalisés.
- **Gestion des comptes et de la page "Mon compte" :**
  - WP User Manager pour la gestion des utilisateurs (inscription, connexion, profils).
  - SysBasics Customize My Account for WooCommerce pour personnaliser les onglets et le contenu de la page « Mon compte ».
- **Paiement :** WooCommerce Stripe Gateway pour le paiement par carte via Stripe.
- **Expérience utilisateur (menus, cookies, devises) :**
  - If Menu – Visibility control for menus pour afficher/masquer certains éléments de menu selon le rôle ou l’état de connexion de l’utilisateur.
  - Cookie Banner for GDPR / CCPA pour l’affichage de la bannière de consentement aux cookies.
  - FOX – Currency Switcher Professional for WooCommerce pour la gestion du changement de devise (si activé).
- **Outils dev / maintenance :**
  - Code Snippets pour injecter le code PHP personnalisé sans modifier directement les fichiers du thème ou des plugins.
  - Better Search Replace pour effectuer des remplacements dans la base de données (notamment lors d’ajustements d’URL ou de migration).

## Organisation des fichiers et du code

- **Thème et structure générale :**
  - Le site utilise le thème Kadence, configuré via le Customizer et les options du thème.
  - Les layouts globaux (header, footer, structure des pages) sont gérés principalement par Kadence et Elementor.

- **CSS personnalisé :**
  - Tous les styles spécifiques au projet sont centralisés dans :
    - `Apparence → Personnaliser → CSS additionnel`
    - D'autre directement via Elementor
  
  - Ce CSS est utilisé pour :
    - adapter l’identité visuelle (couleurs, typographie, espacements),
    - personnaliser certaines sections Elementor (hero, blocs produits, bannières),
    - styliser les boutons, formulaires et éléments des pages de compte / checkout.

- **PHP personnalisé (Code Snippets) :**
  - Aucun fichier PHP du thème Kadence ou des plugins n’a été modifié directement.
  - Le code PHP spécifique au projet est géré via le plugin **Code Snippets**, notamment pour :
    - la gestion de la page de **checkout** (adaptations du comportement de la page de paiement WooCommerce),
    - la **gestion des utilisateurs** (logique personnalisée autour des comptes clients),
    - la **mise à jour du statut en base** (par exemple, mise à jour d’un statut "payé / non payé" en fonction des commandes ou des retours de paiement).

- **Plugins fonctionnels principaux :**
  - **WooCommerce** : gestion e‑commerce (produits, panier, commandes).
  - **WP User Manager** : gestion des comptes utilisateurs (inscription, connexion, profil).
  - **SysBasics Customize My Account for WooCommerce** : personnalisation de la page « Mon compte ».
  - **WooCommerce Stripe Gateway** : intégration du paiement par carte via Stripe.
  - **FOX – Currency Switcher Professional for WooCommerce** : bascule de devise (si utilisé).
  - **If Menu – Visibility control for menus** : affichage conditionnel des entrées de menu.
  - **Cookie Banner for GDPR / CCPA** : gestion du bandeau cookies.
  - **Better Search Replace** : outils de recherche/remplacement dans la base.
  - **Code Snippets** : gestion du PHP personnalisé.

## Auteur

Niriantsoa Hergé
