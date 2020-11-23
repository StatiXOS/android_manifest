[<center><img src="https://raw.githubusercontent.com/sourajitk/STX-Logo/main/stx-2020.png"/></center>](https://github.com/StatiXOS)

## Building Android ##
[Setting Up Build Environment](https://itz63c.github.io/posts/android-build-env/)

## Repo Init ##
```bash
repo init -u https://github.com/StatiXOS/android_manifest.git -b 11
```
## Sync Source ##
```bash
repo sync --force-sync --no-clone-bundle --current-branch --no-tags -j$(nproc --all)
```
## Build Time (Linux x86_64 ONLY) ##
```bash
. build/envsetup.sh
brunch statix_<DEVICE>-userdebug (or statix_<DEVICE>-user)
```
### Submitting Patches ###

Patches are welcomed here at StatiXOS. 

To start contributing, register at https://review.statixos.com and follow the steps below:

First, we need to create ssh keys that are required for pushing patchsets to Gerrit. For that type in the follwing in your terminal console:

```bash
ssh-keygen -t rsa -C "your@email.com"
```

Now head to our Gerrit and click on your "Avatar" which is to the top right of the screen and then click on "Settings".

While in Settings, click on "SSH Public Keys" on the left hand side of the screen and then on "Add Key".

Now on your computer, type in ``cat ~/.ssh/id_rsa.pub``, copy the output and paste the copied contents to "Gerrit SSH Public Keys".

Make your changes and commit with a detailed message. The commit message should start with the name of the project you are working on. This helps us greatly during the review process.

We are almost there! Now to push your patchset to Gerrit, type in the following in your terminal:

```bash
    git push ssh://<username>@review.statixos.com:29418/<project> HEAD:refs/for/11
```

* `<username>` - Your Gerrit username (which can be seen/set [here](https://review.statixos.com/#/settings/))
* `<project>` - The git repo you are pushing to; all options can be viewed at [this link](https://review.statixos.com/#/admin/projects/)
* `<branch>` - The git branch your change is based on; for projects using this manifest, it is `eleven`

[View Code Review](https://review.statixos.com/)

XDA Thread Template: https://del.dog/statix-thread-template
