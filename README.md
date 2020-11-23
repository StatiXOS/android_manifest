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

Patches are always welcome!  Please submit your patches to our Gerrit.

To start contributing, just register at https://review.statixos.com

Open up terminal to create your ssh keys required for submitting patches to gerrit and type in:

```bash
git config --global review.statixos.com.username <username you registered with>

git config --global review.statixos.com.email <your email you registered with>

ssh-keygen -t rsa -C "your@email.com"
```

In our gerrit click on your "Avatar" on the top right, then on "Settings".

While in 'Settings' Click on "SSH Public Keys" on the left hand side and then on "Add Key".

Now on your computer navigate to your home "~/.ssh" and open up "id_rsa.pub", copy/paste the context to "Gerrit SSH Public Keys".

You can send patches to us by using these commands in terminal:

```
    (From root android directory)
    . build/envsetup.sh
    (Go to repo you are patching, make your changes and commit)
    pixelgerrit push eleven

    or

    git push ssh://<username>@review.statixos.com:29418/<project> HEAD:refs/for/<branch>
```

* `<username>` - Your Gerrit username (which can be seen/set [here](https://review.statixos.com/#/settings/))
* `<project>` - The git repo you are pushing to; all options can be viewed at [this link](https://review.statixos.com/#/admin/projects/)
* `<branch>` - The git branch your change is based on; for projects using this manifest, it is `eleven`

Make your changes and commit with a detailed message, starting with what you are working with
Commit your patches in a single commit. Squash multiple commits using this command: `git rebase -i HEAD~<# of commits>`

[View Code Review](https://review.statixos.com/)

XDA Thread Template: https://del.dog/statix-thread-template
