1- From Ready-Made Ticket

Make sure the internet is enabled.

Open Windows PowerShell as administrator, and enter the following commands in the sequence in which they are given.

Enter the Key (Replace <key> with the key from the above list) with the following command:
slmgr /ipk <key>

Download Universal tickets from here and extract the downloaded file.
Now enter below code in PowerShell:
(Get-ItemProperty HKLM:\SYSTEM\CurrentControlSet\Control\ProductOptions).OSProductPfn

This command will you show you some text like Microsoft.Windows.48.X19-98841_8wekyb3d8bbwe

You need to find the exact same name ticket file in the folder which you have extracted earlier.
Copy that ticket file and paste it in the following folder:
C:\ProgramData\Microsoft\Windows\ClipSVC\GenuineTicket

Now run below command in PowerShell to apply the ticket:
clipup -v -o

Activate Windows with the following command:
slmgr /ato

Check Activation Status with the following command:
slmgr /xpr

Done.
