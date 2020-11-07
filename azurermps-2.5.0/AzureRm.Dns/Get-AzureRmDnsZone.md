---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8b71c522a8d4dc006428ca2a400160a0ce7ce68b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850023"
---
# Get-AzureRmDnsZone

## Synopsis
Ruft eine DNS-Zone ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### Standard (Standard)
```
Get-AzureRmDnsZone [<CommonParameters>]
```

### ResourceGroup
```
Get-AzureRmDnsZone [-Name <String>] -ResourceGroupName <String> [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmDnsZone** " Ruft eine DNS-Zone (Domain Name System) aus der angegebenen Ressourcengruppe ab.
Wenn Sie den Parameter *Name* angeben, wird ein einzelnes **dnsZone** -Objekt zurückgegeben.
Wenn Sie den Parameter *Name* nicht angeben, wird ein Array zurückgegeben, das alle Zonen in der angegebenen Ressourcengruppe enthält.
Sie können das **dnsZone** -Objekt verwenden, um die Zone zu aktualisieren, beispielsweise können Sie **Recordset** -Objekte hinzufügen.

## Beispiele

### Beispiel 1: Abrufen einer Zone
```
PS C:\> $Zone = Get-AzureRmDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

In diesem Beispiel wird die DNS-Zone mit dem Namen MyZone.com aus der angegebenen Ressourcengruppe abgerufen und dann in der $Zone-Variablen gespeichert.

### Beispiel 2: Abrufen aller Zonen in einer Ressourcengruppe
```
PS C:\> $Zones = Get-AzureRmDnsZone -ResourceGroupName "MyResourceGroup"
```

In diesem Beispiel werden alle DNS-Zonen in der angegebenen Ressourcengruppe abgerufen und dann in der $Zones-Variablen gespeichert.

### Beispiel 3: Abrufen aller Zonen in einem Abonnement
```
PS C:\> $Zones = Get-AzureRmDnsZone
```

In diesem Beispiel werden alle DNS-Zonen im aktuellen Azure-Abonnement abgerufen und dann in der $Zones-Variablen gespeichert.

## Parameter

### -Name
Gibt den Namen der abzurufenden DNS-Zone an.

Wenn Sie keinen Wert für den Parameter *Name* angeben, ruft dieses Cmdlet alle DNS-Zonen in der angegebenen Ressourcengruppe ab.
Wenn Sie auch den *ResourceGroupName* -Parameter weglassen, ruft dieses Cmdlet alle DNS-Zonen im aktuellen Azure-Abonnement ab.

```yaml
Type: String
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
Type: String
Parameter Sets: ResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine
Mit diesem Cmdlet können Sie keine Pipe-Eingabe durchleiten.

## Ausgaben

### Microsoft. Azure. Commands. DNS. dnsZone
Dieses Cmdlet gibt ein Objekt zurück, das die DNS-Zone darstellt.
Wenn der Zonen Name nicht angegeben wird, wird ein Array von Zone-Objekten zurückgegeben.

## Notizen

## Verwandte Links

[Neu – AzureRmDnsZone](./New-AzureRmDnsZone.md)

[Remove-AzureRmDnsZone](./Remove-AzureRmDnsZone.md)

[Satz-AzureRmDnsZone](./Set-AzureRmDnsZone.md)
