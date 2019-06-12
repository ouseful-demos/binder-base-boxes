# binder-base-boxes
Baseboxes for MyBinder

If a MyBinder repo contains `nbgitpuller`, Binderhub / MyBinder can pass a `git-pull?` argument through as part of a MyBinder launch URL that allows you to pull notebooks from a second, nbgitpulled repository into a container launched from the first repo.

The branches of this repo define various "MyBinder baseboxes" built to include packages relevant to different subject areas. These boxes are prebuilt and can be used as a basis for running your own notebooks stored in regularly updated repos without having to rebuild the base box each time your notebook repo is updated.

To pull the contents of a repo `http://github.com/USER/REPO` into a MyBinder container built from a particular `binder-base-boxes` branch, use a MyBinder URL of the form:

```
https://mybinder.org/v2/gh/ouseful-demos/binder-base-boxes/BASEBOXBRANCH/?urlpath=git-pull?repo=https://github.com/USER/REPO
```

To pull the contents from a particular branch of a repo `http://github.com/USER/REPO/tree/BRANCH`, use a MyBinder URL of the form:

```
https://mybinder.org/v2/gh/ouseful-demos/binder-base-boxes/BASEBOXBRANCH/?urlpath=git-pull?repo=https://github.com/USER/REPO%26amp%3Bbranch=BRANCH
```

*Note the escaping on the `&` conjunction that keeps it inside the scope of the `git-pull?repo` phrase.*

To pull the contents from a particular branch of a repo `http://github.com/USER/REPO/tree/BRANCH` and launch into a particular notebook, use a MyBinder URL of the form:

```
https://mybinder.org/v2/gh/ouseful-demos/binder-base-boxes/BASEBOXBRANCH/?urlpath=git-pull?repo=https://github.com/USER/REPO%26amp%3Bbranch=BRANCH%26amp%3Bsubpath=FILENAME.ipynb
```

Read more: [Feeding a MyBinder Container Built From One Github Repository With the Contents of Another](https://blog.ouseful.info/2019/05/08/feeding-a-mybinder-container-from-one-github-repository-with-the-contents-of-another/).

---

`textanalysis`

music

This box contains various Python packages that support the creation of notebooks relevant to topics in text analysis and text analysis of classics texts.

Example notebooks:

https://mybinder.org/v2/gh/ouseful-demos/binder-base-boxes/textanalysis/?urlpath=git-pull?repo=https://github.com/psychemedia/showntell%26amp%3Bbranch=linguistics

Or launch into a speccific example notebook:

https://mybinder.org/v2/gh/ouseful-demos/binder-base-boxes/textanalysis/?urlpath=git-pull?repo=https://github.com/psychemedia/showntell%26amp%3Bbranch=linguistics%26amp%3Bsubpath=4.2.0%20Classics.ipynb

Note that to pull from the branch we need to properly escape the & conjunction so that it remains within the scope of the git-pull? clause.
