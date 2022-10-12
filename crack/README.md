# SSN/crack
Well there you go ladies and gentlemen, heres the crack.

Lets not forget to thank pxzdano for making this wonderful crack <3.

# Tutorial
## New & Funnel
Well you need to compile `server.go` and i'll show you how:
```bash
apt install golang
go build -o server server.go
screen -S crack -dm ./server
```
after you do so, you need to rewrite the license IP through iptables:
```bash
iptables -t nat -A OUTPUT -p tcp -d 54.39.235.240 --dport 38372 -j DNAT --to-destination 127.0.0.1:80
```
now you're done! enjoy!
## Old
Well you need to compile `server.go` and i'll show you how:
```bash
apt install golang
go build -o server server.go
screen -S crack -dm ./server
```
after you do so, you need to rewrite the license IP through iptables:
```bash
iptables -t nat -A OUTPUT -p tcp -d 54.39.235.240 --dport 8080 -j DNAT --to-destination 127.0.0.1:80
```
now you're done! enjoy!
