# Configuring users

To configure the user globally:

```sh
git config --global user.name "Your beautiful name"
git config --global user.email "name@email.com"
```

This will update the `~/.gitconfig` file.

To configure the user on a specific repository:

```sh
git config --local user.name "Your beautiful name"
git config --local user.email "name@email.com"
```

This will update the `.git/config` file on your repository.