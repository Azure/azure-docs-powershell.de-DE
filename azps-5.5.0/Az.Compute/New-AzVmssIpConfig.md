---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 92F192A5-F75E-4EFE-B2D2-B0DF0B78D3B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpConfig.md
ms.openlocfilehash: e2ca08746ab9b4dc2ef2265a59cdab00ac42cf33
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100144876"
---
# New-AzVmssIpConfig

## SYNOPSIS
Erstellt eine IP-Konfiguration für eine Netzwerkschnittstelle einer VMSS.

## SYNTAX

```
New-AzVmssIpConfig [[-Name] <String>] [[-Id] <String>] [[-SubnetId] <String>]
 [[-ApplicationGatewayBackendAddressPoolsId] <String[]>] [[-LoadBalancerBackendAddressPoolsId] <String[]>]
 [[-LoadBalancerInboundNatPoolsId] <String[]>] [-Primary] [-PrivateIPAddressVersion <String>]
 [-PublicIPAddressConfigurationName <String>] [-PublicIPAddressConfigurationIdleTimeoutInMinutes <Int32>]
 [-DnsSetting <String>] [-IpTag <VirtualMachineScaleSetIpTag[]>] [-PublicIPPrefix <String>]
 [-PublicIPAddressVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "New-AzVmssIpConfig"** erstellt ein IP-Konfigurationsobjekt für eine Netzwerkschnittstelle eines Virtual Machine Scale Set (VMSS).
Geben Sie die Konfiguration dieses Cmdlets als *Parameter "IPConfiguration"* des Add-AzVmssNetworkInterfaceConfiguration an.

## BEISPIELE

### Beispiel 1: Erstellen eines IP-Konfigurationsobjekts für eine VMSS-Schnittstelle
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface02" -SubnetId $SubnetId
```

Mit diesem Befehl wird ein IP-Konfigurationsobjekt namens "ContosoVmssInterface02" erstellt.
Der Befehl verwendet eine zuvor definierte Subnetz-ID, die in $SubnetId.
Der Befehl speichert die Konfigurationseinstellungen in der $IPConfiguration für die spätere Verwendung mit **"Add-AzVmssNetworkInterfaceConfiguration".**

### Beispiel 2: Erstellen eines IP-Konfigurationsobjekts, das EINSTELLUNGEN für den NAT-Pool enthält
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface03" -LoadBalancerInboundNatPoolsId $expectedLb.InboundNatPools[0].Id -LoadBalancerBackendAddressPoolsId $expectedLb.BackendAddressPools[0].Id -SubnetId $SubnetId
```

Mit diesem Befehl wird ein IP-Konfigurationsobjekt namens "ContosoVmssInterface03" erstellt und dann in der $IPConfiguration zur späteren Verwendung gespeichert.
Der Befehl verwendet eine zuvor definierte Subnetz-ID, die in $SubnetId.
Der Befehl speichert die Konfigurationseinstellungen in der $IPConfiguration für die spätere Verwendung.
Der Befehl gibt Werte für die *Parameter LoadBalancerInboundNatPoolsId* und *LoadBalancerBackendAddressPoolsId* an.

## PARAMETERS

### -ApplicationGatewayBackendAddressPoolsId
Gibt ein Array mit Verweisen auf Back-End-Adresspools mit Lastensaldoern an.
Ein Skalierungssatz kann auf Back-End-Adresspools eines öffentlichen und eines internen Lastenausgleichs verweisen.
Für mehrere Skalierungssätze kann nicht derselbe Lastenausgleich verwendet werden.

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
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

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
Die dns-Einstellungen, die auf die öffentlichenIP-Adressen angewendet werden sollen.
Die Domänennamenbeschriftung der Dns-Einstellungen, die auf die PublicIP-Adressen angewendet werden sollen.
Die Verkettung der Domänennamenbezeichnung und des vm-Index sind die Domänennamenbeschriftungen der öffentlichen IP-Adressressourcen, die erstellt werden.

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
Gibt ein Array von Ip-Tag-Objekten an.

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
Gibt ein Array von Verweisen auf die Nat (Incoming Network Address Translation)-Pools der Lastenausgleichspools an.
Ein Skalierungssatz kann auf eingehende NAT-Pools mit einem öffentlichen und einem internen Lastenausgleich verweisen.
Für mehrere Skalierungssätze kann nicht derselbe Lastenausgleich verwendet werden.

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
Gibt ein Array von Verweisen auf eingehende NAT-Pools der Lastensaldor an.
Ein Skalierungssatz kann auf eingehende NAT-Pools mit einem öffentlichen und einem internen Lastenausgleich verweisen.
Für mehrere Skalierungssätze kann nicht derselbe Lastenausgleich verwendet werden.

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

### -Primary
Gibt die primäre IP-Konfiguration für den Fall an, dass die Netzwerkschnittstelle über mehrere IP-Konfigurationen verfügt.

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
Geben Sie die IP-Konfiguration für die private IP-Adresse an.  Der Standardwert wird als IPv4 verwendet.  Mögliche Werte: "IPv4" und "IPv6".

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
Der Konfigurationsname der öffentlichenIP-Adresse.

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
Geben Sie die IP-Konfiguration für die öffentliche IP-Adresse an.  Der Standardwert wird als IPv4 verwendet.  Mögliche Werte: "IPv4" und "IPv6".

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

### -SubnetId
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

### -Confirm
Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.

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

### -Waswenn
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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### System.String

### System.String[]

### System.Int32

### Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag[]

## AUSGABEN

### Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Add-AzVmssNetworkInterfaceConfiguration](./Add-AzVmssNetworkInterfaceConfiguration.md)


