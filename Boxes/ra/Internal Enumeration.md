# Enumeration
Once we have access to buse we see the user has account operator role 

This allows us to change a user password 
`brittanycr:password123!`

This is hinted at in `C:\scripts\`

Once we have access to brittanycr, we can connect to the user directory via smb 

This allows us to access and modify the `hosts.txt` file which is being used with `Invoke-Expression` within the powershell script.

We can modify hosts.txt to contain 
`;C:\temp\shell.exe`

replace the hosts file, and wait until the task scheduler fires. Bish bash bosh `NT Authority/system`