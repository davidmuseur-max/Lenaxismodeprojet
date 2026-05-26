# LENAXIS — Gestion de Projet Cession

Outil web de pilotage interne pour la phase de cession LENAXIS.

## Déploiement sur Vercel — 3 minutes

### Méthode 1 : Drag and Drop (la plus simple)

1. Va sur https://vercel.com et connecte-toi (avec Google, GitHub ou email)
2. Clique sur **Add New** en haut à droite → **Project**
3. Clique sur **Browse** ou glisse directement le dossier contenant `index.html` et `vercel.json`
4. Vercel détecte automatiquement la configuration
5. Dans le champ **Project Name**, tape : `lenaxis-projet`
6. Clique sur **Deploy**
7. Attends 30 secondes
8. Ton URL est prête : `https://lenaxis-projet.vercel.app`

### Méthode 2 : Vercel CLI (si tu as Node.js installé)

```bash
npm install -g vercel
cd dossier-lenaxis-projet
vercel
```

Réponds aux questions :
- Set up and deploy? **Y**
- Project name? **lenaxis-projet**
- Directory? **./**
- Override settings? **N**

### Si le nom est déjà pris

Vercel te proposera des alternatives. Suggestions :
- `lenaxis-cession`
- `lenaxis-projet-david`
- `lenaxis-pilotage`
- `lenaxis-2026`

## Fichiers du projet

- `index.html` — Application complète (HTML + CSS + JS dans un seul fichier)
- `vercel.json` — Configuration de déploiement
- `README.md` — Ce fichier

## Fonctionnalités

- Tableau de bord avec 6 indicateurs clés en temps réel
- 2 graphiques (avancement par responsable, répartition par statut)
- 22 tâches préchargées correspondant au compte rendu de réunion
- Création / modification / clôture / suppression de tâches
- Filtres par responsable, statut, recherche texte
- Tri par échéance, priorité, responsable, statut
- Détection automatique des retards
- Notification quotidienne en bandeau si tâches du jour ou en retard
- Export / Import JSON pour synchronisation entre personnes
- Responsive (utilisable sur mobile)

## Limite importante à connaître

Les données sont stockées localement dans le navigateur (localStorage), pas sur un serveur partagé. Chaque utilisateur voit son propre état. Pour partager les avancements :

1. Faire des modifications
2. Cliquer sur **Export JSON**
3. Envoyer le fichier par mail
4. Le destinataire ouvre l'URL et clique sur **Import JSON**

Pour un vrai partage en temps réel, il faudrait ajouter une base de données (Supabase, Vercel Postgres). Demande à Claude si tu veux faire évoluer dans ce sens.

## Sécurité

- Aucune donnée envoyée à un serveur tiers
- Pas d'authentification requise (URL privée mais publique d'accès)
- Pour limiter l'accès, partager l'URL uniquement à David, Romain, Guillaume, Maître Caprioli
- Les meta-tags interdisent l'indexation par Google

## Support

Toutes les modifications du code peuvent être faites en éditant directement `index.html` puis en redéployant sur Vercel (drag and drop automatique).
