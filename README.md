# GameMaker-Git-Config

### Setting up a Github Git repository for Game Maker: Studio 2
#### Bennett Foddy, NYU Game Center, 2020

## Part I: Setting Up a Github Repository

First step is to create our empty remote repository on Github.com. Go to Github, log in, then press the + button in the upper right to create a new repository.

![New Repo](/images/new_repo.png)


Put in a useful name and description of the project. If you have applied for the free ‘student pack’ (https://education.github.com/pack) you can choose to make the project private (I wouldn’t worry if it has to be public though - nobody is gonna steal your student project’s code). 

![Create New Repo](/images/create_new_repo.png)

Click the green Create Repository button when you’re ready.


The important thing you need is the ‘Clone URL’ of the repo. Click the green ‘Clone or Download’ button, and select ‘use HTTPS’ if it’s not selected by default. Copy the checkout URL, which should start with https://…

We will need this URL to paste in two places within Game Maker.

![Create New Repo](/images/clone.png)


Next we have to enable the built-in Git support in Game Maker, both for the application and for the project. Go to Game Maker preferences, and click Plugins->Source Control

![Create New Repo](/images/gm_source_control.png)

Fill in the ‘Identity’ fields with your name and email address. Then click ‘Add User/Pass Authentication’. Fill in your Github username, password, and checkout URL.

![Create New Repo](/images/git_authentication.png)

To enable it for your project, go to the Resources panel, go to Options->Main, and check ‘enable source control’.

![Create New Repo](/images/enable_button.png)

Now we are ready to attach the remote to the project. Go to the ‘Source Control’ menu that should now be visible at the top of the screen, and …


WARNING WARNING WARNING
DO NOT CLICK ‘CREATE PROJECT REPOSITORY’
That will create a local repository (on your computer, not in the cloud) and it will become substantially more annoying to get it set up right.
END WARNING

Instead, click ‘Import project into repository’

![Create New Repo](/images/import_project.png)

Paste your repository clone URL into the field that appears.

![Create New Repo](/images/clone_url_paste.png)

Press ‘OK’ and everything should now be set up.

##Part II: Using your Github Repository (alone, without teammates)
Work as normal in Game Maker until you have some changes that you wouldn’t want to lose if your computer crashed. The first step is to commit those changes to the local Git repository (on your computer). Go to Source Control->Commit Changes

![Create New Repo](/images/commit_changes.png)

You’ll see a list of files that changed, and you can ‘stage’ them to add them to the commit. You probably want to just click ‘Stage All’ if you’re working alone, since it’s unlikely you have changes you don’t want to check in. 

Important: write a sensible commit message in the ‘Commit Message’ dialog box. An ancient Romanian curse will afflict anyone who writes ‘changed some stuff’ or ‘idk’ or ‘werweerrw’ in this box. But even more importantly, you will need good commit messages if you ever have problems and want to revert to an old version.

Click ‘Commit’ to commit your changes to the local repo.


To get the changes backed up on Github.com, you need to also ‘Push’ your commits to the remote repo. Simply click Source Control->Push Changes and you’re done.

Why wouldn’t you push a commit immediately? In the olden days, sometimes we didn’t have a wifi connection when we were working and we would do a bunch of commits before pushing them all to the remote when we got back to a wifi hotspot.

The other reason is that if you’re working with teammates, you have to pull their changes before you push yours, and maybe you want to save your work to a commit but you’re not ready to deal with everything they changed. But if you’re working alone, you basically always should push as soon as you commit.


What if you made some bad changes and broke your player movement or overwrote a good-looking sprite with a bad one? You want to revert to an older version. Click Source Control->View History. Here you can click your commits to see what files changed in each one.

To return to an older commit, right-click the one you want and choose Revert To This Revision. After a second or two, Game Maker will ask if you want to reload the project (and you should say yes). Done!



Oh no, what if I reverted by mistake??
No worries, the newer files are still there. Just go back to the history and ‘Revert to This Revision’ on the newer commit.


