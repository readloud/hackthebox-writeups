# hackthebox-writeups
A collection of writeups for active HTB boxes.

Please note that these are all completely unformatted, as I will be formatting/editing them once the machines have been retired, so that I can post them onto Medium.

Fully edited stories can be found at https://medium.com/@georgeomnet

##### The passwords to each PDF is the root flag for the machine.

get-appxpackage *Microsoft.Windows.Photos* | remove-appxpackage
Get-AppxPackage -allusers *WindowsStore* | Remove-AppxPackage
Get-AppxPackage -allusers Microsoft.Windows.Photos | Foreach {Add-AppxPackage -DisableDevelopmentMode -Register “$($_.InstallLocation)\AppXManifest.xml”} 