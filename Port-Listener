[int]$port = Read-host "Which port number you want to allow and listen?"
$Listener = [System.Net.Sockets.TcpListener]$port;
New-NetFirewallRule -DisplayName "Allow Inbound Port $port" -Direction Inbound -Protocol TCP -LocalPort $port -Action Allow > $null

$Listener.Start();
while ($true) {
    $input = Read-Host "Listening to port $port now ...
    Press Enter to exit and close"
    break
}
$Listener.Stop();
