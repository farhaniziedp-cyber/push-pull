# Push Pull : compiler l'APK sans rien installer

GitHub compile l'APK pour toi, gratuitement, en 5 à 10 minutes.

## 1. Mettre le projet sur GitHub
1. Crée un dépôt sur github.com (bouton « New »), nom `push-pull`, visibilité privée ou publique.
2. Dézippe ce dossier sur ton ordinateur.
3. Dans le dépôt : « Add file » puis « Upload files ». Glisse tout le contenu du dossier dézippé (dossiers `www`, `assets`, `.github` et les fichiers `package.json`, `capacitor.config.json`, `.gitignore`).
4. Clique « Commit changes ».

GitHub limite l'envoi à 100 fichiers à la fois. Si l'envoi est refusé, fais-le en deux fois : d'abord le dossier `www/ill` (les illustrations), puis le reste.

Si le dossier `.github` n'apparaît pas dans ton dépôt (certains systèmes cachent les dossiers commençant par un point) : « Add file » puis « Create new file », tape le nom `.github/workflows/build-apk.yml` et colle le contenu du fichier du même nom.

## 2. Lancer la compilation
1. Onglet **Actions** du dépôt. Si GitHub demande d'activer les workflows, accepte.
2. Choisis **Build APK** puis « Run workflow » (elle démarre aussi toute seule après un envoi).
3. Attends la coche verte (5 à 10 minutes).

## 3. Récupérer l'APK
1. Ouvre l'exécution terminée, section **Artifacts**, télécharge `push-pull-apk`.
2. Dézippe : tu obtiens `app-debug.apk`.
3. Envoie-le sur ton téléphone (câble, e-mail, Drive).

## 4. Installer sur Android
1. Ouvre le fichier `.apk` depuis ton téléphone.
2. Android demande d'autoriser l'installation depuis cette source : accepte.
3. Si Play Protect avertit que l'appli n'est pas connue, choisis « Installer quand même ». C'est normal : l'APK n'est pas publié sur le Play Store.

## À savoir
- Tes données restent sur le téléphone. Elles ne sont pas reliées à ta version en ligne (pas de synchronisation avec ton compte). Programme, onglet « Copier mes données », pour en faire une copie.
- Hors connexion, l'appli fonctionne. Seules les polices personnalisées passent en police du système.
- Pour changer le nom ou l'identifiant de l'appli : fichier `capacitor.config.json`.
- Illustrations : Workout Guide de Bryl Lim, d'après Everkinetic, licence CC BY-SA 4.0.
