# Cisco-Packet-Tracer
![image 1](Cisco_logo.png)

HWIC-2T->اینتر فیس سریال
WIC-1ENT->یک اینتر فیس اترنت:eternet
WIC-1T->یک اینتر فیس سریال:seric interface
---------------------------------------------------------------------
enable
config terminal
interface fastEternet 0/0
no shutdown
ip address 192.168.10.1 255.255.255.0
exit
interface serial 0/1/0
ip address 192.168.30.1 255.255.255.0
interface serial 0/1/1
ip address 192.168.40.1 255.255.255.0

روی سیستم کلیک می کنیم در  دستکتاب بقیه کار ها میکنیم
درای پنیگ هم رو همون سیستم کلیک بعد به ای پی بعدی

ctrl+z --->router#
show running config  #show all the commands that you use
copy running-config stratup-config    #after reset router it shows all commands
------------------------------------------------------------------------------------

Router(config)#enable password firstname // for router# 
ctrl+z
Router#show running-config
Router(config)#enable secret lastname //satehe amniyati bala tari dare
secret > password in cisco
Router(config)#line vty 0 4
Router(config-line)#password NationalNumber

telnet 20.20.20.1  //in one of the systems ip router midim
password: NationalNumber
Router>enable
Router#show running-config
We can ping in router 
Router>ping 10.10.10.1 

--------------------------------------------------------------------------------

مسیر یابی ایستا(static)/مسیر یابی دستی/ip route
Router#show ip route
Router(config)ip route Net_ID subnetmask getway
Router(config)ip route 0.0.0.0 0.0.0.0 192.168.10.1//age faght yek rah khorooji dasht

---------------------------------------------------------------------------

Net_ID = IP (AND) subnetmask // Net_ID hamoon ip hast age 255... bashe

-------------------------------------------------------------------------------

Router(config)router rip
Router(config-router)network 192.168.10.0// onayee(Net_ID) ke behesh motasel hast

----------------------------------------------------------------

Router (config)router eigrp 100 
Router(config-router)network (Net_ID) (not Subnetmask)
Router(config-router)network 192.168.10.2 255.255.255.252 //Id haye motasel va subnetmask khodesh badan hesab mikone

-----------------------------------------------------------------------------------

Router (config)router ospf 100
Router(config-router)network 192.168.10.2 255.255.255.252 area0 //id haye motasel va subnetmask
