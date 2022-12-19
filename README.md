![GitHub forks](https://img.shields.io/github/forks/Luckyluka17/YCM-Server-template)
![GitHub repo file count (custom path)](https://img.shields.io/github/directory-file-count/Luckyluka17/ycm-server-template/titles?label=cheats%20count)

# Yuzu Cheats Manager Server Template
Ceci est une template que vous pouvez fork pour y mettre vos propres cheats pour Yuzu Cheats Manager.

## Mise en place de votre dépôt
Pour créer votre dépot qui va permettre de télécharger les cheats, vous avez besoin de suivre ce guide dans l'ordre.
### Créer le dépôt
Pour cela, vous devez **poséder** un compte github. Une fois que vous êtes connecté, cliquez sur **Fork**.

[![image](https://user-images.githubusercontent.com/63603989/204081819-6c8d8273-8dac-4e38-a82b-da254b813c47.png)](https://github.com/Luckyluka17/YCM-Server-Template/fork)

### Installer vos cheats
Une fois ceci fait, créez des dossiers **avec les identifiants des jeux** dont vous possédez des cheats codes, à l'intérieur du dossier **titles** (voir exemple).

Si besoin, référez vous au dossier [`0000000000000000`](https://github.com/Luckyluka17/YCM-Server-Template/tree/main/titles/0000000000000000) dans le répertoire [`titles`](https://github.com/Luckyluka17/YCM-Server-Template/tree/main/titles/) (ce dossier est un exemple pour vous montrer comment mettre en place vos cheats).

## Ajouter le dépôt sur l'application

Pour ajouter un serveur sur l'application, vous devez ouvrir l'application Yuzu Cheats Manager. Dans le repertoire où ce trouve **YuzuCheatsManager.exe**, vérifiez que vous possèdez le fichier **settings.json**. Si oui, vous pouvez maintenant fermer l'application.

Effectuez un clique-droit sur le fichier **settings.json**, puis cliquez sur **Ouvrir avec** > **Bloc-notes** (ou un éditeur de code si vous en avez un).

![image](https://user-images.githubusercontent.com/63603989/206850742-73e7463e-0632-42fe-a54c-83d9e642a2e4.png)

Si le fichier a été généré correctement, vous devriez avoir quelque chose qui ressemble à ça :
```json
{
    "verify_updates": true,
    "notify_incompatible_games": true,
    "yuzu_folder": "C:\\Users\\NomDutilisateur\\AppData\\Roaming\\yuzu\\",
    "language": "Fran\u00e7ais",
    "discord_rpc": true,
    "auth_key": "",
    "cheats_names": {},
    "dev_mode": false,
    "servers": {
        "Switch Cheats": "https://github.com/ibnux/switch-cheat/tree/master/sxos/titles/"
    },
    "actual_server": 1
}
```

Dans la clé **servers**, ajoutez votre serveur en lui donnant un nom puis en ajoutant le lien menant vers le dossier **titles** (⚠️ **AJOUTEZ UN / À LA FIN DU LIEN**).

Cela donne :
```json
{
    "verify_updates": true,
    "notify_incompatible_games": true,
    "yuzu_folder": "C:\\Users\\NomDutilisateur\\AppData\\Roaming\\yuzu\\",
    "language": "Fran\u00e7ais",
    "discord_rpc": true,
    "auth_key": "",
    "cheats_names": {},
    "dev_mode": false,
    "servers": {
        "Switch Cheats": "https://github.com/ibnux/switch-cheat/tree/master/sxos/titles/",
        "Nom de votre serveur": "https://github.com/votrepseudogithub/nomdudepot/tree/main/titles/"
    },
    "actual_server": 1
}
```

Une fois que vous avez terminé d'ajouter votre/vos serveur(s),  cliquez sur **Fichier** > **Enregistrer**.
Vous pouvez maintenant fermer le bloc-note.

Ouvrez YuzuCheatsManager, puis ouvrez le menu **Fichier** > **Paramètres** > **Fournisseur de cheats** > **Cliquez sur le serveur de votre choix**

Voilà, c'est tout !
