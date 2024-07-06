# Coding to Cloud w/ Local
This will be done using:
- Git CLI
- OpenSSH CLI
- VSCodium

So retrieve and install these if needed. This will be a minimal technical guide, you may need to seek external resources (or ask a peer) for more step-by-steps for each part, for your respective platform. All of the above are available on Linux, Mac and Windows.

DO NOT 'RELY' ON THE EXAMPLE COMMANDS ATTACHED TO STEPS. They are for your reference only, not explicit and detailed step-by-steps. Especially if you are not on Linux, as they are linux commands.

<br>

### 1. Authenticate your Git client
###### # Openssh should come with ssh-keygen
1. Create an ssh key (ed25519): ssh-keygen -t ed25519
2. Copy the contents of the key: cat ~/.ssh/ed25519.pub
3. Navigate to the keys page in your GitHub profile: https://github.com/settings/keys
4. Add as a new SSH **auth** key
5. You may need to be sure you have an SSH agent running, otherwise the key won't be used: eval $(ssh-agent -s)

<br>

### 2. Configure your Git client
###### # You should be able to use these (non-optional) commands with your git, they aren't just reference.
1. git config --global user.email [your email]
2. git config --global user.name [your github username]
3. (optional) git config --global user.signingkey [GPG key as generated and added to GitHub, verifies your commits]
4. (optional, joint with above) git config --global user.gpgsign true

<br>

### 3. Clone your project locally
1. Navigate to the directory you'd like to edit in: cd Documents/Code/
2. Figure out the repository you:
    - Have access to
    - Would like to edit
###### # You should be able to use these commands with your git, they aren't just reference.
2. git clone git@github.com:ACADEV1/[your repo].git

<br>

### 4. Edit away
1. Open VSCodium and in the top left, press 'File'
2. In the drop-down menu, press 'Open Folder'
3. Navigate to where you cloned the repo/project
4. Press 'Open'

<br>

### 5. Committing and pushing (saving changes)
1. In your git cli, navigate to where you cloned the repo/project: cd Documents/Code/my-repo
2. git status # to see your changes
3. git pull # grab changes from git before you commit any, easy way to avoid conflicts
3. Add your changes
    - git add -p # add interactively
    - git add . # add all indiscriminantly (unsafe) 
4. git push # push up your local changes to the repo

<br>

### 6. Your changes reflected
1. In README.md at the root of the repo there should be a README, open it
2. In this file there should be a URL
3. Upon clicking the URL, given a short moment for the CD system to update, your changes should be visible

<br>

## Does this mean a short wait for each update?!
Yes, there is a short wait for the Continuous Deployment system on Plesk to update the submodules, and reflect your changes. 

As Sammy, the author, who designed the CD system and wrote this doc; i usually use this wait time to double check changes. I sometimes will use the Sandbox described in the Plesk workflow to test small things or double check variables to ensure things worked when in times of uncertainty.

The [Plesk workflow](https://github.com/ACADEV1/.github/blob/dev/docs/workflows/plesk/README.md), has this sandbox where these delays can be avoided. **But, it is a much less safe and more inconvenient way to work with Git as you have to download and merge. It is ideal as a test bed, not as a dev environment**.

The non-cloud local dev environment is under construction to solve this.