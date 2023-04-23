# Mackintosh-Z490-Aorus-Master-i7-10700-RX6600XT
本人长期使用该机，特地定制了ALC1220板载声卡ID18，除SPDIF数吗输出没有设备没有定制外，其它内接口全部测试完好。板载有线网卡I225V也通过bios及Opencore设置实现直接驱动。
## 硬件配置配置
  | 信息 | 备注
-- | -- | --
Gigabyte   Aorus Master Z490 | 2.5Gbit   Ethernet: Intel I225-V | Ventura   驱动成功
Audio:   Realtek ALC1220-VB | 自制ID=18
WiFi   / BT: Intel Wi-Fi 6 AX201 | 关闭
CPU | I7   10700 |  
内存 | 2X8G   3000Hz | 实际2933Hz
显卡 | RX6600XT |  
WiFi / BT | Fenvi   T919 |  
## 声卡定制说明
Realtek ALC1220-VB使用alcid=1能驱动line out接口和前置耳机口，但不能侦测接口是否插入设备，同时工作，很不完美，动手重新定制，alcid=18，后面版line out、line in和mic接口正常工作，且line in和mic可自动侦测插孔和切换。光纤输出接口没有设备，不确定是否好用。另外，多声道功能已舍弃。
机箱前面的hp孔和mic孔分别各一个，且该hp孔与后面板的line out孔可自动切换。
## 板载2.5G网卡驱动说明
Bios开启VT-d，Kernel中quicks去掉DisableIoMapper，I225V有线网卡直接免驱。
## Gigabyte Z490 aorus master EFI of OpenCore.  **禁止用于商业用途。**
