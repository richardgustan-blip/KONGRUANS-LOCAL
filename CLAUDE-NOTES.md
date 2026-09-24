# KONGRUANS - Notes de Projet

## Description
Application PWA de mesure de congruence personnelle (Pensee, Parole, Action).
Permet aux utilisateurs de faire des scans quotidiens, tenir un journal et suivre leur progression.

## Stack Technique
- **Frontend** : React 18 (via CDN), Babel, HTML/CSS
- **Backend** : Supabase (PostgreSQL cloud)
- **Hebergement** : O2Switch (https://richard-gustan.fr/kongruans)
- **Code source** : https://github.com/richardgustan-blip/KONGRUANS-LOCAL

## Configuration Supabase
- **URL** : https://ufemtbfukndbtjhwuhta.supabase.co
- **Anon Key** : eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJzdXBhYmFzZSIsInJlZiI6InVmZW10YmZ1a25kYnRqaHd1aHRhIiwicm9sZSI6ImFub24iLCJpYXQiOjE3OTAyNjQ3NjksImV4cCI6MjEwNTg0MDc2OX0.hnaTPcETrA9Jws2lWZ6_K-ykQhkb_Mf4z7rmcUhnUvc

## Tables Supabase
```sql
-- users (id UUID, email, name, password_hash, created_at)
-- scans (id UUID, user_id, pensee, parole, action, answers JSONB, created_at)
-- journal (id UUID, user_id, content, created_at)
```

## Compte Demo
- Email : testeur@kongruans.app
- Mot de passe : Test1234!

## Fonctionnalites Implementees (v2.0)
1. Authentification (inscription, connexion, deconnexion)
2. Scan quotidien (12 questions, 3 piliers)
3. Triangle de congruence anime (Canvas)
4. Bibliotheque d'exercices (6 exercices)
5. Journal personnel
6. Suivi de progression avec historique
7. PWA installable sur mobile
8. Donnees persistantes via Supabase

## Fichiers du Projet
- `index.html` - Application complete (React + CSS inline)
- `manifest.json` - Configuration PWA (start_url: /kongruans/)
- `netlify.toml` - Config Netlify (non utilise sur O2Switch)
- `.gitignore` - Fichiers ignores

## Historique des Versions
- v1.0 : Version localStorage uniquement
- v1.1 : Corrections PWA et migration
- v2.0 : Integration Supabase (base de donnees cloud)

## Pour Reprendre le Projet
Lors de la prochaine session avec Claude, montrez ce fichier :
"Voici les notes de mon projet KONGRUANS : [contenu de CLAUDE-NOTES.md]"

## Prochaines Ameliorations Possibles
- [ ] Notifications push pour rappel de scan
- [ ] Mode hors-ligne avec synchronisation
- [ ] Export des donnees (PDF/CSV)
- [ ] Statistiques avancees avec graphiques
- [ ] Partage social des resultats
- [ ] Themes personnalisables
