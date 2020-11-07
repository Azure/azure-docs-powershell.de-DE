---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 92F192A5-F75E-4EFE-B2D2-B0DF0B78D3B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmssipconfig
schema: 2.0.0
ms.openlocfilehash: 82c27b6f8f926d273948bdfcb519a10ee1e0a3c7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850107"
---
# New-AzureRmVmssIpConfig

## Synopsis
Erstellt eine IP-Konfiguration für eine Netzwerkschnittstelle eines VMSS.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
New-AzureRmVmssIpConfig [[-Name] <String>] [[-Id] <String>] [[-SubnetId] <String>]
 [[-ApplicationGatewayBackendAddressPoolsId] <String[]>] [[-LoadBalancerBackendAddressPoolsId] <String[]>]
 [[-LoadBalancerInboundNatPoolsId] <String[]>] [-Primary] [-PrivateIPAddressVersion <String>]
 [-PublicIPAddressConfigurationName <String>] [-PublicIPAddressConfigurationIdleTimeoutInMinutes <Int32>]
 [-DnsSetting <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzureRmVmssIpConfig** erstellt ein IP-Konfigurationsobjekt für eine Netzwerkschnittstelle eines virtuellen Computer-Skalierungs Satzes (VMSS).
Geben Sie die Konfiguration dieses Cmdlets als *IPKonfigurationsdateiAddress* -Parameter des Add-AzureRmVmssNetworkInterfaceConfiguration-Cmdlets an.

## Beispiele

### Beispiel 1: Erstellen eines IP-Konfigurationsobjekts für eine VMSS-Schnittstelle
```
PS C:\> $IPConfiguration = New-AzureRmVmssIPConfig -Name "ContosoVmssInterface02" -SubnetId $SubnetId
```

Dieser Befehl erstellt ein IP-Konfigurationsobjekt mit dem Namen ContosoVmssInterface02.
Der Befehl verwendet eine zuvor definierte Subnetz-ID, die in $SubnetId gespeichert ist.
Der Befehl speichert die Konfigurationseinstellungen in der $IPConfiguration-Variablen für die spätere Verwendung mit **Add-AzureRmVmssNetworkInterfaceConfiguration**.

### Beispiel 2: Erstellen eines IP-Konfigurationsobjekts mit NAT-Pooleinstellungen
```
PS C:\> $IPConfiguration = New-AzureRmVmssIPConfig -Name "ContosoVmssInterface03" -LoadBalancerInboundNatPoolsId $expectedLb.InboundNatPools[0].Id -LoadBalancerBackendAddressPoolsId $expectedLb.BackendAddressPools[0].Id -SubnetId $SubnetId
```

Dieser Befehl erstellt ein IP-Konfigurationsobjekt mit dem Namen ContosoVmssInterface03 und speichert es dann zur späteren Verwendung in der $IPConfiguration-Variablen.
Der Befehl verwendet eine zuvor definierte Subnetz-ID, die in $SubnetId gespeichert ist.
Der Befehl speichert die Konfigurationseinstellungen in der $IPConfiguration-Variablen für die spätere Verwendung.
Der Befehl gibt Werte für die Parameter *LoadBalancerInboundNatPoolsId* und *LoadBalancerBackendAddressPoolsId* an.

## Parameter

### -ApplicationGatewayBackendAddressPoolsId
Gibt ein Array von Verweisen auf die Back-End-Adresspools von Load-Balancern an.
Ein Skalierungs Satz kann auf Back-End-Adresspools eines öffentlichen und eines internen Load Balancer verweisen.
Mehrere Skalensätze können nicht dasselbe Lastenausgleichsmodul verwenden.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -DnsSetting
Die DNS-Einstellungen, die auf die publicIP-Adressen angewendet werden sollen.
Die Domänennamen Beschriftung der DNS-Einstellungen, die auf die publicIP-Adressen angewendet werden sollen.
Bei der Verkettung der Domänennamen Beschriftung und des VM-Index handelt es sich um die Domänennamen Bezeichnungen der öffentlichen IP-Adress Ressourcen, die erstellt werden.

```yaml
Type: String
Parameter Sets: (All)
Aliases: PublicIPAddressDomainNameLabel

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ID
Gibt eine ID an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LoadBalancerBackendAddressPoolsId
Gibt ein Array von Verweisen auf eingehende Netzwerkadressübersetzung (NAT)-Pools der Lastenausgleichs Anlagen an.
Ein Skalierungs Satz kann auf eingehende NAT-Pools eines öffentlichen und eines internen Load Balancer verweisen.
Mehrere Skalensätze können nicht dasselbe Lastenausgleichsmodul verwenden.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LoadBalancerInboundNatPoolsId
Gibt ein Array von Verweisen auf eingehende NAT-Pools der Lastenausgleichs Anlagen an.
Ein Skalierungs Satz kann auf eingehende NAT-Pools eines öffentlichen und eines internen Load Balancer verweisen.
Mehrere Skalensätze können nicht dasselbe Lastenausgleichsmodul verwenden.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Gibt den Namen der IP-Konfiguration an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### – Primär
Gibt die primäre IP-Konfiguration an, wenn die Netzwerkschnittstelle mehr als eine IP-Konfiguration aufweist.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivateIPAddressVersion
Geben Sie an, dass die IP-Konfiguration entweder IPv4 oder IPv6 ist. Standard wird als IPv4 verwendet.  Mögliche Werte sind: "IPv4" und "IPv6".

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicIPAddressConfigurationIdleTimeoutInMinutes
Das Leerlauftimeout der öffentlichen IP-Adresse.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: PublicIPAddressIdleTimeoutInMinutes

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicIPAddressConfigurationName
Der Konfigurationsname der publicIP-Adresse.

```yaml
Type: String
Parameter Sets: (All)
Aliases: PublicIPAddressName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Subnet-Nr
Gibt die Subnetz-ID an, in der die Konfiguration die VMSS-Netzwerkschnittstelle erstellt.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird. Das Cmdlet wird nicht ausgeführt.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine
Dieses Cmdlet akzeptiert keine Eingaben.

## Ausgaben

### Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetIPConfiguration

## Notizen

## Verwandte Links

[Add-AzureRmVmssNetworkInterfaceConfiguration](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)


