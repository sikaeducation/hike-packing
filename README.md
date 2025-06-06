# Hike Packing

You've just been on the worst hike of your life, but you have a plan to turn it
all around and it's time to pack. Right now everything is jumbled up in one big
pile. Break up the commit into smaller commits to get organized.

## Instructions

1. Clone this repository to your computer and navigate to it using your terminal
2. Run `./new-game` in your terminal to begin the game.
3. Run `./next`. Split the indicated items out of the big commit into their own
   commits.

## Rebuilding commits

Run `git reset commit-ref-here` to "uncommit" any changes occurred after that
commit. For example, if you have these commits:

- Commit `dddd`: Adds file "4"
- Commit `cccc`: Adds file "3"
- Commit `bbbb`: Adds file "2"
- Commit `aaaa`: Adds file "1"

Running `git reset bbbb` would leave you with:

- Commit `bbbb`: Adds file "2"
- Commit `aaaa`: Adds file "1"

This removes the commits, but leaves the changes in files "3" and "4." You can
rebuild the commits with `git add` and `git commit` as usual to make a new
history.

Remember that you can use `git reflog` and `git reset --hard` to get back to
previous states!

## Relevance

A good Git history provides a meaningful set of save points you can return to,
but it's hard to build an ideal history while simultaneously creativingly
solving problems. Resetting commits allows you to freely commit code and clean
it up later when you can be more analytical about it. It's common to make messy
commits while developing and then reset out those commits to build ideal ones
once a feature or ticket is done.

Please note that resetting commits changes a repository's Git history. This will
cause conflicts with collaborators who have the old history, so it's a good idea
to only reset commits that haven't been worked on publicly yet. If you make a
mistake, you can use `git reflog` and `git reset --hard` to reset the branch
back to a previous state.
