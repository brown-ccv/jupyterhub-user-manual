# Configuring Git and GitHub

We recommend syncying content to and from JupyterHub using Git and GitHub. However, before you can start we need to tell Git and GitHub who we are. JupyterHub contains an utility program that simplifies the process of this configuration which consists of the following steps

1. Make sure you have your **GitHub User Handle** and **Password**
2. [Launch a terminal session ](../getting-started/launch-a-terminal-session.md)
3. Run the `gitconfig` command:`gitconfig -u github_username -n your_name -e your@email.com`
4. Enter your GitHub password when asked.
5. Then, you will get this message:`The authenticity of host 'github.com (192.30.253.113)' can't be established. RSA key fingerprint is SHA256:nThbg6kXUpJWGl7E1IGOCspRomTxdCARLviKw6E5SY8. Are you sure you want to continue connecting (yes/no)?`
6. Type `yes` and hit enter.

To confirm that a SSH key was added to your GitHub, go to [https://github.com/settings/keys](https://github.com/settings/keys).  You should see an entry like the image below, where the name of the key is similar to `jupyter-your_username`

![](../.gitbook/assets/ssh-key.png)

You are all set to start using Git and GitHub inside JupyterHub!

1. 
