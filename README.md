# Gclone Discord Utilities
## Features
1. **Clone**  - Clone a public/private google drive file/folder to your teamdrive.
2. **Mkdir**  - Make Directories directly from discord.
3. **Size**   - Calculate size of google drive files/folders from link.
4. **Move**   - Move files/folders from one location to other.
5. **sync**   - Sync source links to destination links.
6. **Delete** - Delete folders/files.
7. **Name**   - Find name of google drive folders/files from link.
## Prerequisites
- **[Gclone](https://github.com/donwa/gclone)** - Run the shell / batch script if you are on Linux to install, or add the gclone.exe file to your system PATH variables if you are on Windows. Putting the script in the same directory as GClone in Windows will work as well. If you are on MacOS, download the Darwin build of GClone.
- **[AutoRClone](https://github.com/xyou365/autorclone) - (Service accounts folder)** - GClone requires service accounts. To generate and manage them, use AutoRClone. You can then configure GClone using the service accounts.
- **[Git](https://git-scm.com/downloads)** - Install this program, and dont forget to add to PATH. [Docs](https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup)
- **[Heroku CLI](https://devcenter.heroku.com/articles/heroku-cli#install-the-heroku-cli)** - Install the Heroku CLI and add to PATH. [Docs](https://devcenter.heroku.com/articles/heroku-cli#install-the-heroku-cli)

## Deploy to Heroku
<!-- [![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy) -->
### Deploying to heroku takes patience. But its a one time setup. Have patience. If you find any difficulties, follow the video tutorial.
---
## Setup (Heroku):
1. Download the [zip](https://codeload.github.com/jsmsj/Gclone-Discord-Utilities-Heroku/zip/refs/heads/main) of the repo and extract it to a suitable location.
<!-- Download the latest release of [gclone](https://github.com/donwa/gclone/releases/) and add the **gclone** file to the location, where you extracted .zip folder in step 1.-->
2. Add service accounts (100 json files) to the [accounts folder](accounts/).
3. Update the [.env](.env) file.
   1. Add discord bot token
   2. Add bot prefix
   3. Add your discord id to USERIDS
   4. Add your discord id to ADMINS
   5. Add the default destination id 
4. Go to [Heroku dashboard](https://dashboard.heroku.com/).
5. Create a new app and give it a suitable name.
6. Go to its settings, then under the buildpacks section, click **Add Buildpack** and add the following buildpacks:
   1. `heroku/python`
   2. `https://github.com/The-Antrax/heroku-buildpack-rclone-mod.git`
7. Run command prompt in the folder in step 1.
8. Follow these commands:
   1. `heroku login`
   2. `git init`
   3. `heroku git:remote -a "name"` Here name is the name of your heroku project.
   4. `git add . -f`
   5. `git commit -am "first commit"`
   6. `git push heroku master`
9.  Go to Resources tab in heroku dashboard. Refresh it. Click on the ✏️ icon, and toggle on the worker.

---

## Video:
Incase you find any difficulties, follow this video tutorial
### [Vimeo](https://vimeo.com/679652094)
### [Youtube](https://youtu.be/BGeWSOGqxHE)


**Enjoy using Gclone Discord Utilities Bot**

---

# Detailed Tutorial on Gclone and Service accounts setup

## How to create Service Accounts and add them to your teamdrive and setup gclone.

Follow [this tutorial](https://rentry.co/gcloneguide)

---
