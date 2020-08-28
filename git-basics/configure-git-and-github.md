# Set Up Git in JupyterHub

We recommend syncing content to and from JupyterHub using Git and GitHub. However, before you can start, we will need to tell Git and GitHub who we are. JupyterHub contains an utility program that simplifies the process of this configuration which consists of the following steps

### 1. Configure Git

First, add your name and email to git config \(lines 1 and 2\). Also set git to always clone using SSH \(line 3\). Line 4 sets the default branch name to `main` instead of the traditionally used `master`.

```text
git config --global user.name "John Doe" (don't forget the quotes!)
git config --global user.email your_email@example.com
git config --global --add url."git@github.com:".insteadOf "https://github.com/"
git config --global init.defaultBranch main
```

### 2. Generate and SSH Key and add it to GitHub

1. Start a terminal session
2. Generate an ssh key:

   ```text
   ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
   ```

This creates a new ssh key, using the provided email as a label.

```text
> Generating public/private rsa key pair.
```

3. When you're prompted to "Enter a file in which to save the key," press Enter. This accepts the default file location:

```text
> Enter a file in which to save the key (/Users/you/.ssh/id_rsa): [Press enter]
```

4. At the prompt, type a secure passphrase. You can leave that field empty and press enter. If you leave empty, you won't be asked for the passphrase when connecting to GitHub. For more information, see ["Working with SSH key passphrases"](https://docs.github.com/en/articles/working-with-ssh-key-passphrases).

```
> Enter passphrase (empty for no passphrase): [Type a passphrase]
> Enter same passphrase again: [Type passphrase again]
```

```text
    git config --global --add user.name "$NAME"
    git config --global --add user.email $EMAIL
    git config --global --add url."git@github.com:".insteadOf "https://github.com/"
```

5. Add your SSH Key. The command below will show the public SSH key on the terminal. Copy the entire key, starting with `ssh-rsa` and ending with your email.

```text
head ~/.ssh/id_rsa.pub
>ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAACAQCvnp4mhAo9OddNeCFNKGacL6N2Fg4SNzNgLChc55VrrWTpcKOh0QEbqt4urx9ZpB9DgNd+hrpCrMVZBk3mEHeI5egXmstBe/HKN8ySD92DW1ZQbtvx+LOFDTP90oHuC6UHezUvkGEBGapKnlr9pjNYLWpi1cQ5/os99qzH1TH9oYjhdpFHOkh5y6hRkwRhXcsWzYpL5UVn0ZbBslWBD1p31PAwOYfnSE01iNtgyZ1ohyb2S2vk3rh7IWWDuAQreyQf4zoLos7/x47+8q3FLpUhmrGKGf6mCsFLMyBUiDvGHYZ5LdyfiAVXM4fvJ94qniKE0d+Iv0+ia1GwxuaKLDhzeOhQhnkU0F04aJ1Wth3M3cSPl/r2cPoNiqVsuwZkrueNefWqiYUlBBq0gQm95dx3CzZisrT86s+NK7h+XhcDUWW8R6K5MLD/jqH1uMT3MLu6ShP+URu4rm9HrPt/Ie1onlk5bKZK7bqA6qkJeIPDpliGfd/ztoFKpHN//9LYKubcsnXOTLIDuHJdeOkMeMOxHCUCpmeK3AupXKKONt8EXEX8yDjIcKo1baB5Ti2MrO1HGsrJgqbhwvEvHD45sq00miWkV8EFa3Yu9pQ2FaeBv/muPa1CLPMyDrFCFZUJi/q0XLoGcxUxseXm6puCLj91J0wZLZxSbx3wW4aUU97GhQ== your_email@email.com
```

6. Go to [https://github.com](https://github.com). In the upper-right corner of any page, click your profile photo, then click **Settings**.

![Settings icon in the user bar](https://docs.github.com/assets/images/help/settings/userbar-account-settings.png)

7. In the user settings sidebar, click **SSH and GPG keys**.

![Authentication keys](https://docs.github.com/assets/images/help/settings/settings-sidebar-ssh-keys.png)

8. Click **New SSH key** or **Add SSH key**.

![SSH Key button](https://docs.github.com/assets/images/help/settings/ssh-add-ssh-key.png)

9. In the "Title" field, add a descriptive label for the new key. For example, if you're using a personal Mac, you might call this key "Personal MacBook Air".

10. Paste your key into the "Key" field.

![The key field](https://docs.github.com/assets/images/help/settings/ssh-key-paste.png)

11. Click **Add SSH key**.![The Add key button](https://docs.github.com/assets/images/help/settings/ssh-add-key.png)

12. If prompted, confirm your GitHub password.

![Sudo mode dialog](https://docs.github.com/assets/images/help/settings/sudo_mode_popup.png)

### Done!

### 3. For more information check GitHub's documentation: 

 [https://help.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh](https://help.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh)



