# Plan - Landing Page FinForm Expert

## Objectif
Creer une landing page HTML/CSS/JS complete en un seul fichier `index.html` pour **FinForm Expert**, une offre combinant formation Pennylane et sous-traitance comptable pour cabinets, independants et dirigeants.

La page doit etre immediatement utilisable dans un navigateur, sans build tool, avec une direction visuelle premium, claire et professionnelle.

## Positionnement
- Promesse principale : aider les cabinets et equipes comptables a maitriser Pennylane plus vite, avec accompagnement operationnel si besoin.
- Cibles : experts-comptables, collaborateurs comptables, freelances administratifs, dirigeants de TPE/PME.
- Ton : expert, direct, rassurant, oriente resultats.
- Conversion prioritaire : prise de rendez-vous ou demande de diagnostic.
- Conversion secondaire : demande d'informations sur les formations ou la sous-traitance.

## Structure du fichier unique `index.html`

### 1. Head
- Meta tags essentiels : `charset`, `viewport`, title, description SEO.
- Open Graph minimal pour le partage.
- Google Fonts : Bricolage Grotesque pour les titres, Inter pour le texte.
- Preconnect vers les domaines de fonts/CDN.
- CSS natif dans un bloc `<style>`.
- Variables CSS : couleurs, typographie, espacements, rayons, ombres, transitions.

### 2. Sections
1. **Navigation sticky**
   Logo texte + marque visuelle simple, liens d'ancrage, CTA principal, etat compact au scroll.

2. **Hero**
   Proposition de valeur claire, sous-texte oriente benefices, 2 CTA, signaux de confiance, visuel WebGL ou fallback statique.

3. **Pourquoi Pennylane**
   Explication courte des gains : automatisation, collaboration, fiabilite, pilotage.

4. **Formations**
   3 offres lisibles : debutant, avance, cabinet. Chaque carte doit afficher objectif, duree, public et resultat attendu.

5. **Sous-traitance comptable**
   Bento grid ou grille claire avec 5 services : tenue, lettrage, rapprochements, preparation TVA, support Pennylane.

6. **Methode**
   Processus en 3 etapes : diagnostic, montee en competence, suivi operationnel.

7. **Resultats / Statistiques**
   4 indicateurs credibles. Eviter les chiffres inverifiables si aucune source n'est fournie.

8. **Temoignages**
   Carousel ou grille responsive. Prevoir des temoignages generiques mais realistes si aucun vrai contenu n'est fourni.

9. **Tarifs**
   3 niveaux ou 3 scenarios : formation, accompagnement, sous-traitance. Afficher clairement ce qui est inclus.

10. **FAQ**
   Accordeon de 6 a 8 questions sur prerequis, format, duree, certification, sous-traitance, confidentialite, outils.

11. **CTA final**
   Rappel de la promesse, formulaire court ou bouton `mailto:`/lien de contact.

12. **Footer**
   Logo, navigation courte, mentions, contact, rappel des services.

## Direction Visuelle
- Style : premium fintech/comptabilite, sobre, lumineux, avec contrastes nets.
- Palette recommandee : fond clair casse, bleu petrole, vert menthe/teal, accent jaune ou corail tres maitrise.
- Eviter un rendu trop sombre ou trop decoratif : la page doit rester credible pour une audience comptable.
- Utiliser les effets visuels comme soutien de lecture, pas comme contenu principal.

## Effets Et Interactions
- Scene Three.js legere dans le hero : particules ou formes geometriques sobres.
- Fallback gracieux si WebGL est indisponible.
- Revelations au scroll via Intersection Observer ou GSAP.
- Cartes avec effet tilt discret sur desktop seulement.
- Compteurs animes declenches a l'entree dans le viewport.
- Accordeon FAQ accessible.
- Progress bar de scroll optionnelle.
- Respect strict de `prefers-reduced-motion`.

## Contraintes Techniques
- Fichier unique : `index.html`.
- CSS natif uniquement, pas de Tailwind.
- JavaScript natif, avec CDN uniquement si utile.
- CDN autorises : Three.js, GSAP, Lucide icons.
- Responsive desktop/tablette/mobile, avec points de rupture autour de 1024px et 768px.
- `content-visibility: auto` possible sur les sections longues.
- Images ou visuels : privilegier CSS/Canvas/WebGL pour rester autonome, sauf si un asset local est fourni.
- Tous les liens d'ancrage doivent fonctionner.
- Le formulaire doit avoir une experience front-end correcte meme sans backend.

## Accessibilite
- Contrastes lisibles.
- Navigation clavier utilisable.
- Etats `focus-visible` visibles.
- Boutons et liens avec libelles explicites.
- Accordeon FAQ avec `aria-expanded`.
- Animations reduites si l'utilisateur prefere moins de mouvement.
- Aucun texte important uniquement porte par une animation ou un canvas.

## SEO Et Contenu
- Un seul `h1`, clair et oriente offre.
- Hierarchie `h2`/`h3` propre.
- Meta description concise.
- Contenu suffisamment concret pour etre comprehensible sans JavaScript.
- Ajouter des donnees structurees JSON-LD simples si pertinent : `LocalBusiness`, `ProfessionalService` ou `EducationalOrganization`.
- Prevoir des formulations citables : phrases courtes, reponses directes dans la FAQ, benefices explicites.

## Performance
- Limiter le poids et la densite de particules Three.js.
- Charger les scripts CDN avec `defer`.
- Desactiver les effets lourds sur mobile ou batterie faible si necessaire.
- Eviter les animations permanentes hors viewport.
- Tester le rendu sans connexion aux CDN : la page doit rester lisible meme si les effets ne chargent pas.

## Criteres De Livraison
- `index.html` complet et autonome.
- Page lisible et fonctionnelle en ouvrant directement le fichier dans le navigateur.
- Navigation interne operationnelle.
- Responsive verifie sur mobile et desktop.
- Aucune erreur JavaScript bloquante dans la console.
- Fallback visuel en cas d'absence de WebGL.
- Texte francais propre, sans probleme d'encodage.

## Ordre D'implementation Recommande
1. Construire la structure HTML semantique complete.
2. Definir le systeme visuel CSS : variables, layout, responsive.
3. Ajouter les sections statiques et le contenu.
4. Ajouter les interactions simples : navigation, FAQ, compteurs.
5. Ajouter les animations au scroll.
6. Ajouter Three.js en dernier avec fallback.
7. Verifier responsive, accessibilite, console et performance.

## Livrable
- `index.html` : fichier unique complet, propre, responsive et pret a ouvrir dans un navigateur.
