# Creating a project
This guide will help you create a project, including linking it in to git and (in this instance) plesk.

1. Add your repository as a git submodule to p000 dev (for development access), and if in a ready state the same to p000 prod (for production access)
2. Then, in repository settings -> webhooks, add a webhook on push event: https://ws1.startupstatus.co:8443/modules/git/public/web-hook.php?uuid=86f8da09-ea37-298c-6c6a-f08b07d04645
