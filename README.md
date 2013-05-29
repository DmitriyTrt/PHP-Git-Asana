Post-receive hook for Git & Asana integration
=======

## Installation
* Make sure PHP CLI is installed on the machine and reachable by git user.
* Fill config at the beginning with Asana key (you'll probably want to create user called like "Git", because comments will be posted by this user) and the list of branches that should be parsed for references.
* If you want logging, also fill log path. It should be writable by git user.
* Put script to git hooks folder (".git/hooks" or "hooks" for bare repo) and name it "post-receive" (just keep its name).
* Make it executable.
* Commit and push something with Asana tasks referenced. Enjoy results.

## Features

* Post commit messages to the Asana task comments. Reference tasks using its ID (last large number from URL when task is selected or task details opened in Asana), like this: #9999
* Close Asana tasks. Just add "closes" or "fixes" before the task reference like this: closes #9999

## Credits
Developed for [USEUM.org](http://useum.org/)

## License
[GPL v3](http://www.gnu.org/licenses/gpl-3.0.txt)