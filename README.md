Developer Guidelines
====================================
[push rules](#rules)  
[to do list](#checklist)

Rules
-----------------------

1. Always branch **off develop** into a feature or sub development branch before pushing to develop  
i.e. Use the command ``git checkout -b <branchname> develop``.

2. [version-history](../../tree/version-history)<!--https://github.com/IanLoC/CleanerDesktop/tree/version-history--> should never be pulled from.  
The purpose of version history is to log previous versions.

3. ALWAYS **manually select files to move into** to master and version-history. follow the steps listed:
    
    1. Get the latest version of master ``git checkout master && git pull``
    
    2. Get the latest version of version-history ``git checkout version-history && git pull``
    
    3. Append previous release to version-history ``git checkout master -- someversionfilename.zip``\*
    
    4. Update the readme files, patch notes, and logs
    
    5. push
    
4. Branch names should be all lower case, and words separated by dashes to avoid case sensitivity errors

5. ``master`` should not be pushed to directly.

6. ``patch`` branch should update master and develop in the event of a bug. Also update version numbers correspondingly

\* Patches will count toward the most stable version, so to minimize history patches should overwrite and releases are a new index. Additionally, only some minor versions should be kept if dissimilar, or remove features.

Checklist
------------------------
Tasks that need to be completed for the next version:

- [ ] start layout
    - [ ] init file
    - [ ] default positioning of meters
- [ ] basic functionality
    - [ ] get directories
    - [ ] clickable buttons
    - [ ] summonable menu
- [ ] misc
    - [x] repository setup
    - [ ] setup gitignores?
