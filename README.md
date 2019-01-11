# jdownloader2-for-Plexguide
Jdownloader2 yml file for installation via Plexguide with Traefik integration

https://www.timekills.org/pg-apps/

# Google OAuth version


#Instructions for a more automated (not copy and paste into jdownloader2.yml) approach

1. Go to the /opt/mycontainers directory (cd /opt/mycontainers)
2. Type the command: git init
3. Type the command: git remote add jdownloader2 https://github.com/timekills/jdownloader2-for-plexguide.git
4. Type the command: git pull jdownloader2 master
5. (Optional) rm -r README.md if you don't want the README file cluttering up your drectory
6. Run Plexguide

Deploy jdownloader2 app like any other app

# Note for this Google OAuth version - if you get a 400 "That's an error redirect_uri_mismatch"
1. Make sure any other apps with OAuth are working. If they're not, then it's probably the project that you set the OAuth credentials up for isn't set to "public"
2. If other apps are working, then make sure the domain provide you chose when setting up Traefik (i.e. Cloudflare, GoDaddy, NameCheap, etc.) has the "jdownloader2" set as a CNAME or A Record in the DNS settings.
