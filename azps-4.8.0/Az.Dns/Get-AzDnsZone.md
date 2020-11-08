---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/get-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsZone.md
ms.openlocfilehash: 68fff050564eff7014a7428556d3d4b2ce68f06d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009848"
---
# Get-AzDnsZone

## Synopsis
Ruft eine DNS-Zone ab.

## Syntax

### Standard (Standard)
```
Get-AzDnsZone [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroup
```
Get-AzDnsZone [-Name <String>] -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzDnsZone** " Ruft eine DNS-Zone (Domain Name System) aus der angegebenen Ressourcengruppe ab.
Wenn Sie den Parameter *Name* angeben, wird ein einzelnes **dnsZone** -Objekt zurückgegeben.
Wenn Sie den Parameter *Name* nicht angeben, wird ein Array zurückgegeben, das alle Zonen in der angegebenen Ressourcengruppe enthält.
Sie können das **dnsZone** -Objekt verwenden, um die Zone zu aktualisieren, beispielsweise können Sie **Recordset** -Objekte hinzufügen.

## Beispiele

### Beispiel 1: Abrufen einer Zone
```
PS C:\> $Zone = Get-AzDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

In diesem Beispiel wird die DNS-Zone mit dem Namen MyZone.com aus der angegebenen Ressourcengruppe abgerufen und dann in der $Zone-Variablen gespeichert.

### Beispiel 2: Abrufen aller Zonen in einer Ressourcengruppe
```
PS C:\> $Zones = Get-AzDnsZone -ResourceGroupName "MyResourceGroup"
```

In diesem Beispiel werden alle DNS-Zonen in der angegebenen Ressourcengruppe abgerufen und dann in der $Zones-Variablen gespeichert.

### Beispiel 3: Abrufen aller Zonen in einem Abonnement
```
PS C:\> $Zones = Get-AzDnsZone
```

In diesem Beispiel werden alle DNS-Zonen im aktuellen Azure-Abonnement abgerufen und dann in der $Zones-Variablen gespeichert.

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

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
Gibt den Namen der abzurufenden DNS-Zone an.
Wenn Sie keinen Wert für den Parameter *Name* angeben, ruft dieses Cmdlet alle DNS-Zonen in der angegebenen Ressourcengruppe ab.
Wenn Sie auch den *ResourceGroupName* -Parameter weglassen, ruft dieses Cmdlet alle DNS-Zonen im aktuellen Azure-Abonnement ab.

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
Gibt den Namen der Ressourcengruppe an, die die DNS-Zone enthält, die abgerufen werden soll.
Wenn Sie das *ResourceGroupName* nicht angeben, müssen Sie auch den Parameter *Name* weglassen.
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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

## Ausgaben

### Microsoft. Azure. Commands. DNS. dnsZone

## Notizen

## Verwandte Links

[Neu – AzDnsZone](./New-AzDnsZone.md)

[Remove-AzDnsZone](./Remove-AzDnsZone.md)

[Satz-AzDnsZone](./Set-AzDnsZone.md)
