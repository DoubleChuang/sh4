# [如何安裝]
===

* 1.首先將隨身碟放入刷機檔案
	* initrd.ub
	* iptvubootupdate.bin
	* uboot.sh
	* target.tgz  #sh4twbox 6in1


* 2.未插電情況下 將隨身碟插入網樂通

* 3.按住網樂通reset 並插上電源 放開 等待燈號變藍

* 4.透過sudo apt-apt install arp-scan 抓取arp-scan

* 5.使用sudo arp-scan -l 探測所在網段的裝置MAC跟IP

* 6.使用telnet IP 連上裝置

* 7.輸入預設帳密 root twpdatwpda

* 8.輸入 sh4twbox

* 9.輸入p2 

* 10.ENTER三次 他會將sdb(usb)的target.tgz抓到sda

* 11.結束後 拔掉隨身碟拔掉電源  再按住RESET並插上電源

* 12.使用ssh root@IP 連上裝置

* 13.Done




# [目錄位置]
===
 
* 網頁 目錄為 /usr/local/apache/htdocs/
* BT	 目錄為 /BT
* samba目錄為 /BT
* FTP	 目錄為 /

# [連線]
===

transmission: http://ip:9091
FTP			: ftp://ip
 


# [開機]

/etc/rc.local
===

* ftp:
	/etc/init.d/vsftpd start

* samba:
	/etc/init.d/smb start

* apache:
	/usr/local/apache/bin/apachectl start

* transmission(BT):
	transmission-daemon

* mysql:
	/usr/local/mysql/bin/mysqld_safe --user=mysql &

* 紅外線:
	/etc/init.d/lircd start
	
	irexec &

* cvbs輸出:
	cd /root/stmfb
./insmod.sh &
