SSH Keys allow you to connect to GitLab without entering a username and password. Some sites, like GitHub, let you choose which authentication mechanism you want to use, but our GitLab requires SSH Keys. Creating your own is simple.

## Generate your key

In your terminal, run

```sh
ssh-keygen
```

There are three prompts to skip:
1. Choosing a custom file name.
2. Putting a password on your key.
3. Confirming your password.

So hit enter three times to skip these three prompts. Your key has been generated!

## Uploading to GitLab

First, copy the key to your clipboard so you can easily paste it. You can do this from the terminal:

**MacOS**: `pbcopy < ~/.ssh/id_ed25519.pub`

**Git Bash on Windows**: `cat ~/.ssh/id_ed25519.pub | clip`

**Linux**: `xclip -sel clip < ~/.ssh/id_ed25519.pub`

Now, go to git.gmu.edu and login. Click on your avatar in the top right and click "Settings" in the dropdown. Select the "SSH Keys" Menu on the left. Paste your key into the box and click "Add Key".

## Testing

To test if your key worked, run the following command in your terminal:

```sh
ssh -T git@git.gmu.edu
```

You should see a welcome message. If not, ask for help in the #help channel in Slack.
