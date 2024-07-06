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

### [Plesk to DL to Git]()
If you'd like to work with instant updates, even if inconvenient.

<br>

## Does this mean a short wait for each update?
Yes, there is a short wait for the Continuous Deployment system on Plesk to update the submodules, and reflect your changes. 

As Sammy, the author, who designed the CD system and wrote this doc; i usually use this wait time to double check changes. I sometimes will use the Sandbox described in the Plesk workflow to test small things or double check variables to ensure things worked when in times of uncertainty.

The [Plesk workflow](https://github.com/ACADEV1/.github/blob/dev/docs/workflows/plesk/README.md), has this sandbox where these delays can be avoided. **But, it is a much less safe and more inconvenient way to work with Git as you have to download and merge. It is ideal as a test bed, not as a dev environment**.

The non-cloud local dev environment is under construction to solve this.