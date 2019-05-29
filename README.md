# binder-base-boxes
Baseboxes for MyBinder

If a MyBinder repo contains `nbgitpuller`, Binderhub / MyBinder can pass a `git-pull?` argument through as part of a MyBinder launch URL that allows you to pull notebooks from a second, nbgitpulled repository into a container launched from the first repo.

The branches of this repo define various "MyBinder baseboxes" built to include packages relevant to different subject areas. These boxes are prebuilt and can be used as a basis for running your own notebooks stored in regularly updated repos without having to rebuild the base box each time your notebook repo is updated.

Read more: [Feeding a MyBinder Container Built From One Github Repository With the Contents of Another](https://blog.ouseful.info/2019/05/08/feeding-a-mybinder-container-from-one-github-repository-with-the-contents-of-another/).

---

`music`

This box contains various Python packages that support the creation of notebooks relevant to topics in *music*.

Example notebooks:

https://mybinder.org/v2/gh/ouseful-demos/binder-base-boxes/music/?urlpath=git-pull?repo=https://github.com/psychemedia/showntell%26amp%3Bbranch=music

Or launch into a speccific example notebook:

https://mybinder.org/v2/gh/ouseful-demos/binder-base-boxes/music/?urlpath=git-pull?repo=https://github.com/psychemedia/showntell%26amp%3Bbranch=music%26amp%3BsubPath=index_music.ipynb

Note that to pull from the branch we need to properly escape the `&` conjunction so that it remains within the scope of the `git-pull?` clause.
