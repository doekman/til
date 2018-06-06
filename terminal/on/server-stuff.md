macOS server stuff
==================

Commands:

    profiles
    serveradmin
    systemsetup
    sysadminctl


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

* ls -le@O
    - `e` for displaying ACL
    - `@` for displaying extend attributes
    - `O` (capital O) for displaying [SIP][] and flags information
* chmod
* chown
* chflags
* xattr

Links:

* [Managing Permissions via Command Line](http://www.peachpit.com/articles/article.aspx?p=1403238&seqNum=7).
* [Demystifying `root` on macOS, Part 1](https://scriptingosx.com/2018/04/demystifying-root-on-macos-part-1/)


Network shares
--------------

Commands: 

    sharing
    
     #renamen van een share zonder de folder-naam te wijzigen
    man nsmb.conf
    sudo serveradmin fullstatus smb #vooral: smb:currentConnections
    sudo serveradmin settings smb
    sudo serveradmin command smb:command = getConnectedUsers #Opvragen aangesloten gebruikers


MaxFocus
--------

The [MaxFocus'](https://www.solarwindsmsp.com/product/login "MSP Remote Management & Management") _Advanced Monitoring Agent.app_ stores it's configuration at the location `/usr/local/rmmagent`.

[SIP]:    https://support.apple.com/en-us/HT204899
