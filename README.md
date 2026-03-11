# recotech-rdc
Plan d'implémentation pour RecoTech RDC

Ce document décrit l'approche technique pour la création du site e-commerce RecoTech RDC. Le site offrira une expérience fluide, rapide et moderne (type app mobile).

Choix Technologiques
- Framework: React avec Next.js (App Router) pour le rendu côté serveur (SEO) et la rapidité.
- Styling: Tailwind CSS combiné avec du CSS personnalisé pour un design premium sur-mesure et un développement rapide.
- Animations: Framer Motion (pour la roue de la chance et les transitions fluides entre les pages).
- Routage: App Router intégré à Next.js.
- Gestion d'état: Context API / Zustand (pour le Panier, la Roue de la chance).

Fonctionnalités Principales & Additionnelles
1. Roue de la chance (Capture d'Email): Modale animée à la première visite. L'utilisateur doit entrer son adresse e-mail pour tourner la roue et gagner une réduction ou la livraison gratuite.
2. Espace de Témoignages & Avis : Section dédiée pour que les clients puissent noter le service et laisser des commentaires, renforçant la preuve sociale.
3. Paiement et Livraison Locaux : Intégration visuelle des options (M-Pesa, Airtel Money, Orange Money) et livraison par moto/coursier.
4. Bouton d'Assistance WhatsApp : Un bouton flottant pour un contact direct au service client.
5. Produits Complémentaires (Cross-selling) : Suggestion d'accessoires (coque, chargeur).
6. Comparateur de Produits : Comparaison côte à côte des spécifications.

Architecture des Composants Prévue
Pages (Routes Next.js)
- `/` : Accueil (Hero, Roue de la chance, Produits phares, Témoignages).
- `/shop` : Catalogue complet avec filtres de marques et catégories.
- `/product/[id]` : Fiche produit détaillée (Galerie, Specs, Avis).
- `/compare` : Vue comparateur de 2 produits côte à côte.
- `/repair` : Services de réparation avec formulaire.
- `/reviews` : Espace dédié aux témoignages et notes du service.

Composants Core
- `Layout` : Header sticky, Footer complet, Bouton WhatsApp.
- `LuckyWheel` : Modale de la roue (Framer Motion) avec formulaire d'email.
- `ProductCard` : Carte produit réutilisable.
- `CartDrawer` : Panier latéral.

Plan de Test (Verification)
- Simuler un parcours complet : Première visite -> Entrée de l'email -> Roue -> Gain -> Ajout au Panier -> Vérification du Total.
- Vérifier le comparatif de deux produits.
- Tester la soumission d'un témoignage/avis.
- Tester rigoureusement le Responsive Design (iPhone, iPad, Desktop).
