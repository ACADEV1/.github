# Editing files on Plesk (web)
This will be done using:
- Plesk (Web)
- \>16GB free storage
- Access to your project's GitHub repo

⚠️ Try not to use this option to make big changes, make a small changes incrementally.

⚠️ If you go too long without committing (truly saving) back to git, you risk losing your changes and overriding other people's changes. The process becomes unecessarily complicated and involved with large merge conflicts to be resolved.

⚠️ I won't be covering solving merge conflicts here. To avoid merge conflicts, do not leave your changes here without being saved back for too long as your detached/sandboxed instance of the code will become too outdated. 

<br>

### 1. Logon to Plesk
1. Go to https://app1sandbox.startupstatus.co:8443/login_up.php
2. Login with the sandbox credentials:
    - 📧 Request the credentials from itdev@advancingcommunities.au

<br>

### 2. Clone the source
###### Remember this is NOT GIT your changes won't be tracked directly here.
1. Navigate to the app1sandbox.startupstatus.co section, and find the 'Files' option
2. Press the blue + button, and select 'Create directory', set the directory name as your name or GitHub alias
3. Press the empty box to the left of p000 to mark it as checked
4. At the top, press 'Copy'
5. Navigate httpsdocs/[your alias or name]/
6. Press 'Ok'
7. You should find p000 pasted in your dir

<br>

### 3. Sandbox away
Edit and save files, try to recall what exact changes your making. Do not go overboard on changes, do one small change or testing and then proceed to next step (try to stick to fine-grained route).

<br>

### 4. Truly save changes
Just saving changes here is not enough, git is the source of truth. This means we need to get your changes back and rejoin with the HEAD.

The fine-grained route (preferred):
1. Copy your exact changes
2. Find the file in GitHub and paste at the same spot in this tracked file
3. Commit as shown in: [Simple GitHub editor](https://github.com/ACADEV1/.github/blob/dev/docs/workflows/cloud/github/simple.md)
4. Repeat steps 1-3 for each change
5. **Test!!**

The forced route (discouraged):<br>
(Usually, more if you have left it too long with lots of changes, or are under a time pressure.)
1. Archive and download the entire repo dir of which your changes are in **(not category repos like p000/, but pXXX-Some-Repo/)**
2. Unarchive on your local computer
3. Drag and drop the pXXX-Some-Repo/ on it's repo page in GitHub
4. Follow the instructions to add each file
    - If it says the changeset is 'too big', instead drag and drop each of the files you changed as needed to their dirs instead.
5. **Test!!** 

<br>

### 5. Reset your, and the source, sandbox
1. Go to **your root** and select p000 (never touch the source p000, unless you make a small edit/test with it then do the following immediately)
2. If all changes have been saved, do not continue to use it: delete your instance of p000
3. Navigate to 'Scheduled tasks' (same dashboard where 'Files' is found)
4. Find ./p000-deploy.bash and press 'Run now'
6. When the task is finished, repeat step 2.
    - If there is an error in p000-deploy, alert itdev@advancingcommunities.au and create an issue in this .github repo. 
    - Feel free to try the task again, but an error here would mean the method is not currently safe to continue with.

<br>

## Does this mean a short wait for each update?
Not in this case, see the [cloud README](https://github.com/ACADEV1/.github/blob/dev/docs/workflows/cloud/README.md#does-this-mean-a-short-wait-for-each-update)