# jdownloader2-for-Plexguide
Jdownloader2 yml file for installation via Plexguide with Traefik integration

# Alpha - use at own risk. Not tested yet.


#Instructions for a more automated (not copy and paste into jellyfin.yml) approach

Go to the /opt/mycontainers directory (cd /opt/mycontainers)
Type the command: git init
Type the command: git remote add origin https://github.com/timekills/jdownloader2-for-plexguide.git
Type the command: git pull origin master
(Optional) rm -r README.md if you don't want the README file cluttering up your drectory
Run Plexguide
Deploy jellyfin app like any other app
