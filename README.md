# EM Gabon-Université (Libreville, Gabon)

Site vitrine et espace numérique d'EM Gabon-Université (8 composantes, 75 filières).

## Pages publiques
- `index.html` : accueil (diaporama, formations, piliers, actualités, partenaires)
- `ecole.html` : présentation, mot du Président, gouvernance, revue de presse
- `formations.html` : 75 filières filtrables par composante (fiches détaillées)
- `admission.html` : conditions, pré-inscription en ligne en 3 étapes, FAQ
- `vie-etudiante.html` : actualités, facilités, galerie photo filtrable, vidéos
- `contact.html` : coordonnées, formulaire, carte

## Espace numérique (`espace.html`)
| Profil | Accès | Fonctions |
|---|---|---|
| Enseignant | `enseignant.html` | saisie des notes (CC 40 % / examen 60 %, moyenne et mention auto), statistiques de classe, export CSV, annonces et devoirs, messagerie |
| Scolarité | `enseignant.html` | pré-inscriptions reçues (statuts), résultats et classements par classe, messages du site, annonces à toute l'école |
| Étudiant | `etudiant.html` | notes, moyenne générale, rang, bulletin imprimable, annonces, devoirs, emploi du temps, messagerie |

### Comptes de démonstration
- Enseignants : `p.ndong`, `c.mba`, `s.obiang` / `prof2026`
- Scolarité : `scolarite` / `admin2026`
- Étudiants : `EMGU25-001` à `EMGU25-028` / `emgu2026`

## Base de données (Supabase)
- `supabase/install.sql` : tables, règles de sécurité (RLS) par rôle, fonctions, temps réel et comptes de démonstration.
- `assets/js/config.js` : URL du projet et clé publique « anon ». Vide = mode démonstration (données dans le navigateur).
- La scolarité crée les comptes, classes et matières depuis le back-office (« Comptes », « Classes & matières »).
- Avant la mise en production : changer ou supprimer les comptes de démonstration et passer `showDemo` à `false`.

## Déploiement
Site statique hébergé sur GitHub Pages — aucune compilation nécessaire.
