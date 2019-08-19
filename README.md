# syncr

Project to synchronise files easily between source directories and remote servers

## syncr
Syncr uses a configuration file in the project root called ‘project.cfg’. This sets variables to determine where to sync to, destination directories, and the user used.

Run without arguments, syncr will output a dry run of an rsync command to the servers specified. For example, for the guardian project, this would output which files have changed on the local system vs editor1. 

Add parameters -d -s (diff summary) to check each file for actual differences (rather than mode changes, ownership changes etc.) to get a list of files that actually have changed.

Add parameter -x (cannot be done at the same time as -d) to actually synchronise from local to remote. I recommend going through all changes with rmdiff first

## rmdiff
(Remote diff) Run rmdiff <path-to-local-file> and it’ll show you a diff between the local and remote files. Add -e : rmdiff -e <path-to-local-file> to open the files up in vimdiff for inspection

##rmget
Gets the remote version of a file to replace the local

