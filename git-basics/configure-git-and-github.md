# Configuring Git in JupyterHub

We recommend syncying content to and from JupyterHub using Git and GitHub. However, before you can start, we will need to tell Git and GitHub who we are. JupyterHub contains an utility program that simplifies the process of this configuration which consists of the following steps

{% hint style="warning" %}
If you are using **Two-factor Authentication** for your github, then you will need to set up a [personal access token](https://help.github.com/en/articles/creating-a-personal-access-token-for-the-command-line) and follow [these instructions ](configure-git-and-github.md#advanced-topic-the-details-behind-gitconfig)instead
{% endhint %}

1. Make sure you have your **GitHub User Handle** and **Password**
2. Inside your Jupyter Hub [Launch a terminal session ](../getting-started/launch-a-terminal-session.md)
3. In the terminal type the `gitconfig` command:`gitconfig -u github_username -n your_name -e your@email.com`
4. Enter your GitHub password when asked.
5. Then, you will get this message:`The authenticity of host 'github.com (192.30.253.113)' can't be established. RSA key fingerprint is SHA256:nThbg6kXUpJWGl7E1IGOCspRomTxdCARLviKw6E5SY8. Are you sure you want to continue connecting (yes/no)?`
6. Type `yes` and hit enter.

To confirm that a SSH key was added to your GitHub, go to [https://github.com/settings/keys](https://github.com/settings/keys).  You should see an entry like the image below, where the name of the key is similar to `jupyter-your_username`

![](../.gitbook/assets/ssh-key.png)

You are all set to start using Git and GitHub inside JupyterHub!

## Advanced Topic: The details behind gitconfig

While we provide `gitconfig` as an utility function, there is no magic behind it. If you prefer carrying out the configuration on your own, follow the instructions in the following links. You will also need to carryout this steps if you have two factor authentication enabeled.

### 1. Configure Git

```text
    git config --global --add user.name "$NAME"
    git config --global --add user.email $EMAIL
    git config --global --add url."git@github.com:".insteadOf "https://github.com/"
```



### 2. Connecting to GitHub with SSH keys

Follow GitHub's instructions:; [https://help.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh](https://help.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh)



