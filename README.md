# SKC_VPN_KSH
高雄的VPN設定

07/15
更新：
1.
台南 sslvpn network → 10.222.32.100~10.222.32.200
台中sslvpn network → 10.222.20.100~10.222.20.200
高雄sslvpn network → 10.222.40.100~10.222.40.200

2.另外在現有的Switch上，可新增一些安全的防護機制，例：
Port如果是接一般的PC的話，可以設定
interface Ethernet1/0/X
stp edged-port enable  
loopback-detection enable                        →針對迴圈防護
storm-constrain broadcast 1500 1200 pps          →針對廣播風暴防護
storm-constrain control block                    →針對廣播風暴防護

3.將WAN IP轉換為118.163.3.229


07/05:
擎昊Alen以協助開通台中、台南與高雄之Site to Site VPN，各點的FW、SW之GW與Client VLAN IP均可互通
下一階段預計成功設置各點之SSL VPN，讓Client可由外部連入。
台中還需要設置一個Client作為測試之用
各點SW需要開通SSH登入
