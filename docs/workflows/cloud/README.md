# Coding in the Cloud
We provide a few options for coding.
###### ⭐ = Recommended, thus far.

<br>

### [Just on GitHub](https://github.com/ACADEV1/.github/blob/dev/docs/workflows/cloud/github/README.md) ⭐
If you'd like to use this web platform. 

<br>

### [Local to Git](https://github.com/ACADEV1/.github/blob/dev/docs/workflows/cloud/local/README.md)
If you're comfortable with your own vscode environment.

<br>

### [Plesk to DL to Git](https://github.com/ACADEV1/.github/blob/dev/docs/workflows/cloud/plesk/README.md)
If you'd like to work with instant updates, even if inconvenient.

<br>

## Does this mean a short wait for each update?
Yes, there is a short wait for the Continuous Deployment system on Plesk to update the submodules, and reflect your changes. 

As Sammy, the author, who designed the CD system and wrote this doc; i usually use this wait time to double check changes. I sometimes will use the Sandbox described in the Plesk workflow to test small things or double check variables to ensure things worked when in times of uncertainty.

The [Plesk workflow](https://github.com/ACADEV1/.github/blob/dev/docs/workflows/cloud/plesk/README.md), has this sandbox where these delays can be avoided. **But, it is a much less safe and more inconvenient way to work with Git as you have to download and merge. It is ideal as a test bed, not as a dev environment**.

The non-cloud local dev environment is under construction to solve this.

<br>

## How do i merge to production?
If you're the dev:
1. Go to the repo you've made ``dev branch`` changes to.
2. Press the 'Pull Requests' tab
3. Press 'New Pull Request'
4. Make 'base': 'prod' and 'compare': 'dev'
5. Press 'Create Pull Request' (if it's greyed out, it means there is no difference in commits between the two)
6. Add a descriptive title and description of what is being merged to production
7. Add a reviewer and notify the reviewer that the pull request will need approving (double checking)

If you're a reviewer:
1. Open the pull request and press 'Review'
2. It will provide you with options to leave a comment, request a change or approve
3. If you approve, you can proceed to push through the pull request if it's time sensitive ~ or you can leave it to the dev

If you're the dev (continued):
1. When it's approved or amendments are made and it's gone through the process to be approved
2. Press the down arrow next to merge and do 'Squash and merge'
3. Confirm
