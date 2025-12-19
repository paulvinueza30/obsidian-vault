
Idea 1 : A tui for syncing dotfiles into some repo of choice 
we can use this as a way to backup omarchy setups streamlines the process
it would ideally open up a file explorer for ~/.config/ and then you pick the dotfiles you want to backup -> make sure they are not symlinks and hard cpy contents to a default directory -> push the contents up to github repo.

Idea 2: This would be the restore for idea 1 it would be some dynamic script or program that would get all files in that github repo and sync to current environment

Ideally we would be able to backup more than dotfiles , stuff like media, custom scripts, etc.

Maybe we could do dotfiles first then user can select any other thing they would like to keep
