---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicynatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRule.md
ms.openlocfilehash: 05b89c164b8a6cd3f91880edac1536d22817ea57
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100159092"
---
# New-AzFirewallPolicyNatRule

## SYNOPSIS
Erstellen einer neuen Nat-Regel für die Azure-Firewallrichtlinie

## SYNTAX

### SourceAddressAndTranslatedAddress
```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SourceAddressAndTranslatedFqdn
```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedFqdn <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SourceIpGroupAndTranslatedAddress
```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SourceIpGroupAndTranslatedFqdn
```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedFqdn <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "New-AzFirewallPolicyNatRule"** erstellt eine NAT-Regel für eine Azure-Firewallrichtlinie.

## BEISPIELE

### Beispiel 1
```powershell
PS C:\> New-AzFirewallPolicyNatRule -Name NatRule1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress 10.20.30.40 -DestinationPort 1000 -TranslatedAddress "192.168.0.1" -TranslatedPort "100"
```

In diesem Beispiel wird eine NAT-Regel mit der Quelladresse, dem Protokoll, der Zieladresse, dem Zielport, der übersetzten Adresse und dem übersetzten Port erstellt.

### Beispiel 2
```powershell
PS C:\> New-AzFirewallPolicyNatRule -Name NatRule1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress 10.20.30.40 -DestinationPort 1000 -TranslatedFqdn "internalhttp.server.net" -TranslatedPort "100"
```

In diesem Beispiel wird eine NAT-Regel mit der Quelladresse, dem Protokoll, der Zieladresse, dem Zielport, dem übersetzten fqdn und dem übersetzten Port erstellt.

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

### -Beschreibung
Beschreibung der Regel

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

### -DestinationAddress
Die Zieladressen der Regel. Dies muss eine öffentliche IP der Firewall sein.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationPort
Die Zielports der Regel

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Der Name der NAT Rule Collection

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

### -Protocol
Die Protokolle der Regel

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceAddress
Die Quelladressen der Regel

```yaml
Type: System.String[]
Parameter Sets: SourceAddressAndTranslatedAddress, SourceAddressAndTranslatedFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceIpGroup
Die Quell-IP-Gruppen der Regel

```yaml
Type: System.String[]
Parameter Sets: SourceIpGroupAndTranslatedAddress, SourceIpGroupAndTranslatedFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TranslatedAddress
Die übersetzte Adresse für diese NAT-Regel

```yaml
Type: System.String
Parameter Sets: SourceAddressAndTranslatedAddress, SourceIpGroupAndTranslatedAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TranslatedFqdn
Der übersetzte FQDN für diese NAT-Regel

```yaml
Type: System.String
Parameter Sets: SourceAddressAndTranslatedFqdn, SourceIpGroupAndTranslatedFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TranslatedPort
Der übersetzte Port für diese NAT-Regel

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### Keine

## AUSGABEN

### Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN
