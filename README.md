
# My Favorite Git Aliases

In the last few years since switching from SVN to Git, I've picked up a few aliases that have helped me streamline my workflow and be all around more productive. After all, the whole point of shortcuts is to make your life easier right? I'd like to share my aliases with you, however unhelpful they may be.

## Installation

Download the file `gitalias.txt` and put it anywhere you want:

    curl -O https://raw.githubusercontent.com/MegaMattMiller/gitAliases/master/gitAliases.txt

Edit your file `.gitconfig` and include `gitalias.txt` such as:

    [include]
        path = path/to/gitalias.txt

## Branching

```.gitconfig

co = checkout # Shortcut for checkout.
nb = checkout -b # Create a new branch and check it out.
bl = branch -l # List all local branches.
br = branch -r # List all remote branches.
blr = branch -a # Show local and remote branches.
bd = branch -d # Politely ask Git to delete a local branch.
bdf = branch -D # Sternly ask Git to delete a local branch.

```

## Fetching/Syncing/Merging

```.gitconfig

fp = fetch -p # Fetch and prune.
sync = !git pull && git push # Pull then push current branch.
mm = !git fetch -p && git merge origin/master #Merge remote master into the current branch.

```

## Committs

```.gitconfig

cm = commit # Shortcut for commit.
cma = commit -a # Commit all tracked.
cmam = commit -a -m # Commit all tracked with message to follow.
runAway = reset --hard # For when you just want it all to go away.
forgetAbout = rm --cached # Make Git forget about a tracked file.

```

## Utilities

```.gitconfig

alias = config --get-regexp ^alias\\. # List all aliases.
ec = config --global -e # Open .gitconfig in your default editor.

```