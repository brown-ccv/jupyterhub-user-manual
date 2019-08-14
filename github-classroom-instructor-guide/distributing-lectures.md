# Distributing Lectures

## Option 1: Distribute using nbgitpuller

`nbgitpuller` lets you distribute content in a git repository to your students by having them click a simple link. [Automatic, opinioned conflict resolution](https://jupyterhub.github.io/nbgitpuller/topic/automatic-merging.html#topic-automatic-merging) ensures that your students are never exposed to `git` directly. This tools comes pre-installed in your JupyterHub

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
The first time a particular student clicks the link, a local copy of the repository is made for the student. On successive clicks, the latest version of the remote repository is fetched, and merged automatically with the student’s local copy using a [series of rules](https://jupyterhub.github.io/nbgitpuller/topic/automatic-merging.html#topic-automatic-merging) that ensure students never get merge conflicts.

## Option 1: Distribute one lecture materials as assigments

1. Have the materials for one lecture in a repository  
2. Distribute as assignment, with its own link, and no deadline

### Advantages

*  Students can stay as outside collaborators for ever.
* There is no special consideration for shopping period
*  All of their lecture work is automatically set up in your organization … with a default place for them to work there are less chances for them to be pushing it to their own public GitHub…
* Less management of merging conflicts and remotes

### Disadvantages

* There will be a lot of repositories in the organization.
* No simple mechanism for pushing changes after distributiom

## Option2: All lectures in one repository

![Lecture Workflow](../.gitbook/assets/github2fjupyterhublecturesworkflow-6941c84d-791b-41c2-a48a-8a403e9f33b0.png)

**During shopping period:**

1. Set up the lectures to be public
2. Students clone and pull from public repository
3. 
**After shopping period:**

1. Have a first assigment to generate a link.  
2.  Students that accept the link become **outside collaborators** in your organization  
3. Invite the students to join the organization.   
4. You should make a team for the students and give them read access to the private lecture repository  
5. As members of the organization, they can create a repository to push their personal changes to the lectures. In order to sync with their own repository and with yours, they will need to set up two remotes. See [https://help.github.com/articles/adding-a-remote/](https://help.github.com/articles/adding-a-remote/) for more help  
  




### 

