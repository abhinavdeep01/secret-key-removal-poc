__Steps to remove sensitive secrets from git history__

1) git clone --mirror https://<your-repo>.git/
2) cd <your-repo>.git
3) create password.txt inside <your-repo>.git folder (enter secret to be removed e.g. topSecret==>***REMOVED***)
4) Open terminal & run - brew install bfg
5) bfg --replace-text password.txt
6) git reflog expire --expire=now --all && git gc --prune=now --aggressive
7) git push --force
