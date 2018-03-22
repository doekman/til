macOS server stuff
==================

Commands:

    serveradmin


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

* chmod
* chown


Network shares
--------------

Commands: 

    sharing
    sudo serveradmin fullstatus smb

