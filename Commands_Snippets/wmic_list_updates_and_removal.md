## Listing of installed updates

wmic qfe get hotfixid

## For deleting an update

wusa /uninstall /kb:{update_id (that number)} /quiet /norestart 
or  
C:\WINDOWS\$NtUninstallKB*{update_id (without brackets)}*$\spuninst\spuninst.exe /quiet /norestart  

## An automation for removing all would be..

**wmic qfe get hotfixid >> c:\list.txt**  
**Open C:\list.txt in Notepad. (Remove the first line, it's just the title)**  
**for /f %i in ('type c:\list.txt') do echo wusa /uninstall /kb:%i /quiet /norestart >> c:\uninstall.cmd**  
or  
**for /f %i in ('type c:\list.txt') do echo C:\WINDOWS\\$NtUninstall%i$\spuninst\spuninst.exe /quiet /norestart >> c:\uninstall.cmd**  
