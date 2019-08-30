# .dotfiles_cisa - Linux configuration files for home machines #

These are the Linux configuration files that are specific to my home
machines.  The intent is that this repository be checked out into your
home directory.  After that installing the files is as simple as
running `stow` for each (non-.git) entry in the `.dotfiles` directory:

```console
for d in $(find . -maxdepth 1 -mindepth 1 -type d -not -name ".git" -exec basename {} \;)
do
    stow "$d"
done
```

This is precisely what is done in the `deploy.sh` script.
