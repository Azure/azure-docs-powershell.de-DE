---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 92F192A5-F75E-4EFE-B2D2-B0DF0B78D3B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpConfig.md
ms.openlocfilehash: e2ca08746ab9b4dc2ef2265a59cdab00ac42cf33
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93994995"
---
# New-AzVmssIpConfig

## Synopsis
Erstellt eine IP-Konfiguration für eine Netzwerkschnittstelle eines VMSS.

## Syntax

```
New-AzVmssIpConfig [[-Name] <String>] [[-Id] <String>] [[-SubnetId] <String>]
 [[-ApplicationGatewayBackendAddressPoolsId] <String[]>] [[-LoadBalancerBackendAddressPoolsId] <String[]>]
 [[-LoadBalancerInboundNatPoolsId] <String[]>] [-Primary] [-PrivateIPAddressVersion <String>]
 [-PublicIPAddressConfigurationName <String>] [-PublicIPAddressConfigurationIdleTimeoutInMinutes <Int32>]
 [-DnsSetting <String>] [-IpTag <VirtualMachineScaleSetIpTag[]>] [-PublicIPPrefix <String>]
 [-PublicIPAddressVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzVmssIpConfig** erstellt ein IP-Konfigurationsobjekt für eine Netzwerkschnittstelle eines virtuellen Computer-Skalierungs Satzes (VMSS).
Geben Sie die Konfiguration dieses Cmdlets als *IPKonfigurationsdateiAddress* -Parameter des Add-AzVmssNetworkInterfaceConfiguration-Cmdlets an.

## Beispiele

### Beispiel 1: Erstellen eines IP-Konfigurationsobjekts für eine VMSS-Schnittstelle
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface02" -SubnetId $SubnetId
```

Dieser Befehl erstellt ein IP-Konfigurationsobjekt mit dem Namen ContosoVmssInterface02.
Der Befehl verwendet eine zuvor definierte Subnetz-ID, die in $SubnetId gespeichert ist.
Der Befehl speichert die Konfigurationseinstellungen in der $IPConfiguration-Variablen für die spätere Verwendung mit **Add-AzVmssNetworkInterfaceConfiguration**.

### Beispiel 2: Erstellen eines IP-Konfigurationsobjekts mit NAT-Pooleinstellungen
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface03" -LoadBalancerInboundNatPoolsId $expectedLb.InboundNatPools[0].Id -LoadBalancerBackendAddressPoolsId $expectedLb.BackendAddressPools[0].Id -SubnetId $SubnetId
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
Type: System.String[]
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

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
Type: System.String
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
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IpTag
Gibt ein Array von IP-Tag-Objekten an.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LoadBalancerBackendAddressPoolsId
Gibt ein Array von Verweisen auf eingehende Netzwerkadressübersetzung (NAT)-Pools der Lastenausgleichs Anlagen an.
Ein Skalierungs Satz kann auf eingehende NAT-Pools eines öffentlichen und eines internen Load Balancer verweisen.
Mehrere Skalensätze können nicht dasselbe Lastenausgleichsmodul verwenden.

```yaml
Type: System.String[]
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
Type: System.String[]
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
Type: System.String
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
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivateIPAddressVersion
Geben Sie die IP-Konfiguration für private IP-Adresse an.  Standard wird als IPv4 verwendet.  Mögliche Werte sind: "IPv4" und "IPv6".

```yaml
Type: System.String
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
Type: System.Int32
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
Type: System.String
Parameter Sets: (All)
Aliases: PublicIPAddressName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicIPAddressVersion
Geben Sie die IP-Konfiguration für die öffentliche IP-Adresse an.  Standard wird als IPv4 verwendet.  Mögliche Werte sind: "IPv4" und "IPv6".

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicIPPrefix
Die ID des öffentlichen IP-Präfixes

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Subnet-Nr
Gibt die Subnetz-ID an, in der die Konfiguration die VMSS-Netzwerkschnittstelle erstellt.

```yaml
Type: System.String
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
Type: System.Management.Automation.SwitchParameter
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
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### System. String

### System. String []

### System. Int32

### Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetIpTag []

## Ausgaben

### Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetIPConfiguration

## Notizen

## Verwandte Links

[Add-AzVmssNetworkInterfaceConfiguration](./Add-AzVmssNetworkInterfaceConfiguration.md)


