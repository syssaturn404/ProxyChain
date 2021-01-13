### :octocat: Syssaturn404 Repo💫

![image](https://qph.fs.quoracdn.net/main-qimg-9c696d07f4178ae120755e6f93fb4f11)

## What this proxy chain ?
```
Proxy chain adalah aplikasi yang dapat menjalankan semua yang terhubung ke jaringan
atau internet, media / melalui proxy. 
Jenis proxy yang di support adalah SOCK4, SOCK5, HTTP(S), maupun TOR.
```
## How to setup for proxychain ?
```
Fedora, CentOS, Redhat distribusi can make install :
root@fedora~#: su -c "yum install proxychains"
> bila distro yang anda gunakan belum memiliki proxychains di repository
bisa di install dengan mendownload source code dari website proxychain.
file configurasinya ada di dalam dir /etc/proxychains.conf.
Contoh kita menggunakan proxy SOCK5 ip 192.168.56.2
dan port 1080 maka dibagian paling bawah proxychains.conf tambahkan
socks5  192.168.56.2 1080, untuk penggunaan proxychains formatnya
proxychains namaaplikasi contoh menjalankan aplikasi whois
root@fedora~#: proxychains whois linux.com

Kali Linux can make install :
root@kali~#: sudo apt-get install proxychains
root@kali~#: locate proxychains
/etc/proxychains.conf
/etc/alternatives/proxychains
/etc/alternatives/proxychains.1.gz
/usr/bin/proxychains
/usr/bin/proxychains3
/usr/lib/proxychains3
/usr/lib/proxychains3/proxyresolv
/usr/lib/x86_64-linux-gnu/libproxychains.so.3
/usr/lib/x86_64-linux-gnu/libproxychains.so.3.0.0
/usr/share/applications/kali-proxychains.desktop
/usr/share/doc/libproxychains3
/usr/share/doc/proxychains

> config proxychains berada di /etc, kita buka menggunakan gedit :
root@kali~#: sudo gedit /etc/proxychains.conf
set di paling bawah, sama seperti diatas, tambahkan socksnya
lalu kita gunakan proxy chains, formatnya sama seperti diatas
contoh kita menjalankan aplikasi whois 
root@kali~#: proxychains whois linux.com

Output kurang lebih sama, seperti diatas~:
roxyChains-3.1 (http://proxychains.sf.net)
|DNS-request| whois.verisign-grs.com 
|S-chain|-<>-127.0.0.1:9050-<><>-4.2.2.2:53-<><>-OK
|DNS-response| whois.verisign-grs.com is 192.30.45.30
|S-chain|-<>-127.0.0.1:9050-<><>-192.30.45.30:43-<><>-OK
   Domain Name: LINUX.COM
   Registry Domain ID: 4245540_DOMAIN_COM-VRSN
   Registrar WHOIS Server: whois.enom.com
   Registrar URL: http://www.enom.com
   Updated Date: 2019-10-18T18:24:52Z
   Creation Date: 1994-06-02T04:00:00Z
   Registry Expiry Date: 2021-06-01T04:00:00Z
   Registrar: eNom, LLC
   Registrar IANA ID: 48
   Registrar Abuse Contact Email:
   Registrar Abuse Contact Phone:
   Domain Status: clientTransferProhibited https://icann.org/epp#clientTransferProhibited
   Name Server: NS1.DNSIMPLE.COM
   Name Server: NS2.DNSIMPLE.COM
   Name Server: NS3.DNSIMPLE.COM
   Name Server: NS4.DNSIMPLE.COM
   DNSSEC: unsigned
   URL of the ICANN Whois Inaccuracy Complaint Form: https://www.icann.org/wicf/
>>> Last update of whois database: 2021-01-13T17:36:33Z <<<
|DNS-request| whois.enom.com 
|S-chain|-<>-127.0.0.1:9050-<><>-4.2.2.2:53-<><>-OK
|DNS-response| whois.enom.com is 98.124.250.87
|S-chain|-<>-127.0.0.1:9050-<><>-98.124.250.87:43-<><>-OK
