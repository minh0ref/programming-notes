## Multiple github accounts on one machine

Step 1. Generate an SSH key

```sh
cd ~/.ssh
ssh-keygen -t ed25519 -C "your_email_address"
```

Follow the prompts and enter your github username 

Step 2. Add SSH key to SSH Agent

```sh
ssh-add ~/.ssh/id_ed25519_github_username
```

Step 3. Copy the SSH public-key to Github 

`~/.ssh/id_ed25519_github_username.pub`

https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account

Step 4. Add a host entry to the `~/.ssh/config` file

```
Host github_username
  HostName github.com
  User git
  IdentityFile ~/.ssh/id_ed25519_github_username
```

Step 5. Config your remote

```sh
git remote add origin git@github.com-<your-username>[:owner-user-name]/<the-repo-name>.git
```

Step 6. Config git user.name and user.email

```
git config user.email "your email"
git config user.name "your name"
```