# Configuring GitHub

To use GitHub, you first need to set up a SSH key and configure your name and email. We provide a script that does that for you.

1. Open a terminal window
2. Run the `gitconfig` command:`gitconfig -u github_username -n your_name -e your@email.com`
3. Enter your GitHub password when asked.
4. Then, you will get this message:`The authenticity of host 'github.com (192.30.253.113)' can't be established. RSA key fingerprint is SHA256:nThbg6kXUpJWGl7E1IGOCspRomTxdCARLviKw6E5SY8. Are you sure you want to continue connecting (yes/no)?`
5. Type `yes` and hit enter.

To confirm that a SSH key was added to your GitHub, go to [https://github.com/settings/keys](https://github.com/settings/keys).  You should see an entry like the image below, where the name of the key is similar to `jupyter-your_username`

![](../.gitbook/assets/ssh-key.png)

