macOS server stuff
==================

Commands:

    serveradmin
    profiles

Directory binding
-----------------

    # Remove Networkaccountserver
    sudo dsconfigldap -v -x -r archiserver.local
    sudo dsconfigldap -v -x -r ok.archipunt.nl
    # Bind to Networkaccountserver
    sudo dsconfigldap -vsemgxN -a ok.archipunt.nl -c $(hostname -s)


Users and groups
----------------

    # Remove User
    dscl localhost delete /Local/Default/Users/doeke
    # Create mobile user
    /System/Library/CoreServices/ManagedClient.app/Contents/Resources/createmobileaccount -n network_account_username_goes_here

Commands:

    dscl
    id -un #same result as $USER
    id -gn #current group
    groups #same as `id -Gn`


FS Security
-----------

* ls -le@
    - `e` for displaying ACL
    - `@` for displaying extend attributes
* chmod
* chown
* chflags
* xattr

[Managing Permissions via Command Line](http://www.peachpit.com/articles/article.aspx?p=1403238&seqNum=7).


Network shares
--------------

Commands: 

    sharing
    sudo serveradmin fullstatus smb

