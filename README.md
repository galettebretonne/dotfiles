# dotfiles

Source chezmoi, **dépôt public** : relire chaque modification avant `git push`.

- Première installation : faite par le rôle `dotfiles` du dépôt `workstation`
  (ou à la main : `chezmoi init --apply https://github.com/galettebretonne/dotfiles.git`).
- Mise à jour d'une machine : `chezmoi diff` puis `chezmoi update`.
- Procédure complète de synchronisation : voir le README du dépôt `workstation`,
  section « Fichiers de configuration (dotfiles) ».

Les fichiers `.tmpl` sont des modèles : écrire `{{ .chezmoi.homeDir }}` au lieu de `/home/manu`.

Secrets : `~/.config/secrets.env` (chmod 600, jamais versionné), chargé par `.profile`.
