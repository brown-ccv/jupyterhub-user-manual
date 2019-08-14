# Saving and Uploading \(git commit/push\)

Once you have made changes to an assignment and are ready to save your progress, there are a few steps that you must do prior to closing the hub if using git to keep your changes save. Once again, the interaction with git can be via Plugin user interface or a terminal session

## 1. Saving your work using GIT Plugin \(UI\)

 

## Step 1: Open terminal and move to working assignment directory

Launch a terminal on JupyterHub by following the instructions below:

1. Select the local![](https://firebasestorage.googleapis.com/v0/b/gitbook-28427.appspot.com/o/assets%2F-LLCCXzhzhO5fUT5UTHC%2F-LMmBQGJ7BT7b2AWahYH%2F-LMlxyNgzr5hNq7NVLZt%2FScreenshot%20from%202018-09-19%2009-14-01.png?alt=media&token=fe7682b4-5b85-4043-bfca-360ffd79dea8)File Browser from left sidebar
2. Create a new launcher using the ![](https://firebasestorage.googleapis.com/v0/b/gitbook-28427.appspot.com/o/assets%2F-LLCCXzhzhO5fUT5UTHC%2F-LMnMc81jihkXNmOWoVK%2F-LMnMdrGWVaRcDlycwXr%2FScreenshot%20from%202018-09-19%2015-46-05.png?alt=media&token=ce6cda07-111d-4da1-a23e-4f84f72b82c6)New Launcher button
3. Click **Terminal** under the **Other** section
4. A new “Terminal \#” window will appear your browser.
5. Navigate to your current working assignment directory using the cd command

```
$cd {assignmentDirectory}
```

## Step 2: Commit Changes to be Saved \(git add/commit\)

From the directory containing your actively worked on assignment, you must first add and commit changes you have made which will be prepared to be saved remotely on the git repository. Think of this as staging any changes you have made, but not actually saving them yet. This first step provides the opportunity to add a commit message where you can document the changes you have made with this current save, which should be descriptive but not necessarily comprehensive.

```
$git commit -a -m "Notes about changes"
```

{% hint style="warning" %}
Committing changes does not automatically save them to the repository! Don't forget to do step 3 and push the changes.
{% endhint %}

## Step 3: Save Changes to Repository \(git push\)

Once the changes have been stage following [Step 2](../github-classroom-student-guide/submitting-assignments.md#step-2-commit-changes-to-be-saved-git-add-commit), the last step is to actually save the changes to the remote repository using the push command.

```
$ git push
```

It will require you to enter your github credentials and then will begin to save the changes to your remote repository for the git classroom. 

{% hint style="info" %}
 It is recommended that you git commit and push at the end of each working session or whenever a major change has been made to the codebase.
{% endhint %}

