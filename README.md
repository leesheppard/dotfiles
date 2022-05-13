# dotfiles

In addition to, the following sets up installation of Mac AppStore applications as well as brew files. 

Install **Homebrew**: 

	$ /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
	
Install [**mas**](https://github.com/mas-cli/mas):

	$ brew install mas

Install [**Brew Bundle**](https://github.com/Homebrew/homebrew-bundle):

	$ brew bundle
	
You can automatically write a bundle with the command:

	$ brew bundle dump

add the -describe switch to get a description/comment before each item in the Brewfile.

	$ brew bundle dump -describe
	
Save your Brewfile to iCloud or locally. When you set up a new Mac you can use it to automatically install everything.

Once you've created a Brewfile, updating brew is as simple as issuing the command `brew bundle`.

Thanks to brew and mas, updating your Mac system entirely is as simple as:

	$ softwareupdate -ia -verbose ; brew bundle -v ; brew cleanup ; brew doctor -verbose

**softwareupdate** is a built-in MacOS command to update the system from the command line. To see which updates are needed type:

	$ softwareupdate -l


The `-i` switch can be used to specify individual components to be updated, `-ia` says update them all.

Combining `softwareupdate` with `brew bundle -v` will upgrade everything on your system that's been installed using mas or brew.