---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatelinkserviceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkServiceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkServiceIpConfig.md
ms.openlocfilehash: 94375ba7d54095af131d7a61c7b06d50e2ba9521
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151596"
---
# New-AzPrivateLinkServiceIpConfig

## SYNOPSIS
Erstellen Sie eine IP-Konfiguration für einen privaten Linkdienst.

## SYNTAX

```
New-AzPrivateLinkServiceIpConfig -Name <String> [-PrivateIpAddressVersion <String>]
 [-PrivateIpAddress <String>] [-PublicIpAddress <PSPublicIpAddress>]
 [-Subnet <PSSubnet>] [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "New-AzPrivateLinkServiceIpConfig"** erstellt eine private Linkdienst-IP-Konfiguration. Diese Konfiguration wird verwendet, um S NAT für den eingehenden Datenverkehr vom privaten Endpunkt zu verwenden. 

## BEISPIELE

### Beispiel 1
```powershell
New-AzPrivateLinkServiceIpConfig -Name $IpConfigurationName -PrivateIpAddress "10.0.0.5" -Primary
```

In diesem Beispiel wird eine private Linkdienst-IP-Konfiguration im Arbeitsspeicher erstellt.

### Beispiel 2

Erstellen Sie eine IP-Konfiguration für einen privaten Linkdienst. (automatisch generiert)

<!-- Aladdin Generated Example -->
```powershell
New-AzPrivateLinkServiceIpConfig -Name 'IP-Config' -PrivateIpAddress '10.0.0.5' -Subnet <PSSubnet>
```

## PARAMETERS

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

### -Name
Der Name der IpConfiguration

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivateIpAddress
Die private IP-Adresse der ipConfiguration, wenn die statische Zuweisung angegeben ist.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivateIpAddressVersion
Die ip-Version der IP-Konfiguration

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Primary
Geben Sie an, dass die aktuelle IP-Konfiguration primär ist oder nicht.

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

### -Subnet
Subnetz

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### Keine

## AUSGABEN

### Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[New-AzPrivateLinkService](./New-AzPrivateLinkService.md)