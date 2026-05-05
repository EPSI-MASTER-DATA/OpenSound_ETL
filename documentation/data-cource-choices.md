# Choix des sources de données

Comme nous travaillons pour une maison de disque dont l'objectif est de savoir quel artiste faire signer, notre table de faits centrale doit être l'artiste.

## Données descriptives

Le dataset "Spotify Kaggle" (à condition d'être mis à jour quotidiennement ou au moins à chaque lancement de notre pipeline) peut nous servir de base descriptive des morceaux.

On peut récupérer, a minima, des informations sur les morceaux comme :

- 'artists' : l'auteur de la musique,
- 'track_name' : le nom de la musique,
- 'duration_ms' : la durée de la musique en millisecondes,
- 'track_genre' : le style de la musique,
- 'popularity' : le score de popularité de la musique sur Spotify.

## Données comportementales

Grâce à notre premier dataset, nous avons un ensemble de données descriptives autour des morceaux des artistes. On peut compléter ces données avec l'API "Last.fm", qui nous apportera la dimension comportementale des utilisateurs vis-à-vis des morceaux et des artistes présents dans "Spotify Kaggle".

On peut utiliser, a minima, ces endpoints :

- 'chart.getTopTracks' : 'track.name', 'track.playcount', 'track.listeners', 'artist.name',
- 'chart.getTopArtists' : 'artist.name', 'artist.playcount', 'artist.listeners',
- 'chart.getTopTags' : 'tag.name', 'tag.reach', 'tag.taggings',
- 'artist.getInfo' : 'stats.listeners', 'stats.plays',
- 'tag.getTopArtists' : 'artist.name'
