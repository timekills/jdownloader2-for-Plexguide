# jdownloader2-for-Plexguide
Jdownloader2 yml file for installation via Plexguide with Traefik integration
https://www.timekills.org/pg-apps/

## Username and password version

# Default username plex and password guide


#Instructions for a more automated (not copy and paste into jellyfin.yml) approach

1. Go to the /opt/mycontainers directory (cd /opt/mycontainers)
2. Type the command: git init
3. Type the command: git remote add jdownloader2 https://github.com/timekills/jdownloader2-for-plexguide.git
4. Type the command: git pull jdownloader2 timekills-userpass
5. (Optional) rm -r README.md if you don't want the README file cluttering up your drectory
6. Run Plexguide

Deploy jdownloader2 app like any other app

If you want to change the username/password from default plex/guide
1. go to --> http://www.htaccesstools.com/htpasswd-generator/ and create username/password pair. It will give you the plaintext username and hashed password
2. (example username test and password test will give you test:$apr1$n22fgswn$4Wu4q/Dzc7ACcgiLaoU5d/)
3. Edit the /opt/mycontainers/jdownloader2.yml file (eg. sudo nano /opt/mycontainers/jdownloader2.yml )
4. Replace the line traefik.frontend.auth.basic: "plex:$apr1$tosnCNtX$XKXnDaIiW7f0y1nwmd.KL0" with traefik.frontend.auth.basic: "yourNewUsername:YourNewHashedPassword."  Example traefik.frontend.auth.basic: "test:$apr1$n22fgswn$4Wu4q/Dzc7ACcgiLaoU5d/"
Go to plexguide and redeploy/reinstall jdownloader2
