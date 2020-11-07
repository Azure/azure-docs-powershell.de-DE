---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 07FF274A-F365-44E5-A66B-6740CD165664
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 80324e1d6fa87959edb0da8e7aa72f3b2a42a3b6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841831"
---
# Add-AzLoadBalancerFrontendIpConfig

## Synopsis
Fügt eine Front-End-IP-Konfiguration zu einem Lastenausgleichsmodul hinzu.

## Syntax

### SetByResourceSubnet
```
Add-AzLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-PrivateIpAddress <String>] -Subnet <PSSubnet> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResourceIdSubnet
```
Add-AzLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-PrivateIpAddress <String>] -SubnetId <String> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResourceIdPublicIpAddress
```
Add-AzLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 -PublicIpAddressId <String> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResourcePublicIpAddress
```
Add-AzLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 -PublicIpAddress <PSPublicIpAddress> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet **Add-AzLoadBalancerFrontendIpConifg** wird eine Front-End-IP-Konfiguration zu einem Azure Load Balancer hinzugefügt.

## Beispiele

### Beispiel 1: Hinzufügen einer Front-End-IP-Konfiguration mit einer dynamischen IP-Adresse
```
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyRg" | Get-AzVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet | Set-AzLoadBalancer
```

Der erste Befehl ruft das Azure Virtual Network mit dem Namen MyVnet ab und übergibt das Ergebnis mithilfe der Pipeline an das Cmdlet **Get-AzVirtualNetworkSubnetConfig** , um das Subnetz mit dem Namen mysubnet abzurufen.
Der Befehl speichert dann das Ergebnis in der Variablen mit dem Namen $Subnet.
Der zweite Befehl ruft das Lastenausgleichsmodul mit dem Namen MyLB ab und übergibt das Ergebnis an das **Add-AzLoadBalancerFrontendIpConfig-** Cmdlet, das dem Load Balancer eine Front-End-IP-Konfiguration mit einer dynamischen privaten IP-Adresse aus dem Subnetz hinzufügt, das in der Variablen mit dem Namen $MySubnet gespeichert ist.

### Beispiel 2 Hinzufügen einer Front-End-IP-Konfiguration mit einer statischen IP-Adresse
```
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "RG001" | Get-AzVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet -PrivateIpAddress "10.0.1.6" | Set-AzLoadBalancer
```

Der erste Befehl ruft das Azure Virtual Network mit dem Namen MyVnet ab und übergibt das Ergebnis mithilfe der Pipeline an das Cmdlet **Get-AzVirtualNetworkSubnetConfig** , um das Subnetz mit dem Namen mysubnet abzurufen.
Der Befehl speichert dann das Ergebnis in der Variablen mit dem Namen $Subnet.
Der zweite Befehl ruft das Lastenausgleichsmodul mit dem Namen MyLB ab und übergibt das Ergebnis an das **Add-AzLoadBalancerFrontendIpConfig-** Cmdlet, das dem Load Balancer eine Front-End-IP-Konfiguration mit einer statischen privaten IP-Adresse aus dem Subnetz hinzufügt, das in der Variablen mit dem Namen $Subnet gespeichert ist.

### Beispiel 3 Hinzufügen einer Front-End-IP-Konfiguration mit einer öffentlichen IP-Adresse
```
PS C:\>$PublicIp = Get-AzPublicIpAddress -ResourceGroupName "myRG" -Name "MyPub"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -PublicIpAddress $PublicIp | Set-AzLoadBalancer
```

Der erste Befehl ruft die Azure Public IP-Adresse mit dem Namen mypub ab und speichert das Ergebnis in der Variablen mit dem Namen $PublicIp.
Der zweite Befehl ruft das Lastenausgleichsmodul mit dem Namen MyLB ab und übergibt das Ergebnis an das **Add-AzLoadBalancerFrontendIpConfig-** Cmdlet, das dem Lastenausgleichsmodul eine Front-End-IP-Konfiguration hinzufügt, wobei die öffentliche IP-Adresse in der Variablen mit dem Namen $PublicIp gespeichert ist.

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LoadBalancer
Gibt ein **LoadBalancer** -Objekt an.
Dieses Cmdlet fügt dem Load Balancer eine Front-End-IP-Konfiguration hinzu, die dieser Parameter angibt.

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Gibt den Namen der Front-End-IP-Konfiguration an, die hinzugefügt werden soll.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivateIpAddress
Gibt die private IP-Adresse an, die einer Front-End-IP-Konfiguration zugeordnet werden soll.

```yaml
Type: String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicIpAddress
Gibt die öffentliche IP-Adresse an, die einer Front-End-IP-Konfiguration zugeordnet werden soll.

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResourcePublicIpAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicIpAddressId
Gibt an die ID der öffentlichen IP-Adresse, in der eine Front-End-IP-Konfiguration hinzugefügt werden soll.

```yaml
Type: String
Parameter Sets: SetByResourceIdPublicIpAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Subnetz
Gibt das Subnet-Objekt an, in dem eine Front-End-IP-Konfiguration hinzugefügt werden soll.

```yaml
Type: PSSubnet
Parameter Sets: SetByResourceSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Subnet-Nr
Gibt die ID des Subnets an, in dem eine Front-End-IP-Konfiguration hinzugefügt werden soll.

```yaml
Type: String
Parameter Sets: SetByResourceIdSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Zone
Eine Liste der Verfügbarkeits Zonen, die die IP-Adresse angibt, die für die Ressource reserviert ist, muss stammen.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### PSLoadBalancer
Der Parameter "LoadBalancer" akzeptiert den Wert vom Typ "PSLoadBalancer" aus der Pipeline.

## Ausgaben

### Microsoft. Azure. Commands. Network. Models. PSLoadBalancer

## Notizen

## Verwandte Links

[Get-AzLoadBalancerFrontendIpConfig](./Get-AzLoadBalancerFrontendIpConfig.md)

[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)

[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)

[Neu – AzLoadBalancerFrontendIpConfig](./New-AzLoadBalancerFrontendIpConfig.md)

[Remove-AzLoadBalancerFrontendIpConfig](./Remove-AzLoadBalancerFrontendIpConfig.md)

[Satz-AzLoadBalancerFrontendIpConfig](./Set-AzLoadBalancerFrontendIpConfig.md)


