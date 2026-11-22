# Skillbase

Ton carnet personnel pour apprendre n'importe quoi : rassemble les meilleures ressources (vidéos, cours, applis, articles, podcasts, livres) par compétence, note-les sur 100 et suis le temps que tu passes à pratiquer.

## Mettre en ligne avec GitHub Pages

1. Dans ton dépôt, remplace `index.html` par la nouvelle version (à la racine).
2. **Settings → Pages** : *Deploy from a branch*, branche `main`, dossier `/ (root)`.
3. Le site est disponible sur `https://<ton-pseudo>.github.io/<nom-du-depot>/`.

Astuce : sur ton téléphone, ouvre le site puis « Ajouter à l'écran d'accueil » pour l'utiliser comme une appli.

## Fonctionnalités

- **Premier lancement** : prénom, objectif hebdo, choix des compétences que tu apprends.
- **12 catégories, environ 250 compétences** : langues (niveaux A1 → C2), musique, cuisine, code, sport & bien-être, arts, hobbies, sciences, business, écriture, bricolage, jeux.
- **Tes propres catégories et compétences** si quelque chose manque.
- **Statut par compétence** : J'apprends / Je maîtrise / Plus tard, avec ton niveau et ta progression.
- **Ressources** : colle un lien, le type et la source sont détectés (et le titre récupéré pour YouTube et Vimeo quand c'est possible). Statut À voir / En cours / Terminée, favoris, notes perso.
- **Note sur 100** avec détail par critère : les ressources de chaque compétence sont classées selon ta note.
- **Sessions** : enregistre ton temps de pratique. Ça alimente l'objectif de la semaine, la série de jours et la page Progrès.
- **Preuves de niveau** : Elo (chess.com, Lichess, FIDE), certificats de langue (TOEIC, IELTS, DELE, JLPT, HSK…), statistiques Duolingo, temps sur 10 km, 1RM, ceintures, photos de réalisations… Chaque nouvelle valeur s'ajoute à l'historique, avec la courbe et l'écart par rapport à la précédente. Certains modèles indiquent un repère officiel (TOEIC, TOEFL, IELTS → CECRL ; titres FIDE).
- **Moodboard** : photos, citations et un son (lien Spotify, YouTube, Deezer, SoundCloud, Apple Music, ou fichier audio).
- **Photo de profil**.
- **Temps d'écran** : recopie chaque semaine tes apps principales (moyenne par jour), classe ce temps en utile / mitigé / perdu et relie-le à une compétence. L'appli te montre ce que ça représente sur un an.
- **Résumé par IA (optionnel)** : avec ta propre clé API Anthropic (Profil → Réglages), Claude lit le lien que tu colles et remplit le titre, le type, le niveau, la durée et un résumé de deux phrases.
- **Sauvegarde** : export / import d'un fichier JSON depuis le Profil (photos et sons inclus, clé API exclue).

## Où sont mes données ?

Tout est enregistré **dans le navigateur** (localStorage pour les données, IndexedDB pour les photos et les sons), sur l'appareil que tu utilises. Rien n'est envoyé sur un serveur. Si tu vides les données du navigateur, tout est perdu : pense à **exporter une sauvegarde** de temps en temps. C'est aussi comme ça que tu passes tes données d'un appareil à un autre (Exporter sur l'un, Importer sur l'autre).

Appels externes : noembed.com pour récupérer le titre d'une vidéo quand tu colles un lien ; l'API d'Anthropic uniquement si tu as ajouté ta clé pour les résumés IA ; les lecteurs Spotify/YouTube/… pour le son de ton moodboard.

## Pourquoi le temps d'écran n'est pas automatique ?

Ni un site web ni un raccourci iOS ne peuvent lire les données de Temps d'écran de l'iPhone. Seule une application iOS native peut y accéder, via l'API Screen Time d'Apple (avec une autorisation spéciale d'Apple), et même là, les chiffres exacts restent très protégés. En attendant, la saisie hebdomadaire prend environ deux minutes.
