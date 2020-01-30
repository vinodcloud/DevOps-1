* ansible for windows configuration

* Windows Remote Management (WinRM) is a feature of Windows Vista that allows administrators to remotely run management scripts. It handles remote connections by means of the WS-Management Protocol, which is based on SOAP (Simple Object Access Protocol).


https://docs.ansible.com/ansible/latest/user_guide/windows_setup.html#upgrading-powershell-and-net-framework


------------------------Upgrading PowerShell and .NET Framework--------------------------

$url = "https://raw.githubusercontent.com/jborean93/ansible-windows/master/scripts/Upgrade-PowerShell.ps1"
$file = "$env:temp\Upgrade-PowerShell.ps1"
$username = "Administrator"
$password = "&fL)Q-SD.ae"

(New-Object -TypeName System.Net.WebClient).DownloadFile($url, $file)
Set-ExecutionPolicy -ExecutionPolicy Unrestricted -Force

# Version can be 3.0, 4.0 or 5.1
&$file -Version 5.1 -Username $username -Password $password -Verbose


------------------------------WinRM Setup-------------------------------------


$url = "https://raw.githubusercontent.com/ansible/ansible/devel/examples/scripts/ConfigureRemotingForAnsible.ps1"
$file = "$env:temp\ConfigureRemotingForAnsible.ps1"

(New-Object -TypeName System.Net.WebClient).DownloadFile($url, $file)

powershell.exe -ExecutionPolicy ByPass -File $file

----------------------------WinRM Listener-------------------------------------------

winrm enumerate winrm/config/Listener

