# nbgitpuller

[nbgitpuller](https://jupyterhub.github.io/nbgitpuller/index.html) is a tool lets you distribute content in a git repository to your students by having them click a simple link. It relies on [automatic, opinioned conflict resolution](https://jupyterhub.github.io/nbgitpuller/topic/automatic-merging.html#topic-automatic-merging) that ensures that your students are never exposed to `git` directly. This tools comes pre-installed in your JupyterHub

If you are not familiar with git and GitHub, we recommend you visit the [Git](../git-basics/git-cheatsheet.md) section of this dosumentation. Before you can start using `nbgitpuller` you will need a GitHub account and a repository that you wish to distribute to your students. 

Once you have a repository with the material that you wish to distribute, you can generate an _nbgitpuller links_ with the [generator](https://jupyterhub.github.io/nbgitpuller/link).  The requirements of the generator are depicted and explained below. The circled locations required special attention

1. This is the link generated. It can be copied and sent to your students
2. The url of your hub
3. The git repository where you have published your content. Please notice that the url starts can start either with **git://** or **https://.** If you are not expencting your students to have configured github authentication nor have a GitHub account, make sure you use **git://.** 
4. Notice that your URL **does not** end in .git. \(This is often the case if you are pasting URL from GitHub\)
5. The branch of the repository you wish to distribute
6. Optionally, a particular file or directory you want to automatically open for your students once the repository has been synchronized.
7. Choose the **JupyterLab** interaface as this is the default for all of Brown's Hubs
8. If you are distributing the link via **Canvas,** select the appropiate tab

![](../.gitbook/assets/nbgitpuller.png)

1. 
