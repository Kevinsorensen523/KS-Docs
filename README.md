# KS-Docs
Some Random Documentation From KS

## Github SSH Key Error
### Generate a New SSH Key (Optional)
```sh
  ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```

### Add the SSH Key to ssh-agent
```sh
  eval "$(ssh-agent -s)"
  ssh-add ~/.ssh/id_rsa
```

### Add SSH Key to GitHub
```sh
  cat ~/.ssh/id_rsa.pub | xclip -selection clipboard
```
Or manually
```sh
  cat ~/.ssh/id_rsa.pub
```
Then, go to GitHub, navigate to Settings > SSH and GPG keys > New SSH key.
Paste your key into the field, give it a descriptive title, and save it.

### Verify
```sh
  ssh -T git@github.com

```
