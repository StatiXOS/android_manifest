[<center><img src="https://raw.githubusercontent.com/sourajitk/STX-Logo/main/stx-2023.png" height="50%" width="50%;" /></center>](https://github.com/StatiXOS)

## Building Android ##
Your one-stop destination for all the documentation about building Android can be found [here](https://source.android.com/setup/build/building).

## Repo Init ##
```bash
repo init -u https://github.com/StatiXOS/android_manifest.git -b udc-qpr1
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

First, we need to create an SSH key that is required to push patch sets to Gerrit. Type the following command into the terminal:

```bash
ssh-keygen
```

Head to our Gerrit and click on your avatar in the top right corner. Then click "Settings."

In settings, click on "SSH Keys" on the left-hand side of the screen.

Now on your computer, type in cat ~/.ssh/id_rsa.pub, copy the output and paste the copied contents in the box that says "New SSH key" and press on the "Add New SSH Key" button.

Make your changes and commit with a detailed message. The commit message should start with the name of the current project to help us during the review process.

We are almost there! Now to push your patch set to Gerrit, type in the following in your terminal:

```bash
    git push ssh://<username>@review.statixos.com:29419/<project> HEAD:refs/for/<branch>
```

* `<username>` - Your Gerrit username (which can be seen/set [here](https://review.statixos.com/#/settings/))
* `<project>` - The git repo you are pushing to; all options can be viewed at [this link](https://review.statixos.com/#/admin/projects/)
* `<branch>` - The git branch your change is based on; for projects using this manifest, it is `udc-qpr1`

[View Code Review](https://review.statixos.com/)

[XDA Thread Template](https://downloads.statixos.com/template/template.txt)
