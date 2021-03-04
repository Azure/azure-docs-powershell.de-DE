---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: https://docs.microsoft.com/powershell/module/az.dns/get-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsZone.md
ms.openlocfilehash: a788cf3638d124dac164f19171f1be89afc2e385
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935059"
---
# Get-AzDnsZone

## SYNOPSIS
Ruft eine DNS-Zone ab.

## SYNTAX

### Standard (Standard)
```
Get-AzDnsZone [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroup
```
Get-AzDnsZone [-Name <String>] -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESCHREIBUNG
Das **Get-AzDnsZone-Cmdlet** ruft eine Zone des Domain Name System (DNS) aus der angegebenen Ressourcengruppe ab.
Wenn Sie den *Parameter Name angeben,* wird ein einzelnes **DnsZone-Objekt** zurückgegeben.
Wenn Sie den Parameter Name nicht *angeben,* wird ein Array zurückgegeben, das alle Zonen in der angegebenen Ressourcengruppe enthält.
Sie können das **DnsZone-Objekt** verwenden, um die Zone zu aktualisieren, beispielsweise können Sie **ihr RecordSet-Objekte** hinzufügen.

## BEISPIELE

### Beispiel 1: Erhalten einer Zone
```
PS C:\> $Zone = Get-AzDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

In diesem Beispiel wird die DNS-Zone myzone.com aus der angegebenen Ressourcengruppe und dann in der $Zone gespeichert.

### Beispiel 2: Alle Zonen in einer Ressourcengruppe erhalten
```
PS C:\> $Zones = Get-AzDnsZone -ResourceGroupName "MyResourceGroup"
```

In diesem Beispiel werden alle DNS-Zonen in der angegebenen Ressourcengruppe ab- und dann in der $Zones gespeichert.

### Beispiel 3: Alle Zonen in einem Abonnement erhalten
```
PS C:\> $Zones = Get-AzDnsZone
```

In diesem Beispiel werden alle DNS-Zonen im aktuellen Azure-Abonnement ab- und dann in der $Zones gespeichert.

## PARAMETER

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden

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
Gibt den Namen der zu erhaltenden DNS-Zone an.
Wenn Sie keinen Wert für den Parameter *Name* angeben, ruft dieses Cmdlet alle DNS-Zonen in der angegebenen Ressourcengruppe ab.
Wenn Sie auch den *Parameter ResourceGroupName* weglassen, ruft dieses Cmdlet alle DNS-Zonen im aktuellen Azure-Abonnement ab.

```yaml
Type: System.String
Parameter Sets: ResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, die die zu erhaltende DNS-Zone enthält.
Wenn Sie den *ResourceGroupName* nicht angeben, müssen Sie auch den Parameter *Name weglassen.*
In diesem Fall ruft dieses Cmdlet alle DNS-Zonen im aktuellen Azure-Abonnement ab.

```yaml
Type: System.String
Parameter Sets: ResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### System.String

## AUSGABEN

### Microsoft.Azure.Commands.Dns.DnsZone

## NOTIZEN

## VERWANDTE LINKS

[New-AzDnsZone](./New-AzDnsZone.md)

[Remove-AzDnsZone](./Remove-AzDnsZone.md)

[Set-AzDnsZone](./Set-AzDnsZone.md)
