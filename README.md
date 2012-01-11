# git-planbox

## Description

A git subcommand for the Planbox project management tool.

## Installation

### Pear package

1. Run: `pear install apinstein.pearfarm.org/climax-0.0.4 && pear install ardell.pearfarm.org/GitPlanbox-0.0.8`
2. Make sure the pear executable path is in your system path.

### Source installation

1. Clone this repository
2. cd into git-planbox
3. Clone the CLI repo git://github.com/apinstein/climax.git
4. Add dir git-planbox to your path

## Post-installation set-up

1. Set up some info that Planbox will need:

    * `git config --global --add planbox.email <your planbox account email>`
    * `git config --global --add planbox.password <your planbox password>`
    * `git config --add planbox.productid <planbox product id>` Instructions for finding your product id here: https://www.planbox.com/api/help/http under the "Finding the Product Id" section.
    * `git config --add planbox.author <yourname>` [optional]
    * `git config --add planbox.resourceid <your planbox resource id>` [optional] To find your resourceid, log into planbox, select your project, then select "My Work", then look for the integer right after "resource_id" in the url. Similar to instructions for planbox.productid.

2. Run `git planbox <subcommand>`

## Sub-commands

### git-planbox help

Generate a help message.

### git-planbox list

List stories.

### git-planbox show [&lt;storyid&gt;]

Show name, status, description, tasks, and comments for the specified story. If no storyid is specified then git-planbox will attempt to parse a storyid from the current git branch name.

### git-planbox start &lt;storyid&gt;

Start the specified story. Creates a new branch according to the naming template defined in git config. If there is more than one task within the story, git-planbox asks which task you would like to work on, then starts the timer for that task.

### git-planbox pause

Pause timers for in-progress tasks on the current story.

### git-planbox finish

Mark task(s) as completed and stop timers for in-progress tasks on the current story.

## TODO

* Automatically stop other timers when a new task is started.

## License

MIT. Pull requests gladly accepted.
