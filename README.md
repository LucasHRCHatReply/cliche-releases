# Cliché pour macOS

Cliché capture l'écran, annote et enregistre : zone, fenêtre ou plein écran, vignettes flottantes qui restent à l'écran,
texte copié par reconnaissance (OCR), éditeur d'image, capture en défilement et enregistrement vidéo. Tout se passe sur
le Mac : aucun compte, aucune télémétrie.

**Version de départ, nom provisoire.** C'est une première version (0.1.0) : elle fait ce qui est écrit dans les notes de
la Release et rien de plus, et elle a pu être essayée sur très peu de Mac. Le nom « Cliché » peut encore changer.

Ce dépôt ne contient que les versions à installer. Le code source n'est pas public.

## Ce qu'il faut

- un Mac à puce Apple (M1 ou plus récent) ;
- macOS 15 ou plus.

## Installer

Dans Terminal (Cmd + Espace, « Terminal »), une seule commande :

```
curl -fsSL https://raw.githubusercontent.com/LucasHRCHatReply/cliche-releases/main/installer.sh | zsh
```

Le script télécharge la dernière version, vérifie l'empreinte SHA-256 du zip, l'identifiant de l'app et sa signature
(équipe Apple `JT9FY7PP7K`, `codesign --verify --deep --strict`), copie l'app dans ~/Applications, puis l'ouvre.
Relancer la même commande installe une version plus récente.

Autre voie : télécharger `Cliche.dmg` dans les [Releases](../../releases/latest), l'ouvrir, glisser Cliché sur
Applications. Le disque est signé, non notarisé : au premier lancement, clic droit sur l'app › Ouvrir.

Au premier lancement, Cliché demande lui-même ses autorisations (enregistrement de l'écran, puis micro
seulement si on l'active pour un enregistrement).
